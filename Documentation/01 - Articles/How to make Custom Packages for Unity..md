This document outlines how to
# 1 - Create a temporary Unity project
Create an Unity Project locally in your machine. 

## Why?
This project will be the environment the package will be developed in. Note that this Unity project won't be stored in the cloud. Instead, a Git repository will be created inside this Unity project. That is what's saved.

The idea being that it doesn't matter in which project the package is being developed on, as the development of the package should not rely on project-specific settings or assets.

# 2 - 

The folder structure of a custom package is explained in the Unity's official Scripting API [Here](https://docs.unity3d.com/6000.2/Documentation/Manual/cus-layout.html) .

``` txt
<package-root>
  ├── package.json
  ├── README.md
  ├── CHANGELOG.md
  ├── LICENSE.md
  ├── Third Party Notices.md
  ├── Editor
  │   ├── <company-name>.<package-name>.Editor.asmdef
  │   └── EditorExample.cs
  ├── Runtime
  │   ├── <company-name>.<package-name>.asmdef
  │   └── RuntimeExample.cs
  ├── Tests
  │   ├── Editor
  │   │   ├── <company-name>.<package-name>.Editor.Tests.asmdef
  │   │   └── EditorExampleTest.cs
  │   └── Runtime
  │        ├── <company-name>.<package-name>.Tests.asmdef
  │        └── RuntimeExampleTest.cs
  ├── Samples~
  │        ├── SampleFolder1
  │        ├── SampleFolder2
  │        └── ...
  └── Documentation~
       └── <package-name>.md
```



