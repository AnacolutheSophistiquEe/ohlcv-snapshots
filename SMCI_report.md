# SMCI

**Generated** : 2026-10-16T00:24:03.673268+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite normal · $35.08  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (9 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $35.08 (+2.2% vs entrée) · entrée $34.34 · stop $33.48 · T1 $35.55 · R/R 1.41  
> ↳ ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.5% cohérent avec le bruit 5 s (EV-optimal ≈ −2.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +11.8 % ≠ (strike 40.0 − spot 35.08)/spot = +14.0 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -257 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-15 : 35.08 · ATR Wilder 2.46 (7.02 %)_
- **Swing** : plage **32.07 → 30.28** (-8.58 % a -13.68 % sous la cloture, 0.73 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 31.11-32.04 (B) ; 29.85-31.03 (B). stop INDICATIF 27.27 (-9.92 % sous le bas ; sous le support 28.5-29.68 (- 0,5 ATR)).
- **Deep** : plage **30.28 → 24.94** (-13.68 % a -28.91 % sous la cloture, 2.17 ATR) — touchee 44 % → 15 % du temps en 20 seances ; supports reels dans la plage : 29.85-31.03 (B) ; 28.5-29.68 (B) ; 26.67-27.75 (B) ; 25.13-26.06 (A). stop INDICATIF 22.15 (-11.18 % sous le bas ; sous le support 23.38-24.19 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 4.34 ATR sous le plus haut 20 s., RSI(2) 1.0. Limite **33.84** (seance suivante), stop catastrophe 23.99, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 32.59-33.64 (B, -4.09 %) ; 31.11-32.04 (B, -8.65 %) ; 29.85-31.03 (B, -11.53 %) ; 28.5-29.68 (B, -15.38 %) ; 26.67-27.75 (B, -20.88 %) ; 25.13-26.06 (A, -25.7 %)
- Resistances reelles au-dessus : 36.8-37.85 (A, 4.92 %) ; 38.28-39.47 (A, 9.14 %) ; 39.52-40.74 (A, 12.67 %) ; 40.78-41.53 (A, 16.27 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.98 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.54 %)** : le gap seul le franchit 0.798 % des séances (10 fois sur 1253).
   - exécution **4.365 pt plus bas** dans le cas TYPIQUE (médiane), 15.539 au p90, **17.511 au pire**
   - perte réelle **18.539 %** en moyenne _(tirée par la queue)_, jusqu'à **29.051 %** — au lieu des 11.54 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0559 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.818 % | p01 -10.307 % | pire -29.051 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4466** [0.3739 ; 0.521] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3965** [0.346 ; 0.4488] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.308** [0.2611 ; 0.3581] _(largeur 9.7 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : swing (27.6 pt), deep (28.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.63 %** | CVaR **-12.3 %** | vol 5.82 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.64 % contre 6.46 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.06 % vs -16.7 % si l'on extrapolait par √5 _(rapport 1.022 ; < 1 = le √5 surestime)_
- **β de baisse : 1.5252** (β de hausse 1.2158, asymétrie 1.2545) vs IWM — 605 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.838× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 33.2525 sur atr_grid (0.75 ATR, 5.196 %) — p(stop avant cible) 0.6796 [0.63 ; 0.73], R/R 5.201, perte reelle 5.904 % (gap inclus), CVaR 14.341 %, EV 1.0609 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.8197 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 10.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.680, borne haute 0.727 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 14.34 % > budget 12.00 %
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 18 des 18 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 44.8 % de la queue et il ne reste que -489.97 EUR a partager. Prix du risque -0.226 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 10.392 %) — p(stop avant cible) 0.3789 [0.33 ; 0.43], R/R 2.561, perte reelle 11.992 % (gap inclus), EV 1.9453 % — **REFUSE**
      - refuse : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.21 % > budget 12.00 %
   - ⚪ sr_based a 1.31 ATR (stop 12.523 %) — p(stop avant cible) 0.2802 [0.23 ; 0.33], R/R 2.135, perte reelle 14.384 % (gap inclus), EV 2.4343 % — **REFUSE**
      - refuse : cible atteinte seulement 13.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.13 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.83 % > budget 12.00 %
   - 🟢 support a 3.03 ATR (stop 24.434 %) — p(stop avant cible) 0.0901 [0.06 ; 0.12], R/R 1.185, perte reelle 25.924 % (gap inclus), EV 2.8906 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.18 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.12 % > budget 12.00 %
   - 🟢 support a 3.98 ATR (stop 30.992 %) — p(stop avant cible) 0.0697 [0.05 ; 0.10], R/R 0.988, perte reelle 31.095 % (gap inclus), EV 2.5784 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.14 % > budget 12.00 %
   - 🟢 support a 4.81 ATR (stop 36.779 %) — p(stop avant cible) 0.0462 [0.03 ; 0.07], R/R 0.834, perte reelle 36.817 % (gap inclus), EV 2.4374 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.54 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.732 %) — p(stop avant cible) 0.8989 [0.86 ; 0.93], R/R 15.42, perte reelle 1.991 % (gap inclus), EV 0.3057 % — **REFUSE**
      - refuse : cible atteinte seulement 4.1 % du temps (< 15 %) meme a 10 seances : le R/R de 15.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.899, borne haute 0.927 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.464 %) — p(stop avant cible) 0.7699 [0.72 ; 0.81], R/R 7.739, perte reelle 3.968 % (gap inclus), EV 0.9845 % — **REFUSE**
      - refuse : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 7.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.770, borne haute 0.812 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.75 ATR (stop 5.196 %) — p(stop avant cible) 0.6796 [0.63 ; 0.73], R/R 5.201, perte reelle 5.904 % (gap inclus), EV 1.0609 % — **REFUSE**
      - refuse : cible atteinte seulement 10.5 % du temps (< 15 %) meme a 10 seances : le R/R de 5.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.680, borne haute 0.727 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 14.34 % > budget 12.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 6.928 %) — p(stop avant cible) 0.5454 [0.49 ; 0.60], R/R 3.769, perte reelle 8.149 % (gap inclus), EV 1.6243 % — **REFUSE**
      - refuse : cible atteinte seulement 12.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.545, borne haute 0.597 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 19.62 % > budget 12.00 %
   - ⚪ atr_grid a 2.0 ATR (stop 13.856 %) — p(stop avant cible) 0.2291 [0.19 ; 0.28], R/R 1.921, perte reelle 15.982 % (gap inclus), EV 2.5522 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.48 % > budget 12.00 %
   - ⚪ atr_grid a 2.25 ATR (stop 15.588 %) — p(stop avant cible) 0.1959 [0.16 ; 0.24], R/R 1.712, perte reelle 17.938 % (gap inclus), EV 2.5269 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.71 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.45 % > budget 12.00 %
   - ⚪ atr_grid a 2.5 ATR (stop 17.32 %) — p(stop avant cible) 0.1669 [0.13 ; 0.21], R/R 1.553, perte reelle 19.776 % (gap inclus), EV 2.6951 % — **REFUSE**
      - refuse : cible atteinte seulement 13.5 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.93 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 19.052 %) — p(stop avant cible) 0.1324 [0.10 ; 0.17], R/R 1.431, perte reelle 21.466 % (gap inclus), EV 2.9483 % — **REFUSE**
      - refuse : cible atteinte seulement 13.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.18 % > budget 12.00 %
   - 🟢 grid_snapped a 3.03 ATR (stop 23.076 %) — p(stop avant cible) 0.1072 [0.08 ; 0.14], R/R 1.245, perte reelle 24.666 % (gap inclus), EV 2.841 % — **REFUSE**
      - refuse : cible atteinte seulement 13.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.24 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.49 % > budget 12.00 %
   - 🟢 grid_snapped a 3.98 ATR (stop 29.634 %) — p(stop avant cible) 0.0742 [0.05 ; 0.11], R/R 1.03, perte reelle 29.81 % (gap inclus), EV 2.65 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.89 % > budget 12.00 %
   - 🟢 grid_snapped a 4.81 ATR (stop 35.421 %) — p(stop avant cible) 0.0573 [0.04 ; 0.09], R/R 0.865, perte reelle 35.515 % (gap inclus), EV 2.3932 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.53 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 38.104 %) — p(stop avant cible) 0.0357 [0.02 ; 0.06], R/R 0.805, perte reelle 38.135 % (gap inclus), EV 2.4578 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.48 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 41.568 %) — p(stop avant cible) 0.0073 [0.00 ; 0.02], R/R 0.739, perte reelle 41.568 % (gap inclus), EV 2.6093 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.88 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 45.032 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.677, perte reelle 45.363 % (gap inclus), EV 2.6042 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.96 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 48.496 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 0.618, perte reelle 49.652 % (gap inclus), EV 2.5989 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.06 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 51.96 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.553, perte reelle 55.543 % (gap inclus), EV 2.5946 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.20 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 55.424 %) — p(stop avant cible) 0.0014 [0.00 ; 0.01], R/R 0.55, perte reelle 55.854 % (gap inclus), EV 2.5942 % — **REFUSE**
      - refuse : cible atteinte seulement 13.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.21 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 35.075, ATR14 2.43 (6.928 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.345 ATR = 2.39 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.346 % | 34.9535 | 90.74 % | 93.55 % | 94.95 % | 95.45 % | 96.65 % | 97.84 % |
| 0.1 ATR | 0.693 % | 34.832 | 82.18 % | 87.5 % | 89.51 % | 91.41 % | 93.19 % | 95.17 % |
| 0.15 ATR | 1.039 % | 34.7105 | 75.13 % | 82.46 % | 85.37 % | 88.57 % | 90.96 % | 93.94 % |
| 0.2 ATR | 1.386 % | 34.589 | 68.28 % | 77.72 % | 80.93 % | 86.05 % | 89.43 % | 92.61 % |
| 0.25 ATR | 1.732 % | 34.4675 | 62.03 % | 72.98 % | 76.59 % | 82.61 % | 87.3 % | 90.86 % |
| 0.35 ATR | 2.425 % | 34.2245 | 49.35 % | 63.61 % | 69.93 % | 77.45 % | 83.03 % | 88.3 % |
| 0.5 ATR | 3.464 % | 33.86 | 34.94 % | 50.0 % | 58.73 % | 68.96 % | 77.24 % | 83.78 % |
| 0.75 ATR | 5.196 % | 33.2525 | 17.42 % | 33.47 % | 43.29 % | 55.41 % | 66.67 % | 75.56 % |
| 1.0 ATR | 6.928 % | 32.645 | 7.85 % | 21.57 % | 30.47 % | 43.78 % | 57.22 % | 68.79 % |
| 1.25 ATR | 8.66 % | 32.0375 | 3.73 % | 15.02 % | 22.3 % | 33.16 % | 47.87 % | 60.99 % |
| 1.5 ATR | 10.392 % | 31.43 | 1.51 % | 9.58 % | 16.35 % | 25.99 % | 41.57 % | 54.62 % |
| 2.0 ATR | 13.856 % | 30.215 | 0.3 % | 3.53 % | 8.48 % | 16.08 % | 29.67 % | 43.43 % |
| 2.5 ATR | 17.32 % | 29.0 | 0.2 % | 1.51 % | 4.24 % | 9.61 % | 19.31 % | 31.52 % |
| 3.0 ATR | 20.784 % | 27.785 | 0.2 % | 1.21 % | 2.62 % | 5.56 % | 13.82 % | 23.72 % |
| 4.0 ATR | 27.712 % | 25.355 | 0.0 % | 0.6 % | 1.51 % | 2.63 % | 7.42 % | 14.17 % |
| 6.0 ATR | 41.568 % | 20.495 | 0.0 % | 0.2 % | 0.4 % | 0.71 % | 2.03 % | 5.54 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.15 ATR | 0.34 ATR | 0.40 ATR | 0.53 ATR | 0.64 ATR | 0.71 ATR | 0.94 ATR | 1.17 ATR |
| **2 s.** | 0.23 ATR | 0.50 ATR | 0.58 ATR | 0.76 ATR | 0.93 ATR | 1.06 ATR | 1.48 ATR | 1.88 ATR |
| **3 s.** | 0.27 ATR | 0.64 ATR | 0.72 ATR | 0.95 ATR | 1.17 ATR | 1.35 ATR | 1.90 ATR | 2.41 ATR |
| **5 s.** | 0.39 ATR | 0.87 ATR | 0.97 ATR | 1.26 ATR | 1.55 ATR | 1.80 ATR | 2.47 ATR | 3.19 ATR |
| **10 s.** | 0.55 ATR | 1.19 ATR | 1.36 ATR | 1.86 ATR | 2.23 ATR | 2.47 ATR | 3.60 ATR | 4.90 ATR |
| **20 s.** | 0.77 ATR | 1.71 ATR | 1.93 ATR | 2.44 ATR | 2.92 ATR | 3.39 ATR | 4.97 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.395–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.576–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.196 %, prix 33.2525), p(touche) 33.47 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 27.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.722–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (5.196 %, prix 33.2525), p(touche) 43.29 % (en stress 90.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 16.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 0.974–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.66 %, prix 32.0375), p(touche) 33.16 % (en stress 89.9 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 31.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.364–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (10.392 %, prix 31.43), p(touche) 41.57 % (en stress 95.96 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 1.93–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (17.32 %, prix 29.0), p(touche) 31.52 % (en stress 98.98 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 58.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.025 | EV/share : $0.022 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 34 % | T2 — | T3 —
- Kelly (position) : f* 0.045 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.9 | bear 5.0 | side 82.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.102% → cible +3.538% / stop −2.5%, p_fill 52%, n_eff≈58.0) : P(cible|rempli) **23%** · **EV/risk -0.036** (×p_fill ; si rempli -0.17% du capital)
  - **swing** (entrée dip −4.612% → cible +8.121% / stop −7.263%, p_fill 39%, n_eff≈46.5) : P(cible|rempli) **41%** · **EV/risk +0.008** (×p_fill ; si rempli +0.15% du capital)
  - **deep** (entrée dip −7.138% → cible +11.796% / stop −11.19%, p_fill 39%, n_eff≈45.0) : P(cible|rempli) **59%** · **EV/risk +0.129** (×p_fill ; si rempli +3.73% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→62% · +3.0%→43% · +5.0%→22% · +8.0%→9%
- Range intraday médian 5.66% (p90 9.37%) · excursion haute méd. +2.56% / basse méd. −2.37%
- Profil de vol intra : ouverture 3.84% vs midi 1.155% vs clôture 1.48% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓0% ; spike-down 69% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.131 ; neutre — autocorr -0.011)_ ; drift intra méd. 0.304% ; recovery-V 40%
- **σ réalisé intraday** 3.371% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 61% / whipsaw 23%
- POC intraday (dernière séance, temps-au-prix) : 43.4066 (VA 43.1796–43.8039 ; dernier close 43.68)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 23% · rebond 78% · **stop −4.35%** sous le fill (sous le bruit) · cible +2.23% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.21% · baisse 42% (gap-down >1% 31% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −0.93% (p90 −2.5%) · haut méd +1.02% · range méd 2.13%
- Excursion ouverture 15min (n=160) : bas méd −1.13% (p90 −3.1%) · haut méd +1.28% · range méd 2.8%
- Excursion ouverture 30min (n=160) : bas méd −1.36% (p90 −3.6%) · haut méd +1.53% · range méd 3.54%
- Excursion ouverture 60min (n=160) : bas méd −1.66% (p90 −4.07%) · haut méd +1.81% · range méd 4.18%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.69 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 71% (116/159) · gap 37% · délai 0.0min · rebond 57% (69/116) (MFE +1.39%)
   - −1.0% : fill 30min 51% · séance 67% (109/159) · gap 31% · délai 0.0min · rebond 58% (64/109) (MFE +1.64%)
   - −1.5% : fill 30min 45% · séance 61% (99/159) · gap 20% · délai 0.2min · rebond 69% (65/99) (MFE +1.56%)
   - −2.0% : fill 30min 39% · séance 53% (86/159) · gap 16% · délai 1.1min · rebond 72% (57/86) (MFE +1.74%)
   - −3.0% : fill 30min 26% · séance 44% (72/159) · gap 8% · délai 12.8min · rebond 64% (44/72) (MFE +1.42%)
   - −4.0% : fill 30min 13% · séance 31% (52/159) · gap 4% · délai 41.3min · rebond 72% (34/52) (MFE +1.7%)
   - −5.0% : fill 30min 10% · séance 23% (41/159) · gap 3% · délai 49.2min · rebond 78% (30/41) (MFE +2.23%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.62% (p90 −2.8%) → stop au-delà de −1.92% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.66% (p90 −2.62%) → stop au-delà de −1.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.65% (p90 −2.32%) → stop au-delà de −1.68% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=870 jambes) : jambe baissière méd −1.18% (p90 −2.77%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 98% (69/71) · rebond 48% (36/69)
      · −2.0% : fill 94% (65/71) · rebond 74% (41/65)
      · −3.0% : fill 85% (58/71) · rebond 65% (35/58)
      · −4.0% : fill 62% (43/71) · rebond 71% (28/43)
      · −5.0% : fill 46% (34/71) · rebond 76% (24/34)
   - **flat** (13 séances) :
      · −1.0% : fill 85% (12/13) · rebond 75% (9/12)
      · −2.0% : fill 36% (5/13) · rebond 50% (3/5)
      · −3.0% : fill 29% (3/13) · rebond 43% (2/3)
      · −4.0% : fill 10% (1/13) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/13) · rebond 0% (0/0)
   - **gap-up** (75 séances) :
      · −1.0% : fill 38% (28/75) · rebond 74% (19/28)
      · −2.0% : fill 21% (16/75) · rebond 70% (13/16)
      · −3.0% : fill 11% (11/75) · rebond 70% (7/11)
      · −4.0% : fill 8% (8/75) · rebond 72% (5/8)
      · −5.0% : fill 8% (7/75) · rebond 86% (6/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 68% si les 15 1res min sont vertes (80 cas) · 27% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **39min** → P(séance verte=clôture>ouverture) 78% si début vert vs 18% si rouge (base 48% · écart 60 pts) ; prédictivité sature ensuite (plafond brut 213min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=82) : tient le vert **78%** · continue >prix actuel 54% ; creux résiduel méd -1.96% (q20 -3.57%) → **SL/trailing à −3.57%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +4.23% → **scale +1.91% / runner +4.23%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **18%** (continue à baisser 53%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.85%** (au-delà de la MAE q10 -4.85%), cible rebond +1.68% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.7% .. +4.13%] · haut q95 +5.15% · bas q05 -4.15%
   - 60min (n=160) : retour [-4.08% .. +5.23%] · haut q95 +6.49% · bas q05 -5.23%
   - 2h (n=160) : retour [-4.2% .. +6.08%] · haut q95 +7.25% · bas q05 -5.52%
   - 4h (n=160) : retour [-4.43% .. +6.66%] · haut q95 +7.77% · bas q05 -5.98%
   - 6h (n=160) : retour [-4.87% .. +6.53%] · haut q95 +8.68% · bas q05 -6.54%
   - session (n=160) : retour [-4.8% .. +6.89%] · haut q95 +8.93% · bas q05 -6.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (5) pour des stats fiables : 3.1% des séances seulement sont des jours de hausse propre — SMCI = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.59 · part idiosyncratique 0.41
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 26.0  _(survente)_
- **ADX** : 25.7  _(tendance etablie)_
- **MACD** : hist -1.045  _(pas de croisement recent)_
- **BB** : %B -0.12 · largeur 23.9%
- **ATR** : 2.43 (73.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF 0.037  _(neutre)_
- **Vol ratio** : 0.99  _(volume normal)_
- **Choppiness** : 35.3  _(marche directionnel)_
- **MA** : MA20 41.18 · MA50 38.62 · MA200 32.46  _(prix < MA20)_
- **Dist MA** : MA20 -14.8% · MA50 -9.2% · MA200 +8.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (845401 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
