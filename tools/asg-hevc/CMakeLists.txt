find_path( FEI_INCLUDE mfxfeihevc.h PATHS ${MFX_INCLUDE} )

include_directories (
  ${CMAKE_CURRENT_SOURCE_DIR}/../../samples/sample_common/include
  ${CMAKE_CURRENT_SOURCE_DIR}/include
)

list( APPEND LIBS sample_common)

set( defs " -DMFX_VERSION_USE_LATEST " )
set(DEPENDENCIES libmfx)

make_executable( shortname universal "nosafestring" )
set( defs "" )
