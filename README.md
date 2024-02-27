# Vytvořte si domácí úložiště s Raspberry Pi 4: Snadný průvodce 🚀

<!-- Seznámení s projektem -->

***O projektu:***

*Objevte jednoduchost vytvoření vlastního síťového úložiště NAS pomocí Raspberry Pi. NAS (Network Attached Storage) je jako váš vlastní soukromý úložný prostor, kde můžete ukládat a sdílet soubory mezi různými zařízeními. S pomocí softwaru Open Media Vault, uživatelsky přívětivého nástroje pro správu dat, je nastavení tohoto úložiště snadné a bezproblémové. Takže si můžete být jisti, že vytvoření vlastního NAS je jednoduché a přináší vám přístupné úložiště pro vaše soubory a média.*

<br>

<!-- Logo projektu -->

<img src="https://cdn.icon-icons.com/icons2/2389/PNG/512/raspberry_pi_logo_icon_144943.png" alt="RPI Logo" width="135" height="">

<br>

<!-- Co je potřeba -->

**🛠️ Jaký hardware budeme potřebovat:**

Pro tento projekt je vhodné použít zařízení Raspberry Pi (zkráceně RPi), konkrétně model [raspberry pi4 B se 4GB RAM.](https://rpishop.cz/raspberry-pi-4/1598-raspberry-pi-4-model-b-4gb-ram.html) Také budete potřebovat MicroSD kartu o velikosti **minimálně 8GB**. Pro stabilní provoz je doporučuji připojení RPi přímo k domácímu routeru pomocí LAN kabelu a nakonec budeme potřebovat nějaké to externí uložiště pro naše data - *v mém případě se jedná o 4T externí HDD.*

**🖥️ Jaký software budeme potřebovat:**

Pro náš projekt stačí jednoduchý nástroj, který nám umožní stáhnout operační systém **Raspberry OS Lite**. Tímto nástrojem je Raspberry Pi Imager, který si můžete stáhnout [zde.](https://www.raspberrypi.com/software/) 

<!-- návod -->

<br>

**Samotný postup instalace:**

*Nyní, když máme vše připravené, můžeme se pustit do samotné instalace operačního systému a následně instalace programu Open Media Vault (OMV), který nám zajistí konfiguraci našeho domácího síťového uložiště.*

### Krok č.1: Instalace operačního systému

1. **Nainstalujte Raspberry Pi Imager**: Nejprve nainstalujeme software Raspberry Pi Imager. Poté vložíme microSD kartu do našeho počítače a spustíme tento program.

2. **Vyberte operační systém**: Zvolíme možnost "DOPSAT" pro naši microSD kartu a klikneme na "DOPSAT". Poté vybereme instalaci operačního systému Raspberry OS Lite, což je odlehčená verze bez grafického prostředí.

3. **Nastavení rozšířených možností**: Po výběru systému klikneme na ozubené kolečko pro rozšířené možnosti instalace OS. V rozšířené nabídce doporučujeme povolit protokol SSH.

4. **Nastavení uživatelských účtů**: Dále nastavíme uživatelské jméno (pozn. tento uživatel bude také správcem OS, tzv. ROOT uživatel), heslo uživatele a vhodné rozložení klávesnice (doporučujeme anglické, ale můžete přepnout na české).

5. **Spusťte instalaci**: Nyní můžeme spustit instalaci operačního systému na microSD kartu.
