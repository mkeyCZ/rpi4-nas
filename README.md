# Vytvořte si domácí úložiště s Raspberry Pi 4: Snadný průvodce 🚀

<!-- Seznámení s projektem -->

***O projektu:***

*Objevte jednoduchost ve vytvoření vlastního síťového úložiště NAS pomocí Raspberry Pi. NAS (Network Attached Storage) je jako váš vlastní soukromý úložný prostor, kde můžete ukládat a sdílet soubory mezi různými zařízeními. S pomocí softwaru Open Media Vault, uživatelsky přívětivého nástroje pro správu dat, je nastavení tohoto úložiště snadné a bezproblémové. Takže si můžete být jisti, že vytvoření vlastního NAS je jednoduché a přináší vám přístupné úložiště pro vaše soubory a média.*

<br>

<!-- Logo projektu -->

<img src="https://cdn.icon-icons.com/icons2/2389/PNG/512/raspberry_pi_logo_icon_144943.png" alt="RPI Logo" width="135" height="">

<br>

<!-- Co je potřeba -->

**🛠️ Jaký hardware budeme potřebovat:**

Pro tento projekt je vhodné použít zařízení Raspberry Pi (zkráceně RPi), konkrétně model [raspberry pi4 B se 4GB RAM.](https://rpishop.cz/raspberry-pi-4/1598-raspberry-pi-4-model-b-4gb-ram.html) Také budete potřebovat MicroSD kartu o velikosti **minimálně 8GB**. Pro stabilní provoz doporučuji připojení RPi přímo k domácímu routeru pomocí LAN kabelu a nakonec potřebujeme nějaké to externí uložiště pro naše data *(v mém případě se jedná o 4T externí HDD).*

**🖥️ Jaký software budeme potřebovat:**

Pro náš projekt stačí jednoduchý nástroj, který nám umožní stáhnout operační systém **Raspberry OS Lite**. Tímto nástrojem je Raspberry Pi Imager, který si můžete stáhnout [zde.](https://www.raspberrypi.com/software/) 

<!-- návod -->

<br>

**Samotný postup instalace:**

*Nyní, když máme vše připravené, můžeme se pustit do samotné instalace operačního systému a následně instalace programu Open Media Vault (OMV), který nám zajistí konfiguraci našeho domácího síťového uložiště.*

### Krok č.1: Instalace operačního systému

1. **Nainstalujte Raspberry Pi Imager**: Nejprve nainstalujeme software Raspberry Pi Imager. Poté vložíme microSD kartu do našeho počítače a spustíme tento program.

2. **Vyberte operační systém**: Zvolíme možnost "CHOOSE DEVICE (VYBRAT ZAŘÍZENÍ)" a vybereme náš model Raspberry PI4, poté klikneme na "CHOOSE OS (VYBRAT OPERAČNÍ SYSTÉM)"a vybereme "Raspberry Pi OS (other/ostatní)" PRO instalaci operačního systému *Raspberry OS Lite (64-bit)*, což je odlehčená verze bez grafického prostředí (tzv. GUI). Nyní stačí kliknout na "CHOOSE STORAGE (VYBRAT ULOŽIŠTĚ)" a vybereme naší MicroSD kartu.

3. **Nastavení rozšířených možností**: Po výběru systému klikneme na ozubené kolečko (vpravo dole okna programu Raspberry Pi Imager) pro rozšířené možnosti instalace OS. V rozšířené nabídce doporučuji povolit protokol SSH (jedná se o prototokol, který nám umožní vzdálený přístup do daného zařízení). Dále nastavíme uživatelské jméno (pozn. tento uživatel bude také správcem OS, tzv. ROOT uživatel), heslo uživatele a vhodné rozložení klávesnice (doporučuji anglické, ale můžete přepnout na české).

4. **Spusťte instalaci**: Nyní můžeme spustit instalaci operačního systému na microSD kartu.

<br>

### Krok č.2: Po dokončení instalace OS na naší MicroSD kartu

1. Po dokončení instalace OS na naší microSD kartu, ji vložíme do zařízení RPI4, poté zapojíme kabel připojení k domácí síti tzv. kabel LAN a můžeme již zapojit kabel napájení. To spustí ihned bootování systému.

2. Po nabootování systému. Se můžeme ihned k RPI připojit pomocí SSH protokolu. To provedeme tak, že se přes webový prohlížeč připojíme k našemu routeru a podíváme se jakou nám router přidělil domácí IP zařízení RPI. Dále velmi doporučuji vypnout v routeru u zařízení DHCP, aby nám router po každěm restartu nepřiděloval jinou domácí IP, tímto se vyhneme pozdějším problémům s tím, že nebudeme muset pokaždé zjišťovat IP zařízení a domácí uložiště se nám nebude odpojovat.

*Poznámka: bohužel v tomto bych Vám milý čtenáři velmi rád pomohl, ale každý router je jiný a jinak se nastavuje. Pokud si nevíte rady, zkuste se podívat do uživatelské příručky k routeru, či se podívejte na youtube, kde si najdete potřebný videonávod k danému modelu Vašeho routeru.*

3. Po zjištění domácí IP vašeho RPi se můžeme připojit pomocí SSH z vašeho PC. To provedeme tak, že přes jakýkoliv příkazový řádek zadáme příkaz: `ssh uživatel(zadané při konfiguraci instalace OS)@domací ip zařízení`.

4. Po připojení k zařízení RPi zadáme náš první příkaz pro aktualizaci OS zařízení a všech programu a to: `sudo apt update && sudo apt upgrade -y` a zadáme heslo správce (které jsme opět zadávali při konfiguraci instalace OS). Po aktualizaci OS RPi doporučuji provést restart zařízení, to provedeme opět příkazem: `sudo reboot now`.

5. Nyní je vše připravené k instalaci software Open media valout. Tuto instalaci spustíme jednoduše a to příkazem `wget -O - https://raw.githubusercontent.com/OpenMediaVault-Plugin-Developers/installScript/master/install | sudo bash` *(tento příkaz stáhne tzv script/zkratku pro instalci software a rovnou jej spustí)* Jakmile se software nainstaluje doporučuji opět restart zařízení.

6. Nyní se muůžeme pustit do konfigurace vašeho domácího uložiště (NAS). To spustíme ve vašem webovém zařízení kde zadáme domácí ip adresu RPi.
