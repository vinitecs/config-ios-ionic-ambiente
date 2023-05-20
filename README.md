# Configuração ambiente mac IOS

### Processo de instalação do e configuração no MAC

        npm install -g @angular/cli
        npm install -g @ionic/cli

### Instalação do capacitor 

       npm install @capacitor/core
       npm install -D @capacitor/cli
       
       npm install @capacitor/android 
       npm install @capacitor/ios

### Configuração do projeto

Após instalação do projeto realize essas configurações

       npx cap add android
       npx cap add ios


### Configuração IOS:
Para configurações do Xcode pra abrir projeto IONIC no XCODE via CLI execute seguintes codigos:

É necessario instalar o gerenciador de pacotes Homebrew

### ATENÇAO ! não habilite root pra esse comando:

       /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

### No final da instalação link acima  a ferramenta ira disponibilizar o comando baseado no diretorio da sua maquina para executar copie e cole no CMD comando semelhante a esse abaixo:

### ATENÇÃO  não COPIE esse comando do TUTORIAL !!!

EXEMPLO 1:

     echo 'eval $(/opt/homebrew/bin/brew shellenv)' >> /Users/$USER/.zprofile
        
EXEMPLO 2: 

      eval $(/opt/homebrew/bin/brew shellenv)

### Após instalação e configuração do item acima

execute  comando abaixo: 

    sudo brew install ruby
    
    sudo brew install cocoapods 
    
 ou
 
    sudo gem install cocoapods 

### Após instalação do  cocoapods execute seguinte comando;

      pod setup

### Após alterações no codigo do projeto execute seguintes comandos:

      ionic build 
      ionic cap sync 

# OBSERVAÇÃO caso o comando ionic cap sync ou npx cap sync dê erro relacionado a COCOAPODS siga seguintes  Passos :

Acesse diretorio da raiz do projeto: 
     
     ./ios/app
     
Dê o comando:
 
      pod install

Execute: 

     ionic cap sync  ou npx cap sync

Após o comando acima caso queira fazer debug:

     ionic cap run ios

para abrir xcode 

    ionc cap open ios
