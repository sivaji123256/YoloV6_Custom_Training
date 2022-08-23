# YoloV6
YoloV6 Custom Dataset Training 
## 1. Clone the repo as follows:
      !git clone  https://github.com/sivaji123256/YoloV6.git
## 2. Change the directory yolov6 parent folder 
    * Run the following command to install required packages 
       !pip install -r requirements.txt
    * In the parent folder access dataset.yaml file and add the required path to the train dataset and test dateset and change other parametrs as required
    * In the weights add required yolov6 pretrained weights.pt files
## 3. Training on custom dataset
    * Use the following command to start training on custom dataset. 
      !python tools/train.py --batch 16 --conf configs/yolov6s_finetune.py --data-path dataset.yaml --device 0 --epochs 2 --eval-interval 2
    * change the parameters as required
## 4. For evaluation 
    * Run the following command 
      !python tools/eval.py --data dataset.yaml  --weights runs/train/exp/weights/best_ckpt.pt --device 0
## 5. For inference run the following command
      !python tools/infer.py --weights runs/train/exp/weights/best_ckpt.pt --source 100.jpg --yaml dataset.yaml --device 0     
