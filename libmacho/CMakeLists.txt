project(libmacho)

cmake_minimum_required(VERSION 3.13)

add_definitions(-DHAVE_STDINT_H=1)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -nostdinc -D__DARWIN_UNIX03 -fPIC -w")
set(CMAKE_SHARED_LINKER_FLAGS "${CMAKE_SHARED_LINKER_FLAGS} -nostdlib -Wl,-bind_at_load")

set(libmacho_sources
	arch.c
	get_end.c
	getsecbyname.c
	getsegbyname.c
	hppa_swap.c
	i386_swap.c
	i860_swap.c
	m68k_swap.c
	m88k_swap.c
	ppc_swap.c
	slot_name.c
	sparc_swap.c
	swap.c
)

set(DYLIB_INSTALL_NAME "/usr/lib/system/libmacho.dylib")
add_circular(macho FAT
	SOURCES
		${libmacho_sources}
	SIBLINGS
		system_kernel
		system_dyld
		system_c
		system_malloc
)

include(darling_static_lib)
add_darling_static_library(macho_static SOURCES $<TARGET_OBJECTS:macho_obj>)

install(TARGETS macho DESTINATION libexec/darling/usr/lib/system)
