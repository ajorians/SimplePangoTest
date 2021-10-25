cmake_minimum_required(VERSION 3.10)

project(SimplePangoTest)

find_package(PkgConfig REQUIRED)
pkg_check_modules(deps REQUIRED IMPORTED_TARGET glib-2.0 harfbuzz pango cairo pangocairo)

#####################

add_executable(SimplePangoTest main.cpp)

target_link_libraries(SimplePangoTest PRIVATE
	PkgConfig::deps
	)
