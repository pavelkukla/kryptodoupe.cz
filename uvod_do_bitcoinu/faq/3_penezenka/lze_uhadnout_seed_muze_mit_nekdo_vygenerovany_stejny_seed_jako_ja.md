V krátkosti? Ne, pokud dodržíte určitá pravidla.

Seed si můžeme (zjednodušeně) představit, jako bychom 128x nebo 256x (podle toho, jestli má seed 12 nebo 24 slov) hodili mincí a zapisovali. Když padne panna, zapíšu 1. Když padne orel, zapíšu 0. Tohle opakuji tedy 128x (pro náš příklad) a vyjde mi obrovské číslo, které je můj seed (peněženky ho potom převedou do daných [slov](https://github.com/bitcoin/bips/blob/master/bip-0039/bip-0039-wordlists.md), to je jen formalita).

Aby tedy druhý člověk vygeneroval stejný seed, musela by jeho mince dopadnout stejně ve všech 128 případech. Matematika umí tuto pravděpodobnost vyjádřit jako 1 z 2<sup>128</sup>, což je 1 případ z 340,282,366,920,938,463,463,374,607,431,768,211,456 (0.00000000000000000000000000000000000029%). V případě 24 slov je to ještě řádově úplně jinde, 1 z 2<sup>256</sup>, tedy konkrétně 1 z 115,792,089,237,316,195,423,570,985,008,687,907,853,269,984,665,640,564,039,457,584,007,913,129,639,936 případů (0.00000000000000000000000000000000000000000000000000000000000000000000000000086%).

I když uvážíme [Narozeninový paradox](https://betterexplained.com/articles/understanding-the-birthday-paradox/), tak i tak dřív vyhoří a zhasne Slunce, než by nějaký gigapočítač stihnul zkusit tolik kombinací, aby se alespoň v jednom případě trefil. 

Spíš než náhodou vygenerovaný stejný seed vás o vaše bitcoiny připraví nepozornost, prozrazení seedu nebo krádež. 

Pravidla:
- negenerujte si seed manuálně, tzn. žádné brainwallet, ručně poskládaná slova apod. Tohle napadlo už i útočníky a mají běžné fráze předgenerované a jen koukají, kdy si tam někdo pošle bitcoiny, aby si je mohli převést k sobě.
- vždy si nechte vygenerovat seed náhodně, nejlépe v [Trezoru](http://trezor.io/) (nebo [Ledgeru](https://www.ledger.com/)). Ale i softwarové peněženky generují dostatečně bezpečné fráze.
- rozhodně si negenerujte seed v žádné online aplikaci nebo webovém prostředí. Dokonce bych nedoporučoval vytvářet peněženku ani na počítači, opravdu si radši pořiďte HW peněženku nebo alespoň mobilní aplikaci.
- seed nikam nefotit, nepsat do počítače, neukládat na cloud. Seed patří na papír (kov, plech apod.). Tužku a papír ještě nikdo nehacknul.
