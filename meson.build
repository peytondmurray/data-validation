project(
  'tensorflow_data_validation',
  'cpp',
  version: '4.00'
)


# Dependency wrap files for each of the http_archive entries in WORKSPACE
# rules_foreign_cc_dep = dependency('rules_foreign_cc', version: '0.9.0', fallback: ['rules_foreign_cc', 'rules_foreign_cc_dep'])
# bazel_skylib_dep = dependency('bazel_skylib', fallback: ['bazel_skylib', 'bazel_skylib_dep'])
# io_bazel_rules_closure_dep = dependency('io_bazel_rules_closure', fallback: ['io_bazel_rules_closure', 'io_bazel_rules_closure_dep'])
rules_proto_dep = dependency('rules_proto', version: '4.0.0', fallback: ['rules_proto', 'rules_proto_dep'])
protobuf_dep = dependency('protobuf', version: '3.21.9', fallback: ['protobuf', 'protobuf_dep'])
six_archive_dep = dependency('six_archive', version: '1.10.0', fallback: ['six_archive', 'six_dep'])
absl_dep = dependency('absl', fallback: ['absl', 'absl_dep'])
zetasql_dep = dependency('zetasql', fallback: ['zetasql', 'zetasql_dep'])
platforms_dep = dependency('platforms', version: '0.0.6', fallback: ['platforms', 'platforms_dep'])
pybind11_dep = dependency('pybind11', version: '2.11.1', fallback: ['pybind11', 'pybind11_dep'])

py = import('python').find_installation(pure: false)

subdir('tensorflow_data_validation')
