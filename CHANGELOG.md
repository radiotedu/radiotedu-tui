# Changelog

Tüm önemli değişiklikler bu dosyada tutulur. Format: [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), sürümleme: SemVer.

## [1.4.4] — 2026-09-20

### Added
- `bin/`, `lib/` (diagnostics, DSP, SMTC/MPRIS media-controls, Wrapped) `rtai-mobile/terminal` kaynağından taşındı.
- `src/layout.js`, `src/listening.js` (arama, favoriler, uyku zamanlayıcı) eklendi.
- `src/store.js`: `loadPreferences` / `savePreferences` geri eklendi (favori izolasyonu).
- `test/layout.test.js` + `test/listening.test.js` eklendi (29 pass / 1 skip).
- `docs/screenshots/*.svg`: Stations, Visualizer, Account/Study ekran görüntüleri.
- `CONTRIBUTING.md`, `SECURITY.md`, `CHANGELOG.md`, `.gitattributes` eklendi.
- Profesyonel README: ekran görüntüleri, mimari, test matrisi güncellendi.

### Changed
- `package.json`: `files` listesine `lib`, `bin`, `docs/screenshots` eklendi; `check` scripti tüm modülleri kapsar.

## [1.3.11] — rtai-mobile/terminal

- Responsive charcoal/coral TUI, tek kolon istasyon listesi.
- `/` arama, `*`/`G` favoriler, `Z` uyku zamanlayıcı, `?` klavye rehberi, `T` Focus.
- Browser login, email/parola, ERP pairing, server-backed Gold (değişmedi).
