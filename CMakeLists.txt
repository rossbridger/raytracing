cmake_minimum_required(VERSION 3.16)

project(raytracing LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(raytracing main.cpp
    vec3.h
    color.h
    ray.h
    hittable.h
    sphere.h
    hittable_list.h
    rtweekend.h
    interval.h
    camera.h
    material.h
    aabb.h
    bvh.h
    texture.h
    external/stb_image.h
    rtw_stb_image.h
    perlin.h
    quad.h
    constant_medium.h
    onb.h
    pdf.h
)

include(GNUInstallDirs)
install(TARGETS raytracing
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
)
