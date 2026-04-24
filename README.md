## Sobre esta pesquisa
 Uma frase descrevendo a dimensão e a pergunta central investigada.
## O que descobrimos (Principais Achados)
 3 a 5 bullet points com as descobertas mais relevantes.
 Cada bullet deve ter uma fonte citada.
## Ferramentas
### Extensões de Navegador
#### WAVE
**Resumo:**
Destaca visualmente problemas diretamente na página.

**Como funciona:**
Analisa o HTML renderizado e sobrepõe ícones na interface. Não altera o código, apenas interpreta a página como o usuário vê. Permite visualizar estrutura, contraste e landmarks.
 
**O que detecta:**
- Falta de texto alternativo (alt) 
- Problemas de contraste 
- Estrutura de headings (h1–h6) 
- Labels ausentes em formulários 
- ARIA mal utilizado 

**Diferencial:**
Melhor ferramenta para análise visual rápida e compreensão da estrutura da página.
    
#### axe DevTools
**Resumo:**
Focada em desenvolvedores, ideal para testes durante o desenvolvimento.

**Como funciona:**
Usa o motor do axe-core para rodar testes automatizados baseados nas WCAG dentro do navegador ou CI/CD.
    
**O que detecta:**
- Violações WCAG (níveis A, AA) 
- Problemas de ARIA 
- Elementos sem acessibilidade semântica 
- Problemas de navegação por teclado 
**Diferencial:**
Uma das mais completas para integração com código e testes automatizados.
    
#### Access Monitor
**Resumo:**
Validador baseado nas diretrizes WCAG.

**Como funciona:**
Analisa páginas via URL e atribui uma pontuação de acessibilidade.

**O que detecta:**
- Conformidade WCAG 
- Problemas estruturais 
- Falhas de contraste 
- Links e navegação 

**Diferencial:**
Fornece pontuação e classificação, útil para relatórios acadêmicos.
    
#### Sa11y
**Resumo:**
Ferramenta simples para criadores de conteúdo.

**Como funciona:**
Interface amigável que analisa páginas e dá feedback em linguagem simples.

**O que detecta:**
- Links quebrados 
- Falta de alt em imagens 
- Problemas de headings 
- Legibilidade 

**Diferencial:**
Melhor para não desenvolvedores (UX, conteúdo).
    
### Ferramentas Online e Plataformas
#### DYNO Mapper
**Resumo:**
Mapeia sites e testa acessibilidade em escala.

**Como funciona:**
Faz crawling do site e gera relatórios completos.

**O que detecta:**
- Problemas WCAG em múltiplas páginas 
- Estrutura do site 
- Conteúdo inacessível 

**Diferencial:**
Ideal para sites grandes.
    
#### AudioEye
**Resumo:**
Plataforma com automação + IA.

**Como funciona:**
Combina análise automática com revisão humana.

**O que detecta:**
- Problemas WCAG 
- Barreiras reais de uso 
- Ajustes dinâmicos na interface 

**Diferencial:**
Inclui IA + suporte humano, algo que outras não têm.
    
#### Total Validator
**Resumo:**
Valida HTML + acessibilidade.
Como funciona:
Executa validações técnicas e acessibilidade juntas.

**O que detecta:**
- HTML inválido 
- WCAG 
- Links quebrados 

**Diferencial:**
Combina validação técnica + acessibilidade.
    
#### AMAWeb

**Resumo:**
Plataforma para adequação às WCAG.

**Como funciona:**
Audita e acompanha evolução da acessibilidade.

**O que detecta:**
- Problemas WCAG 
- Métricas de melhoria contínua 

**Diferencial:**
Foco em gestão contínua de acessibilidade.
    
#### Google Lighthouse
**Resumo:**
Auditoria geral (performance, SEO, acessibilidade).

**Como funciona:**
Executa testes automatizados e gera score.

**O que detecta:**
- Contraste 
- Elementos sem nome acessível 
- Botões sem label 
- Navegação básica 

**Diferencial:**
Fácil de usar e integrado ao Chrome, mas menos profundo que axe.
    
### Leitores de Tela (Testes Manuais)
#### JAWS
**Resumo:**
Leitor de tela profissional.

**Como funciona:**
Lê o conteúdo da tela e permite navegação por teclado.

**O que detecta:**
- Problemas reais de navegação 
- Ordem de leitura incorreta 
- Falhas de ARIA 

**Diferencial:**
Muito usado no mercado → padrão real de usuários.
    
#### NVDA
**Resumo:**
Leitor gratuito e open source.

**Como funciona:**
Interpreta o DOM e lê via sintetizador de voz.

**O que detecta:**
- Conteúdo inacessível 
- Problemas de foco 
- Navegação ruim 

**Diferencial:**
Melhor opção gratuita para testes reais.
    
#### VoiceOver
**Resumo:**
Leitor nativo Apple.

**Como funciona:**
Baseado em gestos (mobile) e teclado (desktop).

**O que detecta:**
- Problemas em apps mobile 
- Falta de acessibilidade em iOS/macOS 

**Diferencial:**
Essencial para testes mobile (iPhone).
    
### Automação e Frameworks
#### Robot Framework
**Resumo:**
Framework de automação em Python.

**Como funciona:**
Integra ferramentas como axe para testes automatizados.

**O que detecta:**
- Problemas recorrentes 
- Regressões de acessibilidade 

**Diferencial:**
Ideal para testes contínuos (CI/CD).
    
#### A11Watch
**Resumo:**
Monitoramento contínuo.

**Como funciona:**
Executa auditorias automáticas ao longo do tempo.

**O que detecta:**
- Mudanças que quebram acessibilidade 
- Problemas recorrentes 

**Diferencial:**
Foco em monitoramento contínuo, não só testes pontuais.

### Conclusão
Nenhuma ferramenta sozinha garante acessibilidade completa.
Ferramentas automáticas, como axe DevTools e Lighthouse, identificam erros técnicos rapidamente, mas não conseguem avaliar totalmente a experiência real do usuário.

Já leitores de tela, como NVDA e JAWS, permitem identificar problemas reais de navegação e usabilidade, sendo essenciais para testes mais completos.

## Infográfico da pesquisa realizada:
![infográfico](./imagens/Infografico-ferramentas.png)

## Como isso afeta o nosso trabalho como desenvolvedores
 O que a turma deveria fazer diferente depois de ler esta pesquisa?
 Pelo menos 3 práticas concretas, com exemplos de código se possível.
## Referências
 Todas as fontes no formato: Autor/Organização. Título. Ano. URL.
 Mínimo: 5 fontes. Pelo menos 1 acadêmica ou