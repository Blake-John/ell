aux_source_directory(./src SRC)

add_library(A1 ${SRC})

target_include_directories(A1 PUBLIC ./include)