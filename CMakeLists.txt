cmake_minimum_required(VERSION 2.8.9)

project(MultiLevelRegistration)

#-----------------------------------------------------------------------------
# Extension meta-information
set(EXTENSION_HOMEPAGE "http://slicer.org/slicerWiki/index.php/Documentation/Nightly/Extensions/MultiLevelRegistration")
set(EXTENSION_CATEGORY "Registration")
set(EXTENSION_CONTRIBUTORS "Emily Hammond (University of Iowa), Jessica C. Sieren (University of Iowa) ")
set(EXTENSION_DESCRIPTION "Perform rigid registration with increasingly smaller volumes of data defined by regions of interest focusing on a desired anatomy.")
set(EXTENSION_ICONURL "https://github.com/emily-hammond/LongitudinalAnalysis/blob/master/MultiLevelRegistrationLogo_275x235.png")
set(EXTENSION_SCREENSHOTURLS "https://www.slicer.org/wiki/File:MultiLevelRegistrationExample.png")
set(EXTENSION_DEPENDS "NA") # Specified as a space separated string, a list or 'NA' if any

#-----------------------------------------------------------------------------
# Extension dependencies
find_package(Slicer REQUIRED)
include(${Slicer_USE_FILE})

#-----------------------------------------------------------------------------
# Extension modules
add_subdirectory(MultiLevelRegistration)
## NEXT_MODULE

#-----------------------------------------------------------------------------
include(${Slicer_EXTENSION_CPACK})
