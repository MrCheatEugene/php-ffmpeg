# php-ffmpeg
PHP FFmpeg library for Windows&amp;Linux! However, I recommend you using the PHP-FFMpeg/PHP-FFMpeg OG library rather than this one.

Fast and simple example:
```
<?php 
include 'ffmpeg.php';
$ffmpeg=new ffmpeg_php();
$ffmpeg->init('ffmpeg.exe');// initialization. ffmpeg.exe is the ffmpeg binary
$ffmpeg->add_input('test.mp4'); // add input
$ffmpeg->generateHLS('out.mp4');// HLS code generator
echo $ffmpeg->buildString();// returns string with parameters
$ffmpeg->free();//not necessecary, but recommended if you use the same instance in the same script twice

```
Result:

```ffmpeg.exe-i test.mp4-f hls -hls_time 4 -hls_playlist_type event out.mp4```

View source code of the library for more advanced functions and stuff!

p.s I do not like GitHub because it's too complicated to me, and, i'm so sorry about this, but there will be zero docs.View source code of the library yourself to find ACTUAL functions for any release.
