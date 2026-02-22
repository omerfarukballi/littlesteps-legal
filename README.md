# LittleSteps Legal Pages

Bu repo, LittleSteps için TR ve EN yasal sayfaları içerir.

## Dosyalar

- `index.html` → Otomatik dil algılama (`tr`/`en`) + manuel dil seçimi (TR/EN)
- `gizlilik-politikasi.html` → Gizlilik Politikası (TR)
- `kullanim-kosullari.html` → Kullanım Koşulları (TR)
- `hesap-silme.html` → Hesap silme sayfası (TR)
- `privacy-policy.html` → Privacy Policy (EN)
- `terms-of-service.html` → Terms of Service (EN)
- `account-deletion.html` → Account deletion page (EN)

## Nasıl yayınlanır?

### Seçenek 1: GitHub Pages

1. Bu projeyi GitHub’a push edin.
2. Repo → **Settings** → **Pages** → Source: **Deploy from a branch**.
3. Branch: `main` (veya `master`), folder: **/ (root)** veya **docs**.
4. Bu repoda dosyalar root'ta olduğu için URL’ler örnek olarak:
   - `https://KULLANICI_ADI.github.io/REPO_ADI/` (index - otomatik dil)
   - `https://KULLANICI_ADI.github.io/REPO_ADI/gizlilik-politikasi.html`
   - `https://KULLANICI_ADI.github.io/REPO_ADI/kullanim-kosullari.html`
   - `https://KULLANICI_ADI.github.io/REPO_ADI/hesap-silme.html`
   - `https://KULLANICI_ADI.github.io/REPO_ADI/privacy-policy.html`
   - `https://KULLANICI_ADI.github.io/REPO_ADI/terms-of-service.html`
   - `https://KULLANICI_ADI.github.io/REPO_ADI/account-deletion.html`

(Eğer Pages `docs` klasöründen yayınlanacaksa dosyaları `docs/` altına taşıyıp aynı dosya adlarıyla kullanın.)

### Seçenek 2: Vercel / Netlify

- Projeyi Vercel veya Netlify’a bağlayın.
- Root dizini doğrudan bu repo olacak şekilde yayınlayın.
- Dağıtımdan sonra örnek URL’ler:
  - `https://your-site.vercel.app/`
  - `https://your-site.vercel.app/gizlilik-politikasi.html`
  - `https://your-site.vercel.app/kullanim-kosullari.html`
  - `https://your-site.vercel.app/hesap-silme.html`
  - `https://your-site.vercel.app/privacy-policy.html`
  - `https://your-site.vercel.app/terms-of-service.html`
  - `https://your-site.vercel.app/account-deletion.html`

### Seçenek 3: Kendi sunucunuz / alan adınız

- `gizlilik-politikasi.html` ve `kullanim-kosullari.html` dosyalarını sunucuya yükleyin.
- Örnek: `https://example.com/gizlilik-politikasi.html`

## app.json güncellemesi (mobil uygulama)

Yayınladıktan sonra proje kökündeki `app.json` içinde `extra` bölümünde:

- `privacyPolicyUrl` → Gizlilik sayfasının (TR veya EN) **tam URL’i**
- `termsOfServiceUrl` → Kullanım koşulları sayfasının (TR veya EN) **tam URL’i**

değerlerini bu adreslerle değiştirin.

## Hesap silme için backend notu

`hesap-silme.html`, Supabase üzerinde `delete_my_account` RPC fonksiyonunu çağırır.
Bu fonksiyonun Supabase projesinde tanımlı olması gerekir.
