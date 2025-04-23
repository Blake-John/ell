add_library(M1 ./src/M1.cpp)

target_include_directories(M1 PUBLIC ./include)
target_link_libraries(M1 A1)