# LICENSE

cmake_minimum_required(VERSION 3.13 FATAL_ERROR)

project(odpic VERSION 0.1)

add_library(odpic SHARED EXCLUDE_FROM_ALL)

target_compile_definitions(odpic PRIVATE DPI_EXPORTS)
target_include_directories(odpic PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)

target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include/dpi.h)

target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiImpl.h)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiErrorMessages.h)

target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiConn.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiContext.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiData.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiDebug.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiDeqOptions.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiEnqOptions.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiEnv.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiError.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiGen.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiGlobal.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiHandleList.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiHandlePool.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiJson.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiLob.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiMsgProps.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiObject.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiObjectAttr.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiObjectType.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiOci.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiOracleType.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiPool.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiQueue.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiRowid.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiSodaColl.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiSodaCollCursor.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiSodaDb.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiSodaDoc.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiSodaDocCursor.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiStmt.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiSubscr.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiUtils.c)
target_sources(odpic PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/dpiVar.c)

add_subdirectory(samples)
add_subdirectory(test)