# ILFNet
The code of paper: "Accurate Precipitation Forecasting by Efficiently Learning from Massive Atmospheric Variables and Scarce Precipitation Samples".

To get the predicted results:

(1) Create a new environment by:

conda create -n py39 gdal python=3.9

pip install torch==2.0.1

pip install tqdm pandas matplotlib opencv-python lpips scikit-image numba zarr xarray

(3) Download and Modify the paths of the dataset and each necessary file.

(4) Run the script: torchrun --nproc_per_node=1 --master_port=55568 weatherbench2_main/model_prob/PFNet/main_latent.py --epoch 500 --ex_name '260201_usa-precip-baseline' --batch_size 7 --val_batch_size 1 --test 1 --clip_grad 0 --save_iter 10

Should you have any questions, please feel free to contact me at whu_lsl@whu.edu.cn.

