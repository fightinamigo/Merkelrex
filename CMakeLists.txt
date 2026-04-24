cmake_minimum_required(VERSION 3.20)
project(MerkelRex)

set(CMAKE_CXX_STANDARD 20)

add_executable(MerkelRex
        MerkelRex.cpp
        MerkelMain.cpp
        MerkelMain.h
        OrderBook.cpp
        OrderBook.h
        OrderBookEntry.cpp
        OrderBookEntry.h
        CSVReader.cpp
        CSVReader.h
        Wallet.cpp
        Wallet.h
)