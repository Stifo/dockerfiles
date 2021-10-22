# building

docker build -t sht3v0/tensorflow:2.6.0-jupyterlab-gpu .

# running

docker run -it --rm --gpus all -p 8888:8888 -v "$(pwd)"/workspace:/tf/workspace sht3v0/tensorflow:2.6.0-jupyterlab-gpu
