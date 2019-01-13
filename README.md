# tf_teknofest_qa
Teknofest Yapay Zeka yarışmasında kullanılan Soru-Cevap modeli.

Bu model <b>Encoder-Fully Connected</b> yapısındadır. Ayarlanabilir <b>Encoder-Decoder</b> modeli için bu repoya bakılabilir: <a href="https://github.com/fmehmetun/tf_encdec_seq2seq">fmehmetun/tf_encdec_seq2seq</a>

# Model
<p align="center">
<img width="80%" src="img/diyagram.jpg" />
</p align="center">

<b>EncDenseModel.py:</b> Modeli Tensorflow kütüphanesiyle inşa eder.<br>
<b>egit.py:</b> Model verinin oluşturulan matris haliyle eğitilir.<br>
<b>etkilesimli.py:</b> Modelin kullanıcıyla etkileşime geçmesini sağlar.<br>
<b>tahmin_dosya.py:</b> Soruları içeren dosyayı satır satır okur ve cevapları çıkartır.<br>
<b>tahmin_dosya_json.py:</b> JSON girdisi alır ve modelden geçirerek cevapları JSON şeklinde çıkartır.<br>
<b>matris_sozluk_olustur.py:</b> Veri setindeki soru-cevap ikililerini modele verilebilecek matris formatlarına çevirir.<br>
<b>model.json:</b> Yapay zeka modelinde kullanılan parametreleri yapılandırmaya yarar.<br>

Eğitilmiş ağırlıklar buradan indirilip model/ klasörüne atılmalı: <a href="https://drive.google.com/file/d/10OLvPVGFnJXW6k1HWNtIkOSjf_uDq5cQ/view">model.tar.gz/</a>
Sistem FastText'in Türkçe için yayınladığı modeli kullandığı için buradan indirilebilir: <a href="https://s3-us-west-1.amazonaws.com/fasttext-vectors/wiki.tr.zip">wiki.tr.zip/</a>
Ardından matris_sozluk_olustur.py çalıştırılarak JSON formatından soru-cevaplar çıkartılarak matris formatlarına çevrilir.
Bundan sonra modelle etkileşime geçilebilir.
