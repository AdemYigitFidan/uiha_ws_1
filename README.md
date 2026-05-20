# UİHA Otonom Görev Yönetim Sistemi

Bu depo, otonom görev yönetim sistemini ve reaktif karar verme mekanizmasını içermektedir.

## 📂 Dosya Dizin Yapısı

Projemiz üç ana modülden oluşan modüler bir yapıya sahiptir:

```text
uiha_ws/
├── BehaviorTree.CPP/       # Alt modül (Submodule): Ana karar motoru
├── uiha_bt/                # C++ Görev Ağacı Paketi (Düğümler ve Mantık)
│   ├── config/             # XML görev ağacı tanımları
│   ├── include/uiha_bt/    # HPP başlık dosyaları (Düğüm tanımları)
│   └── src/                # CPP kaynak dosyaları (Düğüm mantıkları)
└── uiha_yolo/              # Python YOLO Algılama Paketi
    ├── weights/            # Eğitilmiş model (best.pt)
    └── uiha_yolo/          # YOLO node scriptleri
```

##🛠 Behavior Tree (BT) Motorunu Kurma
Projemiz, endüstri standardı olan BehaviorTree.CPP v4 kütüphanesini kullanmaktadır. Bu kütüphaneyi yerel ortamınıza kurmak ve projenin bir parçası yapmak için aşağıdakileri yapın:

Submodule Tanımlama ve Çekme
Repo klonlandıktan sonra, alt modül olan BT motorunu çekmek için ana dizinde şu komutu çalıştırın:

```text
git submodule update --init --recursive
```
## Görev Ağacı 
### Ana Karar Verme Mekanizmamız
<img width="815" height="323" alt="image" src="https://github.com/user-attachments/assets/79d827b6-cd88-44d4-b3c3-55244344aba3" />

### FailSafe Katmanımız

Olası güvenlik sorunları ve onlara karşı alınması gereken aksiyonlar
<img width="1000" height="469" alt="image" src="https://github.com/user-attachments/assets/901ace38-5000-44b9-856e-5081438d26a8" />


### Görev Seçim Katmanımız

Otonom sistemin hangi görevi yapacağının kararını aldığı ve gerekli aksiyonları aldığı katmandır
<img width="1717" height="545" alt="image" src="https://github.com/user-attachments/assets/5d80027e-b338-43e4-9667-a5b024818072" />

### Görüntü İşleme Katmanı

2. görev söz konusu olduğunda devreye giren taraf
<img width="1651" height="361" alt="image" src="https://github.com/user-attachments/assets/ab70fa6d-2e3c-491e-84bd-92b3779e137b" />






