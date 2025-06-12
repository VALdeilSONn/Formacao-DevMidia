Manhattan - Coffee House: Meu Projeto Web
Olá! Seja bem-vindo(a) ao repositório do meu projeto web para a cafeteria "Manhattan - Coffee House". Este README foi criado para detalhar cada etapa do processo de desenvolvimento, explicando minhas escolhas, a necessidade de cada tag HTML e cada linha de código CSS para que o resultado final se assemelhasse o máximo possível à imagem de referência que recebi.

O Desafio: Replicar um Layout de Cafeteria
Meu objetivo principal era transformar uma imagem estática de um layout de website em um site HTML e CSS funcional e responsivo. A imagem mostrava uma página elegante e rústica, com um cabeçalho fixo, uma grande imagem de capa com texto sobreposto, seções de informações com efeito de paralaxe, uma área de contatos com mapa e um bloco de horários de funcionamento, finalizando com um rodapé.

Desde o início, soube que a chave seria a semântica do HTML e o controle preciso do CSS, especialmente para os efeitos visuais como o paralaxe e as sobreposições.

1. Estrutura Base do HTML: O Esqueleto do Projeto
Comecei criando o arquivo index.html. A primeira coisa que fiz foi configurar o esqueleto básico de qualquer página web:

<!DOCTYPE html>
<html lang="pt-br">

<head>
    <meta charset="UTF-8">
    <title>Manhattan - Coffee House</title>
    <link rel="stylesheet" href="layout-das-telas/style.css">
</head>

<body>
    </body>

</html>

<!DOCTYPE html>: Declara o tipo de documento, informando ao navegador que é um HTML5. É crucial para que o navegador renderize a página no modo padrão, evitando comportamentos estranhos.
<html lang="pt-br">: A tag <html> é o elemento raiz de toda a página. O atributo lang="pt-br" é importante para indicar o idioma do conteúdo. Isso ajuda leitores de tela para pessoas com deficiência visual e mecanismos de busca a entenderem o contexto da página.
<head>: Esta seção não é visível no conteúdo da página, mas contém metadados importantes.
<meta charset="UTF-8">: Essencial para garantir que caracteres especiais (como acentos e "ç") sejam exibidos corretamente, evitando problemas de codificação.
<title>Manhattan - Coffee House</title>: Define o título que aparece na aba do navegador. É importante para a identificação da página pelo usuário e para SEO.
<link rel="stylesheet" href="layout-das-telas/style.css">: Linka meu arquivo CSS (style.css) à página HTML. Eu o coloquei na pasta layout-das-telas para organizar melhor os arquivos do projeto. Sem essa tag, o HTML seria apenas texto sem estilo.
<body>: Aqui é onde todo o conteúdo visível da página é colocado.
2. O Cabeçalho Fixo: div.topo
A imagem de referência mostrava um cabeçalho que parecia fixo no topo da página. Para isso, usei uma div com a classe topo.

<div class="topo">
    <img src="assets/logo.ico" class="logo">
    <div class="menu">
        <a href="#informaçoes">INFORMAÇÕES</a>
        <a href="#contatos">CONTATOS</a>
        <a href="#horarios">HORÁRIOS</a>
    </div>
</div>

<div class="topo">: Usei uma div como um contêiner para o cabeçalho. A classe topo me permitiu estilizar essa seção especificamente.
<img src="assets/logo.ico" class="logo">: Inseri a imagem do logo da cafeteria. O src aponta para onde a imagem está localizada (assets/ é a pasta de recursos visuais). A classe logo me daria controle sobre o tamanho e alinhamento do logo.
<div class="menu">: Outra div para agrupar os links de navegação. Isso facilita a aplicação de estilos como display: flex para alinhar os links.
<a href="#informaçoes">INFORMAÇÕES</a>: Cada <a> (âncora) cria um link. O atributo href="#informaçoes" é crucial aqui: ele é um link interno (ancoragem) que fará a página rolar suavemente para a seção com o id="informaçoes" quando clicado. Isso é essencial para a navegação de uma página única.
No CSS (.topo):

Para o cabeçalho fixo, apliquei:

position: fixed;: Isso remove o elemento do fluxo normal do documento e o fixa na posição especificada na janela de visualização do navegador. Assim, ele permanece no topo mesmo quando o usuário rola a página.
width: 100%; top: 0; left: 0;: Garante que ele ocupe toda a largura e fique colado no topo e à esquerda.
z-index: 1000;: Coloca o cabeçalho acima de outros conteúdos, garantindo que ele não seja coberto por seções rolantes.
display: flex; justify-content: space-between; align-items: center;: Com essas propriedades, o logo e o menu são alinhados nas extremidades opostas do cabeçalho, com alinhamento vertical centralizado.
As cores de fundo (var(--cor-secundaria)) e texto (var(--cor-texto-claro)) foram definidas usando variáveis CSS para facilitar a manutenção e padronização.
3. A Seção Hero: Impacto Visual Inicial
A primeira coisa que o usuário vê na imagem é uma grande imagem de capa com o nome da cafeteria sobreposto. Chamei isso de "Hero Section".


