# Gizlilik ve Kullanım Koşulları Sayfaları

Bu klasördeki HTML dosyalarını **bir yerde yayınlayıp** uygulama ve mağaza başvurularında kullanacağınız URL’leri almanız gerekir.

## Dosyalar

- `gizlilik-politikasi.html` → Gizlilik Politikası
- `kullanim-kosullari.html` → Kullanım Koşulları
- `hesap-silme.html` → E-posta + şifre ile giriş ve hesap silme sayfası

## Nasıl yayınlanır?

### Seçenek 1: GitHub Pages

1. Bu projeyi GitHub’a push edin.
2. Repo → **Settings** → **Pages** → Source: **Deploy from a branch**.
3. Branch: `main` (veya `master`), folder: **/ (root)** veya **docs**.
4. Bu repoda dosyalar root'ta olduğu için URL’ler örnek olarak:
   - `https://KULLANICI_ADI.github.io/REPO_ADI/gizlilik-politikasi.html`
   - `https://KULLANICI_ADI.github.io/REPO_ADI/kullanim-kosullari.html`
   - `https://KULLANICI_ADI.github.io/REPO_ADI/hesap-silme.html`

(Eğer Pages `docs` klasöründen yayınlanacaksa dosyaları `docs/` altına taşıyıp aynı dosya adlarıyla kullanın.)

### Seçenek 2: Vercel / Netlify

- Projeyi Vercel veya Netlify’a bağlayın.
- Root dizini doğrudan bu repo olacak şekilde yayınlayın.
- Dağıtımdan sonra örnek URL’ler:
  - `https://your-site.vercel.app/gizlilik-politikasi.html`
  - `https://your-site.vercel.app/kullanim-kosullari.html`
  - `https://your-site.vercel.app/hesap-silme.html`

### Seçenek 3: Kendi sunucunuz / alan adınız

- `gizlilik-politikasi.html` ve `kullanim-kosullari.html` dosyalarını sunucuya yükleyin.
- Örnek: `https://example.com/gizlilik-politikasi.html`

## app.json güncellemesi

Yayınladıktan sonra proje kökündeki `app.json` içinde `extra` bölümünde:

- `privacyPolicyUrl` → Gizlilik sayfasının **tam URL’i**
- `termsOfServiceUrl` → Kullanım koşulları sayfasının **tam URL’i**

değerlerini bu adreslerle değiştirin.

## Hesap silme için backend notu

`hesap-silme.html`, Supabase üzerinde `delete_my_account` RPC fonksiyonunu çağırır.
Bu fonksiyonun Supabase projesinde tanımlı olması gerekir.
