# IONQ

**Generated** : 2026-10-15T00:23:41.160947+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $31.42  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (8 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot $31.42 (+1.1% vs entrée) · entrée $31.08 · stop $30.31 · T1 $32.37 · R/R 1.68  
> ↳ ¼-Kelly 0.018 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.49% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +15.2 % ≠ (strike 40.0 − spot 31.42)/spot = +27.3 %. Probable spot d'options périmé vs spot courant.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-14 : 31.42 · ATR Wilder 2.68 (8.53 %)_
- **Swing** : plage **28.11 → 26.08** (-10.51 % a -16.98 % sous la cloture, 0.76 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 27.83-28.32 (B) ; 25.5-26.33 (A). stop INDICATIF 20.93 (-19.75 % sous le bas ; sous le support 22.27-23.49 (- 0,5 ATR)).
- **Deep** : plage **26.08 → 21.62** (-16.98 % a -31.19 % sous la cloture, 1.67 ATR) — touchee 47 % → 15 % du temps en 20 seances ; supports reels dans la plage : 25.5-26.33 (A) ; 22.27-23.49 (B). stop INDICATIF 19.27 (-10.86 % sous le bas ; sous le support 20.61-21.5 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.16 ATR sous le plus haut 20 s., RSI(2) 1.2. Limite **30.08** (seance suivante), stop catastrophe 19.36, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 27.83-28.32 (B, -9.85 %) ; 25.5-26.33 (A, -16.19 %) ; 22.27-23.49 (B, -25.24 %) ; 20.61-21.5 (B, -31.56 %) ; 17.88-18.81 (A, -40.12 %) ; 13.38-14.15 (A, -54.96 %)
- Resistances reelles au-dessus : 33.29-34.18 (A, 5.97 %) ; 34.77-36.03 (A, 10.68 %) ; 36.57-37.28 (A, 16.41 %) ; 38.0-38.46 (A, 20.96 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=9.10 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.54 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1253).
   - exécution **1.153 pt plus bas** dans le cas TYPIQUE (médiane), 8.345 au p90, **11.319 au pire**
   - perte réelle **13.966 %** en moyenne _(tirée par la queue)_, jusqu'à **21.859 %** — au lieu des 10.54 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0109 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.087 % | p01 -6.632 % | pire -21.859 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5016** [0.4276 ; 0.5755] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4445** [0.3928 ; 0.4972] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.4139** [0.3629 ; 0.4664] _(largeur 10.3 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.85 %** | CVaR **-10.55 %** | vol 6.12 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 10.57 % contre 5.42 % aujourd'hui, rapport 1.95)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -17.88 % vs -19.88 % si l'on extrapolait par √5 _(rapport 0.899 ; < 1 = le √5 surestime)_
- **β de baisse : 2.1972** (β de hausse 2.0075, asymétrie 1.0945) vs IWM — 606 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 28.195 sur atr_grid (1.25 ATR, 10.25 %) — p(stop avant cible) 0.5513 [0.50 ; 0.60], R/R 2.669, perte reelle 10.348 % (gap inclus), CVaR 11.327 %, EV 0.4934 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.2067 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.551, borne haute 0.603 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.55 ATR (stop 7.177 %) — p(stop avant cible) 0.6707 [0.62 ; 0.72], R/R 3.781, perte reelle 7.305 % (gap inclus), EV 0.6809 % — **REFUSE**
      - refuse : p_stop_first 0.671, borne haute 0.719 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - ⚠ support DETECTE a 0.52 ATR du spot — compartiment <1, mesure a 47.1 % de casse (IC clusterise [0.439 ; 0.504] sur 1187 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 12.3 %) — p(stop avant cible) 0.444 [0.39 ; 0.50], R/R 2.232, perte reelle 12.376 % (gap inclus), EV 0.6111 % — **REFUSE**
      - refuse : R/R 2.23 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.98 % > budget 12.00 %
   - 🟢 support a 2.14 ATR (stop 20.228 %) — p(stop avant cible) 0.1805 [0.14 ; 0.22], R/R 1.359, perte reelle 20.323 % (gap inclus), EV 0.7553 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.57 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 2.05 %) — p(stop avant cible) 0.8893 [0.85 ; 0.92], R/R 13.274, perte reelle 2.081 % (gap inclus), EV 0.379 % — **REFUSE**
      - refuse : cible atteinte seulement 6.5 % du temps (< 15 %) meme a 10 seances : le R/R de 13.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.889, borne haute 0.919 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 1.25 ATR (stop 10.25 %) — p(stop avant cible) 0.5513 [0.50 ; 0.60], R/R 2.669, perte reelle 10.348 % (gap inclus), EV 0.4934 % — **REFUSE**
      - refuse : p_stop_first 0.551, borne haute 0.603 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
   - ⚪ atr_grid a 1.75 ATR (stop 14.35 %) — p(stop avant cible) 0.3556 [0.31 ; 0.41], R/R 1.912, perte reelle 14.445 % (gap inclus), EV 0.3414 % — **REFUSE**
      - refuse : R/R 1.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.02 % > budget 12.00 %
   - ⚪ atr_grid a 2.75 ATR (stop 22.55 %) — p(stop avant cible) 0.1322 [0.10 ; 0.17], R/R 1.223, perte reelle 22.577 % (gap inclus), EV 0.8212 % — **REFUSE**
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.62 % > budget 12.00 %
   - ⚪ atr_grid a 3.0 ATR (stop 24.6 %) — p(stop avant cible) 0.0914 [0.06 ; 0.13], R/R 1.121, perte reelle 24.644 % (gap inclus), EV 0.8716 % — **REFUSE**
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.68 % > budget 12.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 28.7 %) — p(stop avant cible) 0.0608 [0.04 ; 0.09], R/R 0.96, perte reelle 28.76 % (gap inclus), EV 0.718 % — **REFUSE**
      - refuse : R/R 0.96 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.77 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 32.8 %) — p(stop avant cible) 0.0231 [0.01 ; 0.04], R/R 0.84, perte reelle 32.879 % (gap inclus), EV 0.7656 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.40 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 36.9 %) — p(stop avant cible) 0.0121 [0.00 ; 0.03], R/R 0.744, perte reelle 37.126 % (gap inclus), EV 0.8022 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.21 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 41.0 %) — p(stop avant cible) 0.0051 [0.00 ; 0.02], R/R 0.674, perte reelle 41.001 % (gap inclus), EV 0.8194 % — **REFUSE**
      - refuse : R/R 0.67 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.03 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 45.099 %) — p(stop avant cible) 0.001 [0.00 ; 0.01], R/R 0.612, perte reelle 45.099 % (gap inclus), EV 0.8406 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.70 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 49.199 %) — p(stop avant cible) 0.0005 [0.00 ; 0.01], R/R 0.561, perte reelle 49.199 % (gap inclus), EV 0.8573 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.54 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 53.299 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.518, perte reelle 53.299 % (gap inclus), EV 0.8729 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.31 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 57.399 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.481, perte reelle 57.399 % (gap inclus), EV 0.8729 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.31 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 61.499 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.449, perte reelle 61.499 % (gap inclus), EV 0.8729 % — **REFUSE**
      - refuse : R/R 0.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.31 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 65.599 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.421, perte reelle 65.599 % (gap inclus), EV 0.8729 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.31 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 31.415, ATR14 2.576 (8.2 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.382 ATR = 3.132 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.41 % | 31.2862 | 93.76 % | 95.46 % | 96.17 % | 97.57 % | 98.17 % | 98.67 % |
| 0.1 ATR | 0.82 % | 31.1574 | 86.2 % | 91.23 % | 92.33 % | 94.64 % | 95.83 % | 96.82 % |
| 0.15 ATR | 1.23 % | 31.0286 | 78.95 % | 86.39 % | 88.4 % | 91.61 % | 93.6 % | 95.59 % |
| 0.2 ATR | 1.64 % | 30.8998 | 71.4 % | 80.65 % | 84.36 % | 88.47 % | 90.85 % | 93.43 % |
| 0.25 ATR | 2.05 % | 30.771 | 65.36 % | 76.51 % | 80.83 % | 85.95 % | 88.82 % | 91.89 % |
| 0.35 ATR | 2.87 % | 30.5134 | 53.17 % | 67.54 % | 74.27 % | 79.47 % | 84.15 % | 88.3 % |
| 0.5 ATR | 4.1 % | 30.127 | 38.17 % | 54.64 % | 62.36 % | 71.18 % | 78.66 % | 84.39 % |
| 0.75 ATR | 6.15 % | 29.483 | 22.46 % | 39.42 % | 48.54 % | 59.05 % | 69.31 % | 76.8 % |
| 1.0 ATR | 8.2 % | 28.839 | 10.27 % | 24.9 % | 35.02 % | 46.11 % | 58.33 % | 68.17 % |
| 1.25 ATR | 10.25 % | 28.195 | 3.83 % | 14.52 % | 24.22 % | 34.98 % | 50.51 % | 61.81 % |
| 1.5 ATR | 12.3 % | 27.551 | 1.11 % | 7.16 % | 15.84 % | 25.68 % | 41.46 % | 56.16 % |
| 2.0 ATR | 16.4 % | 26.263 | 0.1 % | 1.92 % | 5.15 % | 14.36 % | 28.46 % | 45.28 % |
| 2.5 ATR | 20.5 % | 24.975 | 0.0 % | 0.2 % | 1.21 % | 5.86 % | 18.29 % | 34.29 % |
| 3.0 ATR | 24.6 % | 23.687 | 0.0 % | 0.1 % | 0.4 % | 2.53 % | 11.48 % | 25.87 % |
| 4.0 ATR | 32.8 % | 21.111 | 0.0 % | 0.1 % | 0.1 % | 0.2 % | 2.95 % | 10.57 % |
| 6.0 ATR | 49.199 % | 15.959 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.1 % | 1.23 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.58 ATR | 0.71 ATR | 0.80 ATR | 1.01 ATR | 1.21 ATR |
| **2 s.** | 0.27 ATR | 0.58 ATR | 0.66 ATR | 0.86 ATR | 1.00 ATR | 1.12 ATR | 1.40 ATR | 1.71 ATR |
| **3 s.** | 0.34 ATR | 0.72 ATR | 0.81 ATR | 1.05 ATR | 1.23 ATR | 1.38 ATR | 1.77 ATR | 2.02 ATR |
| **5 s.** | 0.43 ATR | 0.93 ATR | 1.02 ATR | 1.30 ATR | 1.53 ATR | 1.75 ATR | 2.26 ATR | 2.63 ATR |
| **10 s.** | 0.60 ATR | 1.26 ATR | 1.40 ATR | 1.82 ATR | 2.17 ATR | 2.42 ATR | 3.17 ATR | 3.76 ATR |
| **20 s.** | 0.80 ATR | 1.78 ATR | 2.01 ATR | 2.58 ATR | 3.06 ATR | 3.38 ATR | 4.12 ATR | 5.19 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.432–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.658–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.15 %, prix 29.483), p(touche) 39.42 % (en stress 87.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 30.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.815–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.2 %, prix 28.839), p(touche) 35.02 % (en stress 92.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 28.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.025–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.25 %, prix 28.195), p(touche) 34.98 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 21.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.402–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (12.3 %, prix 27.551), p(touche) 41.46 % (en stress 97.98 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 42.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.013–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ✅ optimum identifie (68.6 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.051 | EV/share : $0.040 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 — | T3 —
- Kelly (position) : f* 0.073 | ¼-Kelly 0.018 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 41.7 | bear 5.0 | side 53.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.06% → cible +4.144% / stop −2.486%, p_fill 73%, n_eff≈81.4) : P(cible|rempli) **20%** · **EV/risk -0.072** (×p_fill ; si rempli -0.24% du capital)
  - **swing** (entrée dip −2.34% → cible +11.902% / stop −8.396%, p_fill 71%, n_eff≈84.9) : P(cible|rempli) **32%** · **EV/risk -0.021** (×p_fill ; si rempli -0.25% du capital)
  - **deep** (entrée dip −3.61% → cible +13.382% / stop −12.761%, p_fill 72%, n_eff≈81.4) : P(cible|rempli) **35%** · **EV/risk -0.101** (×p_fill ; si rempli -1.80% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→80% · +2.0%→64% · +3.0%→54% · +5.0%→28% · +8.0%→13%
- Range intraday médian 7.05% (p90 11.57%) · excursion haute méd. +3.57% / basse méd. −2.49%
- Profil de vol intra : ouverture 4.841% vs midi 1.378% vs clôture 1.552% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 62% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; neutre — autocorr 0.011)_ ; drift intra méd. -0.232% ; recovery-V 26%
- **σ réalisé intraday** 4.05% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 57% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 44.6406 (VA 44.2714–45.1154 ; dernier close 43.77)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 78% · **stop −4.38%** sous le fill (sous le bruit) · cible +2.22% · R/R 0.51 (high win-rate)
- Gaps overnight (n=159) : méd. 0.03% · baisse 49% (gap-down >1% 34% · >2% 21%)
- Excursion ouverture 5min (n=160) : bas méd −1.0% (p90 −2.73%) · haut méd +1.28% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.18% (p90 −3.76%) · haut méd +1.47% · range méd 3.38%
- Excursion ouverture 30min (n=160) : bas méd −1.31% (p90 −4.62%) · haut méd +1.81% · range méd 4.16%
- Excursion ouverture 60min (n=160) : bas méd −1.57% (p90 −5.28%) · haut méd +1.87% · range méd 4.67%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 43.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 76% (126/159) · gap 43% · délai 0.0min · rebond 61% (83/126) (MFE +1.81%)
   - −1.0% : fill 30min 60% · séance 70% (119/159) · gap 34% · délai 0.0min · rebond 67% (85/119) (MFE +1.91%)
   - −1.5% : fill 30min 53% · séance 65% (112/159) · gap 30% · délai 0.0min · rebond 70% (78/112) (MFE +2.06%)
   - −2.0% : fill 30min 46% · séance 54% (100/159) · gap 21% · délai 0.0min · rebond 69% (70/100) (MFE +2.17%)
   - −3.0% : fill 30min 37% · séance 43% (81/159) · gap 10% · délai 4.1min · rebond 70% (59/81) (MFE +2.38%)
   - −4.0% : fill 30min 22% · séance 33% (64/159) · gap 4% · délai 15.3min · rebond 69% (48/64) (MFE +2.23%)
   - −5.0% : fill 30min 11% · séance 25% (50/159) · gap 1% · délai 32.0min · rebond 78% (41/50) (MFE +2.22%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.75% (p90 −2.62%) → stop au-delà de −1.83% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.76% (p90 −2.65%) → stop au-delà de −1.69% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.68% (p90 −2.35%) → stop au-delà de −1.31% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1047 jambes) : jambe baissière méd −1.26% (p90 −2.97%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (80 séances) :
      · −1.0% : fill 100% (80/80) · rebond 69% (56/80)
      · −2.0% : fill 87% (73/80) · rebond 75% (54/73)
      · −3.0% : fill 72% (61/80) · rebond 72% (44/61)
      · −4.0% : fill 54% (47/80) · rebond 67% (34/47)
      · −5.0% : fill 38% (37/80) · rebond 70% (28/37)
   - **flat** (15 séances) :
      · −1.0% : fill 62% (10/15) · rebond 84% (9/10)
      · −2.0% : fill 43% (8/15) · rebond 90% (6/8)
      · −3.0% : fill 27% (5/15) · rebond 64% (4/5)
      · −4.0% : fill 23% (4/15) · rebond 57% (3/4)
      · −5.0% : fill 16% (3/15) · rebond 100% (3/3)
   - **gap-up** (64 séances) :
      · −1.0% : fill 41% (29/64) · rebond 55% (20/29)
      · −2.0% : fill 22% (19/64) · rebond 31% (10/19)
      · −3.0% : fill 15% (15/64) · rebond 60% (11/15)
      · −4.0% : fill 14% (13/64) · rebond 84% (11/13)
      · −5.0% : fill 12% (10/64) · rebond 100% (10/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 46% en base · 59% si les 15 1res min sont vertes (90 cas) · 26% si rouges (70 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **56min** → P(séance verte=clôture>ouverture) 66% si début vert vs 19% si rouge (base 46% · écart 47 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=86) : tient le vert **66%** · continue >prix actuel 38% ; creux résiduel méd -1.76% (q20 -4.14%) → **SL/trailing à −4.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.64% / q75 +3.31% → **scale +1.64% / runner +3.31%**, sortie à la clôture
  - **si ROUGE au coude** (n=74) : edge inversé — récupère vert seulement **19%** (continue à baisser 59%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.23%** (au-delà de la MAE q10 -4.23%), cible rebond +1.94% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +5.46%] · haut q95 +7.35% · bas q05 -5.49%
   - 60min (n=160) : retour [-5.25% .. +5.86%] · haut q95 +7.69% · bas q05 -6.74%
   - 2h (n=160) : retour [-6.37% .. +5.93%] · haut q95 +8.07% · bas q05 -7.06%
   - 4h (n=160) : retour [-6.75% .. +6.86%] · haut q95 +8.75% · bas q05 -7.93%
   - 6h (n=160) : retour [-6.62% .. +7.19%] · haut q95 +9.75% · bas q05 -7.92%
   - session (n=160) : retour [-6.36% .. +8.14%] · haut q95 +9.8% · bas q05 -8.19%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 7.5% des séances sont trend-up (mild 0% / strong 7.5%) · base = 12 séances trend-up (n_eff 7.9)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **35%**. Lecture précoce 30 min : signature présente → 13% vs absente 5% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.3% (p75 2.44% / p90 3.18%) · ~4.0 replis/séance, durée méd 70.31 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 30.0 min, n=48)
   - −1.0% → **77%** (reprise méd 34.75 min, n=35)
   - −1.5% → **67%** (reprise méd 44.94 min, n=18)
   - −2.0% → **61%** (reprise méd 64.1 min, n=13)
   - −3.0% → **74%** (reprise méd 175.76 min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−3.18%** (p90, défaut prudent ; serré/agressif −2.44%) ; extension open→close méd +8.16% (q75 +8.39% / q95 +13.57%), MFE méd +9.48% / q90 +12.4%
   - Échelle scale-out : +9.48% (33%) / +10.45% (33%) / +12.4% (34%)
- **DÉSARMER** : repli > **−3.18%** depuis le plus-haut = décay → P(retournement) **26%** (préavis méd 167.77 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.4% : P(retournement après) 0% (mèche méd 2.07%)
- **CONTEXTE** : la dernière heure tient les gains 70% du temps (retour médian dernière heure +0.1%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.48 · part idiosyncratique 0.52
**Short/Insider** : SI —% | insider — | verdict sell_bias_modere
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 8.5  _(survente)_
- **ADX** : 20.5  _(pas de tendance nette)_
- **MACD** : hist -1.229  _(pas de croisement recent)_
- **BB** : %B -0.17 · largeur 35.6%
- **ATR** : 2.58 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.317  _(distribution)_
- **Vol ratio** : 1.44  _(volume normal)_
- **Choppiness** : 28.8  _(marche directionnel)_
- **MA** : MA20 41.16 · MA50 41.04 · MA200 43.05  _(prix < MA20)_
- **Dist MA** : MA20 -23.7% · MA50 -23.5% · MA200 -27.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (875544 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
