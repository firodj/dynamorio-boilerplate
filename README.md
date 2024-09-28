# dynamorio-boilerplate
A DynamoRIO Client or Tool Boilerplate

Assuming, DynamoRIO is cloned into: D:\workspace\dynamorio, and this repo is cloned into D:\workspace\dynamorio-boilerplate

## Compile

```
open "Developer Command Prompt for VS 2022"
cd /d D:\workspace\dynamorio-boilerplate
```

## For Building Win32

```
mkdir build22
cd build22
cmake -A Win32 -DDynamoRIO_DIR=D:\workspace\dynamorio\build22\cmake ..
cmake --build . --config RelWithDebInfo
```

Running:

```
D:\workspace\dynamorio\build22\bin32\drrun.exe -c D:\workspace\dynamorio-boilerplate\build22\RelWithDebInfo\bbbuf.dll -- "C:\Program Files (x86)\app32.exe"
```

## For Building x64

```
mkdir build22x64
cd build22x64
cmake -A x64 -DDynamoRIO_DIR=D:\workspace\dynamorio\build22x64\cmake ..
cmake --build . --config RelWithDebInfo
```

Running:

```
D:\workspace\dynamorio\build22x64\bin64\drrun.exe -c D:\workspace\dynamorio-boilerplate\build22x64\RelWithDebInfo\bbbuf.dll -- "notepad.exe"
```


# Pre-Requisute Build DynamoRIO

```
open "Developer Command Prompt for VS 2022"
cd /d D:\workspace\dynamorio`
```

## Building Win32

```
mkdir build22
cd build22
cmake -A Win32 ..
cmake --build . --config RelWithDebInfo
```

## Building x64

```
mkdir build22x64
cd build22x64
cmake -A x64 ..
cmake --build . --config RelWithDebInfo
```