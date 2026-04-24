## Sobre esta pesquisa
 Uma frase descrevendo a dimensão e a pergunta central investigada.
## O que descobrimos (Principais Achados)
 3 a 5 bullet points com as descobertas mais relevantes.
 Cada bullet deve ter uma fonte citada.
## Ferramentas / Casos / Legislação (depende da sua dimensão)

## Testes em Sites do Grupo J&F
 
**Site analisado:** https://picpay.com/pt-br/pf  
**Data de coleta:** 19–20 de abril de 2026  
**Ferramentas utilizadas:** PageSpeed Insights (Google) e WebPageTest (Catchpoint)
 
> 📁 Na pasta `imagens/` estão as fotos dos testes realizados.
 
---
 
## 1. Scores de Acessibilidade
 
### 1.1 PageSpeed Insights
 
O PageSpeed Insights avalia acessibilidade em uma escala de 0 a 100. Veja os resultados abaixo:
 
| Contexto | Score | Interpretação |
|---|---|---|
| Desktop | 88 / 100 | Aceitável, mas abaixo do ideal (meta: acima de 90) |
| Mobile | 77 / 100 | Problemático — barreiras reais para usuários com deficiência |
 
O score mobile de **77/100** é o mais preocupante. Para um aplicativo financeiro com milhões de usuários, esse nível de acessibilidade indica que parte significativa dos usuários com deficiência encontra dificuldades no celular — justamente o dispositivo mais usado para acessar o PicPay.
 
### 1.2 WebPageTest (Catchpoint)
 
O WebPageTest, executado em **iPhone 15 com Chrome v145**, identificou **5 problemas de acessibilidade, sendo 2 classificados como críticos**. O relatório os aponta na categoria *"Is It Usable?"*, com status *"Not Bad"* — indicando que o site funciona, mas com ressalvas importantes.
 
---
 
## 2. Erros de Acessibilidade Encontrados
 
### 2.1 Tabela de erros, impactos e soluções
 
| Tipo de Erro | Gravidade | Impacto para o Usuário | Proposta de Solução |
|---|---|---|---|
| Imagens sem texto alternativo (`alt`) | 🔴 Crítico | Usuários cegos com leitores de tela não conseguem entender o conteúdo visual | Adicionar o atributo `alt` descritivo em todas as tags `<img>`. Ex: `alt="Pessoa usando o app PicPay no celular"` |
| Elementos interativos sem rótulo (`aria-label`) | 🔴 Crítico | Botões e links sem nome legível impedem navegação por tecnologias assistivas | Adicionar `aria-label` ou `aria-labelledby` em todos os botões e links sem texto visível. Ex: `aria-label="Abrir menu de navegação"` |
| Contraste insuficiente entre texto e fundo | ⚠️ Moderado | Dificulta leitura para usuários com baixa visão ou daltonismo | Revisar a paleta de cores garantindo proporção mínima de contraste de **4,5:1** para texto normal e **3:1** para texto grande, conforme WCAG 2.1 |
| Estrutura de navegação inadequada para leitores de tela | ⚠️ Moderado | Dificulta orientação e navegação de usuários cegos na página | Usar elementos HTML semânticos corretos (`<nav>`, `<main>`, `<header>`, `<section>`) e garantir ordem lógica de foco via teclado (Tab) |
| HTML gerado por JavaScript (client-side rendering) | ⚠️ Moderado | Conteúdo pode não ser lido por tecnologias assistivas que não executam JS | Adotar **Server-Side Rendering (SSR)** ou **Static Site Generation (SSG)** para que o HTML chegue pronto ao navegador, sem depender de JS |
 
### 2.2 Por que o HTML gerado por JS é um problema de acessibilidade
 
O WebPageTest identificou que o HTML da página é gerado após a entrega — ou seja, o site usa JavaScript para montar seu conteúdo. Isso é um problema de acessibilidade porque:
 
- Leitores de tela antigos ou mal configurados podem não aguardar o JS carregar
- O conteúdo pode aparecer fora de ordem para tecnologias assistivas
- Em conexões lentas, o usuário com deficiência fica sem conteúdo por mais tempo
---
 
## 3. Problemas Mais Graves e Por Quê
 
| # | Problema | Nível | Por que é grave |
|---|---|---|---|
| 1 | Score de acessibilidade mobile: 77/100 | 🔴 Crítico | Exclui usuários com deficiência de um serviço financeiro essencial no dispositivo mais usado |
| 2 | 2 problemas críticos identificados pelo WebPageTest | 🔴 Crítico | Erros críticos bloqueiam completamente o acesso de certos grupos de usuários |
| 3 | HTML gerado por JavaScript | 🟠 Alto | Compromete acessibilidade e resiliência; conteúdo pode não ser acessível para tecnologias assistivas |
| 4 | Score de acessibilidade desktop: 88/100 | ⚠️ Moderado | Abaixo do recomendado mesmo no ambiente mais favorável |
 
---
 
*Fonte dos dados: PageSpeed Insights (Google) e WebPageTest (Catchpoint) | Coleta: 19–20 de abril de 2026*
## Como isso afeta o nosso trabalho como desenvolvedores
 O que a turma deveria fazer diferente depois de ler esta pesquisa?
 Pelo menos 3 práticas concretas, com exemplos de código se possível.
## Referências
 Todas as fontes no formato: Autor/Organização. Título. Ano. URL.
 Mínimo: 5 fontes. Pelo menos 1 acadêmica ou    