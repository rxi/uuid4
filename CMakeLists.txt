cmake_minimum_required(VERSION 3.7)
# project(uuid4 VERSION 0.4)

set(headers "src/uuid4.h")
set(sources "src/uuid4.c")

add_library(uuid4 ${sources} ${headers})
target_include_directories(uuid4 PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/src")

install(TARGETS uuid4 EXPORT uuid4 ARCHIVE DESTINATION "lib/" CONFIGURATIONS "Release" INCLUDES DESTINATION "include/uuid4")
install(FILES ${headers} DESTINATION "include/uuid")
