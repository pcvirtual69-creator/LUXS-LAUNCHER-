# Como gerar o APK (sem Android Studio)

### Opção A — GitHub Actions (recomendado)
1. Crie um repositório no GitHub e faça upload de todos os arquivos deste projeto.
2. Vá em **Actions** → o fluxo *Build Android APK (Debug)* já aparecerá. Clique **Run workflow**.
3. Ao terminar, baixe o artefato **SAMP-Launcher-APK** (contém `app-debug.apk`).

> O APK gerado é **debug** (instalável). Para *release*, adicione uma keystore e configure signing no `build.gradle.kts`.

### Opção B — Linha de comando
1. Instale **Java 17**, **Android SDK** (platform 34 e build-tools 34.0.0) e **Gradle 8.5**.
2. No diretório do projeto, rode:
   ```bash
   cd app
   gradle assembleDebug
   ```
3. O APK estará em: `app/build/outputs/apk/debug/app-debug.apk`.

### Dica
Se quiser que eu já configure assinatura *release* e nome do app/ícone, me diga o **nome do app**, **pacote** e envie um **ícone PNG 512x512**.