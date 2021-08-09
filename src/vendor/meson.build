# TODO:
# This is a home for any vendor-related files you want to include.
# We recommend building them as a standalone library.

vendor_inc = [
    include_directories('.'),
]

vendor_sources = [
    files('example.c')
]

clangtidy_files += [
    vendor_sources,
    # Add header-only files here if you want them linted
]

# If you have a vendority with a source file, add it with a subdir() command
# or add it to the `vendor_sources` list above
# subdir('dir')

libvendor = static_library('vendor',
    vendor_sources,
    include_directories: vendor_inc,
    install: false,
    build_by_default: false,
)

libvendor_native = static_library('vendor_native',
    vendor_sources,
    include_directories: vendor_inc,
    install: false,
    build_by_default: false,
    native: true
)

vendor_dep = declare_dependency(
    include_directories: vendor_inc,
    link_with: libvendor,
)

vendor_native_dep = declare_dependency(
    include_directories: vendor_inc,
    link_with: libvendor_native,
)
