# Galeria de Fotos com jQuery

Este projeto consiste em uma **galeria de fotos interativa**, onde os usuários podem adicionar novas imagens a partir de um URL. O projeto utiliza **HTML, CSS e jQuery** para criar um efeito dinâmico ao exibir novas imagens na galeria.

## 🚀 Funcionalidades

- Exibir imagens pré-carregadas na galeria.
- Inserir novas imagens via URL.
- Animações para exibição e remoção do formulário de inserção.
- Efeito de fade-in para novas imagens adicionadas.

## 📌 Tecnologias Utilizadas

- HTML5
- CSS3
- jQuery

## 🖥️ Como Executar o Projeto

1. **Clone o repositório**
   ```bash
   git clone https://github.com/Jeferson7770/jquery-galeria-fotos.git
   ```
2. **Acesse a pasta do projeto**
   ```bash
   cd jquery-galeria-fotos
   ```
3. **Abra o arquivo `index.html` no navegador**

## 📜 Estrutura do Projeto

```
📂 jquery-galeria-fotos
├── 📄 index.html  (Página principal)
├── 📄 main.css    (Estilos do projeto)
├── 📄 main.js     (Scripts jQuery)
├── 📂 images      (Imagens da galeria)
└── 📄 README.md   (Este arquivo)
```

## 📷 Demonstração

<img src="./images/demo.gif" alt="Demonstração da galeria" width="600px">

## 🔧 Explicação do Código jQuery

```javascript
$(document).ready(function(){
    $('header button').click(function(){
        $('form').slideDown(); // Exibe o formulário
    })
    
    $('#botao-cancelar').click(function(){
        $('form').slideUp(); // Esconde o formulário
    })

    $('form').on('submit', function(e){
        e.preventDefault();
        const enderecoDaNovaImagem = $('#endereco-imagem-nova').val();
        const novoItem = $('<li style="display: none"></li>');
        $(`<img src="${enderecoDaNovaImagem}"/>`).appendTo(novoItem);
        $(
            `
                <div class="overlay-imagem-link">
                <a href="${enderecoDaNovaImagem}" target="_blank" title="Ver imagem em tamanho real">
                    Ver imagem em tamanho real
                </a>
                </div>
            `).appendTo(novoItem);
        $(novoItem).appendTo('ul');
        $(novoItem).fadeIn(1000);
        $('#endereco-imagem-nova').val('');
    })
})
```

## 👨‍💻 Desenvolvedor

Projeto desenvolvido por Jeferson Moreira. Obrigado por conferir este projeto! Se gostou, não esqueça de dar uma ⭐️ no repositório. Vamos nos conectar no [LinkedIn](https://www.linkedin.com/in/jefersonmoreiradev/)! 
