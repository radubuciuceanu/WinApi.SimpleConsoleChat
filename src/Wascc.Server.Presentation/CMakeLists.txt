cmake_minimum_required(VERSION ${CMAKE_MINIMUM_REQUIRED_VERSION})

project(${WASCC_SERVER_PRESENTATION} VERSION ${WACC_SERVER_PRESENTATION_VERSION})

file(GLOB HEADERS ./include/${WASCC_SERVER_PRESENTATION}/*.h)
file(GLOB SOURCES ./src/${WASCC_SERVER_PRESENTATION}/*.cpp)

add_executable(${WASCC_SERVER_PRESENTATION} ${SOURCES} ${HEADERS})

target_link_libraries(${WASCC_SERVER_PRESENTATION} PRIVATE ${WASCC_CONSOLE_IO} ${WASCC_NETWORKING_IO})

target_include_directories(${WASCC_SERVER_PRESENTATION} PUBLIC ./include)

target_compile_definitions(${WASCC_SERVER_PRESENTATION} PRIVATE WASCC_SERVER_PRESENTATION=1)