# Provenance (migration Lepton, étape 6 ; chantier environnement de développement Lepton, ENV-47)

`cmsis_device_f7` tag `v1.2.10` = commit `2352e888e821aa0f4fe549bd5ea81d29c67a3222`, sous-module
de STM32CubeF7 v1.17.4 (amont https://github.com/STMicroelectronics/cmsis_device_f7), Apache-2.0
(`LICENSE.md`). Code tiers non modifié (D1a).

Depuis ENV-47, ce répertoire n'est plus une copie : scion **projette** les fichiers du dépôt tiers
(clé `tiers@cmsis-device-f7`, déclarée dans `scion/.scion/` du greffon `family-stm32f7xx`, qui la
porte). Source : miroir de conservation https://github.com/lepton-distribution/mirror-cmsis_device_f7.git
(tenu par `scion mirror-sync`) ; clone partiel sous `<rootstock>/depots/tiers/cmsis-device-f7/v1.2.10`,
au commit du tag. Fichiers projetés : `Include/stm32f7xx.h`, `Include/system_stm32f7xx.h`,
`Include/stm32f746xx.h` (STM32F746G-DISCO), `LICENSE.md`, `README.md` ; les autres puces et les
modèles `Source/Templates` (démarrage, éditions de liens IAR/ARM/GCC) ne sont pas projetés. Pour une
autre puce : ajouter son en-tête au motif de `scion/.scion/.scion.projections`. Seul ce fichier
appartient au greffon.

Contenu : identique à `v1.2.10` par construction (liens vers le clone tiers, que la greffe refuse
hors de son commit épinglé ou modifié). Exige scion ≥ 0.6.1.0.
