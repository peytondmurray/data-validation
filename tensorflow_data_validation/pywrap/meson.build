py.install_sources(
    [
        '__init__.py',
    ],
    subdir: 'tensorflow_data_validation/pywrap',
)

py.extension_module(
    'tensorflow_data_validation_extension',
    src: [
      'tensorflow_data_validation_extension.cc'
      'validation_submodule.cc'
    ],
    # include_directories: [],
    install: true,
    subdir: 'tensorflow_data_validation/pywrap',
    dependencies:
)
