#add the executable target named TestHello
add_executable(TestHello test_hello.cpp)
target_link_libraries(TestHello PRIVATE basic)
add_test(NAME test_hello COMMAND test_hello)

#add the executable target named TestVersionHello
add_executable(TestVersionHello test_version.cpp)
target_link_libraries(TestVersionHello PRIVATE basic)
add_test(NAME test_version COMMAND test_version)