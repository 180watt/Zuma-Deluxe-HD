cmake_minimum_required(VERSION 3.15)
project(
    ZumaHD
    LANGUAGES C
    VERSION 0.1.0
)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

FILE(GLOB_RECURSE SOURCES RELATIVE ${PROJECT_SOURCE_DIR} "src/*.c")

add_executable(
    ZumaHD

    ${SOURCES}
)

target_include_directories(
    ZumaHD PUBLIC

    "${PROJECT_BINARY_DIR}"
    "${PROJECT_SOURCE_DIR}/src"

    "/usr/local/include" # Expat, SDL2, etc
)

target_link_directories(
    ZumaHD PUBLIC

    "/usr/local/lib" # Expat, SDL2, etc
)

target_link_libraries(
    ZumaHD PRIVATE

    SDL2
    SDL2_image
    SDL2_mixer
    expat

    m
)

add_custom_command(TARGET ${PROJECT_NAME}  POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_directory
                ${CMAKE_CURRENT_SOURCE_DIR}/content
                ${CMAKE_CURRENT_BINARY_DIR}/bin)
