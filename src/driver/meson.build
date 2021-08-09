
driver_lib_inc = [
	include_directories('.'),
]

driver_lib = static_library('driver',
    'driver.cpp',
    build_by_default: false,
)

driver_lib_native = static_library('driver_native',
    'driver.cpp',
    build_by_default: false,
    native: true
)

driver_lib_dep = declare_dependency(
	include_directories: driver_lib_inc,
	link_with: driver_lib,
	dependencies: [
		vendor_dep,
	]
)

driver_lib_native_dep = declare_dependency(
	include_directories: driver_lib_inc,
	link_with: driver_lib_native,
	dependencies: [
		vendor_native_dep,
	]
)
