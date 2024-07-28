# REDES-SOCIAL-3D-CSS-PURO
## Criando projeto de redes social 3d com css puro projeto incrivel.

### Projeto feito com muita dedicação e entusiasma, então segue o código galera.

https://github.com/user-attachments/assets/3b7b269e-a768-46ec-aef9-1b24084b6c9f

## Estrutura Básica:
```
<ul>
    <!-- Lista de itens -->
    <li style="--i:6;--clr:#1877f2;"><a href="#"><span><i class="fa-brands fa-facebook-f"></i></span>Facebook</a></li>
    <li style="--i:5;--clr:#25d366;"><a href="#"><span><i class="fa-brands fa-whatsapp"></i></span>Whatsapp</a></li>
    <li style="--i:4;--clr:#1da1f2;"><a href="#"><span><i class="fa-brands fa-twitter"></i></span>Twitter</a></li>
    <li style="--i:3;--clr:#c32aa3;"><a href="#"><span><i class="fa-brands fa-instagram"></i></span>Instagram</a></li>
    <li style="--i:2;--clr:#ff0000;"><a href="#"><span><i class="fa-brands fa-youtube"></i></span>Youtuber</a></li>
    <li style="--i:1;--clr:#0a66c2;"><a href="#"><span><i class="fa-brands fa-linkedin"></i></span>Linkedin</a></li>
</ul>
```
### UMA Explicação Detalhada
#### Tag <ul>: Esta tag cria uma lista não ordenada.
#### Tag <li>: Cada item da lista é representado por um <li>. Vamos detalhar o primeiro item como exemplo:
```
<li style="--i:6;--clr:#1877f2;">
```
#### style="--i:6;--clr:#1877f2;": Define estilos CSS personalizados usando variáveis CSS.
#### --i:6: Define uma variável CSS --i com o valor 6.
#### --clr:#1877f2: Define uma variável CSS --clr com a cor #1877f2 (cor do Facebook).
#### Tag <a>: Cria um link.
```
<a href="#">
```
#### href="#": Define o destino do link. Aqui, # significa que o link não leva a lugar nenhum.
#### Tag <span>: Usada para agrupar conteúdo sem um significado específico, mas que pode ser estilizado com CSS.
```
<span>
```
#### Tag <i>: Usada para incluir ícones de fontes (neste caso, da biblioteca Font Awesome).
```
<i class="fa-brands fa-facebook-f"></i>
```
#### class="fa-brands fa-facebook-f": Define classes da Font Awesome para o ícone do Facebook.
#### Texto: O texto visível do link.
```
FACEBOOK
```
#### Fechamento das Tags: As tags são fechadas para completar a estrutura.
```
</a></li>
```
#### Padrão dos Outros Itens
#### Os outros itens seguem o mesmo padrão, mas com diferentes valores para --i, --clr e as classes dos ícones, correspondendo a cada rede social:

#### --i: É usado para ordenar ou animar os itens.
#### --clr: Define a cor associada à rede social específica.
#### class: Define o ícone da rede social específica usando Font Awesome.
### Resumo
#### <ul>: Cria uma lista.
#### <li>: Cria itens na lista com estilos personalizados.
#### <a>: Cria links para redes sociais.
#### <span> e <i>: Usados para ícones e texto.
#### Variáveis CSS (--i, --clr): Usadas para estilização personalizada.
#### Se precisar de mais alguma coisa ou de explicação sobre outro código, é só avisar!

# AGORA VAMOS EXPLICAR O CSS.
#### Reset e Configuração Global
```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif; 
}
```
#### *: Seleciona todos os elementos.
#### margin: 0 e padding: 0: Remove margens e preenchimentos padrão.
#### box-sizing: border-box: Inclui padding e border na largura e altura dos elementos.
#### font-family: 'Poppins', sans-serif: Define a fonte global para 'Poppins'.
### Estilo do body
```
body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: #434750;
}
```
#### display: flex: Usa flexbox para layout.
#### justify-content: center e align-items: center: Centraliza o conteúdo.
#### min-height: 100vh: Define altura mínima como 100% da altura da viewport.
#### background: #434750: Define a cor de fundo.

