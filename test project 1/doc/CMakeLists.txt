project(docs)

find_package(DoxygenCMake REQUIRED)

log_level(doxygen INFO)
# set(dot.class-diagrams false)
if (TARGET Doxygen::doxygen)
    add_doxygen_targets(PROJECT_FILE Doxyfile EXAMPLE_PATH ../example GENERATE_PDF)
else()
    message(STATUS "No Doxygen found.")
endif()
