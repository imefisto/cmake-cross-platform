cmake_minimum_required(VERSION 3.1...3.14)

project(MyProject VERSION 1.0
	DESCRIPTION "Barebone for cross-platform apps"
	LANGUAGES CXX)

enable_testing()
add_subdirectory(tests)

add_executable(AppProject apps/app.cpp)
