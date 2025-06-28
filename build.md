Need Developer Command Prompt for VS 2022

```bat
cd %USERPROFILE%\Documents\Projects\hadoop\hadoop-common-project\hadoop-common
set Platform=x64
```

Install [CMake](https://cmake.org/download/), include in PATH, test with `cmake --version`

Extract [Maven](https://maven.apache.org/download.cgi), include in PATH, test with `mvn -version`

Extract [protobuf](https://github.com/protocolbuffers/protobuf/releases), include in PATH, test with `protoc --version`

Find Git's **bash.exe**, include in PATH, test with `where bash`:

```bat
set PATH=%PATH%;C:\Program Files\Git\bin
```

To clean:

```bat
mvn clean
```

To build:

```bat
mvn package -e -Pdist -DskipTests -Dtar -Dmaven.javadoc.skip=true
```

The output is target\hadoop-common-3.3.4

```bat
start target\hadoop-common-3.3.4
```