cmake_minimum_required(VERSION 3.0.0)
project(MKL.Template VERSION 0.1.0)

include(CTest)
enable_testing()
set(MKLROOT /opt/intel/compilers_and_libraries_2019.5.281/mac/mkl)
link_directories(${MKLROOT}/lib)
include_directories(${MKLROOT}/include)
add_compile_options(-m64)
add_executable(${PROJECT_NAME} main.cpp)

target_link_libraries(${PROJECT_NAME} mkl_rt
    pthread
    m
    dl
    )
# set(CPACK_PROJECT_NAME ${PROJECT_NAME})
# set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
# include(CPack)
