add_subdirectory(native)
add_subdirectory(core)

if (WITH_AUTH)
  add_subdirectory(auth)
endif()

if (WITH_ANALYSIS)
  add_subdirectory(analysis)
endif()

if (WITH_GUI)
  add_subdirectory(ui)
  add_subdirectory(gui)
endif()

add_subdirectory(providers)
if (NOT IOS)
  add_subdirectory(crssync)
endif()

if ((WIN32 AND NOT MINGW) OR (UNIX AND NOT APPLE AND NOT ANDROID AND NOT IOS))
  add_subdirectory(crashhandler)
endif()
add_subdirectory(test)

if (WITH_DESKTOP)
  add_subdirectory(app)
  add_subdirectory(plugins)
endif()

if (WITH_3D)
  add_subdirectory(3d)
endif()

if (WITH_BINDINGS)
  add_subdirectory(python)
endif()

if (WITH_SERVER)
  add_subdirectory(server)
endif()

if (WITH_CUSTOM_WIDGETS)
  add_subdirectory(customwidgets)
endif()

if (WITH_QUICK)
  add_subdirectory(quickgui)
endif()

if (WITH_QGIS_PROCESS)
  add_subdirectory(process)
endif()
