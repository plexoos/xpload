add_executable(test_xpload
    test_xpload.cpp
)

target_link_libraries(test_xpload xpload CURL::libcurl)
target_include_directories(test_xpload PRIVATE ${CMAKE_SOURCE_DIR}/include)


add_test(NAME "test_xpload" COMMAND bash -c "XPLOAD_CONFIG_NAME=dev ./test_xpload --gtName tag1 --minorIOV 9999999999")
