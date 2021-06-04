## Tipy a triky

1. Seed nepatří do onlinu 

   Seed, ani privátní klíče nikam nepíšeme. Seed je vašich 12/24 slov, u toho je to jasné. Z něj se generují privátní klíče a každá adresa má svůj, pomocí kterého utrácíme zůstatek z adresy. I když je to klíč jen k jedné adrese, tak pokud byste někde uveřejnili svůj rozšířený veřejný klíč (xpub, ypub, zpub), je možné prostředky odcizit i z ostatních adres. Většina peněženek vám vaše privátní klíče ani neukáže, což je správně, práve z tohoto důvodu. Operace s privátními klíči nechme na peněžence a nevymýšlejme kličky. Pokud se nebudete snažit obejít např. Trezor Suite nebo Ledger Live, rozhodně vám nehrozí nebezpečí, protože vám vaše privátní klíče ani neukážou.
2. Passphrase nesmíte zapomenout
   
   Passphrase - pokud používáte passphrase, tak vězte, není to jen "heslo". Passphrase totiž úplně změní (vytvoří úplně jiné) adresy a klíče, než které vám peněženka vygeneruje bez passphrase. Ty "obyčejné", bez passphrase, nikam nezminí, ani prostředky z nich. Jen jsou to úplně oddělené účty a možná bych to mohl přirovnat k dvěma rozdílným seedům (prvních 12/24 slov je společných, a liší se 25.slovem - passphrase). Tzn. že pokud si pošlete prostředky na účet pod passphrase, odpojíte peněženku a přihlásíte se do účtu bez passphrase, tak tam uvidíte nulový zůstatek. Nelekejte se, jen si znovu přihlašte a zadejte passphrase. Vaše prostředky jsou v bezepčí. **Bez passphrase se ale k prostředkům nedostanete, i když znáte seed. Passphrase si někam poznamenejte, nespoléhejte na to, že si ji zapamatujete**.
3. Používejte "bc1" adresy

   Používejte adresy, co začínají "bc1", případně "3". Ušetříte tím spousty satoshi na poplatcích. Adresy s "1" na začátku nechte Satoshimu, ten si může dovolit zaplatit o pár satů navíc :)
4. Konsolidace UTXO

   Jednou za čas se doporučuje "zkonsolidovat UTXO". UTXO jsou zjednodušeně zůstatky na adresách. Čím víc zůstatků (UTXO), tím dražší je výsledná transakce. Pokud převedete všechny prostředky najednou na novou (nejlépe "bc1") adresu, vytvoříte tím pouze 1 zůstatek, který můžete utratit bez problémů za daleko menší poplatek.
5. Brain wallet? Nikdy!

   Pokud by vás napadlo si slova seedu generovat nějak cíleně, nedělejte to prosím. Ač je možné vytvořit si vlastní seed (až na poslední slovo), je to extrémně nebezpečné, protože není zajištěna dostatečná náhodnost a někdo by se jenoduše řečeno prostě mohl trefit do stejného a pak máte problém. Seed vám nejlépe vygeneruje peněženka, ať už softwarová nebo hardwarová.
6. Visící transakce, co se s ní stane?
   
   Pokud podceníte poplatek na transakci, je možné tento poplatek ještě navýšit v peněžence, pokud to podporuje a "připlatit" si tak za rychlost (vyslaná transakce musí podporovat RBF). Pokud ale vaše transakce nepodporuje RBF, nezoufejte. Buď projde časem a nebo se z vaší původní adresy bitcoiny vůbec nedostanou (uzly ji zapomenou, defaultně po 14 dnech, pokud peněženka aktivně nebroadcastuje transakci znovu zpět do sítě). Rozhodně ale nezmizí nikde ve vzduchoprázdnu.
7. Nevymýšlejte kličky a ohejbáky

   Never attempt a "DIY" security scheme that deviates in any way from the best practice recommendation in Storing the Mnemonic Safely. Do not cut your mnemonic in half, make screenshots, store on USB drives or cloud drives, encrypt it, or try any other non-standard method. You will tip the balance in such a way as to risk permanent loss or theft. Many people have lost funds, not from theft but because they tried a non-standard solution without having the expertise to balance the risks involved. The best practice recommendation is carefully balanced by experts and suitable for the vast majority of users.
8. Instalujte opatrně, ověřujte

   Always exercise great care when installing software on any device. There are many fake cryptocurrency wallets that will not only steal your money but might also compromise all other applications on your device.
