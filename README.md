# AI Behavior Prediction - Transformer Model

Bu proje, **Transformer modellerini kullanarak insan davranışlarını tahmin etmek** için geliştirilmiştir.

## 🚀 Proje İçeriği:
- **Veri Ön İşleme:** Veri seti yüklendi ve temizlendi (`data_preprocessing.ipynb`).
- **Model Eğitimi:** `BERT` modeli ile insan davranış tahmini yapıldı (`train_transformer.ipynb`).
- **Model Kaydedildi:** Eğitilmiş model `transformer_model.pt` dosyasında saklandı.
- **Test Edildi:** Model başarıyla tekrar yüklendi ve test edildi.

## 📂 Proje Dosyaları:
- `data_preprocessing.ipynb` → Veri ön işleme
- `train_transformer.ipynb` → Model eğitimi
- `transformer_model.pt` → Eğitilmiş model dosyası

## 🔧 Modeli Kullanma:
Eğitilmiş modeli tekrar yüklemek için:
```python
import torch
from transformers import AutoModel

model = AutoModel.from_pretrained("bert-base-uncased")
model.load_state_dict(torch.load("transformer_model.pt"))
model.eval()
