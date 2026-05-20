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


##🛠 Behavior Tree (BT) Motorunu Kurma
Projemiz, endüstri standardı olan BehaviorTree.CPP v4 kütüphanesini kullanmaktadır. Bu kütüphaneyi yerel ortamınıza kurmak ve projenin bir parçası yapmak için aşağıdaki adımları takip edin:

1. Submodule Tanımlama ve Çekme
Repo klonlandıktan sonra, alt modül olan BT motorunu çekmek için ana dizinde şu komutu çalıştırın:

Bash
git submodule update --init --recursive
