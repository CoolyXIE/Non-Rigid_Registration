cmake_minimum_required(VERSION 2.8.0)

project(NonRigidRegistration CXX)

# PCL related
find_package(PCL REQUIRED HINTS "F:/Libraries/PCL_180_msvc2015_x64")

include_directories(${PCL_INCLUDE_DIRS})

add_executable(NonRigidRegistration 
					NonRigidICP.h
					NonRigidICP.cpp
					main.cpp)
				
target_link_libraries(NonRigidRegistration ${PCL_LIBRARIES})