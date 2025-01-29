# ControleRemoto
```markdown
# Controle Remoto em Java

Este projeto implementa um controle remoto simples em Java, permitindo que o usuário controle um dispositivo (como uma TV) com funcionalidades básicas, como ligar/desligar, ajustar o volume e reproduzir/pausar.

## Estrutura do Projeto

O projeto é composto pelas seguintes classes:

- `Controlador`: Interface que define as operações que um controle remoto deve implementar.
- `ControleRemoto`: Classe que implementa a interface `Controlador` e fornece a lógica para controlar o volume e o estado do dispositivo.
- `Main`: Classe principal que executa o programa.

## Interface Controlador

A interface `Controlador` define os seguintes métodos:

```java
public interface Controlador {
    void ligar();
    void desligar();
    void abrirMenu();
    void fecharMenu();
    void maisVolume();
    void menosVolume();
    void ligarMudo();
    void desligarMudo();
    void play();
    void pause();
}
```

### Métodos da Interface

- `ligar()`: Liga o dispositivo.
- `desligar()`: Desliga o dispositivo.
- `abrirMenu()`: Exibe o menu de controle.
- `fecharMenu()`: Fecha o menu de controle.
- `maisVolume()`: Aumenta o volume do dispositivo.
- `menosVolume()`: Diminui o volume do dispositivo.
- `ligarMudo()`: Ativa o modo mudo (volume 0).
- `desligarMudo()`: Desativa o modo mudo e define o volume para 5.
- `play()`: Inicia a reprodução de mídia.
- `pause()`: Pausa a reprodução de mídia.

## Classe ControleRemoto

A classe `ControleRemoto` implementa a interface `Controlador` e contém os seguintes atributos:

- `volume`: Um inteiro que representa o volume atual do dispositivo.
- `ligado`: Um booleano que indica se o dispositivo está ligado.
- `tocando`: Um booleano que indica se o dispositivo está reproduzindo mídia.

### Atributos

```java
private int volume;
private boolean ligado;
private boolean tocando;
```

### Construtor

```java
public ControleRemoto() {
    this.volume = 50; // Volume inicial
    this.ligado = false;
    this.tocando = false;
}
```

### Métodos

A classe `ControleRemoto` implementa todos os métodos definidos na interface `Controlador`, com a lógica necessária para controlar o dispositivo.

## Classe Main

A classe `Main` contém o método `main`, que é o ponto de entrada do programa. Um exemplo de uso do controle remoto é mostrado abaixo:

```java
public class Main {
    public static void main(String[] args) {
        ControleRemoto remoteControl = new ControleRemoto();
        remoteControl.ligar();
        remoteControl.abrirMenu();
        remoteControl.maisVolume();
        remoteControl.play();
        remoteControl.abrirMenu();
    }
}
```
