# SMCI

**Generated** : 2026-11-05T01:24:46.479482+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $29.59  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot $29.59 (+3.6% vs entrée) · entrée $28.57 · stop $27.82 · T1 $29.82 · R/R 1.67  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.62% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +1.9 % ≠ (strike 32.0 − spot 29.59)/spot = +8.1 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -38 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-04 : 29.59 · ATR Wilder 2.48 (8.39 %)_
- **Swing** : plage **26.52 → 24.66** (-10.39 % a -16.66 % sous la cloture, 0.75 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 25.13-26.06 (A). stop INDICATIF 22.14 (-10.22 % sous le bas ; sous le support 23.38-24.19 (- 0,5 ATR)).
- **Deep** : plage **24.66 → 18.59** (-16.66 % a -37.19 % sous la cloture, 2.45 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 23.38-24.19 (A) ; 18.79-20.71 (A). stop INDICATIF 16.01 (-13.86 % sous le bas ; sous le support 17.25-17.25 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.94 ATR sous le plus haut 20 s., RSI(2) 16.6. Limite **28.35** (seance suivante), stop catastrophe 18.42, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 27.22-27.75 (B, -6.22 %) ; 25.13-26.06 (A, -11.93 %) ; 23.38-24.19 (A, -18.25 %) ; 18.79-20.71 (A, -30.01 %) ; 17.25-17.25 (C, -41.7 %)
- Resistances reelles au-dessus : 31.11-32.04 (A, 5.14 %) ; 32.58-33.64 (A, 10.1 %) ; 33.86-34.98 (A, 14.43 %) ; 35.36-36.4 (A, 19.5 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.14 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (16.0 %)** : le gap seul le franchit 0.399 % des séances (5 fois sur 1253).
   - exécution **8.657 pt plus bas** dans le cas TYPIQUE (médiane), 12.175 au p90, **13.051 au pire**
   - perte réelle **23.404 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 16.0 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0295 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.86 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4776** [0.4041 ; 0.5519] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3331** [0.285 ; 0.384] _(largeur 9.9 pt, n_eff 345.7)_
   - deep : **0.2557** [0.2119 ; 0.3036] _(largeur 9.2 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (30.7 pt), swing (38.1 pt), deep (42.9 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-7.98 %** | CVaR **-12.63 %** | vol 5.95 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 3.83 % contre 6.25 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.54 % vs -16.94 % si l'on extrapolait par √5 _(rapport 1.035 ; < 1 = le √5 surestime)_
- **β de baisse : 1.494** (β de hausse 1.1957, asymétrie 1.2495) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.807× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 28.3429 sur atr_grid (0.5 ATR, 4.215 %) — p(stop avant cible) 0.7397 [0.69 ; 0.78], R/R 8.151, perte reelle 4.802 % (gap inclus), CVaR 12.169 %, EV 0.4956 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.1259 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 4.7 % du temps (< 15 %) meme a 10 seances : le R/R de 8.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.740, borne haute 0.784 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 12.17 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 9 des 9 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 42.9 % de la queue et il ne reste que 45.01 EUR a partager. Prix du risque 0.03 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 12.644 %) — p(stop avant cible) 0.3167 [0.27 ; 0.37], R/R 2.759, perte reelle 14.185 % (gap inclus), EV 1.2645 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.16 % > budget 12.00 %
   - 🟢 support a 1.68 ATR (stop 16.579 %) — p(stop avant cible) 0.2218 [0.18 ; 0.27], R/R 2.12, perte reelle 18.459 % (gap inclus), EV 1.2797 % — **REFUSE**
      - refuse : cible atteinte seulement 6.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.32 % > budget 12.00 %
   - 🟢 support a 2.49 ATR (stop 23.44 %) — p(stop avant cible) 0.135 [0.10 ; 0.17], R/R 1.59, perte reelle 24.616 % (gap inclus), EV 1.2336 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.62 % > budget 12.00 %
   - 🟢 support a 4.05 ATR (stop 36.62 %) — p(stop avant cible) 0.0462 [0.03 ; 0.07], R/R 1.068, perte reelle 36.66 % (gap inclus), EV 0.8537 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.39 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 2.107 %) — p(stop avant cible) 0.8789 [0.84 ; 0.91], R/R 16.365, perte reelle 2.392 % (gap inclus), EV 0.4643 % — **REFUSE**
      - refuse : cible atteinte seulement 3.5 % du temps (< 15 %) meme a 10 seances : le R/R de 16.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.879, borne haute 0.910 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 4.215 %) — p(stop avant cible) 0.7397 [0.69 ; 0.78], R/R 8.151, perte reelle 4.802 % (gap inclus), EV 0.4956 % — **REFUSE**
      - refuse : cible atteinte seulement 4.7 % du temps (< 15 %) meme a 10 seances : le R/R de 8.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.740, borne haute 0.784 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.17 % > budget 12.00 %
   - ⚪ atr_grid a 0.75 ATR (stop 6.322 %) — p(stop avant cible) 0.6142 [0.56 ; 0.66], R/R 5.433, perte reelle 7.204 % (gap inclus), EV 0.5909 % — **REFUSE**
      - refuse : cible atteinte seulement 5.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.614, borne haute 0.664 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 16.56 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 8.429 %) — p(stop avant cible) 0.4816 [0.43 ; 0.53], R/R 3.997, perte reelle 9.793 % (gap inclus), EV 1.0052 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 4.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.85 % > budget 12.00 %
   - ⚪ atr_grid a 1.25 ATR (stop 10.537 %) — p(stop avant cible) 0.404 [0.35 ; 0.46], R/R 3.278, perte reelle 11.942 % (gap inclus), EV 1.0137 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 3.28 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 21.42 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 25.288 %) — p(stop avant cible) 0.1066 [0.08 ; 0.14], R/R 1.494, perte reelle 26.191 % (gap inclus), EV 1.2563 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.21 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 29.503 %) — p(stop avant cible) 0.0739 [0.05 ; 0.11], R/R 1.319, perte reelle 29.681 % (gap inclus), EV 1.0557 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.77 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 37.933 %) — p(stop avant cible) 0.0329 [0.02 ; 0.06], R/R 1.031, perte reelle 37.969 % (gap inclus), EV 0.9331 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.75 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 42.147 %) — p(stop avant cible) 0.0064 [0.00 ; 0.02], R/R 0.928, perte reelle 42.185 % (gap inclus), EV 1.0637 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.47 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 46.362 %) — p(stop avant cible) 0.002 [0.00 ; 0.01], R/R 0.83, perte reelle 47.175 % (gap inclus), EV 1.0575 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.55 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 50.577 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.705, perte reelle 55.543 % (gap inclus), EV 1.0524 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.71 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 54.792 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.703, perte reelle 55.664 % (gap inclus), EV 1.0522 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.71 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 59.006 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.663, perte reelle 59.006 % (gap inclus), EV 1.0604 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.66 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.53 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 63.221 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.619, perte reelle 63.221 % (gap inclus), EV 1.0604 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.53 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 67.436 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.58, perte reelle 67.436 % (gap inclus), EV 1.0604 % — **REFUSE**
      - refuse : cible atteinte seulement 6.8 % du temps (< 15 %) meme a 10 seances : le R/R de 0.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.53 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 29.59, ATR14 2.4943 (8.429 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.348 ATR = 2.933 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.421 % | 29.4653 | 90.84 % | 93.65 % | 94.95 % | 95.55 % | 96.75 % | 97.95 % |
| 0.1 ATR | 0.843 % | 29.3406 | 82.28 % | 87.6 % | 89.51 % | 91.51 % | 93.29 % | 95.28 % |
| 0.15 ATR | 1.264 % | 29.2159 | 75.23 % | 82.56 % | 85.37 % | 88.68 % | 91.06 % | 94.05 % |
| 0.2 ATR | 1.686 % | 29.0911 | 68.28 % | 77.72 % | 80.93 % | 86.25 % | 89.63 % | 92.81 % |
| 0.25 ATR | 2.107 % | 28.9664 | 62.13 % | 73.08 % | 76.69 % | 82.91 % | 87.7 % | 91.27 % |
| 0.35 ATR | 2.95 % | 28.717 | 49.75 % | 63.91 % | 70.23 % | 77.96 % | 83.64 % | 88.91 % |
| 0.5 ATR | 4.215 % | 28.3429 | 34.84 % | 50.3 % | 59.03 % | 69.46 % | 77.85 % | 84.5 % |
| 0.75 ATR | 6.322 % | 27.7193 | 17.42 % | 33.87 % | 43.79 % | 56.02 % | 67.58 % | 76.59 % |
| 1.0 ATR | 8.429 % | 27.0957 | 7.85 % | 21.98 % | 30.98 % | 44.49 % | 58.23 % | 70.02 % |
| 1.25 ATR | 10.537 % | 26.4721 | 3.73 % | 15.32 % | 22.91 % | 33.97 % | 49.09 % | 62.42 % |
| 1.5 ATR | 12.644 % | 25.8486 | 1.51 % | 9.78 % | 16.75 % | 26.49 % | 42.58 % | 56.06 % |
| 2.0 ATR | 16.859 % | 24.6014 | 0.3 % | 3.63 % | 8.68 % | 16.58 % | 30.69 % | 44.87 % |
| 2.5 ATR | 21.074 % | 23.3543 | 0.2 % | 1.51 % | 4.44 % | 10.01 % | 20.22 % | 32.96 % |
| 3.0 ATR | 25.288 % | 22.1071 | 0.2 % | 1.21 % | 2.62 % | 5.97 % | 14.74 % | 25.15 % |
| 4.0 ATR | 33.718 % | 19.6129 | 0.0 % | 0.6 % | 1.51 % | 2.83 % | 8.13 % | 15.3 % |
| 6.0 ATR | 50.577 % | 14.6243 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.65 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.51 ATR | 0.58 ATR | 0.77 ATR | 0.94 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.28 ATR | 0.65 ATR | 0.73 ATR | 0.96 ATR | 1.19 ATR | 1.37 ATR | 1.92 ATR | 2.43 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.99 ATR | 1.28 ATR | 1.57 ATR | 1.83 ATR | 2.50 ATR | 3.31 ATR |
| **10 s.** | 0.57 ATR | 1.23 ATR | 1.41 ATR | 1.90 ATR | 2.27 ATR | 2.52 ATR | 3.72 ATR | 5.03 ATR |
| **20 s.** | 0.81 ATR | 1.77 ATR | 1.99 ATR | 2.50 ATR | 3.02 ATR | 3.52 ATR | 5.10 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.398 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 38.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.581–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.322 %, prix 27.7193), p(touche) 33.87 % (en stress 88.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 29.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.73–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.322 %, prix 27.7193), p(touche) 43.79 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.989–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.429 %, prix 27.0959), p(touche) 44.49 % (en stress 93.94 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.407–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (12.644 %, prix 25.8486), p(touche) 42.58 % (en stress 96.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.994–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (16.859 %, prix 24.6014), p(touche) 44.87 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.013 | EV/share : $-0.010 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 27 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 46.6 | bear 5.0 | side 48.4  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.441% → cible +4.365% / stop −2.619%, p_fill 37%, n_eff≈38.2) : P(cible|rempli) **19%** · **EV/risk +0.052** (×p_fill ; si rempli +0.36% du capital)
  - **swing** (entrée dip −7.57% → cible +16.506% / stop −9.12%, p_fill 21%, n_eff≈23.9) : P(cible|rempli) **25%** · **EV/risk -0.027** (×p_fill ; si rempli -1.18% du capital)
  - **deep** (entrée dip −11.707% → cible +21.955% / stop −14.32%, p_fill 16%, n_eff≈18.3) : P(cible|rempli) **20%** · **EV/risk -0.046** (×p_fill ; si rempli -4.21% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→74% · +2.0%→57% · +3.0%→40% · +5.0%→22% · +8.0%→8%
- Range intraday médian 5.72% (p90 9.37%) · excursion haute méd. +2.42% / basse méd. −2.68%
- Profil de vol intra : ouverture 3.884% vs midi 1.151% vs clôture 1.47% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.077)_ ; drift intra méd. -0.659% ; recovery-V 28%
- **σ réalisé intraday** 3.524% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 60% / whipsaw 24%
- POC intraday (dernière séance, temps-au-prix) : 33.7346 (VA 33.3821–34.0871 ; dernier close 32.95)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 74% · **stop −4.61%** sous le fill (sous le bruit) · cible +2.15% · R/R 0.47 (high win-rate)
- Gaps overnight (n=159) : méd. 0.0% · baisse 50% (gap-down >1% 38% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.11% (p90 −2.79%) · haut méd +0.93% · range méd 2.16%
- Excursion ouverture 15min (n=160) : bas méd −1.42% (p90 −3.55%) · haut méd +1.01% · range méd 2.85%
- Excursion ouverture 30min (n=160) : bas méd −1.65% (p90 −3.98%) · haut méd +1.23% · range méd 3.58%
- Excursion ouverture 60min (n=160) : bas méd −1.91% (p90 −4.46%) · haut méd +1.48% · range méd 4.31%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 32.94 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 73% (116/159) · gap 42% · délai 0.0min · rebond 49% (64/116) (MFE +0.98%)
   - −1.0% : fill 30min 58% · séance 70% (109/159) · gap 38% · délai 0.0min · rebond 51% (60/109) (MFE +1.09%)
   - −1.5% : fill 30min 52% · séance 66% (100/159) · gap 28% · délai 0.0min · rebond 56% (62/100) (MFE +1.13%)
   - −2.0% : fill 30min 47% · séance 59% (87/159) · gap 23% · délai 0.1min · rebond 56% (54/87) (MFE +1.2%)
   - −3.0% : fill 30min 34% · séance 48% (73/159) · gap 11% · délai 2.7min · rebond 62% (43/73) (MFE +1.34%)
   - −4.0% : fill 30min 21% · séance 35% (54/159) · gap 5% · délai 12.5min · rebond 72% (36/54) (MFE +1.72%)
   - −5.0% : fill 30min 15% · séance 29% (44/159) · gap 2% · délai 21.5min · rebond 74% (31/44) (MFE +2.15%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.69% (p90 −2.8%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.84%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.25%) → stop au-delà de −1.73% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=876 jambes) : jambe baissière méd −1.19% (p90 −2.78%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (70 séances) :
      · −1.0% : fill 98% (68/70) · rebond 39% (32/68)
      · −2.0% : fill 96% (64/70) · rebond 57% (37/64)
      · −3.0% : fill 86% (58/70) · rebond 60% (33/58)
      · −4.0% : fill 64% (44/70) · rebond 70% (29/44)
      · −5.0% : fill 53% (36/70) · rebond 71% (24/36)
   - **flat** (14 séances) :
      · −1.0% : fill 90% (13/14) · rebond 84% (10/13)
      · −2.0% : fill 57% (6/14) · rebond 47% (4/6)
      · −3.0% : fill 20% (3/14) · rebond 43% (2/3)
      · −4.0% : fill 7% (1/14) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/14) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 36% (28/75) · rebond 66% (18/28)
      · −2.0% : fill 21% (17/75) · rebond 58% (13/17)
      · −3.0% : fill 13% (12/75) · rebond 78% (8/12)
      · −4.0% : fill 11% (9/75) · rebond 81% (6/9)
      · −5.0% : fill 10% (8/75) · rebond 91% (7/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 67% si les 15 1res min sont vertes (78 cas) · 24% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 83% si début vert vs 11% si rouge (base 43% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=79) : tient le vert **83%** · continue >prix actuel 59% ; creux résiduel méd -1.33% (q20 -2.94%) → **SL/trailing à −2.94%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +2.72% → **scale +1.67% / runner +2.72%**, sortie à la clôture
  - **si ROUGE au coude** (n=81) : edge inversé — récupère vert seulement **11%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.93%** (au-delà de la MAE q10 -3.93%), cible rebond +1.31% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.17% .. +4.1%] · haut q95 +5.04% · bas q05 -5.27%
   - 60min (n=160) : retour [-4.12% .. +4.96%] · haut q95 +6.21% · bas q05 -5.43%
   - 2h (n=160) : retour [-4.55% .. +5.52%] · haut q95 +7.12% · bas q05 -5.93%
   - 4h (n=160) : retour [-4.91% .. +6.39%] · haut q95 +7.24% · bas q05 -6.41%
   - 6h (n=160) : retour [-5.14% .. +6.41%] · haut q95 +7.8% · bas q05 -6.61%
   - session (n=160) : retour [-6.33% .. +6.37%] · haut q95 +7.95% · bas q05 -6.95%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.59%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.54 · part idiosyncratique 0.46
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 37.2  _(momentum baissier)_
- **ADX** : 21.3  _(pas de tendance nette)_
- **MACD** : hist -0.434  _(pas de croisement recent)_
- **BB** : %B 0.15 · largeur 42.1%
- **ATR** : 2.49 (77.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.293  _(distribution)_
- **Vol ratio** : 2.06  _(volume au-dessus de la moyenne)_
- **Choppiness** : 55.6  _(transition)_
- **MA** : MA20 34.77 · MA50 37.84 · MA200 32.66  _(prix < MA20)_
- **Dist MA** : MA20 -14.9% · MA50 -21.8% · MA200 -9.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (731361 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
