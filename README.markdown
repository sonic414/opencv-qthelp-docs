#### OpenCV documentation for Qt Creator

Now with context sensitive help support! 
	- Press F1 when writing opencv keywords
	- with or without: using namespace cv;

Instructions:

Copy opencv-doc.patch to /path/to/opencv/

``` bash

$ cd "/path/to/opencv/"
$ patch -p1 < "opencv-doc.patch"
$ mkdir build && cd build
$ cmake -D BUILD_DOCS=ON -D CMAKE_BUILD_TYPE=Release ..
$ make qthelp_docs
$ qcollectiongenerator doc/_qthelp/OpenCV.qhcp

```

.qch file will be found in /path/to/opencv/build/doc/_qthelp/

Open Qtcreator , Got to Tools > Options > Help > Documentation. Click Add , browse and select the .qch file


![Screenshot](./screenshot.png)


NOTE: Only tested for archlinux - Needs the dependencies of opencv-docs package in AUR