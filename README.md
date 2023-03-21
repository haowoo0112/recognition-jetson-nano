# recognition-jetson-nano  

## How to clean jetson nano  

``` bash 
sudo apt remove -y libreoffice* thunderbird*
sudo apt autoremove -y
sudo apt clean
```

## How to use hello AI world  

``` bash 
sudo apt-get update
sudo apt-get install git cmake libpython3-dev python3-numpy
git clone --depth 1 --branch L4T-R35.2.1 https://github.com/dusty-nv/jetson-inference.git
git submodule update --init
cd jetson-inference
sudo mkdir build
cd build
sudo cmake ../
sudo make
sudo make install
sudo ldconfig
```

## How to use example of recognition  

``` bash 
cd ..
cd example
sudo cp -r my-recognition /media/user/data/
cd ..
cd my-recognition/
sudo mkdir build
cd build
sudo cmake ../
sudo make
sudo cp my-recognition ../
cd ..
./my-recognition black_bear.jpg
```

## Result  
![](https://i.imgur.com/JcjVkYX.png)  