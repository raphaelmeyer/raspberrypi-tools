###############################################################################
cmake_minimum_required(VERSION 3.5)
###############################################################################

project(RaspberryPi-Tools)

include(ExternalProject)

ExternalProject_Add(
  raspberrypi-tools
  URL https://github.com/raspberrypi/tools/archive/master.zip
  DOWNLOAD_NAME rasbperrypi-tools.zip
  CONFIGURE_COMMAND ""
  BUILD_COMMAND ""
  INSTALL_COMMAND ""
  DOWNLOAD_NO_EXTRACT OFF
  )

#add_custom_target(arm-bcm2708
#  COMMAND docker ....
#  )

