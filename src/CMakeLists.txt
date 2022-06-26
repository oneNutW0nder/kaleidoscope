# This will be changed later when more parts are implemented
project(LEXER)

# Add includes used by 'lexer' here and link them on the final line
# target_include_directories(../include/)
add_executable(lexer lexer.cpp)
target_link_libraries(lexer)
