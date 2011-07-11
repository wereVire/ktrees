set(ktrees_SRCS
   ktrees.cpp
   main.cpp
   ktreesview.cpp
 )

kde4_add_ui_files(ktrees_SRCS ktreesview_base.ui prefs_base.ui)

kde4_add_kcfg_files(ktrees_SRCS settings.kcfgc )

kde4_add_executable(ktrees ${ktrees_SRCS})

target_link_libraries(ktrees ${KDE4_KDEUI_LIBS} )

install(TARGETS ktrees ${INSTALL_TARGETS_DEFAULT_ARGS} )


########### install files ###############

install( PROGRAMS ktrees.desktop  DESTINATION ${XDG_APPS_INSTALL_DIR} )
install( FILES ktrees.kcfg  DESTINATION  ${KCFG_INSTALL_DIR} )
install( FILES ktreesui.rc  DESTINATION  ${DATA_INSTALL_DIR}/ktrees )
