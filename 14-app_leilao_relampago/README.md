# UFSC-CTC-INE-INE5646 Programação para Web :: App Leilão Relâmpago

Aplicação que permite ao usuário participar de leilões fictícios de produtos. Um usuário anuncia um produto, indicando o nome e o preço mínimo do produto, e os demais disputam a compra do produto fazendo ofertas.

## Objetivo do Exercício

Demonstrar como o **protocolo Websocket** pode ser usado na comunicação entre os participantes do leilão.

## Instruções

Depois de baixar/clonar o respositório, entre no diretório **cliente** e digite

`npm install`

para instalar os pacotes JavaScript utilizados pelo lado cliente da aplicação.

Repita o comando acima dentro do diretório **servidor** para instalar os pacotes JavaScript utilizados pelo lado servidor da aplicação.

No mesmo diretório **servidor**,  crie o arquivo **.env** e adicione o seguinte conteúdo

```bash
PORTA=3000
```

### Durante o desenvolvimento

O desenvolvimento da aplicação envolve duas frentes de trabalho: a programação necessária para o lado cliente e a programação necessária para o lado servidor.

#### Do Lado Cliente

Para iniciar o desenvolvimento do lado cliente entre no diretório **cliente** e digite

`npm start`

Cada vez que um arquivo no lado cliente for alterado o *webpack* será acionado para gerar uma nova versão dos arquivos usados no lado
cliente. Estes arquivos são armazenados no diretório **publico** dentro do diretório **servidor**.

#### Do Lado Servidor

Para iniciar o desenvolvimento do lado servidor entre no diretório **servidor** e digite

`npm start`

A partir de então a aplicação estará disponível na porta 3000 (ou na porta que você definiu no arquivo **.env**). Para acessar, use o navegador e digite o endereço `https://localhost:3000`

Sempre que um arquivo for salvo a aplicação irá reiniciar automaticamente (graças ao pacote **nodemon**).

### Em produção

Depois que o código da aplicação está pronto é preciso gerar as versões otimizadas (em termos de tamanho e velocidade de execução) dos arquivos do lado cliente e do lado servidor.

#### Lado Cliente

Para gerar a versão em produção do lado cliente entre no diretório **cliente** e digite

`npm run build`

Observe que o tamanho dos arquivos JavaScript armazenados no diretório *servidor/publico* diminuiram drasticamente de tamanho.

#### Lado Servidor

Para gerar a versão em produção do lado servidor entre no diretório **servidor** e digite

`npm run build`

## Executando a aplicação em produção

Para executar a aplicação em modo produção entre no diretório **servidor** e digite

`node build/app.js`
