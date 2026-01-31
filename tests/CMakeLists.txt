include(FetchContent)
FetchContent_Declare(
    googletest
    GIT_REPOSITORY https://github.com/google/googletest.git
    GIT_TAG        v1.14.0
)
FetchContent_MakeAvailable(googletest)

add_executable(Google_Tests_run OrderBookTest.cpp)

target_link_libraries(Google_Tests_run 
    PRIVATE
        ${CMAKE_PROJECT_NAME}_lib
        GTest::gtest_main
)
