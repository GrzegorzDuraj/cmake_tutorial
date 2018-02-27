add_library(MathFunctionsLib MySqrt.cxx)
install (TARGETS MathFunctionsLib DESTINATION bin)
install (FILES "${PROJECT_BINARY_DIR}/MathFunctions.h" DESTINATION include)
install (FILES "${PROJECT_SOURCE_DIR}/MathFunctions.h" DESTINATION include)

#install (FILES "${PROJECT_BINARY_DIR}/TutorialConfig.h" DESTINATION include)
