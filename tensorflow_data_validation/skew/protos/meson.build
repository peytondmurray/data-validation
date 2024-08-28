protoc = find_program('protoc', required : true)
protobuf_dep = dependency('protobuf', required : true)

gen = generator(
  protoc,
  output: ['@BASENAME@.pb.cc', '@BASENAME@.pb.h'],
  arguments: ['--proto_path=@CURRENT_SOURCE_DIR@', '--cpp_out=@BUILD_DIR@', '@INPUT@'],
)
generated = gen.process('feature_skew_results.proto')

# See the following for more information:
# https://stackoverflow.com/questions/56103465/generate-protobuf-python-source-with-meson
py_proc = custom_target(
  'py_proto',
  command: [ 'cp', '@INPUT@', '@OUTPUT@' ],
  input : generated,
  output : 'feature_skew_results_proto_py_pb2.py',
  build_by_default : true,
)

py.install_sources(
    [
        '__init__.py',
        'feature_skew_results_proto_py_pb2.py',
    ],
    subdir: 'tensorflow_data_validation/skew/protos',
)
