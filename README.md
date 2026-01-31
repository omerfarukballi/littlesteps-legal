# Gizlilik ve Kullanım Koşulları Sayfaları

Bu klasördeki HTML dosyalarını **bir yerde yayınlayıp** uygulama ve mağaza başvurularında kullanacağınız URL’leri almanız gerekir.

## Dosyalar

- `gizlilik-politikasi.html` → Gizlilik Politikası
- `kullanim-kosullari.html` → Kullanım Koşulları

## Nasıl yayınlanır?

### Seçenek 1: GitHub Pages

1. Bu projeyi GitHub’a push edin.
2. Repo → **Settings** → **Pages** → Source: **Deploy from a branch**.
3. Branch: `main` (veya `master`), folder: **/ (root)** veya **docs**.
4. `public` klasörünü repo kökünde tutun. URL’ler örnek olarak:
   - `https://KULLANICI_ADI.github.io/LittleSteps/public/gizlilik-politikasi.html`
   - `https://KULLANICI_ADI.github.io/LittleSteps/public/kullanim-kosullari.html`

(GitHub Pages bazen sadece `docs` klasöründen yayın yapar; o zaman `public` içeriğini `docs` altına kopyalayıp `docs/gizlilik-politikasi.html` gibi kullanabilirsiniz.)

### Seçenek 2: Vercel / Netlify

- Projeyi Vercel veya Netlify’a bağlayın.
- Root veya “Public directory” olarak `public` seçin (veya `public` içeriğini site köküne koyun).
- Dağıtımdan sonra örnek URL’ler:
  - `https://your-site.vercel.app/gizlilik-politikasi.html`
  - `https://your-site.vercel.app/kullanim-kosullari.html`

### Seçenek 3: Kendi sunucunuz / alan adınız

- `gizlilik-politikasi.html` ve `kullanim-kosullari.html` dosyalarını sunucuya yükleyin.
- Örnek: `https://example.com/gizlilik-politikasi.html`

## app.json güncellemesi

Yayınladıktan sonra proje kökündeki `app.json` içinde `extra` bölümünde:

- `privacyPolicyUrl` → Gizlilik sayfasının **tam URL’i**
- `termsOfServiceUrl` → Kullanım koşulları sayfasının **tam URL’i**

değerlerini bu adreslerle değiştirin.
