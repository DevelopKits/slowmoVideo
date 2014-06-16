
message(STATUS "slowmoInfo Bundle will be : ${MACOSX_BUNDLE} =>  ${PROJECT_NAME} ")

link_directories(${FFMPEG_LIBRARY_DIR})
add_executable(slowmoInfo slowmoInfo.cpp)
target_link_libraries(slowmoInfo sV ${EXTERNAL_LIBS})

install(TARGETS ${slowmoUI}
        BUNDLE DESTINATION . COMPONENT Runtime
        RUNTIME DESTINATION ${BIN_INSTALL_DIR} COMPONENT Runtime)
#install(TARGETS slowmoInfo DESTINATION ${DEST})
