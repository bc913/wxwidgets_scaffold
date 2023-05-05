project(wx_ui)

add_executable(${PROJECT_NAME} WIN32 "")

target_sources(${PROJECT_NAME} 
    PRIVATE
        main.cpp
)

# target_include_directories(
#     ${PROJECT_NAME}
#     PUBLIC
#     $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include> # or ${PROJECT_SOURCE_DIR}/include
#     $<INSTALL_INTERFACE:${CMAKE_INSTALL_INCLUDEDIR}> # or include
# )

target_link_libraries(${PROJECT_NAME} wx::core wx::base)

# Install
install(
    TARGETS ${PROJECT_NAME}
    EXPORT ${PROJECT_NAME}Targets
    ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
    #PUBLIC_HEADER DESTINATION ${CMAKE_INSTALL_INCLUDEDIR} # Windows ONly
)
