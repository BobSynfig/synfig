## TODO: install headers properly

configure_file(
    etl_profile.h.cmake.in
    ${PROJECT_BINARY_DIR}/ETL/etl_profile.h
)

set(ETL_HEADERS
        "${CMAKE_CURRENT_LIST_DIR}/handle"
#     PRIVATE
        "${CMAKE_CURRENT_LIST_DIR}/_handle.h"

# autogenerated
        "${PROJECT_BINARY_DIR}/ETL/etl_profile.h" 
)

install(
    FILES ${ETL_HEADERS}
    DESTINATION include/ETL
)
