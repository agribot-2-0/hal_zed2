cmake_minimum_required(VERSION 3.0.2)
project(hal_zed2)

add_compile_options(-std=c++17 -Wall -Wextra -pedantic -Werror)

find_package(catkin REQUIRED COMPONENTS
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES hal_zed2
#  CATKIN_DEPENDS zed_wrapper
#  DEPENDS system_lib
)

###########
## Build ##
###########

include_directories(
  ${catkin_INCLUDE_DIRS}
)

#############
## Install ##
#############

install(DIRECTORY launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
