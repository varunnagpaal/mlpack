# Define the files we need to compile
# Anything not in this list will not be compiled into MLPACK.
set(SOURCES
  ada_delta.hpp
  adam.hpp
  rmsprop.hpp
  steepest_descent.hpp
)

# Add directory name to sources.
set(DIR_SRCS)
foreach(file ${SOURCES})
  set(DIR_SRCS ${DIR_SRCS} ${CMAKE_CURRENT_SOURCE_DIR}/${file})
endforeach()
# Append sources (with directory name) to list of all MLPACK sources (used at
# the parent scope).
set(MLPACK_SRCS ${MLPACK_SRCS} ${DIR_SRCS} PARENT_SCOPE)
