# Copyright (C) 2007-2012 LuaDist.
# Created by Peter Drahoš
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.

project ( lcms2 )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )


# LCMS Library
include_directories ( include )
file ( GLOB LCMS_SRCS "src/*.c" "src/*.def" )
add_library ( lcms2 ${LCMS_SRCS} )

# install
install_library ( lcms2 )
install_header ( include/lcms2.h )
install_doc ( doc/ )
install_data ( AUTHORS COPYING ChangeLog NEWS README.1ST )
