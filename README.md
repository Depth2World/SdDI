# SdDI
Self-distilled Depth from Single-shot Structured Light with Intensity Reconstruction (TCI 2023)
### Pipeline
![pipeline](https://github.com/Depth2World/SdDI/blob/main/images/TCI2023pipeline.png)
### Datasets
**Synthetic Kinect Pattern**\
Prepare the synthetic data, which is rendered by the simulator from [CTD](https://github.com/autonomousvision/connecting_the_dots)

**Synthetic Observed Pattern**\
Prepare the synthetic data, which is rendered by the simulator from [DIS](https://github.com/idiap/DepthInSpace)

**Real-world Observed Pattern**\
From [DIS](https://github.com/idiap/DepthInSpace)

### Experiment
For example, we first train the network on **Synthetic Observed Pattern**, and then finetune on **Real-world Observed Pattern**.
#### 1 Synthetic 
1.1 Modify the datapath. Train the teacher model \
  `bash Tea_DIS.sh`\
1.2 Load the teacher model. Train the student model \
  `bash Stu_DIS.sh`

#### 2 Real-world
2.1 Fintune the teacher model \
  `bash Tea_DIS.sh`\
2.2 Load the teacher model. Train the student model \
  `bash Stu_DIS.sh` 


### Evaluation
`python Tea_Test.py` & `python Stu_Test.py`



### Contact 
For questions, feel free to contact us (yueli65@mail.ustc.edu.cn).

### Acknowledgements
We thank the authors who shared the code of their works. Particularly
 [CTD](https://github.com/autonomousvision/connecting_the_dots), 
 [DIS](https://github.com/idiap/DepthInSpace), and 
 [PSMNet](https://github.com/JiaRenChang/PSMNet)
### Citation
If you find it useful, please cite our paper.

    @article{li2023self,
    title={Self-distilled Depth from Single-shot Structured Light with Intensity Reconstruction},
    author={Li, Yue and Peng, Jiayong and Zhang, Yueyi and Xiong, Zhiwei},
    journal={IEEE Transactions on Computational Imaging},
    year={2023},
    publisher={IEEE}
    }

