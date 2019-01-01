cmake_minimum_required(VERSION 2.8)

set(TARGET_NAME myapp)

project(app_project)

include_directories("/usr/local/Cellar/glfw/3.2.1/include" "glad/include")

add_executable(${TARGET_NAME} src/main.cpp glad/src/glad.c)

target_link_libraries(${TARGET_NAME} "/usr/local/Cellar/glfw/3.2.1/lib/libglfw.3.2.dylib")

install(TARGETS ${TARGET_NAME} DESTINATION bin)
