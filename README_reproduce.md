# Download the model
```
mkdir /export/share/projects/videogen/checkpoints/wildcamera/
cd /export/share/projects/videogen/checkpoints/wildcamera/
mkdir Release
cd Release
wget https://huggingface.co/datasets/Shengjie/WildCamera/resolve/main/checkpoint/wild_camera_all.pth?download=true
mv wild_camera_all.pth?download=true wild_camera_all.pth
wget https://huggingface.co/datasets/Shengjie/WildCamera/resolve/main/checkpoint/wild_camera_gsv.pth?download=true
mv wild_camera_gsv.pth?download=true wild_camera_gsv.pth
cd ..
mkdir swin_transformer
cd swin_transformer
wget https://huggingface.co/datasets/Shengjie/WildCamera/resolve/main/checkpoint/swin_large_patch4_window7_224_22k.pth?download=true
mv swin_large_patch4_window7_224_22k.pth?download=true swin_large_patch4_window7_224_22k.pth
```

Correct linking by going to the WildCamera code directory, then call:
```
ln -s /export/share/projects/videogen/checkpoints/wildcamera/ model_zoo
```

# Download demo dataset
```
mkdir /export/share/projects/videogen/data/wildcamera
cd /export/share/projects/videogen/data/wildcamera
wget https://huggingface.co/datasets/Shengjie/WildCamera/resolve/main/asset/dollyzoom.tar
tar -xvf dollyzoom.tar
rm dollyzoom.tar
wget https://huggingface.co/datasets/Shengjie/WildCamera/resolve/main/asset/images-from-github-wt-intrinsic.tar
tar -xvf images-from-github-wt-intrinsic.tar
rm images-from-github-wt-intrinsic.tar
```

Correct linking by going to the WildCamera code directory, then call:
```
ln -s /export/share/projects/videogen/data/wildcamera data
```

# Install additional dependencies
```
pip install -U openmim
mim install mmcv
```