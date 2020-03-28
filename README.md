Simple video stream server written Go which serves the static files. This can be easly done by using the FFMPEG. 

First you have to convert the mp4 files to ".m3u8" and all the .ts files should be in the same place where the main file locates.

The command used in the current project is

ffmpeg -i sit.mp4 -profile:v baseline -level 3.0 -s 640x360 -start_number 0 -hls_time 10 -hls_list_size 0 -f hls index.m3u8

Same can be used for other videos.

Once the server is started use the path as url for example

http://127.0.0.1:8080/index.m3u8 

You can test this in Mac safari which will we have the default steaming faciliyt or this can be tested in the any js supported HLS streaming.
