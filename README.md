# Kaarre – ohjelmistopäivitykset

Tämä repositorio jakaa **Kaarre**-navigointinäytön (ESP32-2424S012C) ja sen Android-sovelluksen
valmiit versiot. Lataussivu: https://paleppp.github.io/kaarre-ota/

Kaarre-sovellus tarkistaa päivitykset osoitteesta

    https://paleppp.github.io/kaarre-ota/manifest.json

ja päivittää sekä itsensä että näytön (Bluetoothin kautta).

## Turvallisuus

- Näytön laiteohjelmisto on **allekirjoitettu** (ECDSA P-256). Näyttö asentaa vain tiedoston,
  jonka allekirjoitus täsmää laitteeseen käännettyyn julkiseen avaimeen ja jonka SHA-256 vastaa manifestia.
- Jos uusi versio ei käynnisty kunnolla, näyttö palaa automaattisesti edelliseen versioon.
- Sovellus tarkistaa ladatun APK:n SHA-256:n, ja Android hyväksyy päivityksen vain samalla avaimella allekirjoitettuna.

## Sisältö

| Polku | |
|---|---|
| `manifest.json` | uusimmat versiot (sovellus + näyttö) |
| `firmware/` | näytön laiteohjelmistot |
| `app/` | Android-sovelluksen APK:t (`kaarre-latest.apk` = uusin) |
| `history.json` | muutoshistoria |
