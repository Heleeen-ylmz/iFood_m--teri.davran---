ANALİZ ÖNCESİ VERİ SETİNE BAKIŞ
############################################################
1)** Veri seti öngörüsü
Ben bu şirketin sahibi olsaydım, neyi bilrsem daha çok para kazanırdım veya daha az zarar ederdim.
Şirket 5 tane kampanya yapmış ama hangisi başarılı oldu? Hangi müşteri grubu gerçekten alışveriş yapıyor?
Geliri yüksek - avantajı olmayan kişiler lüks (şarap, et) daha çok para harcıyorlar ve kampanyalara daha olumlu yanıt veriyorlar. (örnek hipotez)
Müşterilerimin en az %15'ini bir kampanyaya ikna edebiliyor miyim?
Hangi ülkede en çok ne sattım, kampanyalarımı buna göre düzenleyelim.
(eğer İspanya'da meyve, Kanada'da şarap satın fazla ise bütçemi İspanya'da meyve indirimi, Kanada'da şarap tadımı için kullanalım)
Kimlerin harcaması (bağlılığı) yüksek, kimler sistemden çıkmaya meyilli?
Gelir düzeyi ile şarap tüketimi arasındaki korelasyon istatistiksel olarak anlamlı mıdır? (p-value < 0.05?)
Şikayet eden müşterilerin harcama alışkanlıkları nasıl değişti? Şikayet sonrası kampanyalara tepki verdiler mi?
H₁ (gelir ve harcama)
Müşterinin yıllık geliri (income) arttıkça, toplam harcama tutarı lineer olarak artar.
(Pearson korelasyon katsayısı)
H₂ (çocuk ve harcama)
Evde çocuk olması şarap ve et gibi lüks tüketimi anlamlı derecede düşürür.
(T-testi: çocuğu olanlar - olmayanlar)
H₃ (eğitim ve kampanya)
Doktora (PhD) seviyesindeki müşterilerin kampanyalara yanıt verme oranı (Response), lisans mezunlarından daha yüksektir.
(Ki-kare testi: kategorik değişkenler arası ilişki)
H₄ (kanal tercihi)
Müşteri yaşlandıkça, web sitesi yerine mağazadan (NumStore Purchases) alışveriş yapma eğilimi artar.
2)** Yol haritası
A) Descriptive Phase
1.Veri setinde kayıp değerler var mı?
2.Aykırı değerler neler? (1 milyon geliri olan ama hiç alışveriş yapmayan bir veri mi var?)
3.Müşterilerin ülke bazlı dağılımı nasıl?
B) Segmentasyon (Grouping Phase)
4.Müşterileri alt-üst-orta gelir gruba göre sınıflandıralım.
5.Şikayetçi müşteriler en sadik müşterilerimiz olabilir mi? (Harcama toplam tutarı baktım)
C) Verimlilik (Actionable Phase)
6.Hangi kampanya (cmp1... cmp5) en düşük maliyetle en yüksek dönüşü sağladı?
7.İndirimde alışveriş yapan müşteri kitlesi toplam kazancı ne kadarını oluşturuyor?
#########################################################################################
