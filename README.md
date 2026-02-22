# Projeto de extenção de Engenharia de Software
## PROJETO VILA INDUSTRIAL: MEMÓRIA E COMUNIDADE
O Portal da Vila Industrial é um site desenvolvido como projeto de extensão universitária por mim Luana Mozer, da Faculdade Anhanguera, com o objetivo de preservar a memória do bairro Vila Industrial, localizado na Zona Leste de São Paulo, e fortalecer os laços comunitários por meio da tecnologia.

O trabalho consistiu na criação de um site completo, com código 100% original em HTML, CSS e JavaScript, estruturado em sete abas temáticas. A página inicial apresenta um fluxograma interativo com a linha do tempo completa do bairro, de 1920 a 2026, destacando marcos como a fundação da fábrica têxtil, a construção das vilas operárias, a chegada do asfalto, o tombamento da chaminé como patrimônio histórico e a recente revitalização cultural.

A aba de curiosidades reúne lendas locais, como a assombração da chaminé e a figueira centenária, enquanto os depoimentos trazem vozes reais de moradores que compartilham suas vivências no bairro. O mapa interativo, integrado ao Google Maps, mostra os limites da região, coordenadas geográficas e opções de transporte, como a Linha 15-Prata do Monotrilho.

Outras seções abordam pontos de reciclagem e coleta seletiva, organizações não governamentais que atuam no território e opções de lazer, como o parque central, o campo de várzea e o centro cultural instalado na antiga fábrica.

O site foi desenvolvido com design responsivo, garantindo acesso por celulares, tablets e computadores, e utiliza uma paleta de cores que remete à temática industrial, com laranja e cinza como tons principais. A navegação entre abas é dinâmica e suave, proporcionando boa experiência ao usuário.

Além do código, o projeto incluiu pesquisa histórica com moradores, consulta a artigos acadêmicos sobre bairros industriais e referências da Biblioteca Virtual do Estado de São Paulo. O resultado é uma ferramenta acessível que documenta a história do bairro, valoriza o patrimônio local e incentiva a participação comunitária.

O site está disponível online por meio de QR Code para divulgação em panfletos e cartazes, e todo o código foi documentado nesse README detalhado, explicando passo a passo da codificação, estrutura de pastas e orientações para personalização. O projeto cumpre seu papel social ao registrar a memória de um bairro operário e oferecer à comunidade um espaço virtual de pertencimento e informação.


# 👩‍💻 PASSO A PASSO DA CODIFICAÇÃO DO SITE DA VILA INDUSTRIAL
## 1️⃣ PLANEJAMENTO INICIAL E ESTRUTURA HTML
### 1.1 Definição da Arquitetura do Site
O primeiro passo foi planejar a estrutura completa do site, definindo quais abas seriam necessárias para contar a história do bairro de forma completa e útil para a comunidade. Decidimos por 7 abas principais:

Início: Linha do tempo em formato de fluxograma

Curiosidades: Lendas e fatos interessantes

Depoimentos: Vozes dos moradores

Mapa: Localização geográfica e limites

Reciclagem: Pontos de coleta seletiva

ONGs: Organizações locais

Lazer: Opções de entretenimento

### 1.2 Criação do Esqueleto HTML
Começamos com a estrutura básica de um documento HTML5:

html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vila Industrial - História e Comunidade</title>
    <!-- O CSS virá depois -->
</head>
<body>
    <!-- Conteúdo do site -->
</body>
</html>
<br>

### 1.3 Desenvolvimento do Cabeçalho e Navegação
Criamos um header fixo com sticky positioning para que o menu permaneça visível durante a rolagem:

html
<header>
    <div class="header-content">
        <div class="logo">
            <h1>VILA INDUSTRIAL</h1>
            <p>História, Comunidade e Futuro</p>
        </div>
        <nav>
            <ul>
                <li><a href="#home" class="nav-link active" data-section="home">Início</a></li>
                <li><a href="#curiosidades" class="nav-link" data-section="curiosidades">Curiosidades</a></li>
                <!-- Demais itens do menu -->
            </ul>
        </nav>
    </div>
</header><br>

### 1.4 Estruturação das Seções
Cada aba foi criada como uma seção com um ID único e a classe "section". A primeira seção recebe a classe "active-section" para aparecer inicialmente:

html
<section id="home" class="section active-section">
    <!-- Conteúdo da página inicial -->
</section>

<section id="curiosidades" class="section">
    <!-- Conteúdo das curiosidades -->
</section>

## 2️⃣ ESTILIZAÇÃO COM CSS<br>
### 2.1 Reset e Estilos Globais
Começamos resetando as margens e paddings padrão do navegador e definindo a fonte base:

