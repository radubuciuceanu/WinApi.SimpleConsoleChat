cmake_minimum_required(VERSION ${CMAKE_MINIMUM_REQUIRED_VERSION})

project(${WASCC_CLIENT_PRESENTATION} VERSION ${WASCC_CLIENT_PRESENTATION_VERSION})

file(GLOB HEADERS ./include/${WASCC_CLIENT_PRESENTATION}/*.h)
file(GLOB SOURCES ./src/${WASCC_CLIENT_PRESENTATION}/*.cpp)

add_executable(${WASCC_CLIENT_PRESENTATION} ${SOURCES} ${HEADERS})

target_link_libraries(${WASCC_CLIENT_PRESENTATION} PRIVATE ${WASCC_CONSOLE_IO} ${WASCC_NETWORKING_IO})