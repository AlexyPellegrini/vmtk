vtk_module_add_module(VMTK::Common
  EXPORT_MACRO_PREFIX VTK_VMTK_COMMON
  HEADERS
    vtkvmtkMath.h
    vtkvmtkWin32Header.h
    vtkvmtkConstants.h
    vtkvmtkConfigure.h
  SOURCES vtkvmtkMath.cxx
)

vtk_module_definitions(VMTK::Common PRIVATE vtkvmtkCommon_EXPORTS=1)