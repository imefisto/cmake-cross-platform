# Prepare "Catch" library for other executables
# wget https://github.com/catchorg/Catch2/releases/download/v2.7.0/catch.hpp -O extern/catch/catch.hpp

set(CATCH_INCLUDE_DIR ${CMAKE_SOURCE_DIR}/extern/catch)
add_library(Catch INTERFACE)
target_include_directories(Catch INTERFACE ${CATCH_INCLUDE_DIR})

set(TEST_SOURCES
	main.cpp
    # some-class-test.cpp
	)

add_executable(tests ${TEST_SOURCES})
target_link_libraries(tests Catch)
target_include_directories(tests PRIVATE ../include/project/)
