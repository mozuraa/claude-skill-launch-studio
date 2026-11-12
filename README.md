<p align="center">
  <img src="icon.svg" width="160" alt="Launch studio — claquete de cinema com um foguetão a descolar e um megafone">
</p>

<h1 align="center">Launch studio — Claude Skill</h1>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
  <img src="https://img.shields.io/badge/Claude-Skill-D97757" alt="Claude Skill">
  <img src="https://img.shields.io/badge/modos-V%C3%ADdeo%20·%20Kit%20·%20Novidades-8A63D2" alt="Modos">
</p>

<p align="center">
📚 Faz parte da <b><a href="https://github.com/mozuraa/claude-skills">biblioteca de skills de mozuraa</a></b> · Part of <b><a href="https://github.com/mozuraa/claude-skills">mozuraa's skills library</a></b>
</p>

<p align="center"><b><a href="#português">Português</a> · <a href="#english">English</a></b></p>

---

## Português

Fizeste uma coisa. Agora mostra-a. Um **estúdio de lançamento** para o **Claude** que transforma o projeto da pasta atual — site, app, jogo ou ferramenta — num **vídeo de lançamento curto e partilhável**, e prepara **tudo o resto para o anunciar**. Inspirado no [/brag](https://github.com/latent-spaces/brag), com tudo o que ele faz e mais.

| Modo | Para quê | Exemplo de pedido |
|---|---|---|
| 🎬 **Vídeo** | Vídeo de 15–30 s em **9:16, 1:1 e 16:9** a partir de **um só plano**, com capturas reais, música licenciada, legendas `.srt`, voz opcional e PT/EN | "/launch-studio" · "faz um vídeo disto para o TikTok" |
| 📣 **Kit de lançamento** | Textos para **X, LinkedIn, Instagram, TikTok, Product Hunt, Show HN e Reddit**, imagem OG, miniatura, GIF para o README, **pré-visualização da App Store** e checklist com calendário | "prepara o lançamento no Product Hunt" |
| 🔄 **Novidades** | Vídeo e posts do que mudou numa versão, a partir do **git log** ou do **CHANGELOG**, e notas para as lojas | "o que há de novo desde a 1.2?" |

Em todos os modos o Claude **faz perguntas com opções, dá a sua opinião honesta e pede autorização antes de qualquer coisa pesada** (instalar, renderizar, alterar o teu projeto).

### 🎬 Vídeo

```
Briefing ─► Inspecionar ─► Plano ─► ✋ ─► Montar ─► Rascunho ─► ✋ ─► Render final ─► Entrega
```

- **Lê o projeto** (código, cores, fontes, textos, ícone) e responde a 10 perguntas: o que é, para quem, o que o distingue, o momento "uau", o fluxo de uso, onde se arranja…
- **Material real, não maquetas:** explora sites no browser integrado e apps no simulador iOS (ou Android) e guarda capturas e gravações — com barra de estado limpa e dados fictícios.
- **Um plano, três formatos:** guião cena a cena numa grelha de batida, com a arrumação de cada cena em 9:16, 1:1 e 16:9 e as zonas seguras de cada app.
- **11 tons:** `natural`, `premium`, `lancamento-serio`, `caos`, `seco`, `trailer`, `loja`, `devlog`, `tutorial`, `retro`, `acolhedor` — ou uma direção livre ("lançamento falso de 2016"). Aceita os nomes do /brag.
- **Três motores, do mais leve ao mais completo:** ⚡ **Rápido** (só ffmpeg) · 🎨 **Estúdio** (modelo HTML + browser + ffmpeg) · 🧩 **Hyperframes** (se já o tiveres). Sem nada instalado, há um plano B: a composição corre no browser e gravas o ecrã.
- **Som com licença:** a tua música, música **original gerada pela skill** (6 estilos, só com Python) ou faixas *royalty-free* com a licença verificada e registada em `creditos.md`.
- **Legendas** `.srt` (com verificação de legibilidade) e versão com legendas gravadas; **voz-off opcional** (a tua, a do sistema ou outra, nunca imitando pessoas reais).
- **Capa** escolhida e cozida no fotograma 0, para todas as plataformas mostrarem a melhor miniatura.

### 📣 Kit de lançamento

- Textos para cada plataforma com **limites contados**, gancho na primeira linha, texto alternativo e onde pôr o link.
- **Show HN e Reddit** segundo as regras de cada comunidade — e a opinião franca quando o projeto não encaixa.
- **Imagens:** OG 1200×630 (com as meta tags), miniatura 1280×720, imagem social do GitHub, galeria e miniatura do Product Hunt, gráfico do Google Play.
- **GIF de demonstração** para o README, leve e em loop.
- **App Store:** pré-visualização em vídeo com as especificações oficiais (só gravações do ecrã da app, 886×1920, 15–30 s) e capturas.
- **Checklist e calendário** com datas e horas no teu fuso (antes, no dia, depois) e um `.ics` para importares.

### 🔄 Novidades

- Encontra o intervalo (última etiqueta, CHANGELOG, mudança de versão), lê o `git log` e os diffs.
- **Triagem:** novo · melhor · corrigido · interno (fica de fora) · segurança (sem pormenores perigosos).
- Traduz commits em benefícios e escreve as notas para a **App Store** (4 000 car.), o **Google Play** (500 car.), o **GitHub Releases** e o **CHANGELOG**.
- Vídeo de 10–20 s ("Agora podes…", "3 novidades", "antes / depois") e posts.

### O que traz

| Pasta | Conteúdo |
|---|---|
| [`references/video/`](references/video) | [`inspecionar`](references/video/inspecionar.md) · [`plano`](references/video/plano.md) · [`tons`](references/video/tons.md) · [`montagem`](references/video/montagem.md) · [`audio`](references/video/audio.md) |
| [`references/kit/`](references/kit) | [`copy-plataformas`](references/kit/copy-plataformas.md) · [`imagens`](references/kit/imagens.md) · [`checklist`](references/kit/checklist.md) |
| [`references/novidades/`](references/novidades) | [`novidades`](references/novidades/novidades.md) |
| [`assets/compositor/`](assets/compositor) | modelo de composição HTML (cada fotograma é função do tempo) + `capturar.mjs` |
| [`assets/scripts/`](assets/scripts) | `audio.py` (música original, efeitos, grelha de batida) e `legendas.py` (`.srt` + verificação) — só Python 3, sem dependências |
| [`assets/kit/`](assets/kit) | modelos de imagem OG, textos e checklist |
| [`assets/`](assets) | modelos de `plano.md` e `creditos.md` |

Não traz música, sons nem vídeos de terceiros: tudo o que gera é original.

### Segurança e ética

Nunca publica, agenda, envia mensagens, cria contas, compra música ou promoção, nem aceita termos por ti — prepara tudo e diz-te onde carregar. Nunca põe segredos nem dados pessoais num vídeo público, nunca inventa números ou testemunhos, só usa música com licença e não imita vozes de pessoas reais. Não copia anúncios nem a identidade de outras marcas.

### Exemplos

- [Vídeo: o lançamento de uma app de dividir contas, em tom solene](examples/video.md)
- [Kit: lançar uma app de respiração para iPhone (e porque não no Show HN)](examples/kit.md)
- [Novidades: da lista de commits às notas da versão 1.3](examples/novidades.md)

### Instalação

**Claude Code**

```bash
git clone https://github.com/mozuraa/claude-skill-launch-studio.git ~/.claude/skills/launch-studio
```

**Ou com toda a biblioteca, como plugin:**

```
/plugin marketplace add mozuraa/claude-skills
/plugin install estudios@mozuraa-skills
```

**App Claude / claude.ai:** carrega em **Code → Download ZIP** e carrega o ZIP nas **Definições**, na secção **Skills** (em *Capacidades*). Na app, o Claude escreve o plano, os textos e os modelos; renderizar vídeo precisa de um computador com as ferramentas abaixo.

Abre uma sessão nova para a skill ser carregada. Para atualizar: `cd ~/.claude/skills/launch-studio && git pull`.

### Ferramentas (opcionais — a skill pergunta antes de instalar)

| Para | Precisa de |
|---|---|
| Plano, textos, notas da versão, checklist | nada |
| Música, efeitos e legendas | Python 3 |
| Vídeo — motor ⚡ Rápido | ffmpeg |
| Vídeo — motor 🎨 Estúdio | ffmpeg + Node.js + `playwright-core` (~8 MB) + Chrome, Brave, Edge ou Chromium |
| Vídeo — motor 🧩 Hyperframes | Hyperframes já instalado |
| Capturas de apps | Xcode (simulador iOS) ou Android SDK (`adb`) |

### Estrutura

```
claude-skill-launch-studio/
├── SKILL.md                      # os 3 modos, as opções e as regras comuns
├── references/
│   ├── video/                    # inspecionar, plano, tons, montagem, audio
│   ├── kit/                      # copy-plataformas, imagens, checklist
│   └── novidades/                # novidades
├── assets/
│   ├── compositor/               # cena.html, capturar.mjs, LEIA-ME.md
│   ├── scripts/                  # audio.py, legendas.py
│   ├── kit/                      # og-image.html, copy-template.md, checklist-template.md
│   └── plano-template.md · creditos-template.md
├── examples/                     # video.md, kit.md, novidades.md
├── icon.svg · README.md · CHANGELOG.md · LICENSE
```

### Créditos

- Inspirado no **[/brag](https://github.com/latent-spaces/brag)** de latent-spaces (licença MIT): a ideia de transformar o projeto num vídeo de lançamento com música, movimento e texto para partilhar, as opções de tom e de voz, e uma versão leve sem dependências pesadas. O launch-studio é uma reescrita original: nenhum ficheiro, texto, música ou som do /brag foi copiado.
- O motor 🧩 usa o [Hyperframes](https://hyperframes.heygen.com/) apenas se já estiver instalado.

### Contribuir

Tens um tom novo, uma plataforma que falta, um limite que mudou? Abre uma *issue* ou um *pull request*.

### Licença

[MIT](LICENSE) — podes usar, alterar e partilhar livremente, mantendo o aviso de licença. A música e os sons gerados pelos scripts são teus.

---

## English

You built it. Now show it. A **launch studio** for **Claude** that turns the project in the current folder — website, app, game or tool — into a **short, shareable launch video**, and prepares **everything else you need to announce it**. Inspired by [/brag](https://github.com/latent-spaces/brag), doing everything it does and more.

| Mode | What for | Example request |
|---|---|---|
| 🎬 **Video** | A 15–30 s video in **9:16, 1:1 and 16:9** from **one plan**, with real captures, licensed music, `.srt` captions, optional voice-over and PT/EN | "/launch-studio" · "make a TikTok video of this" |
| 📣 **Launch kit** | Copy for **X, LinkedIn, Instagram, TikTok, Product Hunt, Show HN and Reddit**, OG image, thumbnail, README demo GIF, **App Store preview** and a checklist with a schedule | "prepare the Product Hunt launch" |
| 🔄 **What's new** | A video and posts about what changed in a release, from the **git log** or **CHANGELOG**, plus store release notes | "what's new since 1.2?" |

In every mode Claude **asks questions with options, gives its honest opinion and asks before anything heavy** (installing, rendering, changing your project).

### 🎬 Video

- **Reads the project** (code, colours, fonts, copy, icon) and answers 10 questions: what it is, who it's for, what sets it apart, the "wow" moment, the user flow, where to get it…
- **Real footage, not mockups:** explores websites in the built-in browser and apps in the iOS Simulator (or Android) and saves screenshots and recordings — with a clean status bar and fictional data.
- **One plan, three formats:** a scene-by-scene script on a beat grid, with each scene's layout in 9:16, 1:1 and 16:9 and every app's safe zones.
- **11 tones** — `natural`, `premium`, `lancamento-serio` (serious launch), `caos` (chaotic), `seco` (deadpan), `trailer`, `loja` (app store), `devlog`, `tutorial`, `retro`, `acolhedor` (cozy) — or free direction. /brag's tone names work too.
- **Three engines, lightest first:** ⚡ **Quick** (ffmpeg only) · 🎨 **Studio** (HTML template + browser + ffmpeg) · 🧩 **Hyperframes** (if you already have it). With nothing installed there's a plan B: the composition plays in the browser and you screen-record it.
- **Licensed sound:** your own music, **original music generated by the skill** (6 styles, Python only), or royalty-free tracks with the licence checked and logged in `creditos.md`.
- **Captions** as `.srt` (with a readability check) plus a burned-in version; **optional voice-over** (yours, the system voice or another — never imitating real people).
- **Poster frame** picked and baked into frame 0, so every platform shows the best thumbnail.

### 📣 Launch kit

- Per-platform copy with **counted limits**, a hook in the first line, alt text and link placement.
- **Show HN and Reddit** following each community's rules — and an honest call when the project doesn't fit.
- **Images:** OG 1200×630 (with meta tags), 1280×720 thumbnail, GitHub social preview, Product Hunt gallery and thumbnail, Google Play feature graphic.
- A light, looping **demo GIF** for the README.
- **App Store:** preview video to the official specs (app screen recordings only, 886×1920, 15–30 s) and screenshots.
- **Checklist and schedule** with dates and times in your time zone (before, on the day, after) and an `.ics` file to import.

### 🔄 What's new

- Finds the range (last tag, CHANGELOG, version bump) and reads the `git log` and diffs.
- **Triage:** new · better · fixed · internal (left out) · security (no dangerous details).
- Turns commits into benefits and writes notes for the **App Store** (4,000 chars), **Google Play** (500 chars), **GitHub Releases** and the **CHANGELOG**.
- A 10–20 s video ("Now you can…", "3 new things", "before / after") and posts.

### What's inside

Guides in `references/` (video, kit, what's new), an HTML composition template and capture script in `assets/compositor/`, dependency-free Python scripts in `assets/scripts/` (`audio.py` for original music, sound effects and the beat grid; `legendas.py` for `.srt` captions with checks), and templates for the OG image, copy, checklist, plan and credits. No third-party music, sounds or videos are bundled: everything it generates is original. The skill's instructions are in Portuguese; Claude always answers in your language.

### Safety and ethics

It never posts, schedules, sends messages, creates accounts, buys music or promotion, or accepts terms for you — it prepares everything and tells you where to click. It never puts secrets or personal data in a public video, never invents numbers or testimonials, only uses licensed music and never imitates real people's voices. It doesn't copy other brands' ads or identity.

### Examples (in Portuguese)

- [Video: launching a bill-splitting app in a deadly serious tone](examples/video.md)
- [Kit: launching an iPhone breathing app (and why not on Show HN)](examples/kit.md)
- [What's new: from a commit list to version 1.3 release notes](examples/novidades.md)

### Installation

**Claude Code**

```bash
git clone https://github.com/mozuraa/claude-skill-launch-studio.git ~/.claude/skills/launch-studio
```

**Or the whole library, as a plugin:**

```
/plugin marketplace add mozuraa/claude-skills
/plugin install estudios@mozuraa-skills
```

**Claude app / claude.ai:** click **Code → Download ZIP** and upload the ZIP in **Settings → Skills** (under *Capabilities*). In the app, Claude writes the plan, copy and templates; rendering video needs a computer with the tools below.

Start a new session so the skill is loaded. To update: `cd ~/.claude/skills/launch-studio && git pull`.

### Tools (optional — the skill asks before installing anything)

| For | Needs |
|---|---|
| Plan, copy, release notes, checklist | nothing |
| Music, sound effects, captions | Python 3 |
| Video — ⚡ Quick engine | ffmpeg |
| Video — 🎨 Studio engine | ffmpeg + Node.js + `playwright-core` (~8 MB) + Chrome, Brave, Edge or Chromium |
| Video — 🧩 Hyperframes engine | Hyperframes already installed |
| App captures | Xcode (iOS Simulator) or Android SDK (`adb`) |

### Credits

- Inspired by **[/brag](https://github.com/latent-spaces/brag)** by latent-spaces (MIT licence): the idea of turning a project into a launch video with music, motion and share copy, the tone and voice options, and a lean version without heavy dependencies. launch-studio is an original rewrite: no files, text, music or sounds from /brag were copied.
- The 🧩 engine uses [Hyperframes](https://hyperframes.heygen.com/) only if it's already installed.

### Contributing

A new tone, a missing platform, a limit that changed? Open an issue or a pull request.

### License

[MIT](LICENSE) — free to use, modify and share, keeping the licence notice. Music and sounds generated by the scripts are yours.
