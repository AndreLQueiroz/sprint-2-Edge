# sprint-2-Edge



## Índice :page_with_curl:

  * [Descrição do Projeto](#descrição-do-projeto-memo)
     * [Introdução](#introdução-left_speech_bubble)
     * [Umidade](#umidade-droplet)
  * [Acesso ao projeto](#acesso-ao-projeto-file_folder)
  * [Ferramenta utilizada](#ferramenta-utilizada-hammer_and_wrench)
  * [Componentes necessários](#componentes-necessários-toolbox)
  * [Montagem](#montagem-wrench)
     * [Cuidados durante a montagem](#cuidados-durante-a-montagem-warning)
  * [Reprodução](#reprodução-gear)
  * [Pessoas Desenvolvedoras do Projeto](#pessoas-desenvolvedoras-do-projeto-globe_with_meridians)

## Descrição do projeto :memo:

<h3>Introdução :left_speech_bubble:</h3>
<p>
  Nós, NEXT STAGE, gostariamos de mostrar no projeto de arduino que consiste em mostrar a humidade e a temperatura da pista para nao ocorrer nenhum problema durante a corrida, pois alguns dos problemas notados e que as pistas da Formula E nem sempre sao bem revisionadas perante isso gostariamos de mostrar nosso projeto.
<h3>Umidade :droplet:</h3>
<p>
  Diante disso, utilizamos o mesmo sensor, o DHT11, que captura a temperatura da adega, já que ele também captura a umidade do ambiente. Além disso, indicará se a umidade está alta, baixa ou na faixa ideal, entre 50% e 70%. Essas informações também são mostradas no display (LCD). Quando a umidade estiver fora da situação ideal, o LED vermelho será aceso e a buzina (Buzzer) tocará continuamente.
</p>

## Acesso ao projeto :file_folder:

Você pode acessar a [simulação feita no Wooki](https://wokwi.com/projects/409556614371884033)

## Ferramenta utilizada :hammer_and_wrench:

- ``ESP32``
  
## Bibliotecas utilizadas :books:

- ``WiFi.h``
- ``PubSubClient.h``
- ``DHT.h``
  
## Componentes necessários :toolbox:

|   Componente   | Quantidade |
|:--------------:|:----------:|
| ESP32          |      1     |
|      Cabo      |     6      |
|    Cabo USB-C   |      1     |

## Montagem :wrench:

<details>
  <summary>Imagem da Montagem</summary>
  <img src="https://cdn.discordapp.com/attachments/1234868042433822752/1290040192756879390/projetoedge.png?ex=66fb030d&is=66f9b18d&hm=60224bc5677a70afa6d6c54d850dc138d55dd380cff9f2485801986b8cb02fe1&" alt="imagem-montagem">
<sumary>Arquitetura do Projeto</sumary>
<img src="https://cdn.discordapp.com/attachments/1234868042433822752/1290041787175538811/arquitetura.png?ex=66fb0489&is=66f9b309&hm=80b416c9056a68095f72e6c48ca8797813f5560f8a4e716bd39cab57fccf050d&" alt= "imagem-montagem">

</details>


<h3>Cuidados durante a montagem :warning:</h3>

- ``1.`` Conectando o DHT:
  - ``1.1.`` Na simulação e na imagem acima, utilizamos o DHT22, entretanto, no [código do projeto] utilizamos o DHT11;
    - ``1.1.1.`` Esses sensores possuem a diferença de que o DHT22 é mais preciso do que o DHT11, no qual possui uma margem de erro maior;
    - ``1.1.2.`` Se quiser utilizar um DHT22, a única coisa que precisará será trocar ,no código, o tipo do DHT para 22 nessa seguinte parte:
            
      ```cpp
      //Definindo o tipo do DHT  
      #define DHTTYPE DHT11   
      ```
      
  - ``1.2.`` É necessário ter muito cuidado na hora de conectar os cabos, pois se conecta-los errados, o DHT queimará. Segue a Imagem de quais são os terminais do DHT:
      <details>
        <summary>Imagem dos terminais do DHT11</summary>
        <img src="https://github.com/L-A-N-E/CP2_Edge_1SEM/assets/101829188/d26416fb-d639-4760-b590-593932e5a888" alt="Terminais do DHT11">
      </details>
  - ``1.3.`` Conecte o VCC no terminal positivo (5V), GND no terminal negativo (GND), o terminal dos dados no pino 2 e não conecte nada no terminal N.C.;
      <details>
        <summary>Imagem de onde fica o trimpot de ajuste do contraste</summary>
        <img src="https://github.com/L-A-N-E/CP2_Edge_1SEM/assets/101829188/50648d65-2402-4508-a47d-1d38bbf663e5" alt="Terminais do DHT11">
      </details>

## Pessoas Desenvolvedoras do Projeto :globe_with_meridians:
Paulo Poças -Rm556080

Guilherme Gomes - Rm554606

Andre Luiz Fernandes De Queiroz - Rm554503

Israel araujo henriques de Moura - Rm559068
