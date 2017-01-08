# A Discriminatively Learned CNN Embedding for Person Re-identification

In this package, we provide our training and testing code for the paper. 
We also include matconvnet-beta23 modified for our paper.
All codes have been test on Ubuntu14.04 with Matlab R2015b.

#Data
Market1501 (You can find it on https://liangzheng.org)

#To test
1.Use `start-zzd.sh` to start matlab. (You need to add your CUDA path in it. Just type './start-zzd.sh' to run it.)
2.Compile matconvnet. (You just need to uncomment and modify some lines in `gpu_compile.m` and run it. Try it~)
If you meet something wrong, you can refer to http://www.vlfeat.org/matconvnet/install/

2.After compilation, run `test2/test_gallery_res.m` to extract the features of gallery. They will store in a .mat file. You can use it to do evaluation.

#To train
1.compile matconvnet.
If you meet something wrong, you can refer to http://www.vlfeat.org/matconvnet/install/

2.Add your dataset path into `prepare_data.m` and run it. Make sure the code outputs right image path.

3.run `train_id_net_res_2stream.m` to have fun.
