project(cctools_man)

set(OTOOL_MAN1 otool.1)

set(MISC_MAN1
  nm.1 segedit.1 size.1 strip.1 cmpdylib.1 pagestuff.1
  redo_prebinding.1 install_name_tool.1 codesign_allocate.1
  ctf_insert.1 bitcode_strip.1
  # llvm-otool.1 nm-classic.1 size-classic.1 otool-classic.1
  # nmedit.1 libtool.1
  lipo.1 strings.1 checksyms.1 indr.1 segedit.1
  seg_addr_table.1 check_dylib.1
  )

# set(AS_MAN1 as.1)
# set(RANLIB_MAN1 ranlib.1)
# set(EFITOOLS_MAN1 mtoc.1)
# set(GPROF_MAN1 gprof.1) # removed after cctools-839
# set(DYLD_MAN1 dyld.1)

install(FILES
  ${OTOOL_MAN1}
  # ${MISC_MAN1}
  # ${AS_MAN1}
  # ${RANLIB_MAN1}
  # ${GPROF_MAN1} # removed after cctools-839
  # ${DYLD_MAN1}
  DESTINATION libexec/darling/usr/share/man/man1)

# set(DYLD_MAN3 dyld.3 NSModule.3 NSObjectFileImage.3 dyld_debug.3)
# set(DYLD_MANL3 NSObjectFileImage_priv.3)
# set (MAN3
#  kld.3 arch.3 get_end.3 end.3 getsectbyname.3
#  getsectbynamefromheader.3 getsectdata.3 getsectdatafromheader.3
#  getsegbyname.3)

# set(MISC_MAN3 redo_prebinding.3)
# set(CBTLIBS_MAN3 libsyminfo.3)

# install(FILES
#  ${DYLD_MAN3}
#  ${DYLD_MANL3}
#  ${CBTLIBS_MAN3}
#  ${MISC_MAN3}
#  DESTINATION libexec/darling/usr/share/man/man3)

# set(MAN5 Mach-O.5 a.out.5 ranlib.5 stab.5)

# install(FILES
#  ${MAN5}
#  DESTINATION libexec/darling/usr/share/man/man5)

