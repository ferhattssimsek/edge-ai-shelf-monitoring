# Edge-AI Shelf Monitoring

**Uç Birimde Yapay Zekâ ve Ajan Tabanlı Bilgisayarlı Görü ile Akıllı Market Rafı İzleme ve Karar Destek Sistemi**

Bitirme Projesi - Ferhat Şimşek - İstanbul Rumeli Üniversitesi, Bilgisayar Mühendisliği
Danışman: Taner Çevik

## Özet
Rafın önündeki bir uç cihaz, görüntüyü buluta göndermeden boş rafları, eksik ürünleri
ve fiyat etiketlerini gerçek zamanlı tespit eder. Bir yapay zekâ ajanı bu bilgiden
hangi rafın önce doldurulacağını gerekçesiyle önerir.

## Mimari
- **edge/**: Raspberry Pi 5 + AI HAT+ (Hailo-8L), Camera Module 3, YOLOv8, PaddleOCR
- **backend/**: Java Spring Boot, PostgreSQL
- **agent/**: LLM + araç çağırma, kural tabanlı temel yöntem
- **web/**: React panel
- **docs/**: Rapor ve diyagramlar

## Mevcut Durum
- [x] Donanım kuruldu, kamera ve Hailo-8L tanınıyor (HailoRT firmware 4.23.0)
- [x] Hazır YOLOv8 (COCO) modeli ile Pi üzerinde canlı tespit: ~30 FPS
- [ ] Veri seti (SKU-110K + maket raf)
- [ ] Model eğitimi ve Hailo HEF derlemesi
