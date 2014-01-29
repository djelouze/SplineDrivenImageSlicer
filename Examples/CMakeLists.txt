### Find VTK
INCLUDE (${CMAKE_ROOT}/Modules/FindVTK.cmake)
IF (USE_VTK_FILE)
  INCLUDE(${USE_VTK_FILE})
ENDIF (USE_VTK_FILE)

ADD_EXECUTABLE( StraightenedReformattedVolume StraightenedReformattedVolume.cxx )
TARGET_LINK_LIBRARIES( StraightenedReformattedVolume vtkSDIS ${VTK_LIBRARIES} )

ADD_EXECUTABLE( SplineDrivenImageSlicer SplineDrivenImageSlicer.cxx )
TARGET_LINK_LIBRARIES( SplineDrivenImageSlicer vtkSDIS ${VTK_LIBRARIES} )
