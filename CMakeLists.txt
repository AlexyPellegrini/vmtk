# CMake will complain if this is not in this file specifically
cmake_minimum_required(VERSION 3.16.3...4.0)

project(${SKBUILD_PROJECT_NAME})

# vtkAddon comes from Slicer
find_package(Slicer CONFIG REQUIRED)
# We need more modules that the ones exposed by Slicer
find_package(ITK CONFIG REQUIRED)
# Private static library, not a VTK module
add_subdirectory(vtkVmtk/Utilities/OpenNL)

set(modules
  VMTK::Common
  VMTK::IO
  VMTK::Misc
  VMTK::ComputationalGeometry
  VMTK::DifferentialGeometry
  VMTK::Segmentation
)

include(VTKSDKPythonWheelHelper)

vtksdk_build_modules(${SKBUILD_PROJECT_NAME}
  MODULES ${modules}
  DEPENDENCIES slicer_core
)

vtksdk_generate_package_init(${SKBUILD_PROJECT_NAME}
  MODULES ${modules}
  DEPENDENCIES slicer_core
)

vtksdk_install_runtimes_deps(${SKBUILD_PROJECT_NAME}
  MODULES ${modules}
  PATHS
    "$<TARGET_FILE_DIR:ITKCommon>"
)

