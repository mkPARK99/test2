# Project_COD
Car Object Detection Project Code  
<br />

Inference on PC (with Docker)
-----------------------------
1. Git clone
```
$ git clone https://invako-github.airobot.ai.kr/group-ai/Project_COD.git
```
<br />

2. Docker pull (YOLOv7 with TensorRT)
```
$ docker pull nvcr.io/nvidia/pytorch:21.08-py3
```
<br />

3. Create docker container 
```
$ cd Project_COD/
$ nvidia-docker run --name yolov7 -it -v your_coco_path/:/coco/ -v your_code_path/:/yolov7 --shm-size=64g nvcr.io/nvidia/pytorch:21.08-py3
/bin/bash
```
<br />

4. Run main.py
```
$ cd /Project_COD
$ python3 main.py

Developer mode:
$ python3 main.py [video(*.mp4) or rtsp...] [pc] # 순서 상관 없음
```
<br />

Inference on Nano board
-----------------------
1. Git clone
```
$ git clone https://github.com/invakoAI/Project_COD
```
<br />

2. Pre-installation commands
```
$ sudo apt-get update
$ sudo apt install -y zip htop screen libgl1-mesa-glx
$ sudo pip install seaborn thop
```
<br />

Install pt/onnx 

<details><summary> <b>Expand</b> </summary>

Car model onnx:
https://drive.google.com/file/d/1ADichYS8sE9Rt8OAR49wBdNAUfCYMg1J/view?usp=sharing

Plate model onnx: 
https://drive.google.com/file/d/1DvFmKhrs1wIgKCyPZwibue1PoTd7Qpi8/view?usp=sharing

PPE model onnx:
https://drive.google.com/file/d/1lngwOq3-INV2WDZHwAciz6WNXzrlVuZG/view?usp=sharing

</details>

Put them under onnx folder

3. Run main.py
```
$ cd Project_COD
$ python3 video_test_request.py

```
<br />



