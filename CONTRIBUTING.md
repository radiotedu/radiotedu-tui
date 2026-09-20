# RadioTEDU — Katkı Rehberi

Türkçe + English summary. PR'lar için teşekkürler!

## Hızlı Başlangıç

```bash
git clone https://github.com/radiotedu/radiotedu-tui.git
cd radiotedu-tui
node --version  # >=18
npm test
npm run check
node src/index.js
```

## Kurallar

- Sıfır runtime bağımlılık: yeni npm dependency eklemeyin.
- Mevcut stili koruyun: CommonJS, 2-space, ASCII + seçici emoji.
- `src/tui.js` görsel mimaridir; `src/layout.js` + `src/listening.js` legacy 1.3.11 arama/favori/uyku motorudur. İkisini de bozmayın.
- Test eklemeden davranış değiştirmeyin: `npm test` 29 pass / 1 skip çizgisini koruyun.
- Güvenlik: token, parola, Gold üretimi client'ta yapmayın. PKCE + nonce/heartbeat sunucudadır.

## Testler

```bash
npm test        # node --test
npm run check   # tüm modüller için node --check
```

- `test/layout.test.js`: terminal ölçüleri, mouse hit-targets, ANSI sanitizasyon.
- `test/listening.test.js`: arama, uyku zamanlayıcı, favoriler (TUI entegrasyonu v1.4.4'te skip).
- `test/core.test.js`, `api.test.js`, `pkce.test.js`: istasyon sözleşmesi, player argümanları, RFC 7636.

## Commit / PR

- Küçük, tek amaçlı commit'ler.
- Mesaj formatı: `feat:`, `fix:`, `docs:`, `test:`, `chore:`.
- PR'da: ne değişti, nasıl test edildi (`npm test` çıktısı), ekran görüntüsü (TUI değişikliyse).

## Güvenlik

`SECURITY.md` dosyasına bakın. Zafiyetleri public issue açmadan `security@radiotedu.com` adresine bildirin.
