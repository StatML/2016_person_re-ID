# A Discriminatively Learned CNN Embedding for Person Re-identification

In this package, we provide our training and testing code written in [Matconvnet](http://www.vlfeat.org/matconvnet/) for the paper [A Discriminatively Learned CNN Embedding for Person Re-identification] (https://arxiv.org/abs/1611.05666).
 
We also include matconvnet-beta23 which has been modified for our paper. All codes have been test on Ubuntu14.04 and Ubuntu16.04 with Matlab R2015b.

* [Xuanyi Dong](https://github.com/D-X-Y) also realizes our paper in [Caffe](https://github.com/D-X-Y/caffe-reid). Thanks!

![](https://github.com/layumi/2016_person_re-ID/blob/master/figure3.jpg)
#Dataset
Download [Market1501 Dataset] (http://www.liangzheng.org/Project/project_reid.html)
#Models
Since I use the lfs in github, this reposity may be over data quota.
Alternatively, you can download the models from [GoogleDriver](https://drive.google.com/file/d/0B0VOCNYh8HeRbEhIR3FyakkzUlU/view?usp=sharing).

#To Test
1. Use `start-zzd.sh` to start matlab. (You need to add your CUDA path in it. Then just type `./start-zzd.sh` to run it.)

2. Compile matconvnet. (You just need to uncomment and modify some lines in `gpu_compile.m` and run it. Try it~)
If you fail in compilation, you may refer to http://www.vlfeat.org/matconvnet/install/

3. After compilation, run `test2/test_gallery_res.m` to extract the features of gallery. They will store in a .mat file. You can use it to do evaluation.
(For example, you may modify the [Market1501 baseline code](http://www.liangzheng.org/Project/project_reid.html) to evaluate our model. It may take a while.)

#To Train
1. Compile matconvnet. If you fail in compilation, you can refer to http://www.vlfeat.org/matconvnet/install/

2. Add your dataset path into `prepare_data.m` and run it. Make sure the code outputs the right image path.

3. Run `train_id_net_res_2stream.m` to have fun.

# Citation
Please cite this paper in your publications if it helps your research:
```
@article{zheng2016discriminatively,
  title={A Discriminatively Learned CNN Embedding for Person Re-identification},
  author={Zheng, Zhedong and Zheng, Liang and Yang, Yi},
  journal={arXiv preprint arXiv:1611.05666},
  year={2016}
}
```
#Thanks
Thanks for Xuanyi Dong to realize our paper in Caffe.

Thanks for Weihang Chen to report the bug in `prepare_data.m`.
