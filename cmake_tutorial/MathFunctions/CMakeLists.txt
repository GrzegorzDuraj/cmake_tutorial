add_library(MathFunctionsLib MySqrt.cxx)
install (TARGETS MathFunctionsLib DESTINATION bin)


#install (FILES "${PROJECT_BINARY_DIR}/TutorialConfig.h" DESTINATION include)
