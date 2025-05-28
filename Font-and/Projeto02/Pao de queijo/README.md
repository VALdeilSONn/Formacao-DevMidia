# 🧀 Receita de Pão de Queijo | Meu Primeiro Projeto Web 🍞

Seja bem-vindo ao meu primeiro projeto de **HTML e CSS**! 🙌  
Este repositório marca um momento especial da minha jornada como desenvolvedor, onde finalmente consegui transformar conhecimento em prática e construir uma **página web** do zero.

## 📌 Sobre o Projeto

Este projeto apresenta uma deliciosa **receita de pão de queijo**, uma das iguarias mais apreciadas no Brasil. O objetivo foi criar uma página simples, mas bem estruturada, utilizando os princípios fundamentais do **HTML5** e **CSS3**.

## 🚀 Tecnologias Utilizadas

- **HTML5** → Estruturando o conteúdo com boas práticas semânticas.
- **CSS3** → Aplicando estilos para uma experiência visual agradável.
- **Responsividade** → Adaptando a página para diferentes tamanhos de tela.

## 🍽️ Receita de Pão de Queijo

A página contém os seguintes elementos:
✔️ Título chamativo 🏆  
✔️ Imagem ilustrativa 📷  
✔️ Lista de ingredientes 📜  
✔️ Passo a passo detalhado 🛠️  
✔️ Link para uma fonte de referência 📌  

## 🔗 Código Fonte

A estrutura do código segue esta organização:

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/style.css">
    <title>Receitas do Val</title>
</head>
<body>
    <div> <!--INÍCIO DA DIV PRINCIPAL-->
        <h1>Receita de Pão de Queijo</h1>
        <h2>Que tal aprender uma receita fácil de pão de queijo?</h2>

        <img src="Capa-PdQ.jpg" alt="Pão de queijo" title="Pão de Queijo">

        <div> <!--DIV INGREDIENTES-->
            <h3>Ingredientes:</h3>
            <ul>
                <li>2 xícaras de goma de tapioca</li>
                <li>200g de requeijão cremoso (ou cream cheese)</li>
                <li>150g de queijo parmesão fresco ralado</li>
                <li>Sal a gosto</li>
            </ul>
        </div>

        <div> <!--DIV MODO DE PREPARO-->
            <h3>Modo de Preparo:</h3>
            <ol>
                <li>Peneire a goma de tapioca.</li>
                <li>Adicione o requeijão cremoso e misture bem.</li>
                <li>Acrescente o queijo parmesão e misture até formar uma massa homogênea.</li>
                <li>Leve à geladeira por 20 minutos.</li>
                <li>Modele bolinhas e asse a 200°C por 35 minutos.</li>
            </ol>
        </div>

        <p>Para mais receitas como esta, visite <a href="https://receitatodahora.com.br/pao-de-queijo-com-goma-de-tapioca-perfeito-e-so-misturar-os-ingredientes-e-assar/">Receita Toda Hora</a>.</p>
    </div>
</body>
</html>
