# Schéma sítě
![Zadání](./img/img1.png)
# Postup:
**1)** Polož všechny routery (1841), server a PC
> **Poznámka:** V routerech, které vedou do PC a Serveru je nutné použít modul **WIC-1-ENET**

**2)** Nastav routerům IP adresu, serveru a PC pak ***default gateway***

> **Default Gateway** = IP adresa, která je přiřazená portu, kterým PC zapojujete do routeru, většinou tedy `Eth0/0/0` nebo `Eth0/1/0`

**3)** Nastav na routerech OSPF, na Routeru vedoucího do serveru pak default gateway (bude totiž používán jako hlavní brána k "Internetu"

> **Poznámka:** OSPF nastavíme všude kromě propojení PC se serverem, tam později nastavíme NAT

**4)** Portu vedoucímu do PC nastavíme **pasivní rozhraní** = s žádným dalším počítačem napojeným tímhle portem nepůjde router nastavovat

**5)** Na routeru vedoucím do serveru nastavíme NAT

**6)** Na routeru vedoucím do serveru nastavíme SSH, zabezpečíme přihlášení do routeru a příkaz `enable` opatříme heslem
