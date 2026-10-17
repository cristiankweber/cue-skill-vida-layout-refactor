---
name: vida-layout-refactor
description: Refatora layouts de aplicativos para uma interface médica institucional, profissional, limpa, menos poluída e alinhada à identidade visual da Vida Hematologia, Vida Pesquisa Clínica e materiais corporativos anexos.
---

# Vida Layout Refactor Skill

Use esta skill quando o usuário pedir ao Manus para revisar, redesenhar ou refatorar o layout visual de um aplicativo, dashboard, sistema interno, landing page, formulário, relatório web ou interface clínica relacionada à Vida Hematologia, Vida Pesquisa Clínica ou serviços de Hematologia/Transplante.

A missão principal é transformar interfaces funcionais, mas visualmente poluídas ou inconsistentes, em produtos digitais com aparência institucional, confiável, médica, elegante e fácil de usar, preservando a lógica do sistema e melhorando a experiência visual.

## Referências obrigatórias incluídas

Consulte os arquivos em `assets/` antes de propor ou implementar mudanças:

- `assets/vida_hematologia_logo.jpeg`: logotipo principal da Vida Hematologia.
- `assets/vida_hematologia_e_pesquisa_clinica.pdf`: apresentação institucional com referências de cores, uso de cards, fundos claros, vermelho institucional, verde/teal para pesquisa clínica, tipografia condensada em títulos e linguagem visual médica.

Use também:

- `reference/brand_visual_summary.md`: resumo da identidade visual.
- `reference/design_tokens.json`: paleta, espaçamentos, raios, sombras e tokens sugeridos.
- `templates/ui_audit_checklist.md`: checklist de auditoria visual.
- `templates/manus_refactor_prompt.md`: modelo de prompt de execução para o Manus.

## Princípios de refatoração

1. **Profissionalismo médico acima de decoração.**  
   O layout deve transmitir segurança, precisão, organização e cuidado. Evite aparência genérica, excessivamente colorida, infantil, gamificada ou promocional.

2. **Reduzir poluição visual.**  
   Elimine excesso de bordas, sombras fortes, cores competindo entre si, botões redundantes, ícones decorativos sem função, textos repetidos, cards demais na mesma tela e hierarquias confusas.

3. **Criar hierarquia clara.**  
   Cada tela deve ter uma prioridade visual evidente: título, contexto, ação principal, dados essenciais, ações secundárias e detalhes. O usuário deve entender a tela em poucos segundos.

4. **Preservar regra de negócio.**  
   Nunca remova funcionalidades, campos clínicos, cálculos, validações, rotas, permissões ou integrações sem justificativa explícita. A refatoração deve ser majoritariamente visual, estrutural e de UX.

5. **Aplicar identidade visual com moderação.**  
   O vermelho institucional deve funcionar como cor de marca e destaque, não como fundo predominante em todas as telas. Use branco, cinza-claro e tons neutros como base; vermelho para ações, seções institucionais e destaques; teal/verde para pesquisa clínica, módulos científicos ou indicadores de acompanhamento.

6. **Pensar como sistema de design.**  
   Centralize tokens de cor, tipografia, espaçamento, bordas, sombras e componentes. Evite ajustes manuais isolados que criem inconsistência futura.

## Identidade visual esperada

### Personalidade visual

- Institucional
- Médica
- Clara
- Contemporânea
- Sóbria
- Humana
- Técnica
- Premium sem ostentação

### Elementos recorrentes da marca

- Logotipo com símbolo orgânico em vermelho/vinho, remetendo a gota/célula/cuidado.
- Tipografia de títulos em caixa alta, condensada ou semibold.
- Cards brancos ou off-white com cantos arredondados.
- Fundos claros em cinza muito suave.
- Uso de vermelho institucional em títulos, botões, badges e barras de seção.
- Uso de teal/verde para o braço de Pesquisa Clínica.
- Fotografias médicas com overlay claro quando usadas como fundo.
- Layouts com bastante respiro e blocos bem separados.

## Paleta recomendada

Use os tokens do arquivo `reference/design_tokens.json`. Como referência:

- Vinho institucional: `#7A1714`
- Vermelho principal: `#B51F1B`
- Vermelho/coral de apoio: `#E43D3D`
- Teal Pesquisa Clínica: `#008E7D`
- Teal escuro: `#006F63`
- Azul Hospital Regina / institucional secundário: `#1175B8`
- Grafite para texto: `#333333`
- Cinza médio: `#6B6B6B`
- Fundo principal: `#F4F4F3`
- Card: `#FFFFFF`
- Borda suave: `#E7E3DF`

A cor de marca deve orientar a interface, mas não dominar todos os elementos. Para dashboards clínicos, priorize neutralidade e legibilidade.

## Diretrizes de layout

### Estrutura geral

- Preferir layout com sidebar ou navegação superior limpa, sem múltiplas barras concorrentes.
- Usar grid consistente de 8 px.
- Usar largura máxima confortável em telas de conteúdo textual.
- Agrupar informações em seções semânticas: resumo, dados clínicos, pendências, exames, decisões, anexos, histórico.
- Usar cards apenas quando eles melhoram agrupamento; não transformar cada linha em um card.
- Evitar telas longas com todos os dados abertos ao mesmo tempo. Use abas, accordions, filtros e seções recolhíveis quando fizer sentido.

