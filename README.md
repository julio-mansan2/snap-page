# Desafio Snap Page - Frontend-Mentor

Este é um desafio de uma página referente à empresa Snap, proposto pelo site Frontend-Mentor.

## Tabela de Conteúdos

- [Visão Geral](#visão-geral)
    - [Imagens](#imagens)
    - [Link da página](#link)
- [Processo](#processo)
    - [Linguagens utilizadas](#linguagens-utilizadas)
    - [O que aprendi](#o-que-aprendi)
    - [Possíveis evoluções](#possíveis-evoluções)
- [Autor](#autor)

## Visão-geral

### Imagens

<br>

````
Versão de Desktop
````

   <img src="./src/design/desktop-design.gif" alt="desktop-design">

<br>

````
Versão Mobile
````

 <img src="./src/design/mobile-design.gif" alt="mobile-design">

### Link

- Página no GitHub Pages: <a href="https://julio-mansan2.github.io/snap-page/">Clique aqui!</a>

## Processo

### Linguagens utilizadas

<br>

- Marcações semânticas de HTML5
- Propriedades de customização do CSS3
- Estruturas de JavaScript

<br>

### O que aprendi

<br>

- Criar uma navegação em "dropdown" utilizando JS:

````javascript

var acc = document.getElementsByClassName("acordeon");
var i;

for (i = 0; i < acc.length; i++) {
  acc[i].addEventListener("click", function() {
    this.classList.toggle("active");
    var panel = this.nextElementSibling;
    if (panel.style.maxHeight) {
      panel.style.maxHeight = null;
    } else {
      panel.style.maxHeight = panel.scrollHeight + "px";
    } 
  });
}

````

- Criar um menu hambúrguer:

````html

<input id="menu__toggle" type="checkbox" />
<label class="menu__btn" for="menu__toggle">
<span></span>
</label>

````
````css

#menu__toggle {
        opacity: 0;
      }
      #menu__toggle:checked + .menu__btn > span {
        transform: rotate(45deg);
      }
      #menu__toggle:checked + .menu__btn > span::before {
        top: 0;
        transform: rotate(0deg);
      }
      #menu__toggle:checked + .menu__btn > span::after {
        top: 0;
        transform: rotate(90deg);
      }
      #menu__toggle:checked ~ .menu__box {
        right: 0 !important;
      }
      .menu__btn {
        position: fixed;
        top: 1.25rem;
        right: 1.25rem;
        width: 1.6rem;
        height: 1.6rem;
        cursor: pointer;
        z-index: 1;
      }
      .menu__btn > span,
      .menu__btn > span::before,
      .menu__btn > span::after {
        display: block;
        position: absolute;
        width: 100%;
        height: 2px;
        background-color: #616161;
        transition-duration: .25s;
      }
      .menu__btn > span::before {
        content: '';
        top: -0.5rem;
      }
      .menu__btn > span::after {
        content: '';
        top: 0.5rem;
      }
      .menu__box {
        display: flex;
        position: fixed;
        flex-direction: column;
        top: 0;
        right: -100%;
        width: 18.75rem;
        height: 100%;
        margin: 0;
        padding: 5rem 1.25rem;
        list-style: none;
        background-color: #ECEFF1;
        box-shadow: 2px 2px 6px rgba(0, 0, 0, .4);
        transition-duration: .25s;
      }
      .menu__item {
        display: block;
        color: #333;
        font-family: 'Epilogue', sans-serif;
        font-size: 1.25rem;
        text-decoration: none;
        transition-duration: .25s;
      }

    .header  .info {
        position: relative;
        top: 0;
        left: 0.3rem;
        margin: 0.6rem;
      }

    .header .login-area {
        flex-direction: column;
        position: relative;
    }


````
<br>

### Possíveis evoluções

<br>

- Códigos mais compactos;
- Abdicar de setar as medições da imagem de forma manual, resultando em possíveis distorções;
- Praticar a construção de um menu hambúrguer.

<br>

## Autor

GitHub - <a href="https://github.com/julio-mansan2">julio-mansan2</a> <br>
Front-end Mentor - <a href="https://www.frontendmentor.io/profile/julio-mansan2">julio-mansan2</a> <br>
LinkedIn - <a href="https://www.linkedin.com/in/j%C3%BAlio-a-mansan-3415a7249/">Júlio A.</a> <br>
            