set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -g3 -gdwarf-2 -Os -mcpu=cortex-m3 -mthumb")

add_library(tinygpsplus STATIC TinyGPS++.h TinyGPS++.cpp)
target_include_directories(tinygpsplus PRIVATE /usr/local/src/particle/firmware/hal/src/stm32 /usr/local/src/particle/firmware/communication/src /usr/local/src/particle/firmware/hal/inc /usr/local/src/particle/firmware/hal/shared /usr/local/src/particle/firmware/services/inc /usr/local/src/particle/firmware/user/inc /usr/local/src/particle/firmware/system/inc /usr/local/src/particle/firmware/wiring/inc /usr/local/src/particle/firmware/hal/inc)
target_compile_definitions(tinygpsplus PRIVATE ARDUINO=10800 RELEASE_BUILD)

install(TARGETS tinygpsplus
        ARCHIVE DESTINATION lib)
