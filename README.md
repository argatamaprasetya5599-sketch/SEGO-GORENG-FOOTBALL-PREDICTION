# KARYA SEGOGORENG — Football Intelligence V3

Versi production-oriented untuk GitHub Pages, local-first, tanpa API key.

## Fitur
- Premium dark dashboard
- Team mode + manual odds mode
- Home/Away team searchable
- Competition filter
- Market pack: Full, 1X2, HDP, O/U, BTTS
- Manual odds 1X2, Asian Handicap, Over/Under, BTTS
- Minimum sample
- Similarity tolerance
- Top historical matches
- Probability + historical hit rate
- Expected ROI
- BEST VALUE ranking (historical probability minus implied probability)
- Data quality meter
- H2H across competitions
- Historical evidence table
- Quarter-line HDP/O-U architecture
- Local CSV/JSON import
- No API key required

## Deployment
Upload the files to a GitHub repository and enable GitHub Pages from the `main` branch, root folder.

## Production database
Untuk performa terbaik, simpan database sebagai CSV/JSON yang sudah dipreprocess. Dataset besar sebaiknya dipecah/diindeks per competition dan team bila diperlukan.

## Catatan settlement
V3 memakai settlement berbasis line untuk HDP, tetapi modul produksi berikutnya sebaiknya menerapkan settlement quarter-line secara eksplisit (split stake 50/50) dan O/U quarter-line secara eksplisit. Jangan gunakan ROI sebagai jaminan keuntungan.

## No API key
Semua historical analysis berjalan dari dataset lokal. API hanya dibutuhkan jika nanti ingin data fixture/odds live dari provider eksternal.
