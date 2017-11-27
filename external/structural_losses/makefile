nvcc = /usr/local/cuda-8.0/bin/nvcc
cudalib =  /usr/local/cuda-8.0/lib64
tensorflow = /orions4-zfs/projects/optas/Virt_Env/tf_1.3/lib/python2.7/site-packages/tensorflow/include

tf_nndistance_so.so: tf_nndistance_g.cu.o tf_nndistance.cpp
	g++ -std=c++11 tf_nndistance.cpp tf_nndistance_g.cu.o -o tf_nndistance_so.so -shared -fPIC -I $(tensorflow) -lcudart -L $(cudalib) -O2 -D_GLIBCXX_USE_CXX11_ABI=0

tf_nndistance_g.cu.o: tf_nndistance_g.cu
	$(nvcc) -D_GLIBCXX_USE_CXX11_ABI=0 -std=c++11 -c -o tf_nndistance_g.cu.o tf_nndistance_g.cu -I $(tensorflow) -DGOOGLE_CUDA=1 -x cu -Xcompiler -fPIC -O2

clean:
	rm tf_nndistance_so.so
	rm  *.cu.o 