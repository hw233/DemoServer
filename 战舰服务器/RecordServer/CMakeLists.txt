INCLUDE_DIRECTORIES(.)

FILE(GLOB SRC *.h *.cpp)

SOURCE_GROUP("" FILES ${SRC})

ADD_EXECUTABLE(RecordServer
  ${SRC}
)
TARGET_LINK_LIBRARIES(RecordServer
  sdk
  ${Boost_THREAD_LIBRARY}
  ${Boost_SYSTEM_LIBRARY}
  ${ALLOCATOR_LIBRARY}
  ${MYSQLCLIENT_LIBRARY})
