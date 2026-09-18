<div align="center">

# NX8 — Nintendo Switch CFW Pack (4GB / Stock)

![Atmosphère](https://img.shields.io/badge/Atmosph%C3%A8re-1.11.2-blue)
![Hekate](https://img.shields.io/badge/Hekate-6.5.3-orange)
![Firmware](https://img.shields.io/badge/Firmware-22.5.0-green)
![Ultrahand](https://img.shields.io/badge/Overlay-Ultrahand%202.5.3-purple)
![Licença](https://img.shields.io/badge/Licença-GPL%2FMIT%20(componentes)-lightgrey)

Pacote de CFW pronto pra copiar no cartão SD, montado 100% a partir de
código-fonte oficial e releases oficiais dos próprios projetos —
**nenhum binário vem de pack pirata** (CNX/GNX/kefir/etc).

</div>

---

## 🔰 Antes de instalar

1. Este pacote é pro Switch **de fábrica** (4GB de RAM, sem mod) — Erista,
   Mariko, Lite ou OLED sem upgrade de memória.
2. Você precisa injetar `hekate_ctcaer_6.5.3.bin` (ou `payload.bin`) via
   RCM com uma ferramenta como o TegraRcmGUI.
3. **Falta o `prod.keys`** — não incluído de propósito (chaves são
   únicas do seu console, extraídas por você). Sem ele, alguns
   instaladores de conteúdo (DBI) ficam com funções limitadas.
4. Faça backup do seu cartão SD atual antes de copiar qualquer coisa por
   cima.

---

## 📥 Instalação

1. Baixe a versão mais recente na aba
   **[Releases](https://github.com/BLTEC/NX8/releases/latest)**.
2. Extraia o `.zip` baixado.
3. Copie o conteúdo extraído pra **raiz do cartão SD**, mesclando com o
   que já existir (sobrescrever é esperado).
4. Ligue o console normalmente — se o seu Switch já tem **modchip**
   (picofly, hwfly, etc), ele injeta o CFW sozinho no boot, sem precisar
   de RCM manual.
5. No menu do Hekate, escolha a entrada `Atmosphere (emuMMC)` ou
   `Sistema Original (Stock)`.

---

## 🌌 O que está incluído

### Bootloader & CFW
- **Hekate** 6.5.3 / Nyx 1.9.3 — compilado do código-fonte oficial
  (`CTCaer/hekate`).
- **Atmosphère** 1.11.2 — compilado do código-fonte oficial
  (`Atmosphere-NX/Atmosphere`), sem nenhuma modificação de comportamento.
- Logo de boot do Hekate e splash do Atmosphère personalizados.

### 🔒 Proteção / privacidade
- DNS MITM + PRODINFO em branco (só na emuMMC) — bloqueia telemetria e
  servidores da Nintendo, mantendo internet normal pra tudo mais.

### 🧩 Overlay (menu de sobreposição)
- **Ultrahand Overlay** — substituto completo do Tesla Menu, com sistema
  de idiomas (português incluído), temas, sons e loja de pacotes
  integrada.
- **Status Monitor** — CPU/GPU/RAM/temperatura/bateria/frequências em
  tempo real, com gráfico de FPS.
- **ovl-sysmodules** — ativa/desativa sysmodules direto pelo overlay.

### ⚙️ Sysmodules
- **MissionControl** — suporte a controles Bluetooth de terceiros
  (Xbox, PlayStation, Wii/Wii U, etc).
- **emuiibo** — emulação de amiibo.
- **Fizeau** — ajuste de cor/gamma da tela.
- **sys-tune** — controle de volume por app.
- **MasterVolume** — volume master além do limite padrão.
- **sys-con** — suporte extra de controles third-party.
- **SysDVR** — streaming de vídeo/áudio do console pra PC.
- **sys-clk** — overclock/underclock de CPU/GPU/memória (dentro dos
  limites oficiais documentados pelo próprio projeto).
- **SaltyNX** — injeção de código em jogos (base pro FPSLocker e
  ReverseNX-RT).

### 🎮 Jogabilidade
- **FPSLocker** — trava/ajusta FPS por jogo (já com tradução pt-BR
  oficial).
- **ReverseNX-RT** — alterna handheld/dock por jogo (**traduzido pra
  português neste pacote**, recompilado do código-fonte oficial).

### 🛠️ Apps e utilitários
- **EdiZon** — editor de save/cheats.
- **JKSV** — backup de saves.
- **sphaira** e **DBI** — instaladores de conteúdo NSP/XCI (precisam de
  `prod.keys` próprio — ver acima).
- **NX-Activity-Log** — estatísticas de uso.
- **HekateToolbox** — atalhos de manutenção do Hekate.
- **Moonlight-Switch** — cliente de game streaming.
- **NXThemesInstaller** — temas customizados da interface.
- **hbmenu** — menu de homebrew (abre pelo Álbum do sistema).

### 💾 Payloads (`bootloader/payloads/`)
- **TegraExplorer** — explorador de partições/arquivos via RCM.
- **DowngradeFixer** — corrige downgrade de firmware.
- **prodinfo_gen** — gera um PRODINFO mínimo se faltar/corromper (não
  desbane console, só recupera a partição).

---

## ⚠️ Avisos

- 🚫 **Nada de sigpatches, bypass de assinatura ou ferramentas de
  piratear jogos** — este pacote não inclui e não vai incluir.
- 🔑 Sem `prod.keys` próprio, instaladores de NSP/XCI ficam limitados —
  extraia suas próprias chaves com uma ferramenta oficial de dump.
- 🌐 O bloqueio de DNS afeta eShop/jogos online **só na emuMMC** — pra
  jogar online use a entrada `Sistema Original (Stock)`.
- 🧪 Todo componente foi baixado direto da fonte oficial de cada
  projeto e verificado por assinatura — mas teste no seu hardware antes
  de considerar definitivo.

---

## 📜 Disclaimer

- Este projeto é uma **compilação de software homebrew de código aberto**,
  cada um com sua própria licença (majoritariamente GPL-2.0/GPL-3.0/MIT)
  — os créditos abaixo apontam pro repositório oficial de cada um.
- Nenhum arquivo de jogo, chave de sistema (`prod.keys`, `title.keys`)
  ou conteúdo protegido por direitos autorais da Nintendo está incluído
  aqui.
- **Nintendo Switch** e demais marcas mencionadas são propriedade da
  Nintendo Co., Ltd. Este projeto não é afiliado, endossado ou
  patrocinado pela Nintendo.
- Uso por sua conta e risco — modificar o firmware do console pode
  violar os termos de uso da Nintendo.

---

## 🙏 Créditos

Hekate ([CTCaer](https://github.com/CTCaer/hekate)) · Atmosphère
([Atmosphere-NX](https://github.com/Atmosphere-NX/Atmosphere)) ·
Ultrahand Overlay ([ppkantorski](https://github.com/ppkantorski/Ultrahand-Overlay)) ·
Status Monitor ([ppkantorski](https://github.com/ppkantorski/Status-Monitor-Overlay)) ·
ovl-sysmodules ([ppkantorski](https://github.com/ppkantorski/ovl-sysmodules)) ·
MissionControl ([ndeadly](https://github.com/ndeadly/MissionControl)) ·
emuiibo ([XorTroll](https://github.com/XorTroll/emuiibo)) ·
Fizeau ([averne](https://github.com/averne/Fizeau)) ·
sys-tune ([HookedBehemoth](https://github.com/HookedBehemoth/sys-tune)) ·
MasterVolume ([averne](https://github.com/averne/MasterVolume)) ·
sys-con ([cathery](https://github.com/cathery/sys-con)) ·
SysDVR ([exelix11](https://github.com/exelix11/SysDVR)) ·
sys-clk ([retronx-team](https://github.com/retronx-team/sys-clk)) ·
SaltyNX / FPSLocker / ReverseNX-RT ([masagrator](https://github.com/masagrator)) ·
EdiZon ([WerWolv](https://github.com/WerWolv/EdiZon)) ·
JKSV ([J-D-K](https://github.com/J-D-K/JKSV)) ·
sphaira ([NaGaa95](https://github.com/NaGaa95/sphaira)) ·
NX-Activity-Log ([zdm65477730](https://github.com/zdm65477730/NX-Activity-Log)) ·
HekateToolbox ([WerWolv](https://github.com/WerWolv/Hekate-Toolbox)) ·
Moonlight-Switch ([XITRIX](https://github.com/XITRIX/Moonlight-Switch)) ·
NXThemesInstaller ([exelix11](https://github.com/exelix11/SwitchThemeInjector)) ·
DBI ([rashevskyv](https://github.com/rashevskyv/dbi)) ·
nx-hbmenu / nx-hbloader ([switchbrew](https://github.com/switchbrew)) ·
TegraExplorer ([suchmememanyskill](https://github.com/suchmememanyskill/TegraExplorer)) ·
DowngradeFixer ([sthetix](https://github.com/sthetix/DowngradeFixer)) ·
prodinfo_gen ([CaramelDunes](https://github.com/CaramelDunes/prodinfo_gen))

---

<div align="center">

![Licenças](https://img.shields.io/badge/Componentes-GPL--2.0%20%7C%20GPL--3.0%20%7C%20MIT-blue)

Nintendo Switch é uma marca registrada da Nintendo Co., Ltd.

</div>
