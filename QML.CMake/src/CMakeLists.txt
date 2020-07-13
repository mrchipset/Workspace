project(Demo VERSION 0.1)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

find_package(Qt5 COMPONENTS Core Gui Widgets Qml Quick REQUIRED)

set(HEADERS 

)

set(SOURCES 
    main.cpp
    
)

set(QMLS
    main.qml
)

qt5_add_resources(RCC_SOURCES qml.qrc)

add_executable(${PROJECT_NAME} ${SOURCES} ${RCC_SOURCES})
target_link_libraries(${PROJECT_NAME}  Qt5::Core Qt5::Gui Qt5::Qml Qt5::Quick Qt5::Widgets)