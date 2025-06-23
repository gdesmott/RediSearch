# Build the `buffer` module as a standalone static library
# This is required so we can benchmark C code from Rust relying on buffer symbols.
file(GLOB BUFFER_SOURCES "buffer.c")
add_library(buffer STATIC ${BUFFER_SOURCES})
target_include_directories(buffer PRIVATE . ..)