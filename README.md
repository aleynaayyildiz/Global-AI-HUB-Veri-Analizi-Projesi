# Global AI HUB Veri Analizi Projesi
 Online Retail Dataset
 ![image](https://github.com/user-attachments/assets/cf5e1e0c-12b4-4750-b5da-da3b69bc09b0)

VERİ SETİ HAKKINDA

01/12/2010 ile 09/12/2011 tarihleri arasında gerçekleşen tüm işlemleri içeren uluslararası bir veri setidir ve Birleşik Krallık merkezli ve kayıtlı bir mağaza dışı çevrimiçi perakendeye aittir. Şirket esasen her durumda kullanılabilecek benzersiz hediyeler satmaktadır. Şirketin birçok müşterisi toptancıdır.

DEĞİŞKEN BİLGİSİ

- **StockCode**: Ürün (madde) kodu. Nominal, her bir farklı ürüne benzersiz olarak atanmış 5 haneli tam sayı.

- **Description**: Ürün (madde) adı. Nominal.

- **Quantity**: Her bir ürün (madde) için işlem başına miktarlar. Sayısal.

- **InvoiceDate**: Fatura Tarihi ve saati. Sayısal, her işlemin oluşturulduğu gün ve saat.

- **UnitPrice**: Birim fiyat. Sayısal, ürünün birim fiyatı sterlin cinsinden.

- **CustomerID**: Müşteri numarası. Nominal, her bir müşteri için benzersiz olarak atanmış 5 haneli tam sayı.

- **Country**: Ülke adı. Nominal, her bir müşterinin ikamet ettiği ülkenin adı.

## VERİ HAZIRLIK VE TESPİTLER

- **Eksik ve tutarsız veriler üzerinde kapsamlı bir temizlik işlemi uygulandı:**

  - **Country Kolonu**: Eksik değerler, `InvoiceNo`'ya göre dolduruldu. Geriye kalan eksik değerler daha ileri yöntemlerle tamamlandı.
  
  - **CustomerID Kolonu**: Eksik müşteri kimlikleri, `InvoiceNo` ile eşleştirilerek doldurulmaya çalışıldı.
  
  - **StockCode ve Description Kolonları**: Ürün açıklamaları ve stok kodları arasında birebir eşleşmeler tespit edilerek eksik veriler tamamlandı.
  
  - **Zaman Değerleri**: Tarih ve saat sütunlarında eksik veya hatalı değer bulunmadı, ancak veriler haftalık, aylık ve günlük periyotlarla analiz için dönüştürüldü.

- **Aykırı Değer Analizi:**

  - `Quantity` ve `UnitPrice` kolonlarında aykırı değerler tespit edildi. Bu aykırı değerler temizlenirken, iş süreçlerine zarar vermeyecek şekilde dikkatle ele alındı.
  ## Veri Analizi

### Zaman Analizi:
- **Haftanın Günlerine Göre Alışveriş Yoğunluğu**: 
  - Perşembe günleri en yoğun alışveriş günü olarak tespit edilmiştir.
  - Cumartesi günlerinin ise satış açısından en düşük yoğunluğa sahip olduğu gözlemlenmiştir.
  
- **Saatlik Analiz**: 
  - Öğleden sonra saatlerinde (12:00 PM - 3:00 PM) alışveriş yoğunluğunun arttığı belirlenmiştir.

### En Çok Gelir Getiren Ürünler:
- **En Yüksek Gelir Getiren Ürünler**: 
  - "WHITE HANGING HEART T-LIGHT HOLDER" ve "PARTY BUNTING", en yüksek gelir getiren ürünler olarak öne çıkmıştır.
  
- **Toplam Gelir Üzerindeki Etki**:
  - İlk 10 ürün, toplam gelir üzerinde büyük bir etkiye sahiptir ve bu ürünler satış stratejileri için kritik öneme sahiptir.

### Müşteri Davranışları:
  - Eksik `CustomerID` değerleri doldurulduktan sonra, müşteri bazlı analizler yapılabilir hale getirilmiştir.

