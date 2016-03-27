# AutoMux
Require ffmpeg<br>
修改了用法，更符合cmd常见用法<br>
修复了路径名不能包含中文的bug<br>
用法：<br>
python 脚本路径 -v 视频路径 -a 音频路径 -n [num]开始数字~[num]结束数字 -t 音轨号(第一条音轨一般为0)<br>
仅-v 必填 -a 默认同-v -n默认1~1 -t默认0<br>
1——————————————————————————————————————<br>
python E:\python\automux\automux.py -v E:\python\automux\[num].mp4 -a E:\python\automux\02.mp4 -n 2~4<br>
上面脚本的意思是把02.mp4的第一条音轨分别和02.mp4、03.mp4、04.mp4的第一条视频轨合并<br>
(数字2、4代表[num]从02取到04，请注意0是程序自动加的，请不要手动添加)<br>
<br>
2——————————————————————————————————————<br>
python E:\python\automux\automux.py -v E:\python\automux\[num].mp4 -a E:\python\automux\逸站[num]要完.aac -n 1~12 -t 0<br>
逸站01要完.aac的第一条音轨和01.mp4合并为01_mmux.mp4<br>
逸站02要完.aac的第一条音轨和02.mp4合并为02_mmux.mp4<br>
······<br>
逸站12要完.aac的第一条音轨和12.mp4合并为12_mmux.mp4<br>
<br>
3——————————————————————————————————————<br>
当只有一个视频需要封装时:<br><br>
python E:\python\automux\automux.py -v E:\python\automux\逸站12要完.mp4 -a E:\python\automux\逸站12要完.aac<br>
音频请自行转码，不符合规范的音频只会有一个不明显的报错。此时生成的视频文件一般只有几十kb<br>
<br>
