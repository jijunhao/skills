conda导出已有环境：
conda env export > environment.yaml

环境会被保存在 environment.yaml文件中。当我们想再次创建该环境，或根据别人提供的.yaml文件复现环境时，可以：

conda env create -f environment.yaml

就可以复现安装环境。移植过来的环境只是安装了你原来环境里用conda install等命令直接安装的包，你用pip之类装的东西没有移植过来，需要你重新安装。



pip导出安装的库到requirements.txt

pip freeze > requirements.txt

pip导入requirements.txt中列出的库到系统

pip install -r requirements.txt