cmake_minimum_required (VERSION 2.8)

project (classification_modified)

add_executable(classification_modified main.cpp)

include_directories ( /home/raiden/caffe/include
    /home/raiden/cpp_classify_so_demo/lib
    /usr/local/include
    /usr/local/cuda/include
    /usr/include )
	
target_link_libraries(classification_modified  
        /home/raiden/cpp_classify_so_demo/lib/build/libclassification.so
        /home/raiden/caffe/build/lib/libcaffe-nv.so
        /usr/local/lib/libopencv_highgui.so   
        /usr/local/lib/libopencv_core.so
        /usr/local/lib/libopencv_imgproc.so
        /usr/lib/x86_64-linux-gnu/libglog.so  
        /usr/lib/x86_64-linux-gnu/libboost_system.so  
        )
