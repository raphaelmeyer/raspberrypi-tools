# raspberrypi-tools
Docker image with toolchain for Raspbian

https://github.com/raspberrypi/tools

    // rsync -rl --delete-after --safe-links pi@host:/{lib,usr} /local/path/rootfs


    docker run --rm -t -v /tmp/test:/home/user/src:ro raphaelmeyer/arm-bcm2708 cmake -DCMAKE_TOOLCHAIN_FILE=/opt/cmake/raspbian.cmake /home/user/src
    docker run --rm -t -v /tmp/test:/home/user/src:ro raphaelmeyer/arm-bcm2708 cmake --build .


/tmp/test/CMakeLists.txt

    project(Hello)
    
    add_executable(hello main.cc)

/tmp/test/main.cc

    #include <iostream>
    
    int main() {
      std::cout << "hello" << "\n";
    }

