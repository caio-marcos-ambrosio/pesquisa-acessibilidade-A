## Sobre esta pesquisa
 Uma frase descrevendo a dimensão e a pergunta central investigada.
## O que descobrimos (Principais Achados)
 3 a 5 bullet points com as descobertas mais relevantes.
 Cada bullet deve ter uma fonte citada.
## Ferramentas / Casos / Legislação (depende da sua dimensão)
 A seção principal com o produto obrigatório da sua dimensão.
 (relatório, mapa comparativo ou infográfico — em formato Markdown ou imagem)
## Como isso afeta o nosso trabalho como desenvolvedores
Após a pesquisa, a turma deve mudar a forma de desenvolver: acessibilidade não é um ajuste final, mas parte do processo desde o início. Abaixo estão práticas essenciais que devem ser adotadas.

 #### 1. Usar HTML semântico (evitar “gambiarras” com `<div>`)

 Antes (errado):

 `<div onclick="comprar()">Comprar</div>`

 Depois (certo):

 `<button onclick="comprar()">Comprar</button>`

 Explicação:
 O `<button>`:
 - É conhecido por leitores de tela
 - Funciona automaticamente com teclado (Enter/Espaço)
 
 A `<div>` não possui esses comportamentos por padrão.


 #### 2. Garantir a navegação por teclado
 
Testar e desenvolver pensando em usuários que não utilizam mouse.

 Exemplo: 

```html
<button id="menuBtn">Abrir menu</button>
<nav id="menu" hidden>
  <a href="#">Início</a>
  <a href="#">Perfil</a>
</nav>
```
```javascript
const btn = document.getElementById("menuBtn");
const menu = document.getElementById("menu");

btn.addEventListener("click", () => {
  const aberto = menu.hasAttribute("hidden");
  
  if (aberto) {
    menu.removeAttribute("hidden");
    btn.setAttribute("aria-expanded", "true");
    menu.querySelector("a").focus();
  } else {
    menu.setAttribute("hidden", "");
    btn.setAttribute("aria-expanded", "false");
    btn.focus();
  }
});
```

O que mudou:
- Uso de aria-expanded (É um atributo ARIA que indica se um elemento está aberto ou fechado)
- Controle de foco com `.focus()` (Um método do JavaScript que coloca o foco em um elemento)
- Interface funcional sem mouse
 
#### 3. Adicionar atributos de acessibilidade (ARIA)

ARIA (Accessible Rich Internet Applications)

É um conjunto de atributos que melhoram a acessibilidade de elementos na web.

- Fornece informações extras para tecnologias assistivas (como leitores de tela)
- Não muda o visual, mas muda como o conteúdo é interpretado


Exemplo:

```html
<button aria-expanded="false" aria-controls="faq1" onclick="toggleFaq()">
  Ver resposta
</button>

<div id="faq1" hidden>
  Esta é a resposta da pergunta.
</div>
```
```javascript
function toggleFaq() {
  const btn = document.querySelector("button");
  const conteudo = document.getElementById("faq1");

  const aberto = btn.getAttribute("aria-expanded") === "true";

  btn.setAttribute("aria-expanded", !aberto);
  conteudo.hidden = aberto;
}
```
Isso é importante pois os leitores de tela conseguem entender se um elemento está aberto/fechado.

#### Testar menualmente 
Não confiar apenas em ferramentas automáticas.

Práticas simples:
- Navegar usando apenas Tab, Enter e Shift + Tab
- Verificar se todas as funções são acessíveis
- Testar com leitor de tela (ex: NVDA)

#### Depois da pesquisa, a turma deve:
- parar de pensar só no visual e focar no significado do código
- Garantir que tudo funcione sem mouse
- Incluir acessibilidade no processo desde o início

## Referências
 Todas as fontes no formato: Autor/Organização. Título. Ano. URL.
 Mínimo: 5 fontes. Pelo menos 1 acadêmica ou