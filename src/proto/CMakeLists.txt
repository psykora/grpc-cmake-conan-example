protobuf_generate_grpc_cpp(GRPC_SRCS GRPC_HDRS helloworld.proto)
protobuf_generate_grpc_python(GRPC_PY_SRCS helloworld.proto)

add_library(proto ${GRPC_SRCS} ${GRPC_HDRS})

target_include_directories(proto PUBLIC "${_gRPC_PROTO_GENS_DIR}")

target_link_libraries(proto
    gRPC::grpc++_unsecure
)
