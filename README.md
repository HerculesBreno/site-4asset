# Site 4Asset — Marketing

Site institucional B2B da **4Asset Tecnologia S.A.** (Grupo Verante).
🌐 Ao vivo em: **https://herculesbreno.github.io/site-4asset/**

---

## 🚀 Editar o site (pro time de marketing)

**Abrir o ambiente de edição com um click:**

[![Abrir no GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/HerculesBreno/site-4asset?quickstart=1)

> 💡 Primeira vez? Veja [**`GUIA-MARKETING.md`**](./agente-claude/4-GUIA-MARKETING.md) — guia em PT-BR, sem jargão técnico.

### O que acontece quando você clica no botão acima

1. Abre uma janela do **VS Code direto no navegador** (não precisa instalar nada)
2. Em ~30 segundos o ambiente fica pronto com **Claude Code já instalado**
3. Você abre o **painel do Claude** na lateral e digita o que quer mudar:
   - *"trocar o whatsapp do rodapé pra (48) 99999-8888"*
   - *"/dream-team quero rever o título do hero"*
4. Claude propõe a mudança, você aprova, e ele **abre um Pull Request** automaticamente
5. Liderança de marketing **revisa e clica em Merge** no GitHub → site atualiza em ~30s

**Você nunca toca em código direto.** Tudo via chat.

---

## 📚 Comandos disponíveis (dentro do Claude Code)

| Comando | Quando usar |
|---|---|
| `/edit-copy [o que mudar]` | Edição direta de texto/número/foto. **80% dos pedidos.** |
| `/dream-team [pedido]` | Análise estratégica com 9 especialistas de marketing |
| `/seo-review [seção]` | Neil Patel + Rand Fishkin só sobre SEO |
| `/cro-review [seção]` | Peep Laja + Joanna Wiebe + Lenny Rachitsky só sobre conversão |
| `/status` | Lista PRs abertos no repositório |
| `/ajuda` | Mostra este menu |

Linguagem natural também funciona, sem precisar do `/`.

---

## 🛠 Pro time técnico

### Estrutura

```
.
├── index.html              ← site principal (single-page, scroll snap)
├── privacidade.html        ← política LGPD
├── *.png, *.jpg, *.svg     ← assets de imagem
├── clientes/               ← logos de clientes
├── .devcontainer/          ← config do Codespace (Claude Code + Node + Python)
├── .claude/                ← slash commands e permissions
├── .vscode/                ← tasks (preview)
├── CLAUDE.md               ← contexto que o Claude carrega automaticamente
└── agente-claude/          ← documentação legacy do fluxo via claude.ai
```

### Hosting

- **GitHub Pages** (branch `main`, root)
- Build: nenhum (HTML estático puro)
- Deploy: automático ao merge em `main`
- TTL: ~30 segundos pra propagar

### Rodar localmente (sem Codespace)

```bash
python -m http.server 8000
# abre http://localhost:8000
```

### Stack

HTML5 + CSS3 + JavaScript vanilla. Sem build, sem framework, sem dependência runtime. Compatibilidade alvo: Chrome/Edge/Safari/Firefox modernos.

---

## 📞 Contato

- Hercules — gestão técnica do site
- Maurício — co-aprovador de mudanças críticas
- Time de marketing — autores das mudanças
