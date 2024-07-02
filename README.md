## Các bước để fine-tuning dựa trên YOLOv10 mình để trong file [code_helmet_yolov10](https://github.com/NguyenThanhDat10012004/yolov10_detect_helmet/blob/main/helmet_yolov10.ipynb).
## Các bước để sử dụng model mình đã train xong 
## B1: git clone git của mình về máy
```bash
! git clone https://github.com/NguyenThanhDat10012004/yolov10_detect_helmet.git
```
## B2: cài đặt các gói tài nguyên 
```bash
%cd yolov10
! pip install -q -r requirements.txt
! pip install -e .
```
## B3: khởi tạo model
```python
from ultralytics import YOLOv10

MODEL_PATH = "..."# Đường dẫn đến mô hình bạn đã tải 
model = YOLOv10 ( MODEL_PATH )
```
## B4: predict thử 1 ảnh nhé 
```python
IMG_PATH = "..." # đường dẫn đến ảnh bạn muốn predict
result = model ( source = IMG_PATH ) [0]
```
## B5: lưu ảnh để xem 
```python
result.save("...") # đường dẫn tới chỗ bạn muốn lưu kết quả 
```