<div class="hero" id="hero">
    <img src="assets/parallax-imagem1.png" class="img-capa">
    <div class="titulo-hero">
        <h1>MANHATTAN - COFFEE HOUSE</h1>
    </div>
</div>

<div class="hero" id="hero">: O contêiner principal para a seção hero. O id="hero" permite que o link de "volta ao topo" no rodapé funcione.
<img src="assets/parallax-imagem1.png" class="img-capa">: Esta é a imagem de fundo principal da seção. É uma <img> tag porque ela é o conteúdo visual principal aqui, não apenas um ornamento.
<div class="titulo-hero">: Um contêiner para o título, para que eu pudesse estilizá-lo e posicioná-lo sobre a imagem.
<h1>MANHATTAN - COFFEE HOUSE</h1>: A tag <h1> é usada para o título mais importante da página. Isso é crucial para SEO, pois indica o tópico principal da página.
No CSS (.hero e .hero .img-capa):

position: relative; no .hero: Necessário para que a imagem de capa e o título possam ser posicionados absolute em relação a ele.
position: absolute; width: 100%; height: 100%; object-fit: cover; na .img-capa: Posiciona a imagem para cobrir todo o div.hero, e object-fit: cover garante que ela se ajuste sem distorcer, cortando as partes que não cabem.
filter: brightness(0.6);: Apliquei um filtro de brilho para escurecer a imagem levemente, garantindo que o texto branco do título se destacasse melhor, como na imagem de referência.
Para .titulo-hero, usei position: relative; z-index: 2; para garantir que o título ficasse acima da imagem. Adicionei um background-color: var(--cor-fundo-transparente); e padding para o texto ter um fundo sutil e se destacar.
O h1 recebeu font-family: 'Cinzel', serif; e text-transform: uppercase; para replicar o estilo sofisticado da imagem.
4. Seções de Informação: Conteúdo e Efeitos de Paralaxe
A imagem de referência alternava entre seções de texto simples em fundo claro e seções de texto em destaque sobre imagens com efeito de paralaxe. Para isso, decidi refatorar um pouco o HTML e o CSS que você havia me enviado, para torná-lo mais flexível e fácil de manter.

HTML:

Eu alterei a classe informaçoes para secao-info para as seções de texto simples e criei secao-info-destaque para as seções com paralaxe. Além disso, adicionei classes parallax-bg-1 e parallax-bg-2 para diferenciar as imagens de fundo. Retirei as tags <img> que estavam dentro dessas divs, pois a imagem seria aplicada via CSS como background-image para o efeito de paralaxe.

<div class="secao-info" id="informaçoes">
    <h3>EXPERIMENTE O MELHOR CAFÉ DA CIDADE!</h3>
    <p>O café não é uma simples bebida que foi preparada por alguém...</p>
</div>

<div class="secao-info-destaque parallax-bg-1">
    <p><strong>Um bom café é motivo de alegria!</strong></p>
</div>

<div class="secao-info">
    <h3>O QUE É O CAFÉ MANHATTAN?</h3>
    <p>Segundo a Metodologia da Avaliação Sensorial da SCA...</p>
</div>

<div class="secao-info-destaque parallax-bg-2">
    <p><strong>A vida só começa depois do café!</strong></p>
</div>

<div class="secao-info">
    <h3>CONHEÇA O CAFÉ GOURMET MANHATTAN?</h3>
    <p>As características desse tipo de café gourmet de Manhattan...</p>
</div>

<div class="secao-info">: Usado para as seções com fundo branco e texto em marrom escuro.
<h3>: Para os subtítulos das seções. Semanticamente, h3 é apropriado aqui, seguindo o h1 da seção hero.
<p>: Para os parágrafos de texto.
<div class="secao-info-destaque parallax-bg-1">: Esta é a chave para o efeito de paralaxe.
secao-info-destaque: Uma classe genérica para aplicar os estilos de texto e overlay comuns a essas seções.
parallax-bg-1 (e parallax-bg-2): Classes específicas para definir qual imagem de fundo será usada.
<strong>: Para dar ênfase ao texto, deixando-o em negrito.
No CSS (.secao-info e .secao-info-destaque):

