# TF + GPU + JupyterLab Dockerfile
Adopted Tensorflow's [gpu-jupyter.Dockerfile](https://github.com/tensorflow/tensorflow/blob/9a0854ca7684078ea9a160c3eae66a3862d64ba5/tensorflow/tools/dockerfiles/dockerfiles/gpu-jupyter.Dockerfile) to contain jupyter-lab

## building
```bash
docker build -t sht3v0/tensorflow:2.6.0-jupyterlab-gpu .
```

## running
```bash
docker run -it --rm --gpus all -p 8888:8888 -v "$(pwd)"/workspace:/tf/workspace sht3v0/tensorflow:2.6.0-jupyterlab-gpu
```
