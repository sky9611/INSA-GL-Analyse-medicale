cmake_minimum_required(VERSION 3.7)

#-------------------------------------#
#------------ CLIENT TEST ------------#
#-------------------------------------#

set(TARGET_NAME MedAnalysisServerUnitTest)

#---- Source files ----#

file(GLOB_RECURSE SOURCE_FILES "*.cpp")


#---- Target ----#

add_executable(${TARGET_NAME} ${SOURCE_FILES})
target_link_libraries(${TARGET_NAME} MedAnalysisServer Catch)
target_include_directories(${TARGET_NAME} PUBLIC ${HDR_SERVER})
