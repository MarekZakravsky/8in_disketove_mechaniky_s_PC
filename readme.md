# Ročníkový projekt: adaptace 8 palcové disketové mechaniky pro použítí se "standardním" počítačem




## 🚩 Obsah

- [Úvod](#Úvod)
- [Napájení](#Napájení)
- [Data](#Data)

## Úvod
8" disketové mechaniky jsou největším formátem (velikostně) ze třech "běžných" velikostí disket a i když se nikdy z praktických důvodů nerošířil do domácích a osobních počítačů
i tak si našel své místo v minipočítačích (např.: CDC centurion [Centurion minicomputer](https://www.youtube.com/playlist?list=PLnw98JPyObn0wJFdbcRDP7LMz8Aw2T97V), TESLA SAPI-1 [Web o SAPI](http://www.sapi.cz/)),
v ranných průmyslových počítačích ze kterých zřejmě pochazějí mé jednotky které mi daroval pan Petr Laštovic
a zřejmě pocházejí z přístoje jako tento Linotronic 300 :


<img src="https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/images/linotype-hell-linotronic-330-imagesetter-p30516837_2.jpg" />


a ve firemních počítačích jako např: TRS model 2.
Celkově však 8" diskety (a dnes už diskety obecně) upadly mimo komunitu retro nadšenců upadly v zapomnění, tak proč je nezkusit znovu oživit!


## Napájení

8" disketové mechaniky obecně (v mém případě model Shugart 801) vyžadují pro provoz čtyři různá napětí
a to :
|Napětí|Popis|
| --- | --- |
|+5VDC| Napájení logiky |
|-5VDC| Napájení logiky |
|+24VDC| Pohon krokového motoru hlavy|
|+230VAC| Pohon vřetene jednotky|

### AC
Napájení střídavým proudem je v tomto případě tak jednoduché jak jen může být.

<img src="https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/images/IMG20240516202339.jpg" height = "400" height = "800" />

Jedná se pouze o přímý kabel s vidlicí 230V na jednom konci a konektorem 1-480303-0 na druhé straně viz: [manuál](https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/SA800%20OEM%20Manual.pdf#page=<27>) strana 27.

### DC
Stejnosměrné napájení je už zajmavěší část a téměř projekt sám o sobě.

<img src="https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/images/IMG20240516205932.jpg" height = "400" height = "800" />

V podstatě je to standardní 24V zabudovatelný zdroj (stříbrná krabička nahoře) a Československý pulsní stabilizovaný zdroj ZDR-1A
značky TESLA z již zmíněného počítače SAPI-1 (možná projekt do 4. ročníku (ano mám i něj)) který poskytuje +-5VDC a právě ten málem ukončil
tento projekt těsně před koncem a to díky těmto dvěma:

<img src="https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/images/IMG20240516211020.jpg" height = "400" height = "800" />

pro mně již pověstně nespolehlivé filtry TESLA řady TC naštěstí se tato součástka stále vyrábí a tak stačilo ji pouze objednat a zapájet všech 10 spojů.
Tyto dva zdroje pracují spolu a jejich vývody jsou vedeny do konektoru 1-480270-0 jehož pinout je též uveden v [manuál](https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/SA800%20OEM%20Manual.pdf#page=<27>) strana 27.
Takže po pár dalších lapálií s pojistkami jsou aktuálně provozuschopné všechny zroje a DC je funkční.

## Data

U dat už se konečně dostáváme od elektrotechniky k IT, jedna z nejlepčích věcí na 8" mechanikách je že i když mají 50ti pinový card-edge konektor tak jsou téměr plně kompatibilní s pozdějším standardem vedeným 34 pinovým rorhraním a IDC konektory
takže vlastně stačí pouze vytvořit vhodný adaptér na což je několik postupů, buď lze vzít 50p a 34p IDC F konektory a zapájet mezi ně drátky nebo se dá verze koupit na Ebayi nebo a to je cesta kterou jsem si vybral může človek s pomocí trocha reverzního inženýrství
vyprojektovat, nechat si na zakázku vyrobit a vlastnoručně osadit vlastní desky. Za úvod do SW na projektování PCB chci poděkovat Jurovi že mi značně usnadnil výběr vhodné stránky nakonec jsem použil stránku EasyEda

<img src="https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/images/Edaeasy.PNG" />

deska v EasyEda:

<img src="https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/images/Schematic_Floppy-disk-drive-adapter_2024-05-16.png" />
- elektrické schéma inspirováno [obrázek](https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/images/s-l1610.png) pozn. tento obrázek není mé dílo pochází z [Ebay](https://www.ebay.com/itm/115729590176)
<img src="https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/images/deska.PNG" />
- see-through obou stran desky
<img src="https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/images/deska3d.PNG" />
- 3D render
