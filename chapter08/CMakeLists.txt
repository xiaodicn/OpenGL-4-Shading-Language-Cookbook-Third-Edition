set( target chapter08 )
set( chapter08_SOURCES
	frustum.cpp
	main.cpp
	sceneao.cpp
	scenejitter.cpp
	scenepcf.cpp
	sceneshadowmap.cpp
	sceneshadowvolume.cpp )

add_executable( ${target} ${chapter08_SOURCES} )

target_compile_definitions(${target}
		PRIVATE
		GLFW_INCLUDE_NONE
		)

target_link_libraries( ${target}
		PRIVATE
		ingredients
		glfw
		${OPENGL_gl_LIBRARY}
		)


file(COPY ${CMAKE_CURRENT_SOURCE_DIR}/shader DESTINATION ${CMAKE_CURRENT_BINARY_DIR})
