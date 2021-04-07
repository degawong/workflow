
PROJECT(harpocrates)

set(CMAKE_CXX_STANDARD 20)

cmake_minimum_required(VERSION 3.0)

add_definitions("-g")

file(
	GLOB_RECURSE
	src_file
	${CMAKE_CURRENT_SOURCE_DIR}/*.h
	${CMAKE_CURRENT_SOURCE_DIR}/*.cc
	${CMAKE_CURRENT_SOURCE_DIR}/*.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/*.hpp
)

add_executable(
	${PROJECT_NAME}
	# ${src_file}
	harpocrates.cpp
)

target_include_directories(
	${PROJECT_NAME}
	PUBLIC
	${CMAKE_CURRENT_SOURCE_DIR}
)