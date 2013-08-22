cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project(gtk2_practice)

#file(MAKE_DIRECTORY ../${bin})
#########################################################
# FIND GTK2.0
#########################################################
#Require GTK 2.6 or later
#find_package(GTK2 2.6 REQUIRED gtk)

       

#Require GTK 2.10 or later and Glade
#find_package(GTK2 2.10 REQUIRED gtk glade)

#Search for GTK/GTKMM 2.8 or later
find_package(GTK2 2.8 COMPONENTS gtk gtkmm)
       

if(GTK2_FOUND)
  include_directories(${GTK2_INCLUDE_DIRS})

  add_executable(../bin/gtk2_simple gtk2_simple/src/gtk2_simple.c)
  target_link_libraries(../bin/gtk2_simple ${GTK2_LIBRARIES})

  add_executable(../bin/gtk2_centering gtk2_simple/src/gtk2_centering.c)
  target_link_libraries(../bin/gtk2_centering ${GTK2_LIBRARIES})

  add_executable(../bin/gtk2_application_icon gtk2_simple/src/gtk2_application_icon.c)
  target_link_libraries(../bin/gtk2_application_icon ${GTK2_LIBRARIES})

  add_executable(../bin/gtk2_buttons gtk2_simple/src/gtk2_buttons.c)
  target_link_libraries(../bin/gtk2_buttons ${GTK2_LIBRARIES})

endif()






