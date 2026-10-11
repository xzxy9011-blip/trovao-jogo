# Operação Trovão — gerar o APK

## Opção A: sem instalar nada (GitHub faz o APK pra você)
1. Crie uma conta grátis em github.com e um repositório novo (ex.: operacao-trovao).
2. Envie TODOS os arquivos desta pasta, incluindo a pasta oculta .github (pelo computador: arraste a pasta para a página do repositório).
3. Abra a aba Actions > "Build APK" > Run workflow (ou ele roda sozinho ao enviar).
4. Em ~5 minutos, abra a execução concluída e baixe "operacao-trovao-apk" (um .zip com o app-debug.apk).
5. Passe o APK para o celular, abra e permita "instalar apps desconhecidos".

## Opção B: no seu computador (precisa de Node 18+, Java 17 e Android Studio)
npm install
npx cap add android
npx @capacitor/assets generate --android
npx cap sync android
# adicione android:screenOrientation="sensorLandscape" na <activity> do AndroidManifest.xml
npx cap open android   # Build > Build APK(s)
