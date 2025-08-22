# Migrare pentru Codemagic / Gradle suportat

- Am păstrat TOATE fișierele originale.
- Folderele platformă originale au fost mutate pentru referință:
  - `android_legacy/`, `ios_legacy/`, `macos_legacy/`, `linux_legacy/`, `windows_legacy/`
- Pe CI, workflow-ul din `codemagic.yaml` regenerează folderele corecte cu `flutter create .`
  pentru a evita eroarea: "Your app is using an unsupported Gradle project".
- Poți șterge folderele `*_legacy` după ce confirmi că build-ul funcționează.

## Pași local (opțional)
1. Șterge folderele platformă curente dacă există (`android/`, `ios/`, etc.).
2. Rulează `flutter create .` în rădăcina proiectului.
3. `flutter pub get`
4. `flutter build apk`
