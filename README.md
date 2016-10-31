### OpenCV: Open Source Computer Vision Library

<<<<<<< HEAD
=======
[![Gittip](http://img.shields.io/gittip/OpenCV.png)](https://www.gittip.com/OpenCV/)

#### Building RoboRIO Target

`gradlew -Pplatform=linux-arm` will generate a RoboRIO target image.
Additionally, `-Ptoolchain=xxx` can be used to override `CMAKE_TOOLCHAIN_FILE`
for different compilers.

Building for RoboRIO requires a Unix-type environment with JDK, cmake, ant,
python, and frc-toolchain installed
(https://launchpad.net/~wpilib/+archive/ubuntu/toolchain/).
Ubuntu for Windows can be used for this purpose (install the default-jdk
package for the JDK).

#### Building Windows Target

The platform will default to the current Windows host platform, but cross
builds are possible by specifying `-Pplatform=windows-x86` or
`-Pplatform=windows-x86_64`.  The build files default to using Visual Studio
2013, but Visual Studio 2015 can be used with `-Pvsversion=2015`.  If `cmake`
is not on the system PATH, its location can be specified with
`-PcmakePath=...`.  You will need to run gradle from the appropriate VS native
tools command prompt window for the selected platform.

Apache Ant is required to build the Java bindings.  It must be installed into
`Program Files (x86)\apache-ant` for the build to find it.  The `JAVA_HOME`
environment variable needs to point to the JDK.

Python is required to build the Java bindings.  Recommend both 32-bit and 64-bit
versions be installed (it seems to search for a version matching the platform
bitness).

An example complete build and publish of 32 and 64 bit and RoboRIO packages:
`gradlew -Pplatform=windows-x86_64 "-PcmakePath=C:\Program Files (x86)\CMake\bin\cmake.exe" -Pvsversion=2015 publish` (in x64 Native Tools Command Prompt)
`gradlew -Pplatform=windows-x86 "-PcmakePath=C:\Program Files (x86)\CMake\bin\cmake.exe" -Pvsversion=2015 publish` (in x86 Native Tools Command Prompt)

>>>>>>> Fix the Windows build and update README.
#### Resources

* Homepage: <http://opencv.org>
* Docs: <http://docs.opencv.org/master/>
* Q&A forum: <http://answers.opencv.org>
* Issue tracking: <https://github.com/opencv/opencv/issues>

#### Contributing

Please read before starting work on a pull request: <https://github.com/opencv/opencv/wiki/How_to_contribute>

Summary of guidelines:

* One pull request per issue;
* Choose the right base branch;
* Include tests and documentation;
* Clean up "oops" commits before submitting;
* Follow the coding style guide.
