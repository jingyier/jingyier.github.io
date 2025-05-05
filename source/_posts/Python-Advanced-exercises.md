---
title: Python_Advanced_exercises
date: 2025-05-01 09:48:44
tags: [学习]
---
## exercises 笔记
### IOU
```
def calculate_iou(box1, box2):
    # 计算交集区域的坐标
    x_left = max(box1[0], box2[0])
    y_top = max(box1[1], box2[1])
    x_right = min(box1[2], box2[2])
    y_bottom = min(box1[3], box2[3])
```
box是一个矩形，其四个参数两两一组，(box[0],box[1])是矩形左上角的坐标，(box[2],box[3])是矩形右下角的坐标，
用max,min函数得到
```
    # 计算交集区域的面积
    intersection_width = max(0, x_right - x_left)
    intersection_height = max(0, y_bottom - y_top)
    intersection_area = intersection_width * intersection_height

```
wight与height为负时box1和box2无交集，用max将其置为0，这样得到的交集面积也为0

```
    # 计算两个框各自的面积
    area1 = (box1[2] - box1[0]) * (box1[3] - box1[1])
    area2 = (box2[2] - box2[0]) * (box2[3] - box2[1])

    # 计算并集面积
    union_area = area1 + area2 - intersection_area

    # 处理并集面积为0的情况（避免除以0）
    if union_area == 0:
        return 0.0

    # 计算IoU
    iou = intersection_area / union_area
    return iou

```