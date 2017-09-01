cmake_minimum_required(VERSION 3.6)
project(bfelf_loader C CXX)

set(TIDY_EXCLUSIONS ,-cppcoreguidelines-pro-type-const-cast)
include(${CMAKE_INSTALL_PREFIX}/cmake/CMakeGlobal_Project.txt)

# ------------------------------------------------------------------------------
# Subdirectories
# ------------------------------------------------------------------------------

if(NOT WIN32 AND ENABLE_UNITTESTING AND BUILD_SHARED_LIBS)
    add_subdirectory(tests)
endif()

# ------------------------------------------------------------------------------
# Install
# ------------------------------------------------------------------------------

install(FILES include/bfelf_loader.h DESTINATION include)