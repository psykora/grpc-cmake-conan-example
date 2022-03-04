add_executable(client main.cpp)

target_include_directories(client PUBLIC proto)

target_link_libraries(client proto)
