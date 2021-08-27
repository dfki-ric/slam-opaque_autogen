cmake_minimum_required(VERSION 3.1)
project(opaque_autogen VERSION 0.0)

install(
    DIRECTORY
        ${PROJECT_SOURCE_DIR}/orogen
    DESTINATION
        ${CMAKE_INSTALL_PREFIX}/share
)