.secao-info: Simplesmente defini paddings, alinhamento de texto, cores de fundo e texto.
.secao-info-destaque:
background-size: cover; background-position: center;: Garante que a imagem de fundo cubra a seção e esteja centralizada.
background-attachment: fixed;: Esta é a propriedade mágica do paralaxe! Ela faz com que a imagem de fundo permaneça fixa em relação à janela de visualização, criando a ilusão de profundidade quando a página rola.
position: relative; overflow: hidden;: Essenciais para o pseudo-elemento ::before.
::before { content: ''; position: absolute; top: 0; left: 0; width: 100%; height: 100%; background-color: var(--cor-fundo-overlay); z-index: 1; }: Criei um overlay semi-transparente sobre a imagem de fundo. Isso é crucial para que o texto em branco seja legível sobre a imagem escura, como na imagem de referência.
position: relative; z-index: 2; no parágrafo dentro de .secao-info-destaque: Garante que o texto fique acima do overlay.
As regras parallax-bg-1 e parallax-bg-2 foram usadas para apontar para as imagens de fundo específicas: url('../assets/parallax-imagem2.jpg') e url('../assets/parallax-imagem3.jpg').
5. Contatos e Endereço: Mapa e Informações
A seção de contatos incluía um mapa e informações de contato.

<div class="contatos" id="contatos">
    <h3>Contatos e Endereço</h3>
    <div class="mapa-info">
        <iframe src="https://maps.google.com/maps?q=Av.%20Ayrton%20Senna,%202000&t=&z=13&ie=UTF8&iwloc=&output=embed"></iframe>
        <div class="info">
            <p>Telefone e WhatsApp: (71) 99999-9999</p>
            <p>Email: contato@manhattan.com</p>
            <p>Endereço: Av Ayrton Senna, 2000 - Barra da Tijuca - Rio de Janeiro</p>
        </div>
    </div>
</div>

<div class="contatos" id="contatos">: O contêiner para toda a seção. O id="contatos" é para a ancoragem do menu.
<h3>: O título da seção.
<div class="mapa-info">: Um contêiner flexível para agrupar o iframe do mapa e as informações.
<iframe src="https://maps.google.com/maps?q=Av.%20Ayrton%20Senna,%202000&t=&z=13&ie=UTF8&iwloc=&output=embed">: Inseri um iframe para o mapa. Idealmente, você usaria um link real para o Google Maps ou OpenStreetMap para um mapa funcional, mas para o layout, um placeholder funciona. A tag <iframe> é usada para incorporar conteúdo de outra fonte.
<div class="info">: Contêiner para as informações de contato.
<p>: Para cada linha de informação de contato.
No CSS (.contatos):

background-image: url('../assets/parallax-imagem4.png');: Usei a imagem da cafeteria com o balcão como fundo da seção, exatamente como na imagem de referência.
Apliquei o mesmo padrão de position: relative; overflow: hidden; e ::before para criar o overlay escuro sobre a imagem de fundo, garantindo a legibilidade do texto branco.
display: flex; flex-direction: column; align-items: center; no .mapa-info: Isso alinha o mapa e as informações um abaixo do outro por padrão (para mobile) e centraliza-os.
@media (min-width: 769px) { .contatos .mapa-info { flex-direction: row; justify-content: center; } }: Uma media query para desktop que muda a flex-direction para row, colocando o mapa e as informações lado a lado.
Estilizei o iframe com width: 100%; max-width: 600px; height: 350px; border-radius: 8px; box-shadow; para que ficasse parecido com o bloco na imagem.
6. Horários de Funcionamento: Organização em Grid
A seção de horários tinha um layout de grade, que se encaixava perfeitamente com CSS Grid.

<div class="horarios" id="horarios">
    <h3>HORÁRIOS DE FUNCIONAMENTO</h3>
    <ul>
        <li>
            <h3>SEGUNDA</h3>
            <div></div>
            <p>FECHADO</p>
        </li>
        </ul>
</div>

<div class="horarios" id="horarios">: Contêiner principal da seção, com id para ancoragem.
<h3>: Título da seção.
<ul>: Uma lista não ordenada para os dias da semana e horários. Semanticamente, uma lista é perfeita para itens repetitivos.
<li>: Cada item da lista representa um dia.
<h3>: Usei h3 para o nome do dia.
<div class="divisor"></div>: Uma div vazia que eu estilizaria para criar a linha horizontal divisória.
<p>: Para o horário de funcionamento.
No CSS (.horarios):

