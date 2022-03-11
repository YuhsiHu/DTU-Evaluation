# DTU-Evaluation
Matlab code for DTU dataset evaluation.

## Environment
Matlab R2018a with **statistics and machine learning** toolbox.

## Data preparation
For quantitative evaluation on DTU dataset, download [SampleSet](http://roboimagedata.compute.dtu.dk/?page_id=36) and [Points](http://roboimagedata.compute.dtu.dk/?page_id=36). Unzip them and place `Points` folder in `SampleSet/MVS Data/`.
  The structure looks like:
```
SampleSet
├──MVS Data
      └──Points
```

## Parameter settings
In `BaseEvalMain_web.m`, set parameters as following steps:
1. Set `dataPath` as path to standard point clouds like `${YOUR_ROOT_DIR}/SampleSet/MVS Data/`.
2. Set `plyPath` as the directory that stores the reconstructed point clouds like `${YOUR_ROOT_DIR}/eval` 
3. Set `resultsPath` as the directory to store the evaluation results(.mat file) like `${YOUR_ROOT_DIR}/results`.
4. Set `method_string` as the prefix of the point cloud file. For example, if the file name of a  reconstructed point cloud is `final3d_model001_l3.ply`, the prefix is `final3d_model`. The `001` means scan1 and `l3` implies Lighting condition.
5. Then run `BaseEvalMain_web.m` in matlab.
