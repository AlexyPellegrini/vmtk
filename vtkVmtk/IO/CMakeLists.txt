
set(classes
  vtkvmtkDolfinWriter
  vtkvmtkFDNEUTReader
  vtkvmtkFDNEUTWriter
  vtkvmtkFluentWriter
  vtkvmtkPNGWriter
  vtkvmtkTetGenReader
  vtkvmtkTetGenWriter
  vtkvmtkXdaReader
  vtkvmtkXdaWriter
)

vtk_module_add_module(VMTK::IO
  EXPORT_MACRO_PREFIX VTK_VMTK_IO
  CLASSES ${classes}
)

vtk_module_definitions(VMTK::IO PRIVATE vtkvmtkIO_EXPORTS=1)
