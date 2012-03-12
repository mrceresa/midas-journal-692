cmake_minimum_required(VERSION 2.6)
INCLUDE(${CMAKE_SOURCE_DIR}/IJMacros.txt)

PROJECT(itkFastBilateralImageFilter)

SET(Required_Packages ITK)

FOREACH(Package ${Required_Packages})
  LOADPACKAGE(${Package})
ENDFOREACH(Package)

ADD_EXECUTABLE(FastBilateral2D_UC FastBilateral2D_UC_main.cxx)  
TARGET_LINK_LIBRARIES(FastBilateral2D_UC ITKCommon ITKIO)

ADD_EXECUTABLE(FastBilateral2D_SS FastBilateral2D_SS_main.cxx)  
TARGET_LINK_LIBRARIES(FastBilateral2D_SS ITKCommon ITKIO)

ADD_EXECUTABLE(FastBilateral3D_SS FastBilateral3D_SS_main.cxx)  
TARGET_LINK_LIBRARIES(FastBilateral3D_SS ITKCommon ITKIO)



