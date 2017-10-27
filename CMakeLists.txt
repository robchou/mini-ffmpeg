project(ffmpeg)
cmake_minimum_required(VERSION 2.8)
set(SRC_FILES ./libavcodec/allcodecs.c
              ./libavcodec/dsputil.c
              ./libavcodec/imgconvert.c
              ./libavcodec/utils_codec.c
              ./libavcodec/msrle.c
              ./libavcodec/truespeech.c
              ./libavformat/allformats.c
              ./libavformat/avidec.c
              ./libavformat/avio.c
              ./libavformat/aviobuf.c
              ./libavformat/cutils.c
              ./libavformat/file.c
              ./libavformat/utils_format.c
              ffplay.c
    )

include_directories(./libavutil ./libavcodec ./libavformat)

add_executable(ffplay ${SRC_FILES})

target_link_libraries(ffplay SDL SDLmain)
