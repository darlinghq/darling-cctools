project(cctools_misc)

# To avoid name conflicts with tools from cctools-port
FUNCTION(add_cctools_misc exe)
	add_darling_executable(${exe}_cctools_misc
		${exe}.c
		$<TARGET_OBJECTS:libstuff>)
	set_target_properties(${exe}_cctools_misc
		PROPERTIES OUTPUT_NAME ${exe})
	install(TARGETS ${exe}_cctools_misc
		DESTINATION ${CCTOOLS_INSTALL_DEST})
ENDFUNCTION(add_cctools_misc)

add_cctools_misc(lipo)
add_cctools_misc(strings)
add_cctools_misc(size)
add_cctools_misc(checksyms)
add_cctools_misc(indr)
add_cctools_misc(strip)
add_cctools_misc(segedit)
add_cctools_misc(cmpdylib)
add_cctools_misc(pagestuff)
add_cctools_misc(redo_prebinding)
add_cctools_misc(seg_addr_table)
add_cctools_misc(check_dylib)
add_cctools_misc(seg_hack)
add_cctools_misc(install_name_tool)
add_cctools_misc(codesign_allocate)
add_cctools_misc(ctf_insert)
add_cctools_misc(bitcode_strip)
add_cctools_misc(nm)

add_cctools_misc(libtool)

# TODO: nmedit -- strip with -DNMEDIT
# TODO: libredo_prebinding
