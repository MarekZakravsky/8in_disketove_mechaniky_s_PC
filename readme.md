# Ročníkový projekt: adaptace 8 palcové disketové mechaniky pro použítí se "standardním" počítačem




## 🚩 Obsah

- [Úvod](#Úvod)
- [Napájení](#Napájení)

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

Jedná se pouze o přímý kabel s vidlicí 230V na jednom konci a konektorem 1-480303-0 na druhé straně viz: [manuál](https://github.com/MarekZakravsky/8in_disketove_mechaniky_s_PC/blob/main/SA800%20OEM%20Manual.pdf#page=<27>).

### DC





