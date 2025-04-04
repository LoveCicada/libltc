libLTC
------

Linear (or Longitudinal) Timecode (LTC) is an encoding of SMPTE timecode data
as a Manchester-Biphase encoded audio signal.
The audio signal is commonly recorded on a VTR track or other storage media.

libltc provides functionality to encode and decode LTC audio from/to
SMPTE or EBU timecode, including SMPTE date support.

libltc is the successor of [libltcsmpte](https://sourceforge.net/projects/ltcsmpte/).
For more information, please see the FAQ in the documentation.

Documentation
-------------

The API reference, examples, as well as introduction can be found at

https://x42.github.io/libltc/

This site is part or the source-code in the doc/ folder.


Add CMakeLists.txt
--------------

```bash
mkdir build 
cd build
cmake ..
cmake --build . --config Debug
cmake --build . --config Release
cmake --build . --config RelWithDebInfo
```