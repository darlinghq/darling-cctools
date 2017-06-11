project(cctools)
set(CCTOOLS_VERSION 895)
set(CCTOOLS_INSTALL_DEST "libexec/darling/usr/libexec/DeveloperTools")
include_directories(BEFORE ${CMAKE_CURRENT_SOURCE_DIR}/include)

add_subdirectory(libstuff)
add_subdirectory(man)
add_subdirectory(otool)
add_subdirectory(misc)
