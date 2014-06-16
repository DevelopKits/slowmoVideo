
include_directories(..)

set(SRCS
    visualizeFlow.cpp
)

link_directories(${FFMPEG_LIBRARY_DIR})
add_executable(slowmoVisualizeFlow ${SRCS})
target_link_libraries(slowmoVisualizeFlow sVvis )

install(TARGETS slowmoVisualizeFlow DESTINATION ${DEST})
