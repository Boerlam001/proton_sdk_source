Cross Platform 3D engine with OpenGL ES1 ES2 on Proton
=================
1.
Proton 3d engine impelement Irrlicht and Bullet with OpenGL ES1.0 ES2.0
You can build on Win32, MacOS, Android, Ios

2.
Rember first run
On Win32 --->
xxxxxx/media/update_media.bat

On MacOs --->
chmod 777 xxxxxx/media/update_media.sh
xxxxxx/media/update_media.sh

3.
If debug c++ in Android, please set
android:installLocation="internalOnly" of AndroidManifest.xml

4.
Switch OGLES1 -> OGLES2
(a.) find App.cpp
irr::video::E_DRIVER_TYPE AppGetOGLESType()
return irr::video::EDT_OGLES1; -> return irr::video::EDT_OGLES2;

(b.) find SharedActivity.java
public AppGLSurfaceView(Context context, SharedActivity _app)
//setEGLContextClientVersion(2); -> setEGLContextClientVersion(2);
