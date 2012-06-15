CMAKE_MINIMUM_REQUIRED(VERSION 2.6 FATAL_ERROR)
CMAKE_POLICY(VERSION 2.6)
FIND_PACKAGE(Torch REQUIRED)

# don't actually have any c code but want common infrastructure
SET(src   dummy.c) 
SET(luasrc init.lua)

ADD_TORCH_PACKAGE(csv ${src} ${luasrc} "CSV reader")

