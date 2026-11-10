---
{"dg-publish":true,"permalink":"/projects/project-log/","tags":["gardenEntry"],"dg-note-properties":{}}
---

笔记的发布地址: https://my-digital-garden-8o3.pages.dev
#### 2026.11.10
- 和翁工. 储工讨论相关的方案, 讨论为什么昨天计算出来的功率差这么多

现在我按照翁工的计算方式, 使用1.5(UdxId)+1.5(UqxIq)来计算, 通过对电压和电流进行滑动平均滤波, 下面是计算的结果: 

| 窗口频率       | 窗口时长     | P 均值         |
| ---------- | -------- | ------------ |
| 20 Hz      | 50 ms    | 0.9064 W     |
| 100 Hz     | 10 ms    | 1.0058 W     |
| **200 Hz** | **5 ms** | **1.1675 W** |
| 1000 Hz    | 1 ms     | 2.2736 W     |
| 5000 Hz    | 0.2 ms   | 86.9081 W    |

![img_v3_0217a_4a47c27c-35a8-4c63-bc5a-4bdd8471005g.jpg\|462](/img/user/Projects/assets/Project_log/img_v3_0217a_4a47c27c-35a8-4c63-bc5a-4bdd8471005g.jpg)