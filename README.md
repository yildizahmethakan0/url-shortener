# URL Shortener API

Bu proje, .NET ile geliştirilmiş basit bir URL kısaltma servisidir. API, kısaltılmış bağlantılar oluşturma, analiz etme ve yönlendirme işlemleri için üç temel uç nokta sunar.

## Endpoints

### 1. Kısaltılmış URL Oluşturma  
**POST /link/add**  
- Kullanıcıdan gelen uzun URL'yi alır.  
- Benzersiz bir kısa URL oluşturur.  
- Kısa URL'yi veritabanında saklar.  
- İsteğe bağlı olarak son kullanma süresi belirlenebilir.

### 2. Kısaltılmış URL Analizi  
**GET /link/analyze?url={shortened_url}**  
- Belirtilen kısa URL hakkında analiz bilgisi döner.  
- Erişim sayısı ve bazı ek veriler yer alabilir.

### 3. Yönlendirme  
**GET /{shortened_code}**  
- Girilen kısa URL kodunu alır.  
- Kullanıcıyı orijinal uzun URL'ye yönlendirir.

## Özellikler

- Girilen URL'lerin doğruluğunu kontrol eder.  
- Her bağlantı için benzersiz kısa URL üretir.  
- Kısaltılmış bağlantılar için son kullanma tarihi tanımlanabilir.  
- Bağlantı kullanımına dair analiz verileri toplar.

## Kurulum ve Kullanım

1. Reponun klonlanması:
```bash
git clone https://github.com/yildizahmethakan0/url-shortener.git
cd url-shortener
