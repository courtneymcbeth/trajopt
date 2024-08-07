# TrajOpt

Documentation: http://rll.berkeley.edu/trajopt

----------------------------------------------

## 1. Start docker container

```bash
docker run -it cielavenir/openrave:jammy
```

## 2. Install TrajOpt dependencies

```bash
apt-get install libopenscenegraph-dev cmake libboost-all-dev libeigen3-dev python3-numpy
```

## 3. Clone modified TrajOpt repo

```bash
cd /root && git clone https://github.com/courtneymcbeth/trajopt.git
```

## 4. Setup build directory

```bash
cd trajopt && mkdir build && cd build
```

```bash
cmake ..
```

## 5. Make TrajOpt

```bash
make -j4
```

## 6. Add TrajOpt to Python path

```bash
export PYTHONPATH=/root/trajopt/:$PYTHONPATH
```

```bash
export PYTHONPATH=/root/trajopt/build/lib/:$PYTHONPATH
```

## 7. Try running tests

```bash
ctest --verbose
```