### Cards

- Fundo branco.
- Borda `1px solid` suave.
- Raio entre 16 e 24 px.
- Sombra muito discreta ou inexistente.
- Padding generoso, geralmente 20–32 px.
- Título curto e hierarquia clara.
- Evitar múltiplos cards coloridos competindo entre si.

### Tabelas

- Cabeçalho fixo ou visualmente destacado.
- Linhas com espaçamento confortável.
- Zebrado muito sutil apenas se melhorar leitura.
- Ações de linha agrupadas em menu ou botões discretos.
- Filtros no topo, com busca clara.
- Evitar excesso de colunas; usar detalhes expansíveis quando necessário.

### Formulários

- Agrupar campos por contexto clínico.
- Usar labels sempre visíveis.
- Textos auxiliares curtos.
- Estados de erro claros e não agressivos.
- Botão principal único por etapa.
- Campos obrigatórios sinalizados de forma discreta.
- Evitar formulários em tela cheia sem seções.

### Dashboards

- Começar por KPIs essenciais, não por todos os gráficos.
- Separar indicadores assistenciais, operacionais e de qualidade.
- Gráficos com paleta sóbria.
- Evitar gráficos 3D, excesso de cores, sombras intensas e legendas confusas.
- Dar contexto ao número: período, denominador, tendência e interpretação.

### Tipografia

- Títulos: semibold/bold, caixa alta apenas em rótulos, abas ou headers curtos.
- Texto clínico: legível, tamanho mínimo 14–16 px.
- Evitar condensar textos longos.
- Usar peso tipográfico para hierarquia, não apenas cor.
- Preferir espaçamento de linha confortável em textos médicos.

## Padrão de implementação

Ao receber um projeto de aplicativo, siga este fluxo:

1. **Mapear a tecnologia.**
   Identifique framework, estrutura de pastas, arquivos de estilo, sistema de componentes e pontos de entrada.

2. **Auditar telas principais.**
   Liste problemas de hierarquia, poluição visual, inconsistência, responsividade, acessibilidade, navegação, excesso de cores e desalinhamento com a marca.

3. **Criar plano de refatoração.**
   Divida em etapas pequenas: tokens, componentes base, layout global, telas críticas, refinamento e validação.

4. **Centralizar design tokens.**
   Crie ou ajuste variáveis CSS, Tailwind config, theme provider, arquivo de tokens ou design system, conforme a stack.

5. **Refatorar componentes reutilizáveis.**
   Priorize botões, cards, inputs, badges, tabelas, modais, headers, sidebars, breadcrumbs e estados vazios.

6. **Aplicar nas telas de maior impacto.**
   Comece por dashboard inicial, tela de listagem, tela de cadastro/edição, visualização detalhada e geração de relatórios.

7. **Revisar acessibilidade.**
   Checar contraste, foco por teclado, labels, tamanho de clique, responsividade e feedback de erro.

8. **Entregar resumo objetivo.**
   Informe o que foi alterado, quais arquivos foram modificados, decisões de design e próximos ajustes recomendados.

## Regras específicas para evitar poluição

- Remover gradientes desnecessários, exceto se forem extremamente sutis.
- Não usar vermelho para todos os botões. Ação primária pode ser vermelha; ações secundárias devem ser neutras.
- Evitar caixas dentro de caixas dentro de caixas.
- Evitar ícones grandes sem função.
- Reduzir número de badges por item.
- Transformar textos repetitivos em rótulos curtos.
- Separar informação crítica de informação administrativa.
- Diminuir densidade visual sem esconder informação necessária.
- Substituir múltiplas ações concorrentes por ação primária + menu de ações secundárias.
- Evitar sombras coloridas e bordas saturadas.
- Usar estados vazios com orientação prática, não ilustrações chamativas.

## Critérios de aceitação

Uma refatoração só está adequada quando:

- A tela parece pertencer à Vida Hematologia ou Vida Pesquisa Clínica.
- A hierarquia visual ficou clara.
- A interface ficou mais limpa e menos cansativa.
- O usuário consegue identificar a ação principal rapidamente.
- O sistema continua funcional.
- Componentes reutilizáveis ficaram mais consistentes.
- Cores da marca foram aplicadas sem excesso.
- O layout funciona em desktop e telas menores.
- O contraste é adequado.
- O código ficou mais organizado, não apenas visualmente alterado.

## Saída esperada do Manus

Ao final, forneça:

1. Resumo das principais mudanças.
2. Lista de arquivos alterados.
3. Explicação das decisões visuais.
4. Pendências ou limitações encontradas.
5. Sugestões de próximos refinamentos.
6. Quando possível, screenshots ou descrição antes/depois.

## Tom de resposta

Responda de forma técnica, objetiva e executiva. Evite linguagem genérica como “deixei mais bonito”. Prefira explicar em termos de hierarquia, densidade, contraste, consistência, legibilidade, identidade visual, design system e usabilidade clínica.
