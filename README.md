<img width="522" height="374" alt="image" src="https://github.com/user-attachments/assets/55c1a838-3f96-430a-bc1c-99cd88b91358" />


📦 1. Setup Environment

  conda create -n polarnet python=3.8
  
  conda activate polarnet
  
📥 2. Install dependencies

  pip install -r requirements.txt\
  
🏋️ 3. Training

  python train.py
  
🔮 4. Inference 

  python infer.py

🎨 5. Visualization 

python visualize.py \
--sequence 11 \
--dataset ./dataset \
--predictions ./out/SemKITTI