### Estilo da Lista (ul)
```
ul {
    position: relative;
    transform: skewY(-15deg);
}
```
#### position: relative: Define a posição relativa.
#### transform: skewY(-15deg): Inclina o elemento no eixo Y
### Estilo dos Itens da Lista (ul li)
```
ul li {
    position: relative;
    list-style: none;
    width: 120px;
    background: #3e3f46;
    padding: 15px;
    transition: 0.5s;
    z-index: calc(1 * var(--i));
}
```
#### position: relative: Define a posição relativa.
#### list-style: none: Remove a marcação da lista.
#### width: 120px: Define a largura.
#### background: #3e3f46: Define a cor de fundo.
#### padding: 15px: Define preenchimento.
#### transition: 0.5s: Define transições suaves de 0,5 segundos.
#### z-index: calc(1 * var(--i)): Define a ordem de empilhamento com base na variável --i
### Efeito de Hover nos Itens da Lista (ul li:hover)
```
ul li:hover {
    transform: translateX(-50px);
    background: var(--clr);
}
```
#### transform: translateX(-50px): Move o item 50px para a esquerda ao passar o mouse.
#### background: var(--clr): Muda a cor de fundo para a cor definida na variável --clr
#### Estilo do Pseudo-elemento ::before
```
ul li::before {
    content: '';
    position: absolute;
    top: 0;
    left: -40px;
    width: 40px;
    height: 100%;
    background: #3e3f46;
    filter: brightness(0.7);
    transform-origin: right;
    transform: skewY(45deg);
    transition: 0.5s;
}
```
#### content: '': Cria um elemento vazio.
#### position: absolute: Define a posição absoluta.
#### top: 0 e left: -40px: Posiciona o elemento.
#### width: 40px e height: 100%: Define dimensões.
#### background: #3e3f46: Define a cor de fundo.
#### filter: brightness(0.7): Aplica um filtro de brilho.
#### transform-origin: right: Define a origem da transformação.
#### transform: skewY(45deg): Inclina o elemento no eixo Y.
#### transition: 0.5s: Define transições suaves.
#### Efeito de Hover no Pseudo-elemento ::before
```
ul li:hover::before {
    background: var(--clr);
    filter: brightness(0.7);
}
```
#### background: var(--clr): Muda a cor de fundo para a cor definida na variável --clr.
#### filter: brightness(0.7): Mantém o filtro de brilho.
### Estilo do Pseudo-elemento ::after
```
ul li::after {
    content: '';
    position: absolute;
    top: -40px;
    left: 0;
    width: 100%;
    height: 40px;
    background: #3e3f46;
    filter: brightness(0.9);
    transform-origin: bottom;
    transform: skewX(45deg);
    transition: 0.5s;
}
```
#### top: -40px: Posiciona o elemento acima do item.
#### transform: skewX(45deg): Inclina o elemento no eixo X.
### Efeito de Hover no Pseudo-elemento ::after
```
ul li:hover::after {
    background: var(--clr);
    filter: brightness(0.9);
}
```
#### Estilo do Link (ul li a)
```
ul li a {
    text-decoration: none;
    color: #999;
    display: block;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    transition: 0.5s;
}
```
#### text-decoration: none: Remove a sublinha dos links.
#### color: #999: Define a cor do texto.
#### display: block: Exibe o link como bloco.
#### text-transform: uppercase: Converte o texto para maiúsculas.
#### letter-spacing: 0.05em: Define o espaçamento entre letras.
#### transition: 0.5s: Define transições suaves.
### Efeito de Hover no Link (ul li:hover a)
```
ul li:hover a {
    color: #fff;
}
```
#### color: #fff: Muda a cor do texto para branco ao passar o mouse.
## Estilo Específico do Último Item da Lista (ul li:last-child::after)
```
ul li:last-child::after {
    box-shadow: -120px 120px 20px rgba(0,0,0,0.25);
}
box-shadow: h-offset v-offset blur spread color;
```
#### A propriedade box-shadow adiciona sombra a um elemento. A sintaxe é:
#### box-shadow: h-offset v-offset blur spread color;
#### box-shadow: -120px 120px 20px rgba(0,0,0,0.25): Aplica uma sombra específica ao último item.
#### h-offset: Deslocamento horizontal da sombra. Pode ser positivo (para a direita) ou negativo (para a esquerda).
#### v-offset: Deslocamento vertical da sombra. Pode ser positivo (para baixo) ou negativo (para cima).
#### blur: O quanto a sombra será desfocada. Valores maiores resultam em uma sombra mais suave.
#### spread: Expande ou contrai a sombra. Valores positivos expandem, enquanto valores negativos contraem.
#### color: A cor da sombra
#### -120px: A sombra é deslocada 120 pixels para a esquerda.
#### 120px: A sombra é deslocada 120 pixels para baixo.
#### 20px: A sombra tem um desfoque de 20 pixels.
#### rgba(0,0,0,0.25): A cor da sombra é preta com 25% de opacidade.
#### Este estilo é aplicado especificamente ao último item da lista (li:last-child), e ao pseudo-elemento ::after.
#### Esse pseudo-elemento provavelmente cria uma sombra visual interessante para destacar o último item da lista.
#### Estilo do span Dentro dos Itens da Lista (ul li span)
```
ul li span {
    position: absolute;
    top: 0;
    left: -40px;
    width: 40px;
    height: 100%;
    transform-origin: right;
    transform: skewY(45deg);
    transition: 0.5s;
    display: flex;
    justify-content: center;
    align-items: center;
    opacity: 0.5;
    font-size: 1.25em;
}
```
#### display: flex: Usa flexbox para layout.
#### justify-content: center e align-items: center: Centraliza o conteúdo.
#### opacity: 0.5: Define a opacidade.
#### font-size: 1.25em: Define o tamanho da fonte.
#### Efeito de Hover no span (ul li:hover span)
```
ul li:hover span {
    opacity: 1;
}
```
#### opacity: 1: Muda a opacidade para 100% ao passar o mouse.

