cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  test2.c
)

add_executable(paltest_pal_except_test2
  ${SOURCES}
)

add_dependencies(paltest_pal_except_test2 CoreClrPal)

target_link_libraries(paltest_pal_except_test2
  pthread
  rt
  m
  CoreClrPal
)
