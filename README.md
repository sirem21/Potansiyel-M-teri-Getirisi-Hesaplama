# Gezinomi Miuul Project
Miuul Python Programming for Data Science  (Case Study)
Projenin amaci: Kural Tabanlı Sınıflandırma ile Potansiyel Müşteri Getirisi Hesaplama
İş Problemi: Gezinomi yaptığı satışların bazı özelliklerini kullanarak seviye tabanlı (level based) yeni satış tanımları oluşturmak ve bu yeni satış tanımlarına göre segmentler oluşturup bu segmentlere göre yeni gelebilecek müşterilerin şirkete ortalama ne kadar kazandırabileceğini tahmin etmek istemektedir. Örneğin: Antalya’dan Herşey Dahil bir otele yoğun bir dönemde gitmek isteyenbir müşterinin ortalama ne kadar kazandırabileceği belirlenmekisteniyor.
Veri Seti Hikayesi: gezinomi_miuul.xlsx veri seti Gezinomi şirketinin yaptığı satışların fiyatlarını ve bu satışlara ait bilgiler içermektedir. Veri seti her satış işleminde oluşan kayıtlardan meydana gelmektedir. Bunun anlamı tablo tekilleştirilmemiştir. Diğer bir ifade ile müşteri birden fazla alışverişyapmış olabilir.

# miuul_gezinomi.xlsx' Değişkenler
SaleId: Satis Id
SaleDate : Satış Tarihi
Price: Satış için ödenen fiyat
ConceptName:Otel konsept bilgisi
SaleCityName: Otelin bulunduğu şehir bilgisi
CheckInDate:Müşterinin otelegirişitarihi
CInDay:Müşterinin otele giriş günü
SaleCheckInDayDiff: Check in ile giriş tarihi gün farkı
Season:Otele giriş tarihindeki sezon bilgisi

# Görev 1: Aşağıdaki Soruları Yanıtlayınız
Soru1 : miuul_gezinomi.xlsx dosyasını okutunuz ve veri seti ile ilgili genel bilgileri gösteriniz..
Soru 2:Kaçunique şehirvardır? Frekanslarınedir?
Soru 3:Kaç unique Concept vardır?
Soru4: Hangi Concept’den kaçar tane satış gerçekleşmiş?
Soru5: Şehirlere göre satışlardan toplam ne kadar kazanılmış?
Soru6:Concept türlerine göre göre ne kadar kazanılmış?
Soru7: Şehirlere göre PRICE ortalamaları nedir?
Soru 8:Conceptlere göre PRICE ortalamaları nedir?
Soru 9: Şehir-Concept kırılımındaPRICE ortalamalarınedir?

# Görev 2: SaleCheckInDayDiff değişkenini kategorik bir değişkene çeviriniz.
• SaleCheckInDayDiff değişkeni müşterinin 
CheckIn tarihinden ne kadar önce satin alımını tamamladığını gösterir.
• Aralıkları ikna edici şekilde oluşturunuz.
Örneğin: ‘0_7’, ‘7_30', ‘30_90', ‘90_max’ aralıklarını kullanabilirsiniz.
• Bu aralıklar için "Last Minuters", "Potential Planners", "Planners", "Early Bookers“ isimlerini kullanabilirsiniz.

# Görev 3: COUNTRY, SOURCE, SEX, AGE kırılımında ortalama kazançlar nedir?
![image](https://github.com/sirem21/Potential-Customer-ROI-Calculation/assets/134364808/d0f1dc20-529d-49a9-a566-06ad24be18fb)

# Görev 4: City-Concept-Season kırılımının çıktısını PRICE'a göre sıralayınız
![image](https://github.com/sirem21/Potential-Customer-ROI-Calculation/assets/134364808/373a8d50-f691-4b72-ae00-0288e065b90e)

# Görev 5: Indekste yer alan isimleri değişken ismine çeviriniz.
Üçüncü sorunun çıktısında yer alan PRICE dışındaki tüm değişkenler index isimleridir. Bu isimleri değişken isimlerine çeviriniz

# Görev 6: Yeni seviye tabanlı müşterileri (persona) tanımlayınız.
• Yeni seviye tabanlı satışları tanımlayınız ve veri setine değişken olarak ekleyiniz.
• Yeni eklenecek değişkenin adı: sales_level_based
• Önceki soruda elde edeceğiniz çıktıdaki gözlemleri bir araya getirerek sales_level_based değişkenini oluşturmanız gerekmektedir.
![image](https://github.com/sirem21/Potential-Customer-ROI-Calculation/assets/134364808/57499c4e-247c-4a32-b3a8-1883037a8e99)

# Görev 7: Yeni müşterileri (personaları) segmentlere ayırınız.
• Yeni personaları PRICE’a göre 4 segmente ayırınız.
• Segmentleri SEGMENT isimlendirmesi ile değişken olarak agg_df’e ekleyiniz.
• Segmentleri betimleyiniz (Segmentlere göre group by yapıp price mean, max, sum’larını alınız).

# Görev 8: Yeni gelen müşterileri sınıflandırıp, ne kadar gelir getirebileceklerini tahmin ediniz.
• Antalya’da herşey dahil ve yüksek sezonda tatil yapmak isteyen bir kişinin ortalama ne kadar gelir kazandırması beklenir?
• Girne’de yarım pansiyon bir otele düşük sezonda giden bir tatilci hangi segmentte yer alacaktır?
