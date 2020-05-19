# Panda3D-shared-object
Shared object for run la librairie Panda3D

1- git clone this repository
   ```git clone https://github.com/Cerfio/Panda3D-shared-object```
2- copy the external objects to /usr/lib
   ```cp -r Panda3D-shared-object/panda3d /usr/lib
3- Youpi, you can exec your binary


If you need to compile your project in C++, you can use my docker
https://hub.docker.com/r/cerfio/panda3d_cpp

1- docker pull cerfio/panda3d_cpp
2- docker run --rm -v "{projectLocationToBuild}:/home/buildpanda3d}:Z" -it cerfio/panda3d_cpp /bin/zsh -c 'useradd buildpanda3d && su - buildpanda3d'
3- g++ -std=c++11 example_file.cpp -I/usr/include/panda3d -L/usr/lib/panda3d -I/usr/include/python2.7 -lp3framework -lpanda -lpandafx -lpandaexpress -lp3dtoolconfig -lp3dtool -lp3direct -pthread
