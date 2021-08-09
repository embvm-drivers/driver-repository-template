example_app_sources = [
	'main.cpp'
]

example_app = executable('example_app',
	example_app_sources,
	dependencies: [
		driver_lib_dep,
	],
	install: false,
)

executable('example_app_native',
	example_app_sources,
	dependencies: [
		driver_lib_native_dep,
	],
	install: false,
	native: true
)

#############################
# Output Conversion Targets #
#############################

example_app_bin = custom_target('example_app.hex',
	input: example_app,
	output: 'example_app.hex',
	command: host_hex_conversion,
	build_by_default: true
)

example_app_hex = custom_target('example_app.bin',
	input: example_app,
	output: 'example_app.bin',
	command: host_bin_conversion,
	build_by_default: true
)

