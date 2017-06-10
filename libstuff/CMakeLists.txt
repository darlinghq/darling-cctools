project(libstuff)

add_definitions(
	-DCCTOOLS_VERSION="\\"995\\""
	)

set(stuff_sources
  allocate.c errors.c arch.c execute.c bytesex.c rnd.c hppa.c
  swap_headers.c reloc.c version_number.c get_toc_byte_sex.c
  best_arch.c fatals.c arch_usage.c ofile.c ofile_error.c print.c
  set_arch_flag_name.c seg_addr_table.c dylib_table.c
  breakout.c writeout.c checkout.c fatal_arch.c ofile_get_word.c
  vm_flush_cache.c hash_string.c dylib_roots.c guess_short_name.c
  SymLoc.c get_arch_from_host.c crc32.c macosx_deployment_target.c
  symbol_list.c unix_standard_mode.c lto.c llvm.c coff_bytesex.c
  apple_version.c
)

add_library(libstuff OBJECT ${stuff_sources})
