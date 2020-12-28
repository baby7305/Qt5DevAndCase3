# Qt5DevAndCase3
**《Qt5开发及实例第三版》** 书中代码

## 添加环境变量 ##
`C:\Qt\Qt5.14.2\5.14.2\msvc2015_64\bin\`

## CMake编译构建 ##

- ### clion配置 ###
  - Preferences--->Build--->Toolchains，选择visual studio 2019编译器。
  - Preferences--->Build--->Cmake，在cmake options中输入：-D参数
  `-DCMAKE_BUILD_TYPE=Debug -DCMAKE_PREFIX_PATH=C:\\Qt\\Qt5.14.2\\5.14.2\\msvc2015_64`

- ### visual studio配置 ###
  - CMakeSettings.json
    ```json
    {
    "configurations": [
        {
        "name": "x64-Debug (默认值)",
        "generator": "Ninja",
        "configurationType": "Release",
        "inheritEnvironments": [ "msvc_x64_x64" ],
        "buildRoot": "${projectDir}\\out\\build\\${name}",
        "installRoot": "${projectDir}\\out\\install\\${name}",
        "cmakeCommandArgs": "-DCMAKE_PREFIX_PATH=C:\\Qt\\5.14.2\\msvc2015_64",
        "buildCommandArgs": "",
        "ctestCommandArgs": ""
        }
    ]
    }
    ```

## xmake编译构建 ##

- 显示详细报错信息
`xmake -rvD`
- 清空项目，刷新环境，不如直接删掉.xmake和build目录直接
`xmake c`
- 构建项目
`xmake build`
- 执行项目
`xmake run`