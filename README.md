# doudizhu_server

使用boost.asio写的斗地主server, 客户端是telnet

## build

```
mkdir -p build;cd build
qmake -o Makefile ../src/doudizhu_server.pro
# 编辑 INCPATH
# INCPATH       = -I. -I/your_boost/boost_1_69_0  -I/usr/lib/qt/mkspecs/linux-g++
make
```

## run

```
mkdir -p database/userinfo
./doudizhu_server

# telnet
telnet 127.0.0.1 23333
register name pass
login name pass

game ready
game rob
game play card_no
```

## 摘要

CFLAGS

CXXFLAGS

对应文件编译时的参数


LFLAGS

LIBS

对应文件链接成一个可执行文件时的参数


才此处为了方便，牺牲了动态链接编译和链接均加上了 `-static -static-libstdc++ -static-libgcc`
