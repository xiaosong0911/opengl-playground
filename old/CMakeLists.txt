include_directories("${CMAKE_INSTALL_PREFIX}/include")
add_subdirectory(imgui-app)
include_directories(imgui-app)
include_directories(imgui-app/imgui)

add_executable(shadertoy
    shadertoy.cc
    )
target_link_libraries(shadertoy
    imgui-app
    )

add_executable(particles
    particles-demo.cc
    )
target_link_libraries(particles
    imgui-app
    )

add_executable(simple-demo
    simple-demo.cc
    simple.h
    )
target_link_libraries(simple-demo
    imgui-app
    )

add_executable(main
    main.cc
    )
target_link_libraries(main
    imgui-app
    )
