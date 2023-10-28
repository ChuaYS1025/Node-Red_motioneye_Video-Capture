# Node-Red_motioneye_Video-Capture
Capture video(s) using node-red with motioneye on specific time or condition

Items/software to install:
Install motioneye: link >> https://github.com/motioneye-project/motioneye/wiki/Install-On-Debian
Install ffmpeg >> sudo apt install -y ffmpeg

Under Motioneye:
1) Setup the camera in motioneye
2) Enable the video streaming functions in motioneye and click on the streaming URL to get the link should be example: http://127.0.0.1:8081

![image](https://github.com/ChuaYS1025/Node-Red_motioneye_Video-Capture/assets/106689692/d1f1dba5-d152-4031-a9e9-bb378c7cc433)

Under Node-Red:
**In node-red exec node**
command:
"ffmpeg -i http://127.0.0.1:8081/ -t 30 -y -vcodec copy -an" 

Explanation:
http://127.0.0.1:8081/ >> streaming url
-t >> time in seconds (10 secs video saving 50 seconds of the footage)
-an >>save location of the file 
-vcodec >> decode the video

![image](https://github.com/ChuaYS1025/Node-Red_motioneye_Video-Capture/assets/106689692/3bc66b75-b15b-4e39-b96c-dd242ff0f7f1)

Suggestions for improvement:
Can integrate with other node or functions to make it to your own applications. 
Example:
Integrate with PLC (Omron, Mitsubishi), sensor to capture specific time video and durations.
Node-red has lots of module able to install and integrate it with this video capture.

Credit to https://flows.nodered.org/flow/0da4d606575df13700461400178aca4e 



