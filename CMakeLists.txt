cmake_minimum_required(VERSION 3.8)

cmake_policy(SET CMP0079 NEW)

project("torque")

add_definitions(-DUNICODE -D_UNICODE)
add_subdirectory("engine")
add_subdirectory("lib")

target_link_libraries(engine 
    zlib 
    libjpeg 
    libpng 
    lungif 
    ${CMAKE_CURRENT_SOURCE_DIR}/lib/xiph/win32/vorbis_static.lib
    ${CMAKE_CURRENT_SOURCE_DIR}/lib/xiph/win32/ogg_static.lib
    ${CMAKE_CURRENT_SOURCE_DIR}/lib/xiph/win32/theora_static.lib
    Winmm
    Imm32
    Ws2_32
)

target_link_options(engine PUBLIC "$<$<C_COMPILER_ID:MSVC>:-SAFESEH:NO>")

target_include_directories(engine PUBLIC "engine")

# this is bad
target_include_directories(engine PUBLIC "lib/openal/win32")
target_include_directories(engine PUBLIC "lib/zlib")
target_include_directories(engine PUBLIC "lib/ljpeg")
target_include_directories(engine PUBLIC "lib/ljpeg/extras")
target_include_directories(engine PUBLIC "lib/lpng")
target_include_directories(engine PUBLIC "lungif")
target_include_directories(engine PUBLIC "lib/xiph/include")