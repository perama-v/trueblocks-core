# minimum cmake version supported
cmake_minimum_required (VERSION 3.0)

# library project
project (cache)

# The sources to be used
file(GLOB SOURCE_FILES "*.cpp" "classes/*.cpp")

# Output
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_SOURCE_DIR}/libs")

# Define the executable to be generated
add_library(${PROJECT_NAME} STATIC ${SOURCE_FILES})

# Headers require
target_include_directories(${PROJECT_NAME} PUBLIC "${CMAKE_SOURCE_DIR}/libs/utillib")
target_include_directories(${PROJECT_NAME} PUBLIC "${CMAKE_SOURCE_DIR}/libs/etherlib")
target_include_directories(${PROJECT_NAME} PUBLIC "${CMAKE_SOURCE_DIR}/libs/acctlib")
target_include_directories(${PROJECT_NAME} PUBLIC "${CMAKE_SOURCE_DIR}/libs/pinlib")
target_include_directories(${PROJECT_NAME} PUBLIC "${CMAKE_SOURCE_DIR}/libs/cachelib")
