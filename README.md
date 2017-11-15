QtDownloadManager
=================

Qt download manager example that illustrates how to query the file size and whether the server supports resume functionality.

Original code taken from:
* http://kunalmaemo.blogspot.co.nz/2010/05/simple-download-manager-in-qt-with.html
* http://kunalmaemo.blogspot.co.nz/2011/07/simple-download-manager-with-pause.html
* https://gitorious.org/kunaltest/kunaltest/source/87fac9934ac327037fc637fdf7d2a28295da8d85:downloadmanager

Useful StackOverflow posts:
* http://stackoverflow.com/questions/12469072/is-it-possible-to-detect-the-resume-able-links-via-qnetworkaccessmanager
* http://stackoverflow.com/questions/10206898/how-to-download-large-file-quickly-in-qt
* http://stackoverflow.com/questions/1208821/reading-the-final-name-of-a-file-downloaded-using-qnetworkaccessmanager



* http 断点续传关键：
- 文件服务器支持 Accept-Ranges
- 正确计算当前已经下载的字节，并把它保存到一个临时文件中，文件以Append的方式打开
- 发送给服务器的请求，有一个 Range: bytes=1-100 形式的header
- 其它和一般的下载相同。
