cmake_minimum_required(VERSION 3.10)

if(NOT TARGET basic)
	# set the project name
	project(HelloProjTest)
	find_package(HelloProj)
	enable_testing()
endif()



#add the executable target named TestHello
add_executable(TestHello test_hello.cpp)
target_link_libraries(TestHello PRIVATE basic)
add_test(NAME test_hello COMMAND TestHello)

#add the executable target named TestVersionHello
add_executable(TestVersionHello test_version.cpp)
target_link_libraries(TestVersionHello PRIVATE basic)
add_test(NAME test_version COMMAND TestVersionHello)