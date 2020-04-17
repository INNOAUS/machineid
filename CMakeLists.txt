project("machineid")

cmake_minimum_required(VERSION 3.5)

set(CMAKE_CXX_STANDARD 11)

add_library(${PROJECT_NAME} STATIC src/machineid/machineid.cpp)
target_include_directories(machineid
	PRIVATE src
	PUBLIC include)

INSTALL (
  FILES ${CMAKE_SOURCE_DIR}/include/machineid/machineid.h
  DESTINATION include/machineid
  )

INSTALL(TARGETS ${PROJECT_NAME}
    LIBRARY DESTINATION lib
    ARCHIVE DESTINATION lib
    RUNTIME DESTINATION lib)
