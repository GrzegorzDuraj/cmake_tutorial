cmake_minimum_required(VERSION 3.4)
project (Tutorial)

#The version number. 
set (Tutorial_VERSION_MAJOR 1)
set (Tutorial_VERSION_MINOR 0)
set (CMAKE_INSTALL_PREFIX "c:/STM32_Toolchain/Programy_cube/cmake_training/cmake_tutorial_install")


configure_file(
	"${PROJECT_SOURCE_DIR}/TutorialConfig.h.in"
	"${PROJECT_BINARY_DIR}/TutorialConfig.h"
	)

# add the binary tree to the search path for include files
# so that we will find TutorialConfig.h 
include_directories("${PROJECT_BINARY_DIR}")
#include_directories("${PROJECT_BINARY_DIR}/MathFunctions")



option(USE_CLANG "build application with clang" ON)#OFF is the default
option(USE_MYMATH "Use tutorial provided math implementations" ON)

#add th MathFunctions library?
if (USE_MYMATH)
	include_directories("${PROJECT_BINARY_DIR}/MathFunctions")
	add_subdirectory(MathFunctions)
	set (EXTRA_LIBS ${EXTRA_LIBS} MathFunctionsLib)
endif (USE_MYMATH)





#add_executable
add_executable(Tutorial tutorial.cxx)
target_link_libraries (Tutorial ${EXTRA_LIBS})




#add the install targets
install (TARGETS Tutorial DESTINATION bin)
install (FILES "${PROJECT_BINARY_DIR}/TutorialConfig.h" DESTINATION include)
#install (FILES "${PROJECT_BINARY_DIR}/tutorial.cxx" DESTINATION include)
#install (FILES "${PROJECT_BINARY_DIR}/tutorial.cxx" DESTINATION include)