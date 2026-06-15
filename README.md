# PHÂN VÙNG ẢNH CHO LIDAR Point Cloud
Mô hình dự đoán Pagnotic Segmantation cho Lidar Point Cloud, giúp phân biệt các lớp, hiểu cấu trúc môi trường

<p align="center">
        <img src="imgs/Visualization.gif" width="60%"> 
</p>

# CẤU TRÚC DỰ ÁN
```
SourceCode/
│── configs/      
│── dataloader/         
│── dataset/
│── network/    
│── pretrained_weight/    
│── utils/
│── train.py
│── visualize.py
│── infer.py
```

## Set up data và môi trường

1,Tạo môi trường `conda create -n polarnet python=3.8`
                  `conda activate polarnet`
2, Tải môi trường`pip install -r requirements.txt`

2, Tải data http://www.semantic-kitti.org/dataset.html.

3, Giải nén

4, Đặt data ở vị trí như dưới:

```
./
├── train.py
├── ...
└── dataset/
    ├──sequences
        ├── 00/           
        │   ├── velodyne/	# Unzip from KITTI Odometry Benchmark Velodyne point clouds.
        |   |	├── 000000.bin
        |   |	├── 000001.bin
        |   |	└── ...
        │   └── labels/ 	# Unzip from SemanticKITTI label data.
        |       ├── 000000.label
        |       ├── 000001.label
        |       └── ...
        ├── ...
        └── 21/
	    └── ...
```

## Training
```
python train.py
```

## Infer
```
python infer.py
```
## Visualize
```
python visualize.py --sequence {} --dataset ./dataset --predictions ./out
```
