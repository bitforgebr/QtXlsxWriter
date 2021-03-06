project(QtXlsxWriter)

find_package(Qt5 COMPONENTS Core Gui)

add_definitions(-DXLSX_NO_LIB)

include_directories(${Qt5Core_PRIVATE_INCLUDE_DIRS} ${Qt5Gui_PRIVATE_INCLUDE_DIRS})

add_library(QtXlsx STATIC
    src/xlsx/xlsxformat.cpp
    src/xlsx/xlsxdatavalidation.cpp
    src/xlsx/xlsxabstractsheet.cpp
    src/xlsx/xlsxstyles.cpp
    src/xlsx/xlsxdocument.cpp
    src/xlsx/xlsxcolor.cpp
    src/xlsx/xlsxmediafile.cpp
    src/xlsx/xlsxcell.cpp
    src/xlsx/xlsxdrawinganchor.cpp
    src/xlsx/xlsxdocpropsapp.cpp
    src/xlsx/xlsxdrawing.cpp
    src/xlsx/xlsxrichstring.cpp
    src/xlsx/xlsxabstractooxmlfile.cpp
    src/xlsx/xlsxnumformatparser.cpp
    src/xlsx/xlsxtheme.cpp
    src/xlsx/xlsxcellformula.cpp
    src/xlsx/xlsxzipreader.cpp
    src/xlsx/xlsxdocpropscore.cpp
    src/xlsx/xlsxrelationships.cpp
    src/xlsx/xlsxchart.cpp
    src/xlsx/xlsxworksheet.cpp
    src/xlsx/xlsxcontenttypes.cpp
    src/xlsx/xlsxchartsheet.cpp
    src/xlsx/xlsxworkbook.cpp
    src/xlsx/xlsxcellrange.cpp
    src/xlsx/xlsxsimpleooxmlfile.cpp
    src/xlsx/xlsxsharedstrings.cpp
    src/xlsx/xlsxconditionalformatting.cpp
    src/xlsx/xlsxutility.cpp
    src/xlsx/xlsxcellreference.cpp
    src/xlsx/xlsxzipwriter.cpp
)

set_property(TARGET QtXlsx PROPERTY AUTOMOC ON)

target_link_libraries(QtXlsx Qt5::Core Qt5::Gui)