background-image: url('../assets/cafeteria.jpg');: Defini a imagem da cafeteria como fundo.
Novamente, o ::before para o overlay escuro e position: relative; z-index: 2; para os filhos para garantir a legibilidade.
display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 30px;: Este é o coração do layout de grade!
display: grid;: Habilita o modo de grid.
grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));: Cria colunas flexíveis. auto-fit tenta encaixar o máximo de colunas possível. minmax(250px, 1fr) garante que cada coluna tenha pelo menos 250px, mas pode crescer para ocupar o espaço disponível. Isso torna o layout responsivo automaticamente em parte.
gap: 30px;: Adiciona um espaçamento entre os itens da grade.
Cada li recebeu um background-color: rgba(0, 0, 0, 0.4); para criar o efeito de "cartão" semitransparente sobre a imagem de fundo, como na referência.
7. O Rodapé: Informações Finais e Botão "Voltar ao Topo"
O rodapé continha informações de copyright e um botão para rolar a página de volta ao topo.


<div class="rodape" id="rodape">
    <p>© Manhattan - Coffee House - Todos os direitos reservados</p>
    <p>Desenvolvido por Valdeilson Souza</p>
    <a href="#hero"><img src="assets/seta-para-cima.png" alt=""></a>
</div>

<div class="rodape" id="rodape">: O contêiner do rodapé.
<p>: Para o texto de copyright e de desenvolvimento.
<a href="#hero"><img src="assets/seta-para-cima.png" alt=""></a>: Um link que contém uma imagem de seta. O href="#hero" faz com que, ao clicar, a página retorne suavemente para a seção hero (que tem o id="hero").
No CSS (.rodape):

Posicionei a seta usando position: absolute; bottom: 20px; right: 30px; dentro do rodape que tem position: relative;.
Adicionei estilos para o botão da seta, como background-color, border-radius: 50% para deixá-lo circular, padding e box-shadow para replicar o visual da imagem.
transition: transform 0.3s ease; e transform: translateY(-5px); no hover da seta para uma pequena animação ao passar o mouse, dando um toque extra.
8. Responsividade: Adaptando para Todas as Telas
A responsividade era um requisito chave. O design precisava se adaptar a diferentes tamanhos de tela (celular, tablet, desktop). Usei Media Queries para isso.

@media (max-width: XXXpx): Esta regra CSS permite aplicar estilos apenas quando a largura da tela é menor ou igual ao valor especificado.
Minhas estratégias:
Topo: Em telas menores, mudei a flex-direction para column no .topo e o menu para flex-wrap para que os itens se ajustassem em várias linhas se necessário.
Hero: Diminuí a height e o font-size do h1 para que a seção hero ficasse proporcional em telas menores.
Informações: Ajustei os padding das seções para ocuparem mais espaço horizontalmente em telas menores.
Contatos: Em telas menores, o mapa-info volta para flex-direction: column para que o mapa e as informações fiquem empilhados verticalmente.
Horários: As colunas do grid do .horarios ul mudam de repeat(auto-fit, minmax(250px, 1fr)) para 1fr (uma única coluna) em telas menores que 768px, garantindo que os itens de horário não fiquem muito apertados.
Tamanhos de Fonte: Reduzi gradualmente os tamanhos de fonte de h1, h3 e p em diferentes breakpoints para manter a legibilidade e o equilíbrio visual.
Posicionamento: Ajustei a posição do botão "voltar ao topo" no rodapé para não ficar muito perto das bordas em telas pequenas.
Conclusão
Este projeto foi um exercício valioso na replicação de um layout visual para um ambiente web interativo. As principais lições aprendidas e aplicadas foram:

Semântica HTML: Usar as tags HTML corretas (h1, p, ul, a, etc.) para o propósito certo não apenas ajuda no SEO, mas também torna o código mais compreensível e acessível.
Poder do CSS: O CSS é incrivelmente poderoso para controle visual. display: flex, display: grid, position: absolute/relative, background-attachment: fixed e ::before foram ferramentas essenciais para criar o layout e os efeitos visuais desejados.
Media Queries: Indispensáveis para garantir que o site seja utilizável e visualmente agradável em qualquer dispositivo, do celular ao desktop.
Organização e Manutenção: O uso de variáveis CSS (:root) e a refatoração das classes (secao-info, secao-info-destaque) tornaram o código mais limpo e fácil de modificar no futuro.
Atenção aos Detalhes: Pequenos ajustes de padding, margin, font-size e box-shadow fazem uma grande diferença no resultado final para que ele se pareça com a imagem de referência.
Estou muito feliz com o resultado e a experiência adquirida neste projeto. Espero que este README seja útil para entender o processo e as escolhas por trás do desenvolvimento da página da "Manhattan - Coffee House"!