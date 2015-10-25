cmake_minimum_required(VERSION 3.3)
project(triangle)

# Tell CMake to run moc when necessary:
set(CMAKE_AUTOMOC ON)

# As moc files are generated in the binary dir, tell CMake
# to always look for includes there:
set(CMAKE_INCLUDE_CURRENT_DIR ON)

# Widgets finds its own dependencies.
find_package(Qt5Widgets REQUIRED)


add_executable(triangle main.cpp openglwindow.cpp)

qt5_use_modules(triangle Widgets)