project(libstuff)

add_definitions(
	-DCURRENT_PROJECT_VERSION="\\\"${CCTOOLS_VERSION}\\\""
)

set(stuff_sources
  allocate.c
  apple_version.c
  arch.c
  arch_usage.c
  args.c
  best_arch.c
  breakout.c
  bytesex.c
  checkout.c
  coff_bytesex.c
  crc32.c
  dylib_roots.c
  dylib_table.c
  errors.c
  execute.c
  fatal_arch.c
  fatals.c
  get_arch_from_host.c
  get_toc_byte_sex.c
  guess_short_name.c
  hash_string.c
  hppa.c
  llvm.c
  lto.c
  macosx_deployment_target.c
  ofile.c
  ofile_error.c
  ofile_get_word.c
  print.c
  reloc.c
  rnd.c
  seg_addr_table.c
  set_arch_flag_name.c
  swap_headers.c
  symbol_list.c
  SymLoc.c
  unix_standard_mode.c
  version_number.c
  vm_flush_cache.c
  write64.c
  writeout.c
)

# can't be an object library because Apple relies on certain behavior specific to how static libraries work
# (like ignoring duplicate symbols)
add_darling_static_library(libstuff FAT SOURCES ${stuff_sources})
