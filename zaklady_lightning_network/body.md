## 1. Co je Lightning network
Připadají vám bitcoinové transakce drahé? Někdo by řekl, že je to špatně, ale princip ukládání dat v bitcoinové síti je na jednu stranu ohromně bezpečný, ale na druhou stranu extrémně nákladný. Bitcoinové on-chain transakce (transakce na základní vrstvě, posílání z adresy na adresu) budou tedy časem dražší a dražší, jak poroste zájem o síť.

Řešením tohoto problému by měla být právě Lightning network (zkráceně LN, případně Blesková síť). Pro začátek si ji můžeme představit jako např. lístek v kavárně. Pokud jdu do kavárny a dám si kávu, vodu, případně desert, neplatím za každou položku zvlášť, ale na konci mé návštěvy přijde obsluha, sečte mi účet a já zaplatím pouze jednou. Místo tedy 3 transakcí jsem provedl pouze jednu. Lightning network funguje stejně, akorát si nejdřív peníze "nabiji" a poté je můžu utrácet, aniž bych zapisoval do blockchainu (drahé transakce), jakmile budu chtít srovnat účty, zase si je "vyberu" zpět na svoji BTC adresu. 

Nabití i vybrání je ale stejně dvě transakce do blockchainu, snažím se tedy nabít adekvátní množství peněz, které budu chtít utrácet a potom mi už stačí jen uskutečnit více než dvě transakce, aby se mi tato "investice" vyplatila. Těch transakcí můžu provést třeba tisíc a bude mě to stát vždy jen pár satoshi na poplatku (pro uzly, které mi transakci zpracují). Mohu tedy teď posílat a platit, aniž bych se staral o aktuální stav bitcoinové sítě.

V názvosloví Lightning network se tomuto "nabití" říká otevření platebního kanálu a "výběru" se říká uzavření platebního kanálu. Tohle za vás ale většinou vyřeší většina peněženek, takže nemusíte úplně znát celou teorii za Lightning network. Pokud chcete občas poslat nebo přimout nějaké satoshi, stačí si tedy stáhnout peněženku Phonix a dobít si ji nějakým obnosem (zaplatíte provozovateli asi 1% poplatek + 3000 satoshi za otevření kanálu). Tímto kanálem potom můžete posílat ven z peněženky. Doporučuji si otevřít větší kanál, abyste zaplatili jen jednou. Pokud bude chtít posílat platby třeba po 10,000 satoshi, nemá cenu otevírat kanál 20,000 satoshi, protože ho vyčerpáte už dvěma platbami. Raději tedy nabít třeba 1,000,000 satoshi a potom si užívat výhod Lightning network dlouhodobě.

K tomu, abyste mohli přímat stejným kanálem, musíte nejdřív z tohoto kanálu něco utratit. Zní to trochu nelogicky, ale přestavte si to jako dvě nádoby, z nichž jedna je naplněná po okraj vodou (vaše dobitá peněženka) a stejně velká nádoba je hned vedle, úplně prázdná. Můžeme mezi nimi v podstatě zadarmo čerpat tam a zpět. Z prázdné nádoby není co čerpat. Nejdříve musíme vyčerpat vodu z plné (z peněženky) do prázdné (kamarádovi, eshopu, poslání donejtu apod). Pokud si uvolním ze své nádoby (peněženky) dost, může mi opačným směrem začít také prodoudit voda (mohu příjmat transakce). Je to jedna z aktuálních "slabin" Lightning network, ale časem se plánuje i oboustranné plnění kanálů (obě nádoby budou třeba z poloviny plné), bude tedy možné hned jak posílat, tak příjmat satoshi. Pokud budu chtít přijmout větší transakci, než je kapacita kanálu, peněženka si nechá otevřít nový, větší kanál. Děje se to automaticky, vlastně to ani nepoznáte, pokud si nevšimnete, že jednou vám přišlo o třeba 3000 satoshi a k tomu 1% z celé částky méně, než jste čekali (to indikuje vznik nového kanálu) - někde na pozadí totiž proběhne on-chain platba, nikdo vás nechce oškubat, jen je třeba reálně tuhle kapacitu někde alokovat, což stojí prostředky.
___

##2. Pár základních pojmů

###Blockchain
Distribuovaná kniha všech transakcí, které síť zpracovává. Bitcoin je tedy systém, jehož produktem je blockchain. Lightning network nepracuje na bázi blockchainu, je to síť spoléhající na externí (bitcoinový) blockchain, aby byla dostatečně zabezpěčená.

###Digitální podpis
Digitální podpis je způsob, jak matematicky ověřit pravost zprávy nebo jiných dokumentů. Pokud sedí podpis, můžeme si být jistí, že zprávu poslal ten správný odesílatel a že nám nikdo nepodvrhnul její obsah nebo ji nějak nezměnil. Ani odesílatel už potom nemůže popřít, že ji někdy podepsal.

### Uzel (Node)
A computer that participates in a network. A Lightning node is a computer that participates in the Lightning Network. A Bitcoin node is a computer that participates in the Bitcoin Network. Typically a Lightning Network user will run a Lightning node and a Bitcoin node.
Počítač, který spoluzodpovídá za síť. Lightningový uzel se tedy podílí na Lightningové síti, bitcoinový uzel zase na bitcoinové síti (která produkuje blockchain). Typicky každý Lightningový uzel je zároveň i bitcoinovým uzlem.

###On-Chain vs. Off-Chain transakce
A payment is "on-chain" if it is recorded as a transaction on the Bitcoin (or other underlying) blockchain. Payments sent via payment channels between Lightning nodes, and which are not visible in the underlying blockchain, are called "off-chain" payments. Usually in the Lightning Network, the only on-chain transactions are those used to open and close a Lightning payment channel.
Platby "on-chain" jsou zapsány na samotný bitcoinový blockchain. Platby mezi lightningovými uzly nejsou zaznamenávány na tento blockchain a říká se jim tak "off-chain" platby. Jediné "on-chain" platby v lightningové síti jsou otevření a uzavření platebního kanálu.

###Platba
When value is exchanged on the Lightning Network, we call this a "payment" as compared to a "transaction" on the Bitcoin blockchain.
Poslání hodnoty přes lightningovou síť nazýváme "platba", kdežto platba na blockchainu se nazývá "transakce".

###Platební kanál
A financial relationship between two nodes on the Lightning Network, typically implemented by multi-signature Bitcoin transactions that share control over bitcoin between the two Lightning nodes.
Platební vztah mezi dvěma uzly v lightningové síti. Typicky je to bitcoinová transakce podepsaná dvěma uzly, které oba spoluzodpovídají za bitcoiny mezi těmito dvěma uzly.

###Směrování vs. posílání
Unlike Bitcoin where transactions are "sent" by broadcasting them to everyone, Lightning is a routed network where payments are "routed" across one or more payment channels following a path from sender to recipient.
Mimo normálního poslání platby dovoluje lightningová síť i směrovat platby jiných. Uzel tak může sloužit jen ke zpracování platby pro další účastníky v síti, za což si vezme tento uzel drobný poplatek.

###Transakce
A data structure that records the transfer of control over some funds (e.g. some bitcoin). The Lightning Network relies on Bitcoin transactions (or those of another blockchain) to track control of funds.
Lightningové platby spoléhají na transakce v bitcoinové síti, které jsou extrémně zabezpečené a garantují tak bezpečnosti pro platby na lightningové síti.

