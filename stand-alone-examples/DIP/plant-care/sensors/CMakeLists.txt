project(sensors)

include_directories(${PROJECT_SOURCE_DIR}/include)

set(SOURCE
    ${PROJECT_SOURCE_DIR}/include/sensors/SunlightSensor.hpp
    ${PROJECT_SOURCE_DIR}/include/sensors/MoistureSensor.hpp
    ${PROJECT_SOURCE_DIR}/include/interfaces/WaterDevice.hpp
    ${PROJECT_SOURCE_DIR}/include/interfaces/WindowDevice.hpp
    ${PROJECT_SOURCE_DIR}/src/SunlightSensor.cpp
    ${PROJECT_SOURCE_DIR}/src/MoistureSensor.cpp
)

add_library(${PROJECT_NAME} STATIC ${SOURCE})
target_include_directories(${PROJECT_NAME} PUBLIC ${PROJECT_SOURCE_DIR}/include)
