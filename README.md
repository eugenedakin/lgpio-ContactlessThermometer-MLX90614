# lgpio-ContactlessThermometer-MLX90614
Eugene uses the Raspberry Pi to detect ambient and object temperature. Thsi is a non-contact thermometer using GY-906 sensor on a MLX90614 board, and is useful for temperature monitoring and many other practical tasks. This was created in Xojo 2023 r4. 

Ensure I2C is enabled on the Raspberry Pi.

The teaser video can be viewed at: [![MPU6050 Xojo Teaser Video](https://github.com/eugenedakin/lgpio-ContactlessThermometer-MLX90614/blob/main/MLX90614-300x300.png)](https://www.youtube.com/watch?v=mGKfjxuV2BM&ab_channel=EugeneDakin "MLX90614 Teaser")

To use the lgpio with Raspberry Pi 4 or older systems, get the successful chip handle (not a zero) with the following command:
| Initialize the Raspberry Pi 4 lgpio |
| --------------------------------- |
| MyChipHandle = lgGpiochipOpen(0) //dev/gpiochip0 for Raspberry Pi 4 or older |

To use the lgpio with the Raspberry Pi 5 board, get the chip handle with the following command:
| Initialize the Raspberry Pi 5 lgpio |
| --------------------------------- |
| MyChipHandle = lgGpiochipOpen(4) //dev/gpiochip4 for Raspberry Pi 5 |

Install instructions are:

1) install Raspberry Pi OS (64-bit)
2) Open a terminal and type the following commands:
3) sudo apt install swig python3-dev
4) sudo apt install python3-setuptools
5) sudo apt install libunwind8
6) wget https://github.com/joan2937/lg/archive/master.zip
7) unzip master.zip
8) cd lg-master
9) make
10) sudo make install
11) Turn on the I2C communication protocol on the Raspberry Pi
12) create a MLX90614 example program and copy the program and libraries to the RaspberryPi Desktop (make a 64-bit version)
13) give the executable permission to run with something like: 'sudo chmod +x MLX90614'
14) run the program with something like: 'sudo ./MLX90614'

Breadboard Layout

![](https://github.com/eugenedakin/lgpio-ContactlessThermometer-MLX90614/blob/main/BreadBoard.png)

Screen Grab of running program

![](https://github.com/eugenedakin/lgpio-ContactlessThermometer-MLX90614/blob/main/ScreenGrab.png)
