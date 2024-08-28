py.install_sources(
  '__init__.py',
  subdir: 'tensorflow_data_validation/anomalies'
)

py.extension_module(
    'slicetools',
    'slicetools.pyx',
    install: true,
    subdir: 'versioned_hdf5',
    dependencies: compiled_deps,
    cython_args: ['--cplus'],
    override_options : ['cython_language=cpp'],
)
