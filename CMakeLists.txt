cmake_minimum_required(VERSION 2.8)
set (CMAKE_CXX_STANDARD 11)
set(CMAKE_BUILD_TYPE Debug)
project(bird_flocking)
add_executable(bird_flocking src/example1.cpp src/InitShader.cpp)

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
find_package(GLEW REQUIRED)
find_package(glm REQUIRED)
include_directories( ${OPENGL_INCLUDE_DIRS}  ${GLUT_INCLUDE_DIRS} ${GLEW_INCLUDE_DIRS} ${GLM_INCLUDE_DIRS} include/)

target_link_libraries(bird_flocking ${OPENGL_LIBRARIES} ${GLUT_LIBRARY} ${GLEW_LIBRARY} ${GLM_LIBRARY})