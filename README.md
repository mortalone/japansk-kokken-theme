# Japansk Kokken

Et roligt Home Assistant-theme med elfenbensfarvede, let gennemsigtige kort, salviegrønne ikoner og terracotta-accenter. Indeholder farvevariabler til Bubble Card og højdevariabler til det tilhørende køkkendashboard. Ingen blur eller baggrundsanimationer.

## Installation via HACS

1. Åbn HACS → menuen med tre prikker → Custom repositories / Brugerdefinerede repositories.
2. Indsæt `https://github.com/mortalone/japansk-kokken-theme`.
3. Vælg typen **Theme**, og tilføj repositoryet.
4. Find **Japansk Kokken** i HACS og vælg Download.
5. Sørg for, at `configuration.yaml` indeholder:

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

Hvis `frontend:` allerede findes, skal `themes:` indsættes under den eksisterende blok. Hvis denne konfiguration er ny, kontrollér konfigurationen og genstart Home Assistant. Ellers udfør `frontend.reload_themes` under Udviklerværktøjer → Handlinger. Genindlæs derefter browseren.

Vælg **Japansk Kokken** i brugerprofilen eller sæt følgende på din dashboardvisning:

```yaml
theme: Japansk Kokken
```

Det tilhørende køkkendashboard vælger allerede dette theme. Dashboard-YAML og baggrund installeres separat; HACS installerer kun theme-filen. Temaet har samme lyse farvepalette i både light og dark tilstand.

## Tilpasning

- `kitchen-photo-height`: fælles højde på de fire fotokort, standard `220px`.
- `kitchen-calendar-height`: kalenderhøjde, standard `320px`.
- `ha-card-background`: standardbaggrund på Home Assistant-kort.
- `kitchen-card-background`: kortbaggrund brugt af dashboardets Bubble-styles.
- `bubble-main-background-color`: generel Bubble Card-baggrund.

Højdevariablerne virker på kort, som refererer til dem via card-mod. Custom kort kan kræve egne CSS-tilpasninger. Theme alene tilføjer ingen custom kort.

Lokale ændringer i HACS' theme-fil kan overskrives ved opdatering. Gem derfor fælles ændringer i repositoryet eller brug en separat lokal kopi til personlige varianter.

## Opdatering

Temaet udgives med versionsnumre, fx v0.1.0, via GitHub Releases. Vælg en udgivet version i HACS; genindlæs themes og browseren efter opdatering. Maintainer: opdater RELEASE_NOTES.md og derefter VERSION (major.minor.patch). GitHub Actions opretter release og tag automatisk.

## Afprøvning

YAML og filplacering er kontrolleret. Temaet er endnu ikke afprøvet i den konkrete Home Assistant-installation eller målt på tabletten.
