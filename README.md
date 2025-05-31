# 🔢🅰️ Gerador de Números e Letras
<!--
![App Preview](https://github.com/souzaseven/horatrabalhada/blob/Desafios/Hora%20trabalhada/horatrabalhada.png?raw=true)
-->
Uma ferramenta web para criar imagens personalizadas com números e letras em formatos circulares ou quadrados, com opções de download em PNG e ICO.

## ✨ Funcionalidades

- **Geração Instantânea**
  - Atualização em tempo real conforme digitação
  - Suporte para números, letras ou combinações
  - Ajuste automático de tamanho de fonte

- **Personalização Avançada**
  - Escolha entre formato circular ou quadrado
  - Seletor de cores para fundo e texto
  - Visualização imediata das alterações

- **Exportação Flexível**
  - Download em formato PNG (imagem)
  - Download em formato ICO (ícone)
  - Botão para limpar todos os campos

## 🎨 Design e Interface

```css
.container {
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.btn {
    padding: 10px 15px;
    color: #fff;
    border-radius: 5px;
}
```
⚙️ Funcionamento Técnico
Lógica de Renderização
```Javascript
function generateImage() {
    let displayText = combined || (number + letter);
    
    if (shape === 'circle') {
        ctx.arc(canvas.width / 2, canvas.height / 2, 120, 0, Math.PI * 2);
    } else {
        ctx.fillRect((canvas.width / 2) - 120, (canvas.height / 2) - 120, 240, 240);
    }
    
    // Ajuste automático de tamanho de fonte
    do {
        ctx.font = `bold ${fontSize}px Arial`;
        fontSize -= 10;
    } while (textWidth > 240 && fontSize > 20);
}
```
Event Listeners
```Javascript
document.getElementById('numberInput').addEventListener('input', generateImage);
document.getElementById('clearButton').addEventListener('click', clearFields);

```
📂 Estrutura do Projeto
gerador-numeros-letras/
├── index.html          # Estrutura principal <br>
├── style.css           # Estilos responsivos  <br>
└── script.js           # Lógica de renderização  <br>

🚀 Como Usar
Insira seu conteúdo:
Número no campo "Número"
Letra no campo "Letra"
Ou combinação no campo "Número e Letra"

Personalize:
Selecione o formato (círculo ou quadrado)
Escolha as cores de fundo e texto

Exporte:
Clique em "Baixar Imagem" para PNG
Clique em "Baixar Ícone" para ICO
Use "Limpar Conteúdo" para recomeçar

🛠️ Tecnologias Utilizadas
Frontend
HTML5 Canvas para renderização
CSS Flexbox para layout
JavaScript ES6 para lógica

Bibliotecas
Bootstrap para componentes básicos
Font Awesome para ícones

📜 Licença
MIT License - Livre para uso e modificação
