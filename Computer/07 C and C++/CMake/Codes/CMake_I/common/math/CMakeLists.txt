find_package(OpenCV REQUIRED)

add_library(math ./src/Math.cpp)

target_include_directories(math PUBLIC ./include)

target_include_directories(math PUBLIC ${OpenCV_INCLUDE_DIRS})
target_link_libraries(math ${OpenCV_LIBS})