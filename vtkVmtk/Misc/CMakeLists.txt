set (classes
  vtkvmtkAnnularCapPolyData
  vtkvmtkBoundaryLayerGenerator
  vtkvmtkCurvedMPRImageFilter
  vtkvmtkImageBoxPainter
  vtkvmtkIterativeClosestPointTransform
  vtkvmtkLevelSetSigmoidFilter
  vtkvmtkLinearizeMeshFilter
  vtkvmtkLinearToQuadraticMeshFilter
  vtkvmtkLinearToQuadraticSurfaceMeshFilter
  vtkvmtkMeshLambda2
  vtkvmtkMeshProjection
  vtkvmtkMeshVelocityStatistics
  vtkvmtkMeshVorticity
  vtkvmtkMeshWallShearRate
  vtkvmtkPolyDataNetworkExtraction
  vtkvmtkPolyDataNormalPlaneEstimator
  vtkvmtkPolyDataKiteRemovalFilter
  vtkvmtkPolyDataSizingFunction
  vtkvmtkPolyDataToUnstructuredGridFilter
  vtkvmtkRBFInterpolation
  vtkvmtkSimpleCapPolyData
  vtkvmtkSmoothCapPolyData
  vtkvmtkStreamlineClusteringFilter
  vtkvmtkStreamlineOsculatingCentersFilter
  vtkvmtkStreamlineToParticlesFilter
  vtkvmtkSurfaceDistance
  vtkvmtkSurfaceProjection
  vtkvmtkTopologicalSeamFilter
  vtkvmtkUnstructuredGridTetraFilter
)

vtk_module_add_module(VMTK::Misc
  EXPORT_MACRO_PREFIX VTK_VMTK_IO
  CLASSES ${classes}
)

vtk_module_definitions(VMTK::Misc PRIVATE vtkvmtkMisc_EXPORTS=1)
