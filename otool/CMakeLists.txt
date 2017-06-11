project(otool)

set(otool_sources
	main.c
	ofile_print.c
	m68k_disasm.c
	i860_disasm.c
	m88k_disasm.c
	i386_disasm.c
	ppc_disasm.c
	hppa_disasm.c
	sparc_disasm.c
	arm_disasm.c
	print_objc.c
	print_objc2_32bit.c
	print_objc2_64bit.c
	print_bitcode.c
	coff_print.c
	arm64_disasm.c
	dyld_bind_info.c
)

add_darling_executable(otool 
	${otool_sources} 
	$<TARGET_OBJECTS:libstuff>)
target_link_libraries(otool cxx objc)

install(TARGETS otool DESTINATION ${CCTOOLS_INSTALL_DEST})
