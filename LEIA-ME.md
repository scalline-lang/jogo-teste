# Duelo de Bolso para Android

Projeto Android do jogo Duelo de Bolso. O jogo inteiro fica dentro do app (pasta `app/src/main/assets`) e funciona sem internet. O álbum e o progresso ficam salvos no próprio celular.

Requer Android 8.0 ou mais novo.

## Jeito 1: o GitHub gera o APK para você (não precisa instalar nada)

1. Crie uma conta grátis em github.com, se ainda não tiver.
2. Clique em **New repository**, dê um nome (por exemplo `duelo-de-bolso`) e crie.
3. Na página do repositório, clique em **uploading an existing file** e arraste **todo o conteúdo desta pasta** (incluindo a pasta `.github`). Clique em **Commit changes**.
   - Se a pasta `.github` não subir pelo navegador (alguns sistemas escondem pastas que começam com ponto), crie o arquivo pelo site: **Add file > Create new file**, digite o nome `.github/workflows/gerar-apk.yml` e cole o conteúdo do arquivo de mesmo nome.
4. Vá na aba **Actions**. A tarefa **Gerar APK** começa sozinha e leva uns 3 a 5 minutos.
5. Quando ficar verde, clique nela e, em **Artifacts**, baixe **DueloDeBolso-apk**. Vem um .zip com o `app-debug.apk` dentro.
6. Passe o APK para o celular, abra e permita **instalar apps de fontes desconhecidas** quando o Android pedir.

## Jeito 2: Android Studio

1. Instale o Android Studio.
2. **File > Open** e escolha esta pasta.
3. Espere o Gradle sincronizar e clique em **Run** com o celular conectado, ou use **Build > Build APK(s)**.

## Atualizar o jogo

Quando o jogo mudar, troque o arquivo `app/src/main/assets/index.html` pela versão nova e aumente o `versionCode` em `app/build.gradle` (1, 2, 3...). Depois gere o APK de novo.

## Observações

- O APK gerado é de teste (debug). Serve para instalar no seu celular e passar para amigos. Para publicar na Play Store, é preciso gerar uma versão assinada (release).
- As fontes do título usam internet quando disponível. Sem internet, o jogo usa as fontes do próprio celular e funciona normalmente.
