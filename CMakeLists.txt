cmake_minimum_required(VERSION 2.8.7)

project(uriparser C CXX)

include_directories(
   "${CMAKE_CURRENT_SOURCE_DIR}/include"
  )


  file(GLOB URIPARSER_SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/src/*.c")
  file(GLOB URIPARSER_HEADERS  
            "${CMAKE_CURRENT_SOURCE_DIR}/include/*.h" 
            "${CMAKE_CURRENT_SOURCE_DIR}/src/*.h")
 
file(COPY "${CMAKE_CURRENT_SOURCE_DIR}/include/" DESTINATION "${CMAKE_BINARY_DIR}/include/") 
set (CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
add_library(uriparser ${URIPARSER_SOURCES} ${URIPARSER_HEADERS})




	


