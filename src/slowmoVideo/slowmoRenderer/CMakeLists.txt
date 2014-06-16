
include_directories(..)

set(SRCS
    rendererMain.cpp
    slowmoRenderer_sV.cpp
)
set(SRCS_MOC
    slowmoRenderer_sV.h
)
qt4_wrap_cpp(MOC_OUT ${SRCS_MOC})

link_directories(${FFMPEG_LIBRARY_DIR})
add_executable(slowmoRenderer ${SRCS} ${MOC_OUT})
target_link_libraries(slowmoRenderer sVproj )
install(TARGETS slowmoRenderer DESTINATION ${DEST})
