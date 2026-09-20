# Security Policy

## Supported Versions

| Version | Supported |
| ------- | --------- |
| 1.4.x   | ✅ |
| 1.3.x   | ⚠️ sadece kritik düzeltmeler |
| < 1.3   | ❌ |

## Reporting a Vulnerability

- Lütfen public issue açmayın.
- E-posta: `security@radiotedu.com`
- İçerik: etkilenen sürüm, yeniden üretim adımları, log (token/parola koymayın), etki tahmini.
- 72 saat içinde ilk yanıt, 14 gün içinde durum güncellemesi hedeflenir.

## Güvenlik Mimarisi

- RFC 7636 PKCE S256 ile ERP/device eşleştirme.
- Token'lar `0600` dosya maskesiyle yerel profilde saklanır.
- Gold/Study ödülleri sunucu nonce + heartbeat ile doğrulanır; client-side mint yoktur.
- Terminal çıktısı ANSI enjeksiyonuna karşı sanitize edilir (`src/layout.js: clean()`).
