cmake_minimum_required(VERSION 2.8.3)
project(jsk_arc2017_baxter)

find_package(catkin REQUIRED)

################################################
## Declare ROS messages, services and actions ##
################################################

# XXX

################################################
## Declare ROS dynamic reconfigure parameters ##
################################################

# XXX

###################################
## catkin specific configuration ##
###################################

catkin_package()

###########
## Build ##
###########

# XXX

#############
## Install ##
#############

# XXX

#############
## Testing ##
#############

if(CATKIN_ENABLE_TESTING)
  find_package(jsk_tools REQUIRED)
  find_package(jsk_2016_01_baxter_apc REQUIRED)
  if(${jsk_tools_VERSION} VERSION_GREATER 2.0.13)
    jsk_tools_add_shell_test(COMMAND "rosrun jsk_apc2016_common euslint ${PROJECT_SOURCE_DIR}")
  endif()
endif()
