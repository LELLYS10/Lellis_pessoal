# Sistema — MacBook + Mac Mini

> Mapa de onde cada coisa mora e como manter os dois Macs iguais.
> Criado em 03/09/2026.

## Regra de ouro

Cada coisa tem **um dono só** (o GitHub) e as duas máquinas são cópias dele.
Nunca edite a mesma nota nos dois Macs ao mesmo tempo sem antes abrir o Obsidian e deixar ele puxar.

---

## 1. Cofre Lellis Pessoal

- **Onde:** `~/Lellis Pessoal`
- **GitHub:** `LELLYS10/Lellis_pessoal`
- **Conteúdo:** financeiro-pessoal, hermes, pessoal, policial
- **Sincronia:** plugin obsidian-git

**Configuração corrigida em 03/09/2026:**

| Ajuste | Antes | Agora | Para quê |
|---|---|---|---|
| Enviar pro GitHub | desligado | a cada 10 min | o outro Mac enxerga o que você escreveu |
| Buscar do GitHub | 10 min | 5 min | você recebe rápido o que fez no outro Mac |
| Buscar ao abrir | não | **sim** | abriu o Obsidian, já está atualizado |
| Salvar só o marcado | sim | não (salva tudo) | nada fica de fora por esquecimento |

Antes disso, o cofre ficou **quase um mês sem enviar nada** (último envio: 07/08).
Era essa a causa das máquinas viverem diferentes.

---

## 2. Cofre CENTRAL-CREDPLUS

- **Status:** existe só nesta máquina, ainda **sem backup e sem sincronia**
- **Pendência:** localizar a pasta, colocar no GitHub e clonar no Mac Mini

---

## 3. Skills (Codex)

- **Onde:** `~/.codex/skills` — 12 skills
- **Status:** virou repositório git em 03/09/2026, com backup inicial feito
- **Pendência:** enviar pro GitHub (comando abaixo)

Skills: caveman (5), chatgpt-apps, hatch-pet, openclaw-credplus-agentes,
skill-n8n-automacao, social-content-studio, whatsapp-api, whatsapp-n8n-nao-oficial.

---

## Comandos

### Trazer o cofre para o Mac Mini (roda uma vez lá)

```bash
cd ~
git clone https://github.com/LELLYS10/Lellis_pessoal.git "Lellis Pessoal"
```

Depois abra o Obsidian no Mac Mini → "Gerenciar cofres" → "Abrir pasta como cofre" → escolha `~/Lellis Pessoal`.
O plugin obsidian-git já vem junto, com os ajustes certos.

### Enviar as skills pro GitHub (roda uma vez neste Mac)

Crie um repositório **privado** chamado `codex-skills` em github.com/new, depois:

```bash
cd ~/.codex/skills
git remote add origin https://github.com/LELLYS10/codex-skills.git
git push -u origin main
```

E no Mac Mini:

```bash
cd ~/.codex && git clone https://github.com/LELLYS10/codex-skills.git skills
```

### Rotina do dia a dia

- Sentou no Mac: **abra o Obsidian primeiro** e espere uns segundos. Ele puxa sozinho.
- Vai sair do Mac: deixe o Obsidian aberto uns 10 min, ou clique no ícone do obsidian-git e mande enviar.
- Mexeu numa skill: `cd ~/.codex/skills && git add -A && git commit -m "o que mudei" && git push`

---

## Pendências

- [ ] Localizar e versionar o cofre CENTRAL-CREDPLUS
- [ ] Criar o repositório `codex-skills` no GitHub e enviar
- [ ] Clonar o cofre e as skills no Mac Mini
- [ ] Conferir se o repositório `Lellis_pessoal` está privado
