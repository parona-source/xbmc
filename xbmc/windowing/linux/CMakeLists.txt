set(SOURCES "")
set(HEADERS "")

if(TARGET ${APP_NAME_LC}::DBus)
  list(APPEND SOURCES OSScreenSaverFreedesktop.cpp)
  list(APPEND HEADERS OSScreenSaverFreedesktop.h)
endif()

if(TARGET ${APP_NAME_LC}::EGL)
  list(APPEND SOURCES WinSystemEGL.cpp)
  list(APPEND HEADERS WinSystemEGL.h)
endif()

if(SOURCES)
  core_add_library(windowing_linux)
endif()