## VAMOS EXPLICAR MAIS ALGUMAS PROPRIEDADES DE CSS A PARTE AQUI.
### filter: brightness(0.9);
##### A propriedade filter aplica efeitos gráficos como desfoque, brilho e saturação aos elementos.
##### brightness(0.9): Ajusta o brilho do elemento. Valores menores que 1 reduzem o brilho, valores maiores que 1 aumentam o brilho. No seu código, brightness(0.9) reduz o brilho do elemento para 90% de sua luminosidade original.
##### Aplicado no contexto do hover
```
ul li:hover::after {
    background: var(--clr);
    filter: brightness(0.9);
}
```
##### Quando o item da lista é passado o mouse, a cor de fundo muda para a cor definida na variável --clr, e o brilho é ajustado para 90% da luminosidade original, criando um efeito visual de destaque.

### transform-origin: right;
##### A propriedade transform-origin define a posição de origem da transformação aplicada a um elemento. A sintaxe é:
```
transform-origin: x-axis y-axis z-axis;
```
##### x-axis: Ponto de origem no eixo X (horizontal).
##### y-axis: Ponto de origem no eixo Y (vertical).
##### z-axis: Ponto de origem no eixo Z (profundidade), usado em transformações 3D
#### No código:
```
transform-origin: right;
```
##### right: Define a origem da transformação no lado direito do elemento. Isso significa que qualquer transformação aplicada (como rotação ou inclinação) terá como ponto de referência o lado direito do elemento.
### transform: skewY(45deg);
##### A propriedade transform aplica transformações 2D ou 3D a um elemento. A sintaxe comum para skewY é:
```
transform: skewY(angle);
```
##### skewY(angle): Inclina o elemento ao longo do eixo Y pelo ângulo especificado.
#### NO CÓDIGO
```
transform: skewY(45deg);
```
#### 45deg: Inclina o elemento em 45 graus ao longo do eixo Y. Isso cria um efeito de inclinação diagonal.

#### Aplicado no contexto:
```
ul li::before {
    content: '';
    position: absolute;
    top: 0;
    left: -40px;
    width: 40px;
    height: 100%;
    background: #3e3f46;
    filter: brightness(0.7);
    transform-origin: right;
    transform: skewY(45deg);
    transition: 0.5s;
}
```
##### transform-origin: right: Define a origem da transformação no lado direito do pseudo-elemento ::before.
##### transform: skewY(45deg): Inclina o pseudo-elemento em 45 graus no eixo Y, criando um efeito de inclinação que adiciona uma dimensão visual interessante.
### Resumo
##### box-shadow: -120px 120px 20px rgba(0,0,0,0.25);: Adiciona uma sombra deslocada 120px para a esquerda e para baixo, com um desfoque de 20px e uma cor preta semi-transparente, ao último item da lista.
##### filter: brightness(0.9);: Reduz o brilho do elemento para 90%, criando um efeito de escurecimento sutil.
##### transform-origin: right;: Define que as transformações (como inclinação) têm origem no lado direito do elemento.
##### transform: skewY(45deg);: Inclina o elemento em 45 graus no eixo Y, adicionando um efeito visual de inclinação.
##### Essas propriedades juntas criam uma interface visualmente rica e interativa para os itens da lista, com efeitos de sombra, transformação e ajuste de brilho que respondem ao comportamento do usuário, como o hover.




