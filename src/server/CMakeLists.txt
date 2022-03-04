add_executable(server main.cpp)

target_include_directories(server PUBLIC proto)

target_link_libraries(server proto)
