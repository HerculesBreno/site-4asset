# PRD TEMPLATE

> Adicione este arquivo em: **Project → Knowledge → Upload file**
> O Claude usa este template ao final do fluxo do Dream Team antes de criar o PR.

---

# PRD — [TÍTULO CURTO DO PEDIDO]

## 1. Identificação

- **Solicitado por:** [nome ou email do marketeer]
- **Data:** [data ISO YYYY-MM-DD]
- **Canal:** Claude Project · site-4asset
- **Tipo de pedido:** [copy · SEO · conversão · funil · tagging · atribuição · design · estratégia · outro]

## 2. Pedido original

> [Cole aqui a mensagem completa do usuário, sem editar]

## 3. Contexto identificado

- **Página/seção afetada:** [ex: Hero · Pilares · Cards de produto]
- **Arquivos:** `[ex: index.html (linhas 1234-1267)]`
- **Versão atual no site:** https://herculesbreno.github.io/site-4asset/

## 4. Análise do Dream Team

> Para cada especialista convocado, registre o parecer em primeira pessoa.

### [Nome do especialista 1] · [domínio]
[Parecer de 2-4 parágrafos no estilo da persona, incluindo:
- Diagnóstico do problema
- Recomendação concreta
- Hipótese mensurável (se aplicável)
- Riscos identificados]

### [Nome do especialista 2] · [domínio]
[mesmo formato]

[...continua para cada especialista convocado]

## 5. Síntese consolidada

### Consensos
- [Ponto onde todos concordam]
- [...]

### Tensões / Trade-offs
- **[Especialista A] x [Especialista B]:** [resumo da discordância e o que está em jogo]
- [...]

### Recomendação final
[Sua proposta como orquestrador, considerando o contexto da 4Asset — público B2B, posicionamento premium, métricas via RD Station + GA4. Deixe explícito o caminho escolhido entre as tensões.]

## 6. Implementação proposta

### Arquivos afetados
- `[arquivo]` — [linhas] — [tipo de mudança]

### Antes
```html
[trecho atual do código, fiel ao repositório]
```

### Depois
```html
[trecho proposto]
```

### Alterações em CSS / JS
- [Se houver, listar. Se não houver, escrever "Nenhuma."]

### Impacto em outras páginas/seções
- [Lista de impactos colaterais detectados ou "Nenhum"]

## 7. Métricas de validação

> Como vamos saber se a mudança funcionou?

- **Métrica primária (North Star):** [ex: leads qualificados via RD Station]
- **Métricas secundárias:** [ex: scroll depth na dobra X, click-through no CTA Y]
- **Linha de base atual:** [valor atual ou "auditoria pendente"]
- **Hipótese de impacto:** [ex: "esperamos +15% em clicks no CTA hero em 30 dias"]
- **Janela de avaliação:** [ex: 30 dias após deploy]
- **Tagueamento adicional necessário?** [se sim, listar evento + dataLayer schema]

## 8. Auditorias e dependências externas

> O Dream Team identificou que algumas validações dependem de dados ao vivo. Listar aqui o que precisa ser auditado fora deste PR.

- [ ] [Ex: confirmar com Julius que o evento `cta_hero_click` está disparando no GTM]
- [ ] [Ex: validar com Mercer que o RD Station passa UTM `source=site_4asset` para o GA4]
- [ ] [Ex: pedir SparkToro audit do share of search vs concorrentes (Rand)]

## 9. Riscos identificados

- **[Risco 1]:** [descrição + mitigação]
- **[Risco 2]:** [descrição + mitigação]

## 10. Aprovações

- [ ] Aprovação do solicitante (marketing)
- [ ] Aprovação do gestor (você, dono do site)
- [ ] Aprovação do dev (apenas se mudança envolver CSS/JS/estrutura)

---

## 11. PR Output

Quando o PRD for aprovado, o agente gera o PR com:

- **Branch:** `dreamteam/[descricao-kebab-case]`
  *(ou `marketing/[descricao]` se foi edição direta sem Dream Team)*
- **Título:** `[dreamteam] [resumo de até 60 chars]`
- **Corpo do PR:** todo este PRD colado, com a seção "PR Output" suprimida.
- **Assinatura final do PR:**
  ```
  Solicitado por: [nome]
  Analisado pelo Dream Team em: [data]
  Especialistas convocados: [lista]
  ```
