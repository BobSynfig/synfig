add_library(mod_yuv420p MODULE
        "${CMAKE_CURRENT_LIST_DIR}/main.cpp"
        "${CMAKE_CURRENT_LIST_DIR}/trgt_yuv.cpp"
)

target_link_libraries(mod_yuv420p libsynfig)

install (
    TARGETS mod_yuv420p
    DESTINATION lib/synfig/modules
)
