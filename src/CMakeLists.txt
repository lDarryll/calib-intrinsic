# add_library(monocular_calibration
# 	../include/MonocularCalibration.h MonocularCalibration.cpp
# )
# add_executable(calib main.cpp)
# target_link_libraries(calib monocular_calibration ${OpenCV_LIBS})
#-----------------------------------------------------------------------------

add_executable(calib_intrinsic calib_intrinsic.cpp)
target_link_libraries(calib_intrinsic ${OpenCV_LIBS})

