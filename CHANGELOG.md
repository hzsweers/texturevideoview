Change Log
==========

Version 1.1.0
-------------

 * synced TextureVideoView with latest sources from Android 6.0.1_r10
   (un-hides [setVideoURI(Uri uri, Map<String, String> headers)][1],
   uses proper audio focus, source code indention)
 * reverted to Android framework behaviour: OnCompletionListener may be called more than once again
   (see #6, thanks to @MrNovado)

   **This may break your code!** The OnCompletionListener itself is now responsible for guarding
   any unwanted invocation.

 [1]: http://developer.android.com/reference/android/widget/VideoView.html#setVideoURI%28android.net.Uri,%20java.util.Map%3Cjava.lang.String,%20java.lang.String%3E%29

Version 1.0.2
-------------

 * fixed a sizing bug when auto-starting the video with view size != video size (thanks to @lhunath)
 * fixed potential activity leak when streaming videos over HTTP(S) (thanks to @koral)

Version 1.0.1
-------------

 * fixed potential leak by releasing surface when destroyed

Version 1.0.0
-------------

 * initial public release on github