css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background: #f4f4f4;
    color: #333;
    line-height: 1.6;
}
### 2.2 Definição da Paleta de Cores
Escolhemos cores que remetem à temática industrial:

Laranja (#e65100): Cor principal, usada em detalhes e hover

Cinza escuro (#455a64, #2c3e50): Cabeçalho e rodapé

Cinza claro (#f4f4f4): Fundo do site

Branco: Cards e elementos de destaque

### 2.3 Estilização do Cabeçalho e Menu
css
header {
    background: linear-gradient(135deg, #455a64 0%, #2c3e50 100%);
    color: white;
    padding: 1rem;
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo h1 {
    background: #e65100;
    padding: 0.2rem 1rem;
    border-radius: 30px;
}

nav ul li a {
    color: white;
    text-decoration: none;
    padding: 0.5rem 1rem;
    border-radius: 20px;
    transition: all 0.3s;
}

nav ul li a:hover,
nav ul li a.active {
    background: #e65100;
    transform: translateY(-2px);
}
### 2.4 Criação dos Cards e Elementos Comuns
Desenvolvemos um padrão de cards que se repete em várias seções:

css
.card {
    background: white;
    border-radius: 15px;
    padding: 1.5rem;
    box-shadow: 0 5px 15px rgba(0,0,0,0.08);
    transition: transform 0.3s;
}

.card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 20px rgba(0,0,0,0.12);
}

h2 {
    color: #2c3e50;
    border-left: 6px solid #e65100;
    padding-left: 1rem;
}

.grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
}
### 2.5 Implementação do Sistema de Abas
Criamos a lógica visual para mostrar apenas a seção ativa:

css
.section {
    display: none;
    animation: fadeIn 0.5s;
}

.section.active-section {
    display: block;
}

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
}
### 2.6 Desenvolvimento do Fluxograma
A parte mais desafiadora foi criar o fluxograma interativo. Usamos uma estrutura flexível com setas entre os itens:

css
.fluxograma-item {
    display: flex;
    margin-bottom: 1.5rem;
    align-items: flex-start;
}

.fluxograma-ano {
    min-width: 120px;
    background: rgba(230, 81, 0, 0.1);
    border: 2px solid #e65100;
    border-radius: 30px;
    padding: 0.5rem 1rem;
    text-align: center;
    margin-right: 2rem;
}

.fluxograma-conteudo {
    flex: 1;
    background: white;
    padding: 1.5rem;
    border-radius: 15px;
    border-left: 6px solid #e65100;
    transition: transform 0.3s;
}

.fluxograma-conteudo:hover {
    transform: translateX(10px);
}

.fluxograma-setas {
    margin-left: 120px;
    color: #e65100;
    font-size: 2rem;
}
### 2.7 Estilização do Mapa
Configuramos o container do mapa e os cards de informações geográficas:

css
.map-container {
    width: 100%;
    height: 500px;
    border: 3px solid #e65100;
    border-radius: 15px;
    overflow: hidden;
}

.map-info {
    background: #f9f9f9;
    border-left: 4px solid #e65100;
    padding: 1.5rem;
    border-radius: 10px;
}

.map-coordinates {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1rem;
}
## 2.8 Cards Temáticos
Cada seção ganhou estilos específicos:

css
/* Curiosidades */
.curiosity-card {
    background: linear-gradient(135deg, #fff5f0 0%, #fff 100%);
    border-left: 4px solid #e65100;
    padding: 1.2rem;
}

/* Depoimentos */
.testimonial::before {
    content: '"';
    font-size: 4rem;
    color: #e65100;
    opacity: 0.3;
    position: absolute;
    top: -10px;
    left: 10px;
}

/* Listas */
.points-list li::before {
    content: '✓';
    color: #e65100;
    margin-right: 1rem;
}

/* Lazer */
.tag {
    background: #e65100;
    color: white;
    padding: 0.2rem 0.8rem;
    border-radius: 15px;
    display: inline-block;
}
### 2.9 Responsividade com Media Queries
Garantimos que o site funcione em todos os dispositivos:

css
@media (max-width: 768px) {
    .header-content {
        flex-direction: column;
        text-align: center;
    }
    
    .fluxograma-item {
        flex-direction: column;
    }
    
    .fluxograma-ano {
        margin-right: 0;
        margin-bottom: 1rem;
    }
    
    .fluxograma-setas {
        margin-left: 0;
    }
    
    .map-container {
        height: 350px;
    }
}
## 3️⃣ INTERATIVIDADE COM JAVASCRIPT
### 3.1 Sistema de Navegação entre Abas
O JavaScript gerencia a troca de abas quando o usuário clica no menu:

javascript
document.querySelectorAll('.nav-link').forEach(link => {
    link.addEventListener('click', function(e) {
        e.preventDefault();
        
        // Remove a classe active de todos os links e seções
        document.querySelectorAll('.nav-link').forEach(l => l.classList.remove('active'));
        document.querySelectorAll('.section').forEach(s => s.classList.remove('active-section'));
        
        // Ativa o link clicado
        this.classList.add('active');
        
        // Ativa a seção correspondente
        const sectionId = this.getAttribute('data-section');
        document.getElementById(sectionId).classList.add('active-section');
    });
});
### 3.2 Lógica de Funcionamento

Limpeza: Remove todas as classes ativas

Ativação: Adiciona classe ativa ao link clicado

Exibição: Mostra a seção correspondente ao link

## 4️⃣ CONTEÚDO E INFORMAÇÕES
### 4.1 Pesquisa Histórica
Realizamos pesquisa com:

Moradores antigos do bairro

Documentos da Associação de Moradores

Artigos acadêmicos sobre bairros industriais

Acervo da Biblioteca Virtual do Estado

### 4.2 Linha do Tempo (1920-2026)
Organizamos cronologicamente os principais eventos:

html
<div class="fluxograma-item">
    <div class="fluxograma-ano">1920</div>
    <div class="fluxograma-conteudo">
        <h4>🌱 Fundação da Indústria Têxtil</h4>
        <p>A Fábrica Têxtil Santo Antônio é inaugurada...</p>
    </div>
</div>
<!-- Repetido para cada ano -->

### 4.3 Coleta de Depoimentos
Gravamos entrevistas com moradores e transcrevemos, corrigindo a gramática mas mantendo a essência:

html
<div class="testimonial">
    <p>"Moro aqui com meu marido há uns 40 anos. O bairro sempre foi assim calmo, tranquilo, todo mundo se conhece aqui."</p>
    <div class="testimonial-author">
        <div class="author-avatar">MA</div>
        <div><strong>Maria Aparecida do Carmo</strong><br>Moradora há 40 anos</div>
    </div>
</div>

### 4.4 Mapeamento Geográfico
Configuramos o Google Maps com as coordenadas exatas do bairro:

html
<iframe 
    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d14628.218651283107!2d-46.5523456871582!3d-23.5677206!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94ce5f04b6db1dcd%3A0x5a6dd3fb2459b9c0!2sVila%20Industrial%2C%20S%C3%A3o%20Paulo%20-%20SP!5e0!3m2!1spt-BR!2sbr!4v1700000000000!5m2!1spt-BR!2sbr" 
    width="100%" 
    height="100%" 
    style="border:0;" 
    allowfullscreen="">
</iframe>

## 5️⃣ OTIMIZAÇÕES E AJUSTES FINAIS
### 5.1 Correção de Erros
Identificamos e corrigimos:

Linha do tempo: Recolocamos a linha central que havia sumido

Depoimentos: Ajustamos a gramática e pontuação

Mapa: Aumentamos o zoom para mostrar os limites do bairro

Responsividade: Ajustamos para telas muito pequenas

### 5.2 Testes em Múltiplos Navegadores
Testamos o site em:

✅ Google Chrome

✅ Microsoft Edge

✅ Chrome (Android)

### 5.3 Validação de Código
Verificamos:

✅ HTML 

✅ CSS 

✅ JavaScript 


## 6️⃣ PUBLICACÃO E DIVULGAÇÃO
### 6.1 Hospedagem
Disponibilizamos o site em plataformas gratuitas:

GitHub Pages para versionamento

Netlify para publicação rápida

000webhost como backup

### 6.2 QR Code
Geramos um QR Code que direciona para o site, para ser impresso em panfletos e cartazes espalhados pelo bairro.

### 6.3 Documentação
Criamos este README detalhado para que outros possam entender, replicar ou contribuir com o projeto.

## 🎯 CONCLUSÃO
O site da Vila Industrial foi desenvolvido seguindo as melhores práticas de desenvolvimento web:

HTML semântico para acessibilidade e SEO

CSS modular com design responsivo

JavaScript funcional para interatividade

Conteúdo relevante baseado em pesquisa real

Design atrativo que valoriza a identidade do bairro

O resultado é uma ferramenta poderosa de preservação da memória e fortalecimento comunitário, que pode ser facilmente adaptada para outros bairros e comunidades.


## ⏱️ Tempo de desenvolvimento: Aproximadamente 2 semanas (pesquisa + codificação + testes + documentação)

## 👥 Público-alvo: Moradores, pesquisadores, estudantes e visitantes da Vila Industrial
