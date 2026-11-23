# App da Mídia FM (Android)

App nativo da rádio: toca o stream ao vivo, continua tocando com a tela desligada, mostra controles na notificação e na tela de bloqueio, e tem atalhos para WhatsApp, Instagram, Facebook e site.

## Como gerar o APK

### Opção 1: pelo GitHub (sem instalar nada)

1. Crie uma conta em github.com e um repositório novo (pode ser privado).
2. Envie todo o conteúdo desta pasta para o repositório (botão *Add file > Upload files*).
3. Abra a aba **Actions**, escolha **Gerar APK** e clique em **Run workflow**.
4. Quando terminar (uns 4 a 6 minutos), abra a execução e baixe o arquivo **midia-fm-apk** na seção *Artifacts*. Dentro do zip está o `app-debug.apk`.

### Opção 2: pelo Android Studio

1. Instale o Android Studio (developer.android.com/studio).
2. Abra esta pasta com *File > Open* e espere o Gradle sincronizar.
3. Vá em *Build > Build Bundle(s) / APK(s) > Build APK(s)*.
4. O arquivo fica em `app/build/outputs/apk/debug/app-debug.apk`.

## Como instalar no celular

Envie o APK para o celular (WhatsApp, e-mail, cabo), abra o arquivo e permita a instalação de fontes desconhecidas quando o Android pedir.

## O que alterar depois

Tudo da rádio fica em `app/src/main/java/br/com/radiomidiafm/app/RadioConfig.kt`: link do stream, número do WhatsApp, mensagem pronta e links das redes. O logo da tela principal está em `app/src/main/res/drawable-nodpi/logo_midiafm.jpg`.

## Publicar na Google Play

O APK gerado é de teste (assinado com chave de depuração), bom para instalar direto nos celulares. Para a Play Store é preciso gerar um pacote `.aab` assinado com uma chave sua e criar uma conta de desenvolvedor Google. Dá para configurar isso neste mesmo projeto.
