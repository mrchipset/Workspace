cmake_minimum_required(VERSION 3.0.0)
project(QML-QuickStart VERSION 0.1.0)

set(Qt5_DIR /usr/local/Cellar/qt/5.13.2/lib/cmake/Qt5)
find_package(Qt5 COMPONENTS Widgets Qml Widgets Quick REQUIRED)

add_subdirectory(src)
