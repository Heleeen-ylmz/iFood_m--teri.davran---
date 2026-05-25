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
*Müşterinin yıllık geliri (income) arttıkça, toplam harcama tutarı lineer olarak artar.
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

A,B,C Aşamalrı bitti çıkarımlarımıza bakalım.

Veriden Stratejiye: Bir Pazarlama Analitiği Hikayesi

Python ve SQL kullanarak yürüttüğüm müşteri davranış analizi projesinin ilk aşamalarını (A, B ve C) tamamladım! Ham verileri işlenebilir içgörülere dönüştürürken pazarlama bütçelerini optimize edecek çok çarpıcı sonuçlar elde ettim:

 Sonuç 1: Kampanya Başarısında Rekor Oran

Şirketin geçmişte gerçekleştirdiği 5 farklı kampanyanın başarı oranları %1.36 ile %7.42 arasında seyrederken; uygulanan en güncel stratejiyle (Response) bu başarı oranını %15.06 seviyesine çıkardık. Bu, geçmiş ortalamaların tam 2.5 katı bir başarı demek!

 Sonuç 2: "Doğru" Müşteriyi Yakalamak

Tekliflerimizi kabul eden müşterilerin toplam harcama ortalaması 985.66 birim iken, kabul etmeyenlerin ortalaması 540.41 birimde kaldı. Yani son kampanyamız, indirim kovalayan kitleyi değil; markaya en çok finansal değer katan "Yüksek Değerli" (High-Value) müşterileri yakalamayı başardı.
Peki, bu muazzam harcama farkı ve katılım oranları sadece istatistiksel bir tesadüf mü? >
Bir sonraki paylaşımımda, bu sonuçların arkasındaki bilimsel kanıtları sunmak için Bağımsız İki Örneklem T-Testi ve Ki-Kare (Chi-Square) hipotez analizleriyle veriyi daha derinden konuşturacağım.

HİPOTEZ TESTLERİ DE BİTTİ DETAYLI SONUCLAR ADI GECEN DOSYADA VAR(not düşerek ilerledim)

son kısım*MÜŞTERİ_SEGMANTASYONU SUNUÇLARI:

Elbow Method ile 4 gruba ayırmaya karar verdim müşterileri.

Şirket cirosunun %80'ini sırtlayan Cluster 3 (VIP) ve Cluster 0 (Şarap Severler) grupları sistemden son derece memnun ve şikayet oranları çok düşük. Ancak sitemizi en sık ziyaret eden Cluster 2 (Genç Fırsatçılar) bütçe yetersizliğinden sepeti dolduramıyor. En yaşlı kitlemiz olan Cluster 1 ise ciddi bir memnuniyetsizlik (%1.54 şikayet) yaşıyor, acilen operasyonel destek verilmeli.

