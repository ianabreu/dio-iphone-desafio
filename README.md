## Desafio - Programação Orientada a Objetos

Este repositório representa um desafio de modelagem e diagramação UML do componente iPhone, abrangendo suas funcionalidades como Reprodutor Musical, Aparelho Telefônico e Navegador na Internet. Este projeto faz parte do Bootcamp Santander 2024 - Backend com Java.

## Modelo do Diagrama

```mermaid
classDiagram
    class ReprodutorMusical {
        <<interface>>
        + tocar(musica : string) : void
        + pausar() void
        + selecionarMusica(musica : string) : void
        + girarTela() : void
    }

    class AparelhoTelefonico {
        <<interface>>
        + ligar(numero : string) : void
        + atender() : void
        + iniciarCorreioVoz() : void
        - verificarRede() : Boolean
    }

    class NavegadorInternet {
        <<interface>>
        + exibirPagina(url : string) : void
        + adicionarNovaAba() : void
        + atualizarPagina() : void
        - validarConectadoInternet() : void
        - salvarHistorico() : void
    }

    class iPhone {
        + desbloquearTela(): void
        + aumentarVolume(): void
        + diminuirVolume(): void

+ voltarAoInicio(): void

+ deslizarTela(direcao: string): void
    }

    iPhone --> ReprodutorMusical
    iPhone --> AparelhoTelefonico
    iPhone --> NavegadorInternet

```
