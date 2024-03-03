cmake_minimum_required(VERSION 3.5)
project(HelloWorldGTK)

find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK4 REQUIRED gtk4)

# Add the executable
add_executable(hello-world-gtk main.c)

# Include directories
target_include_directories(hello-world-gtk PUBLIC ${GTK4_INCLUDE_DIRS})

# Link the libraries
target_link_libraries(hello-world-gtk ${GTK4_LIBRARIES})
