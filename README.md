<p align="center">
  <img src="assets/branding/logo.jpg" alt="Critter Slide Logo" width="380" style="border-radius: 16px; box-shadow: 0 8px 16px rgba(0,0,0,0.3);"/>
</p>

# Critter Slide 🧩✨

[![Java 17](https://img.shields.io/badge/Java-17%2B-orange.svg?style=flat-square)](https://www.oracle.com/java/)
[![libGDX 1.12.1](https://img.shields.io/badge/libGDX-1.12.1-red.svg?style=flat-square)](https://libgdx.com/)
[![Platform](https://img.shields.io/badge/Platform-Desktop-blue.svg?style=flat-square)](https://libgdx.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)

**Critter Slide** é um jogo de quebra-cabeça clássico (*sliding puzzle*) dinâmico e divertido desenvolvido em **Java** com o framework **libGDX**. Deslize criaturas simpáticas geradas em tempo real e ordene o tabuleiro de jogo sob diferentes níveis de dificuldade!

---

## ✨ Características Principais

* **👾 Gráficos Procedurais 3D:** Os sprites das criaturas (critters) são desenhados dinamicamente via código (`Pixmap`), oferecendo um visual cartoon fofo e polido com efeitos de relevo 3D, reflexos de iluminação (*gloss*), bochechas rosadas e sombras projetadas.
* **📱 Tela Responsiva (Perfect Proportions):** Integração com `OrthographicCamera` e `FitViewport`. A proporção clássica de 4:3 é mantida dinamicamente. O jogo redimensiona perfeitamente em telas cheias, janelas menores ou displays de alta densidade de pixels (High-DPI) com letterboxing/pillarboxing limpos.
* **💥 Efeitos Especiais & "Juice":**
  * **Rastro de Poeira (Dust Trails):** Partículas dinâmicas seguem as criaturas enquanto deslizam, combinando com a cor do personagem.
  * **Impacto Dinâmico (Screen Shake & Bursts):** Efeito de colisão da câmera e explosão de faíscas ao encaixar uma criatura no tabuleiro ou ao clicar incorretamente.
  * **Festa de Vitória:** Ao vencer, confetes e estrelas explodem e caem pela tela com uma vibração intensa na câmera.
* **🔊 Sintetizador de Áudio Procedural:** Os efeitos sonoros do jogo são gerados dinamicamente via sintetizador e armazenados em cache local, dispensando pacotes pesados de áudio externos.
* **🎚️ Três Modos de Dificuldade:** Tabuleiros 3x3 (Fácil), 4x4 (Médio) e 5x5 (Difícil), com número de movimentos e recordes calculados na tela.

---

## 🎮 Como Jogar

1. No **Menu Principal**, escolha o tamanho do puzzle:
   * **Fácil:** Grid 3x3
   * **Médio:** Grid 4x4
   * **Difícil:** Grid 5x5
2. **Deslize** clicando em qualquer criatura diretamente adjacente ao espaço vazio para movê-la.
3. Organize as peças sequencialmente (**1, 2, 3...**) da esquerda para a direita, de cima para baixo, deixando o espaço vazio no canto inferior direito.
4. Use o botão **Dica** para espiar a imagem resolvida por 3 segundos sempre que precisar de ajuda.
5. Complete e assista à animação de vitória! Clique para voltar ao menu.
6. Pressione **ESC** a qualquer momento para retornar ao menu anterior ou fechar o jogo.

---

## 🚀 Requisitos e Execução

### Requisitos Mínimos
* **Java Development Kit (JDK) 17 ou superior**
* Acesso à internet na primeira execução (para download das dependências do libGDX via Gradle).

### Instruções

Abra a pasta do projeto no seu terminal e execute:

```bash
# Executar o jogo diretamente
./gradlew run

# Compilar o código do projeto
./gradlew compileJava

# Limpar o diretório de build
./gradlew clean

# Gerar um arquivo executável autônomo (JAR) em build/libs/
./gradlew jar
```

---

## 📁 Estrutura de Diretórios

A arquitetura do projeto é organizada e segue as melhores práticas do ecossistema libGDX e Gradle:

```
critter-slide/
├── assets/                    # Identidade visual e materiais de branding do repositório
├── build.gradle               # Configurações de compilação, plugins e dependências
├── src/main/java/             # Código-fonte Java do jogo
│   └── com/critterslide/
│       ├── DesktopLauncher.java    # Configuração da janela Desktop (LWJGL 3)
│       ├── CritterSlideGame.java   # Inicialização das classes principais do jogo
│       ├── model/
│       │   ├── Board.java          # Estado do tabuleiro, embaralhamento e regras
│       │   └── TileAnimation.java  # Cálculo de interpolação e easing das peças
│       ├── screens/
│       │   ├── MenuScreen.java     # Layout e interações do menu principal
│       │   └── GameScreen.java     # Tela de jogo, HUD, partículas e lógica
│       └── utils/
│           ├── Assets.java         # Gerador procedural de texturas e imagens do jogo
│           ├── Constants.java      # Constantes de tamanhos, velocidades e movimentos
│           ├── ParticleSystem.java # Gerenciador de física e desenho de partículas
│           ├── ScreenShake.java    # Controle de deslocamento da câmera
│           ├── SoundGenerator.java # Sintetizador matemático de ondas sonoras
│           └── SoundManager.java   # Gerenciador de canais e cache de som local
└── src/main/resources/        # Recursos nativos (fontes básicas, ícone e logo)
```

---

## 🛠️ Tecnologias Utilizadas

* **Java 17 (LTS)**
* **libGDX 1.12.1** (Engine de desenvolvimento de jogos 2D/3D multiplataforma)
* **LWJGL 3** (Lightweight Java Game Library - backend para a versão Desktop)
* **Gradle** (Automação de compilação e gerenciador de dependências)

---

## ⚖️ Licença

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para obter mais informações.
