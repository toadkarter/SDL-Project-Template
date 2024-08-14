cmake_minimum_required(VERSION 3.10)

project(ProjectName)

find_package(SDL2 REQUIRED)
find_package(SDL2_image REQUIRED)
include_directories(include ${SDL2_INCLUDE_DIRS} ${SDL2_IMAGE_INCLUDE_DIRS})

file(GLOB SRC_FILES "src/*.c")

# Add executable target
add_executable(${PROJECT_NAME} ${SRC_FILES})
target_link_libraries(${PROJECT_NAME} ${SDL2_LIBRARIES} ${SDL2_IMAGE_LIBRARIES})