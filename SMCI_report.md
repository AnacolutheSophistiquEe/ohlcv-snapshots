# SMCI

**Generated** : 2026-11-06T01:23:30.452919+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : volatilité réalisée 5.2 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 1/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $27.09  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot $27.09 (+1.5% vs entrée) · entrée $26.70 · stop $25.95 · T1 $27.95 · R/R 1.67  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.81% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +8.1 % ≠ (strike 32.0 − spot 27.09)/spot = +18.1 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -55 % hors [0,100] (R² max 0.75). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-05 : 27.09 · ATR Wilder 2.57 (9.5 %)_
- **Swing** : plage **23.9 → 21.95** (-11.79 % a -18.99 % sous la cloture, 0.76 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 23.38-24.19 (A). stop INDICATIF 17.5 (-20.25 % sous le bas ; sous le support 18.79-20.71 (- 0,5 ATR)).
- **Deep** : plage **21.95 → 15.63** (-18.99 % a -42.31 % sous la cloture, 2.45 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 18.79-20.71 (A) ; 17.25-17.25 (C). stop INDICATIF 13.05 (-16.47 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.35 ATR sous le plus haut 20 s., RSI(2) 6.5. Limite **25.8** (seance suivante), stop catastrophe 15.5, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 25.13-26.06 (A, -3.8 %) ; 23.38-24.19 (A, -10.71 %) ; 18.79-20.71 (A, -23.55 %) ; 17.25-17.25 (C, -36.32 %)
- Resistances reelles au-dessus : 28.61-29.85 (A, 5.61 %) ; 29.9-31.11 (A, 10.37 %) ; 31.84-33.07 (A, 17.53 %) ; 33.51-34.51 (A, 23.7 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.22 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (12.44 %)** : le gap seul le franchit 0.718 % des séances (9 fois sur 1253).
   - exécution **4.902 pt plus bas** dans le cas TYPIQUE (médiane), 14.858 au p90, **16.611 au pire**
   - perte réelle **19.221 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 12.44 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0487 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 9 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.86 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4547** [0.3818 ; 0.5291] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3029** [0.2563 ; 0.3528] _(largeur 9.7 pt, n_eff 345.7)_
   - deep : **0.2586** [0.2146 ; 0.3066] _(largeur 9.2 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 960 séances)** : VaR **-8.14 %** | CVaR **-12.87 %** | vol 6.06 %/j
   - _fenêtre arrêtée : rupture de regime a 1020 seances en arriere (volatilite 3.91 % contre 6.27 % aujourd'hui, rapport 0.62)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.79 % vs -17.03 % si l'on extrapolait par √5 _(rapport 1.045 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5074** (β de hausse 1.1896, asymétrie 1.2672) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.649× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 26.4641 sur atr_grid (0.25 ATR, 2.31 %) — p(stop avant cible) 0.8718 [0.83 ; 0.90], R/R 20.007, perte reelle 2.598 % (gap inclus), CVaR 7.255 %, EV 0.4198 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 2.1004 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 20.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.872, borne haute 0.904 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 7.25 % > budget 4.68 %
- Budget de queue : **4.68 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.122 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 37.9 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 0.67 ATR (stop 9.094 %) — p(stop avant cible) 0.4632 [0.41 ; 0.52], R/R 4.997, perte reelle 10.401 % (gap inclus), EV 0.9367 % — **REFUSE**
      - refuse : cible atteinte seulement 2.8 % du temps (< 15 %) meme a 10 seances : le R/R de 5.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 20.90 % > budget 4.68 %
   - ⚪ atr_based a 1.5 ATR (stop 13.863 %) — p(stop avant cible) 0.2739 [0.23 ; 0.32], R/R 3.341, perte reelle 15.555 % (gap inclus), EV 1.3272 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 3.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 22.99 % > budget 4.68 %
   - 🟢 support a 1.48 ATR (stop 16.588 %) — p(stop avant cible) 0.2202 [0.18 ; 0.27], R/R 2.814, perte reelle 18.468 % (gap inclus), EV 1.2891 % — **REFUSE**
      - refuse : cible atteinte seulement 2.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.30 % > budget 4.68 %
   - 🟢 support a 3.04 ATR (stop 30.984 %) — p(stop avant cible) 0.0639 [0.04 ; 0.09], R/R 1.672, perte reelle 31.087 % (gap inclus), EV 1.0567 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.12 % > budget 4.68 %
   - ⚪ atr_grid a 0.25 ATR (stop 2.31 %) — p(stop avant cible) 0.8718 [0.83 ; 0.90], R/R 20.007, perte reelle 2.598 % (gap inclus), EV 0.4198 % — **REFUSE**
      - refuse : cible atteinte seulement 1.4 % du temps (< 15 %) meme a 10 seances : le R/R de 20.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.872, borne haute 0.904 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 7.25 % > budget 4.68 %
   - ⚪ atr_grid a 2.0 ATR (stop 18.483 %) — p(stop avant cible) 0.181 [0.14 ; 0.22], R/R 2.537, perte reelle 20.483 % (gap inclus), EV 1.3683 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.54 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.82 % > budget 4.68 %
   - ⚪ atr_grid a 2.25 ATR (stop 20.794 %) — p(stop avant cible) 0.1552 [0.12 ; 0.20], R/R 2.336, perte reelle 22.248 % (gap inclus), EV 1.3806 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.34 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.23 % > budget 4.68 %
   - ⚪ atr_grid a 2.5 ATR (stop 23.104 %) — p(stop avant cible) 0.1394 [0.11 ; 0.18], R/R 2.146, perte reelle 24.218 % (gap inclus), EV 1.2777 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.21 % > budget 4.68 %
   - ⚪ atr_grid a 2.75 ATR (stop 25.415 %) — p(stop avant cible) 0.1046 [0.08 ; 0.14], R/R 1.977, perte reelle 26.29 % (gap inclus), EV 1.2669 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.25 % > budget 4.68 %
   - ⚪ atr_grid a 3.5 ATR (stop 32.346 %) — p(stop avant cible) 0.0601 [0.04 ; 0.09], R/R 1.6, perte reelle 32.488 % (gap inclus), EV 0.9886 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.52 % > budget 4.68 %
   - ⚪ atr_grid a 4.0 ATR (stop 36.967 %) — p(stop avant cible) 0.0423 [0.02 ; 0.07], R/R 1.405, perte reelle 36.998 % (gap inclus), EV 0.9212 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.23 % > budget 4.68 %
   - ⚪ atr_grid a 4.5 ATR (stop 41.588 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 1.25, perte reelle 41.588 % (gap inclus), EV 1.0836 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.38 % > budget 4.68 %
   - ⚪ atr_grid a 5.0 ATR (stop 46.208 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 1.11, perte reelle 46.835 % (gap inclus), EV 1.0801 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.11 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.11 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.50 % > budget 4.68 %
   - ⚪ atr_grid a 5.5 ATR (stop 50.829 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.936, perte reelle 55.543 % (gap inclus), EV 1.0697 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.94 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.67 % > budget 4.68 %
   - ⚪ atr_grid a 6.0 ATR (stop 55.45 %) — p(stop avant cible) 0.0013 [0.00 ; 0.01], R/R 0.93, perte reelle 55.867 % (gap inclus), EV 1.0693 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.68 % > budget 4.68 %
   - ⚪ atr_grid a 6.5 ATR (stop 60.071 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.865, perte reelle 60.071 % (gap inclus), EV 1.0782 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.87 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.87 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.50 % > budget 4.68 %
   - ⚪ atr_grid a 7.0 ATR (stop 64.692 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.803, perte reelle 64.692 % (gap inclus), EV 1.0782 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.50 % > budget 4.68 %
   - ⚪ atr_grid a 7.5 ATR (stop 69.313 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.75, perte reelle 69.313 % (gap inclus), EV 1.0782 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.75 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.75 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.50 % > budget 4.68 %
   - ⚪ atr_grid a 8.0 ATR (stop 73.933 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.703, perte reelle 73.933 % (gap inclus), EV 1.0782 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.50 % > budget 4.68 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 27.09, ATR14 2.5036 (9.242 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.349 ATR = 3.225 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.462 % | 26.9648 | 90.94 % | 93.75 % | 95.06 % | 95.65 % | 96.85 % | 97.95 % |
| 0.1 ATR | 0.924 % | 26.8396 | 82.38 % | 87.7 % | 89.61 % | 91.61 % | 93.39 % | 95.28 % |
| 0.15 ATR | 1.386 % | 26.7145 | 75.33 % | 82.66 % | 85.47 % | 88.78 % | 91.16 % | 94.05 % |
| 0.2 ATR | 1.848 % | 26.5893 | 68.38 % | 77.82 % | 81.03 % | 86.35 % | 89.74 % | 92.81 % |
| 0.25 ATR | 2.31 % | 26.4641 | 62.24 % | 73.19 % | 76.79 % | 83.01 % | 87.8 % | 91.27 % |
| 0.35 ATR | 3.235 % | 26.2138 | 49.85 % | 64.01 % | 70.33 % | 78.06 % | 83.74 % | 88.91 % |
| 0.5 ATR | 4.621 % | 25.8382 | 34.94 % | 50.4 % | 59.13 % | 69.57 % | 77.95 % | 84.5 % |
| 0.75 ATR | 6.931 % | 25.2123 | 17.52 % | 33.87 % | 43.9 % | 56.12 % | 67.68 % | 76.69 % |
| 1.0 ATR | 9.242 % | 24.5864 | 7.85 % | 21.98 % | 31.08 % | 44.59 % | 58.33 % | 70.12 % |
| 1.25 ATR | 11.552 % | 23.9605 | 3.73 % | 15.32 % | 23.01 % | 34.07 % | 49.19 % | 62.53 % |
| 1.5 ATR | 13.863 % | 23.3346 | 1.51 % | 9.78 % | 16.85 % | 26.59 % | 42.68 % | 56.16 % |
| 2.0 ATR | 18.483 % | 22.0829 | 0.3 % | 3.63 % | 8.68 % | 16.68 % | 30.69 % | 44.97 % |
| 2.5 ATR | 23.104 % | 20.8311 | 0.2 % | 1.51 % | 4.44 % | 10.01 % | 20.22 % | 33.06 % |
| 3.0 ATR | 27.725 % | 19.5793 | 0.2 % | 1.21 % | 2.62 % | 5.97 % | 14.74 % | 25.26 % |
| 4.0 ATR | 36.967 % | 17.0757 | 0.0 % | 0.6 % | 1.51 % | 2.83 % | 8.13 % | 15.4 % |
| 6.0 ATR | 55.45 % | 12.0686 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.75 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.35 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.51 ATR | 0.58 ATR | 0.77 ATR | 0.94 ATR | 1.07 ATR | 1.49 ATR | 1.89 ATR |
| **3 s.** | 0.28 ATR | 0.65 ATR | 0.73 ATR | 0.96 ATR | 1.19 ATR | 1.37 ATR | 1.92 ATR | 2.43 ATR |
| **5 s.** | 0.40 ATR | 0.88 ATR | 0.99 ATR | 1.29 ATR | 1.58 ATR | 1.83 ATR | 2.50 ATR | 3.31 ATR |
| **10 s.** | 0.57 ATR | 1.23 ATR | 1.41 ATR | 1.90 ATR | 2.27 ATR | 2.52 ATR | 3.72 ATR | 5.03 ATR |
| **20 s.** | 0.81 ATR | 1.77 ATR | 2.00 ATR | 2.50 ATR | 3.03 ATR | 3.53 ATR | 5.12 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile VIDE (borne basse 0.399 ATR au-dessus du haut de la grille, 0.35 ATR) _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 37.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.582–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.931 %, prix 25.2124), p(touche) 33.87 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.732–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.931 %, prix 25.2124), p(touche) 43.9 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.991–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (9.242 %, prix 24.5863), p(touche) 44.59 % (en stress 93.94 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.411–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (13.863 %, prix 23.3345), p(touche) 42.68 % (en stress 96.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.999–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (18.483 %, prix 22.083), p(touche) 44.97 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.025 | EV/share : $-0.019 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 58.1 | bear 5.0 | side 36.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.447% → cible +4.689% / stop −2.813%, p_fill 75%, n_eff≈78.4) : P(cible|rempli) **12%** · **EV/risk -0.101** (×p_fill ; si rempli -0.38% du capital)
  - **swing** (entrée dip −3.199% → cible +10.674% / stop −9.547%, p_fill 61%, n_eff≈70.2) : P(cible|rempli) **28%** · **EV/risk +0.007** (×p_fill ; si rempli +0.10% du capital)
  - **deep** (entrée dip −4.937% → cible +23.727% / stop −14.583%, p_fill 57%, n_eff≈64.7) : P(cible|rempli) **18%** · **EV/risk +0.123** (×p_fill ; si rempli +3.14% du capital)
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
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.59 · part idiosyncratique 0.41
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-06 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-3 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-10 — US CPI (headline) (J-3 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 39.0  _(momentum baissier)_
- **ADX** : 22.8  _(pas de tendance nette)_
- **MACD** : hist -0.607  _(pas de croisement recent)_
- **BB** : %B 0.01 · largeur 41.6%
- **ATR** : 2.5 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.285  _(distribution)_
- **Vol ratio** : 1.44  _(volume normal)_
- **Choppiness** : 41.8  _(transition)_
- **MA** : MA20 33.98 · MA50 37.64 · MA200 32.63  _(prix < MA20)_
- **Dist MA** : MA20 -20.3% · MA50 -28.0% · MA200 -17.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (735732 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
