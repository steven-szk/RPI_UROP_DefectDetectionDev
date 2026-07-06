# RPI_UROP_DefectDetectionDev
Development U-Net for UROP project running on RPI5

IP: 192.168.137.147
ssh steven@192.168.137.147
password: 

# New venv with picamera2 system packages
python3 -m venv --system-site-packages .venv

# activate venv 
source .venv/bin/activate

# deactivate venv
deactivate

# install packages
sudo apt install -y python3-picamera2 python3-libcamera
pip install -r requirements.txt


# IP server:
http://192.168.137.147:1234/




# STEPS FOR NEW PI:
sudo apt-get update 
sudo apt-get upgrade -y
git clone https://github.com/ICRS/Unibots-Team-1
# ORRRR: ./init.sh at the directory
python3 -m venv --system-site-packages .venv
source .venv/bin/activate
sudo apt install -y python3-picamera2 python3-libcamera
pip install torch torchvision --index-url https://download.pytorch.org/whl/cpu
pip install -r requirements.txt
yolo export model=custom_model_5.pt format=ncnn imgsz=640