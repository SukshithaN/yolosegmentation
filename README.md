# yolosegmentation
for converting json files to yolo format
pip install labelme2yolo
labelme2yolo --json_dir /path/to/labelme_json_dir/
this itself will  give yout the data.yaml file


training
yolo task=segment mode=train model=yolov8s-seg.pt data=/path/to/dataset/data.yaml epochs=100 imgsz=640

testing
yolo task=segment mode=predict model=path/to/trained/model.pt source=path/to/image.jpg 
