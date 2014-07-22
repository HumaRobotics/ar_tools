
cmake_minimum_required(VERSION 2.8.3)
project(artoolkit)


find_package(catkin REQUIRED)


find_package(GLUT)
find_package(OpenGL)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES artoolkit

)


message(Making artoolkit)

#set(ENV{ARTOOLKIT_CONFIG} "v4l2src device=/dev/video0 use-fixed-fps=false ! ffmpegcolorspace ! capsfilter caps=video/x-raw-rgb,bpp=24 ! identity name=artoolkit ! fakesink")
execute_process(COMMAND make all	 
				WORKING_DIRECTORY ${CATKIN_DEVEL_PREFIX}/../src/ar_tools/artoolkit/)
message(Done making artoolkit)
