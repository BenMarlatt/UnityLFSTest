# Configuring Git for Unity Projects

This repo provides an example of installing and configuring Git for Unity projects, including the installation of Git LFS (Large File Storage) and configuration of .gitattributes and .gitignore files specific to Unity development. 
## Install Git
To start using Git, you need to download and install it from [this link](https://git-scm.com/download/win). Git is a command-line tool that helps you manage changes within files or directories. You can also use [GitHub Desktop](https://desktop.github.com/), a graphical interface that provides better visibility of changes.

## Install Git LFS

To enable large file storage (LFS) for your Unity project, download and install Git LFS from [this link](https://git-lfs.com/). This process varies by operating system, but it's already included with Git in the Windows distribution

## Configure .gitattributes and .gitignore for Unity

The `.gitattributes` file allows you to assign attributes to files and directories. In our use case, we're assigning the `lfs` attribute to directories to indicate that they should be stored differently.

Here's an example of a `.gitattributes` file:

```
## git-lfs ##

#Image
*.jpg               filter=lfs diff=lfs merge=lfs -text
*.jpeg              filter=lfs diff=lfs merge=lfs -text
*.png               filter=lfs diff=lfs merge=lfs -text
*.gif               filter=lfs diff=lfs merge=lfs -text
*.psd               filter=lfs diff=lfs merge=lfs -text
*.ai                filter=lfs diff=lfs merge=lfs -text

#Audio
*.mp3               filter=lfs diff=lfs merge=lfs -text
*.wav               filter=lfs diff=lfs merge=lfs -text
*.ogg               filter=lfs diff=lfs merge=lfs -text

#Video
*.mp4               filter=lfs diff=lfs merge=lfs -text
*.mov               filter=lfs diff=lfs merge=lfs -text

#3D Object
*.FBX               filter=lfs diff=lfs merge=lfs -text
*.fbx               filter=lfs diff=lfs merge=lfs -text
*.blend             filter=lfs diff=lfs merge=lfs -text
*.obj               filter=lfs diff=lfs merge=lfs -text

#ETC
*.a                 filter=lfs diff=lfs merge=lfs -text
*.exr               filter=lfs diff=lfs merge=lfs -text
*.tga               filter=lfs diff=lfs merge=lfs -text
*.pdf               filter=lfs diff=lfs merge=lfs -text
*.zip               filter=lfs diff=lfs merge=lfs -text
*.dll               filter=lfs diff=lfs merge=lfs -text
*.unitypackage      filter=lfs diff=lfs merge=lfs -text
*.aif               filter=lfs diff=lfs merge=lfs -text
*.ttf               filter=lfs diff=lfs merge=lfs -text
*.rns               filter=lfs diff=lfs merge=lfs -text
*.reason            filter=lfs diff=lfs merge=lfs -text
*.lxo               filter=lfs diff=lfs merge=lfs -text

```

The `.gitignore` file controls which files, directories, and patterns Git will ignore when adding files to commits. This is useful for avoiding temporary, cached, or local configuration files.

Here's an example of a `.gitignore` file:

```
# This .gitignore file should be placed at the root of your Unity project directory
#
# Get latest from https://github.com/github/gitignore/blob/main/Unity.gitignore
#
/[Ll]ibrary/
/[Tt]emp/
/[Oo]bj/
/[Bb]uild/
/[Bb]uilds/
/[Ll]ogs/
/[Uu]ser[Ss]ettings/

# MemoryCaptures can get excessive in size.
# They also could contain extremely sensitive data
/[Mm]emoryCaptures/

# Recordings can get excessive in size
/[Rr]ecordings/

# Uncomment this line if you wish to ignore the asset store tools plugin
# /[Aa]ssets/AssetStoreTools*

# Autogenerated Jetbrains Rider plugin
/[Aa]ssets/Plugins/Editor/JetBrains*

# Visual Studio cache directory
.vs/

# Gradle cache directory
.gradle/

# Autogenerated VS/MD/Consulo solution and project files
ExportedObj/
.consulo/
*.csproj
*.unityproj
*.sln
*.suo
*.tmp
*.user
*.userprefs
*.pidb
*.booproj
*.svd
*.pdb
*.mdb
*.opendb
*.VC.db

# Unity3D generated meta files
*.pidb.meta
*.pdb.meta
*.mdb.meta

# Unity3D generated file on crash reports
sysinfo.txt

# Builds
*.apk
*.aab
*.unitypackage
*.app

# Crashlytics generated file
crashlytics-build.properties

# Packed Addressables
/[Aa]ssets/[Aa]ddressable[Aa]ssets[Dd]ata/*/*.bin*

# Temporary auto-generated Android Assets
/[Aa]ssets/[Ss]treamingAssets/aa.meta
/[Aa]ssets/[Ss]treamingAssets/aa/*
```
