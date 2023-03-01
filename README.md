# Dynamic fry counting based on multi-object tracking and one-stage detection
## Counting Result Samples

### For video examples please download and watch：[video link](https://github.com/hanyuyaa/Dynamic-fry-counting/blob/master/Samples/videos/counting.mp4)
---
![image](https://github.com/hanyuyaa/Dynamic-fry-counting/blob/master/Samples/images/all.png)
## Abstract
Fry counting is an essential task in aquaculture that provides valuable information for feedstuff feeding, culture density adjustment, and estimating fish economic benefit. However, most current computer vision-based fry counting methods are designed for statically counting, with a fixed number of fry in a container. As a result, these methods are not suitable for dynamic scenarios, such as flowing water, due to the effects of factors like water velocity and uneven lighting, which can cause errors in counting. To address this issue and improve accuracy, we propose a dynamic fry counting method capable of dealing with large-number fry counting. Specifically, we regard fry counting as a Multiple Object Tracking (MOT) problem based on Tracking-By-Detection (TBD) framework. Firstly, a streaming fry dataset is constructed for training the detection model and videos with varying numbers of fry are manually counted for counting tests. Secondly, due to the highly similar appearance of fry, Simple Online and Realtime Tracking (SORT) is combined with You Only Look Once Version 5 Nano (YOLOv5-Nano) to achieve fry tracking. To achieve stable tracking of fry movement, the SORT algorithm is improved based on multi-matching and trajectory recovery, reaching 82.6% multi-object tracking accuracy. Finally, fry counting is realized based on the intersection of a counting line and moving trajectories. The results indicate that the proposed counting method achieves 96.4% accuracy and can be implemented on CPU at 5-10 frames per second (fps) and GPU at 15-35 fps. In conclusion, the proposed method automatically counts the number of fry in videos with higher speed and greater accuracy, facilitating automated fishery farming.

## Contributions
* Fry counting is considered a dynamic task, and we design counting method based on the rapidly developing TBD algorithms, which reduces the impact of fish occlusion on counting results to some extent.  
* To address the effect of different occlusion degrees between fry on tracking, we improve the SORT algorithm by multiple matching and trajectory recovery, design matching algorithms for different objects of multiple matching, and obtain high accuracy on multi-object tracking.
* The proposed dynamic fry counting model has a simple structure with fewer parameters. As a result, the computing speed on CPU and GPU can reach 5-10fps and 15-35fps, respectively, which has a real-time performance and lays the foundation for practical use.

## Updates
* [2023-02-25] We have updated the count results for dynamic fry counting


