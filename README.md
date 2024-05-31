# Projeto iPhone

Este projeto é uma simulação das funcionalidades básicas do iPhone, conforme apresentado no lançamento do iPhone em 2007. O objetivo é modelar e diagramar as funcionalidades de um Reprodutor Musical, Aparelho Telefônico e Navegador na Internet utilizando UML e implementá-las em Java.

## Funcionalidades Modeladas

### Reprodutor Musical
- `tocar()`: Reproduz a música atual.
- `pausar()`: Pausa a música atual.
- `selecionarMusica(String musica)`: Seleciona uma música para tocar.

### Aparelho Telefônico
- `ligar(String numero)`: Faz uma ligação para o número especificado.
- `atender()`: Atende uma chamada.
- `iniciarCorreioVoz()`: Inicia o correio de voz.

### Navegador na Internet
- `exibirPagina(String url)`: Exibe a página da web especificada pelo URL.
- `adicionarNovaAba()`: Adiciona uma nova aba no navegador.
- `atualizarPagina()`: Atualiza a página atual.
  
## Clone o repositório
git clone https://github.com/hyppoliteaurelus/IPHONE-DESAFIO-DIO.git

## Diagrama UML

```plantuml
@startuml

interface ReprodutorMusical {
    + tocar(): void
    + pausar(): void
    + selecionarMusica(String musica): void
}

interface AparelhoTelefonico {
    + ligar(numero: String): void
    + atender(): void
    + iniciarCorreioVoz(): void
}

interface NavegadorInternet {
    + exibirPagina(String url): void
    + adicionarNovaAba(): void
    + atualizarPagina(): void
}

class iPhone implements ReprodutorMusical, AparelhoTelefonico, NavegadorInternet {
    + tocar(): void
    + pausar(): void
    + selecionarMusica(musica: String): void
    + ligar(numero: String): void
    + atender(): void
    + iniciarCorreioVoz(): void
    + exibirPagina(url: String): void
    + adicionarNovaAba(): void
    + atualizarPagina(): void
}

@enduml


