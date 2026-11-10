# Provenance (migration Lepton, étape 6 ; chantier environnement de développement Lepton, ENV-47)

`stm32f7xx-hal-driver` tag `v1.3.3` = commit `e1446fa12ffda80ea1016faf349e45b2047fff12`,
sous-module de STM32CubeF7 v1.17.4 (amont https://github.com/STMicroelectronics/stm32f7xx-hal-driver),
BSD-3-Clause (`LICENSE.md`). Code tiers non modifié (D1a).

Depuis ENV-47, ce répertoire n'est plus une copie : scion **projette** les fichiers du dépôt tiers
(clé `tiers@stm32f7xx-hal-driver`, déclarée dans `scion/.scion/` de ce greffon, qui la porte).
Source : miroir de conservation https://github.com/lepton-distribution/mirror-stm32f7xx-hal-driver.git
(tenu par `scion mirror-sync`, `scion/.scion/.scion.mirrors`) ; clone partiel sous
`<rootstock>/depots/tiers/stm32f7xx-hal-driver/v1.3.3`, au commit du tag. Fichiers projetés :
`Inc/**`, `Src/**` (`Legacy/` et modèles `*_template.*` compris), `LICENSE.md`, `README.md`
(196 fichiers) ; notes de version HTML, `_htmresc/`, `.github/` et fichiers de contribution non
projetés. Seul ce fichier appartient au greffon. Configuration (`stm32f7xx_hal_conf.h`) fournie par
le BSP de la carte.

Contenu : identique à `v1.3.3` par construction (liens vers le clone tiers, que la greffe refuse
hors de son commit épinglé ou modifié). Exige scion ≥ 0.6.1.0.
Mise à jour : changer la version de la clé dans `scion/.scion/` (`.scion.sources.list`,
`.scion.ramifications`), avec le CMSIS device du même couple STM32CubeF7
(`kernel/core/ucore/cmsis-5/Device/ST/STM32F7xx/`), puis regreffer.
