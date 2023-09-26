# SwiftWhileKonuAnlatimi
Swift programlama dilinde while döngüsü, belirli bir koşul doğru olduğu sürece belirtilen 
işlemleri tekrarlayan bir döngü türüdür. while döngüsü, başlangıçta koşulu kontrol eder ve 
koşul doğru olduğu sürece döngü içindeki kodu çalıştırır. İşte while döngüsünün temel kullanımı:
while kosul {
    // Koşul doğru olduğu sürece yapılacak işlemler
}

kosul ifadesi, her döngü adımında kontrol edilen bir mantıksal ifadedir. Eğer bu koşul doğruysa, 
döngü içindeki işlemler tekrarlanır. Eğer koşul yanlışsa, döngü sona erer ve program diğer işlemlere devam eder.

İşte birkaç örnek:

Sayıları Toplama
var toplam = 0
var sayi = 1

while sayi <= 10 {
    toplam += sayi
    sayi += 1
}

print("Toplam: \(toplam)")

Bu örnekte, while döngüsü kullanarak 1'den 10'a kadar olan sayıları topluyoruz.

Kullanıcıdan Girdi Alma

import Foundation

var kullaniciAdi: String?

while kullaniciAdi == nil {
    print("Lütfen kullanıcı adınızı girin: ")
    if let giris = readLine() {
        kullaniciAdi = giris
    }
}

print("Merhaba, \(kullaniciAdi!)")

Bu örnekte, kullanıcıdan bir kullanıcı adı girmesini isteyen bir döngü kullanıyoruz. Kullanıcı adı girildiğinde döngü sona erer.

Sonsuz Döngü

Bir while döngüsünün koşulu hiçbir zaman yanlış olmayabilir, bu nedenle döngü sonsuz bir döngü haline gelebilir. Bu tür bir 
döngüyü durdurmak için dikkatli olmalısınız ve uygun bir koşul eklemelisiniz.

var sonsuz = 1

while true {
    print("Bu bir sonsuz döngüdür.")
    
    if sonsuz == 10 {
        break // Sonsuz döngüyü sonlandır
    }
    
    sonsuz += 1
}

Bu örnekte, while true ifadesi ile sonsuz bir döngü oluşturduk, ancak break ifadesini kullanarak döngüyü belirli bir koşulda sonlandırıyoruz.

while döngüsü, belirli koşullar altında tekrarlayan işlemler yapmanızı sağlar. Ancak, sonsuz döngülerin kaçınılmaz olarak
programınıza zarar verebileceğini unutmamalısınız, bu nedenle döngüyü sonlandırmak için uygun bir koşul eklemek önemlidir.
