py.install_sources(
    [
        '__init__.py',
        'constants.py',
        'types.py',
        'types_test.py',
        'version.py',
    ],
    subdir: 'tensorflow_data_validation',
)

subdir('anomalies')
subdir('api')
subdir('arrow')
subdir('coders')
subdir('integration_tests')
subdir('pywrap')
subdir('skew')
subdir('statistics')
subdir('utils')

anomalies_srcs = []
foreach file : anomalies_src_files
  anomalies_srcs += files(join_paths('anomalies', file))
endforeach

pywrap_srcs = []
foreach file : pywrap_src_files
  pywrap_srcs += files(join_paths('pywrap', file))
endforeach

library(
  'anomalies',
  anomalies_srcs,
  # include_directories: 'anomalies',
  include_directories: ['..'],
)

py.extension_module(
    'tensorflow_data_validation_extension',
    pywrap_srcs,
    install: true,
    subdir: 'tensorflow_data_validation/pywrap',
)
