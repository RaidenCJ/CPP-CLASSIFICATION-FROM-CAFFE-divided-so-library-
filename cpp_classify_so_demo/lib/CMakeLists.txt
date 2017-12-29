cmake_minimum_required (VERSION 2.8)  
      
SET (SRC_LIST classification.cpp)
include_directories ( /home/raiden/caffe/include  
        /usr/local/include 
        /usr/local/cuda/include 
        /usr/include  
        /home/raiden/caffe/cmake )  

add_library(classification SHARED ${SRC_LIST})  
