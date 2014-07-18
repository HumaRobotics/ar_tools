
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
execute_process(COMMAND make all	 
				WORKING_DIRECTORY ${CATKIN_DEVEL_PREFIX}/../src/ar_tools/artoolkit/)
message(Done making artoolkit)