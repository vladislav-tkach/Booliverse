## CMakeUserPresets.json

From CMake documentation:
> CMakeUserPresets.json is meant for developers to specify their own local build details

The file should be located in the root directory of the project. Simply copy the following snippet into the file and modify it using your local paths.

Regarding the use of presets please use CMake documentation.

An example of such a file that you can easily modify for your case:
```json
{
  "version": 5,
  "include": [
    "cmake/configurePresets/OSSpecificPresets.json",
    "cmake/configurePresets/CustomToolkitPathsPreset.json"
  ],
  "configurePresets": [
    {
      "name": "local_toolkit_paths",
      "hidden": true,
      "inherits": "custom_toolkit_paths",
      "description": "This is base preset for inheritance. This preset sets custom toolkit paths",
      "cacheVariables": {
        "CMAKE_EXE_LINKER_FLAGS": "-static"
      },
      "environment": {
        "CustomToolkitRoot": "C:/Local Toolkit",
        "CustomToolkitPaths": "$env{CustomToolkitRoot}/mingw64/bin${pathListSep}$env{CustomToolkitRoot}/ninja-release/bin"
      }
    },
    {
      "name": "ninja_multi_config_preset",
      "hidden": true,
      "description": "This is base preset for inheritance. This preset uses Ninja Multi-Config generator",
      "generator": "Ninja Multi-Config"
    },

    {
      "name": "user_windows_ninja_mingw64",
      "inherits": [ "windows_specific_preset", "local_toolkit_paths", "ninja_multi_config_preset" ],
      "displayName": "Ninja Multi-Config + MinGW_w64 preset",
      "description": "This Windows-specific preset uses Ninja Multi-Config and MinGW_w64 provided in CustomToolkitPaths environment variable",
      "binaryDir": "build"
    },
    {
      "name": "user_windows_ninja_mingw64_debug",
      "inherits": [ "windows_specific_preset", "local_toolkit_paths", "ninja_multi_config_preset" ],
      "displayName": "Ninja Multi_config + MinGW_w64 preset with CMake debug info",
      "description": "This Windows-specific preset uses Ninja Multi-Config and MinGW_w64 provided in CustomToolkitPaths environment variable and shows CMake debug info",
      "warnings": {
        "dev": true,
        "deprecated": true,
        "uninitialized": false,
        "unusedCli": true,
        "systemVars": true
      },
      "errors": {
        "dev": true,
        "deprecated": true
      },
      "debug": {
        "output": true,
        "tryCompile": true,
        "find": true
      }
    }
  ],
  "buildPresets": [
    {
      "name": "local_jobs_number",
      "hidden": true,
      "description": "This is base preset for inheritance. This preset sets the number of parallel jobs",
      "jobs": 4
    },
    
    {
      "name": "user_windows_debug",
      "inherits": "local_jobs_number",
      "configurePreset": "user_windows_ninja_mingw64",
      "configuration": "Debug"
    },
    {
      "name": "user_windows_release",
      "inherits": "local_jobs_number",
      "configurePreset": "user_windows_ninja_mingw64",
      "configuration": "Release"
    },
    {
      "name": "user_windows_relwithdebinfo",
      "inherits": "local_jobs_number",
      "configurePreset": "user_windows_ninja_mingw64",
      "configuration": "RelWithDebInfo"
    },
    {
      "name": "user_windows_minsizerel",
      "inherits": "local_jobs_number",
      "configurePreset": "user_windows_ninja_mingw64",
      "configuration": "MinSizeRel"
    }
  ]
}
```