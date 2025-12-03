cmake_minimum_required(VERSION 3.10)
project(OpenGLTestSuit VERSION 0.1 LANGUAGES C CXX)

find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)
find_package(glfw3 REQUIRED)

add_executable(opengl_test src/main.cpp)

set_property(TARGET opengl_test PROPERTY CXX_STANDARD 17)

target_link_libraries(opengl_test
    OpenGL::GL
    GLEW::GLEW
    glfw
)
