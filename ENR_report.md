# ENR

**Generated** : 2026-10-26T01:07:45.957319+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 1/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €118.68  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €118.68 (+0.7% vs entrée) · entrée €117.81 · stop €108.39 · T1 €120.89 · R/R 0.33  
> ↳ P(T1 av. stop) 14 % _(réel 5 s)_ · EV/risk -0.062 _(réel 5 s)_ · _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -132 % hors [0,100] (R² max 0.63). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 18.7 < 20 (tendance pas encore confirmée) alors que Choppiness 35.0 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Strong Pass (negative EV)'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-23 : 118.68 · ATR Wilder 5.9 (4.98 %)_
- **Swing** : plage **111.89 → 106.91** (-5.72 % a -9.92 % sous la cloture, 0.84 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 109.88-110.08 (C). stop INDICATIF 100.26 (-6.22 % sous le bas ; sous le support 103.21-104.4 (- 0,5 ATR)).
- **Deep** : plage **106.91 → 98.51** (-9.92 % a -17.0 % sous la cloture, 1.42 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 103.21-104.4 (B) ; 98.56-100.32 (A). stop INDICATIF 89.31 (-9.33 % sous le bas ; sous le support 92.27-94.76 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.47 ATR sous le plus haut 20 s., RSI(2) 8.5. Limite **115.73** (seance suivante), stop catastrophe 92.11, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 113.47-114.51 (A, -3.51 %) ; 109.88-110.08 (C, -7.25 %) ; 103.21-104.4 (B, -12.03 %) ; 98.56-100.32 (A, -15.47 %) ; 92.27-94.76 (A, -20.16 %) ; 89.1-89.92 (A, -24.24 %)
- Resistances reelles au-dessus : 122.83-124.46 (A, 3.49 %) ; 130.89-133.3 (A, 10.29 %) ; 133.85-135.72 (A, 12.78 %) ; 137.46-140.18 (A, 15.83 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.67 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.79 %)** : le gap seul le franchit 0.549 % des séances (7 fois sur 1274).
   - exécution **1.958 pt plus bas** dans le cas TYPIQUE (médiane), 17.215 au p90, **28.967 au pire**
   - perte réelle **13.645 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 6.79 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0377 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.376 % | p01 -5.39 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0063** [0.0007 ; 0.0276] _(largeur 2.7 pt, n_eff 173.1)_
   - swing : **0.4069** [0.3561 ; 0.4593] _(largeur 10.3 pt, n_eff 345.8)_
   - deep : **0.3825** [0.3324 ; 0.4345] _(largeur 10.2 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 83.0 observations effectives », dont la borne haute a 95 % vaut environ 3.6 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.75 %** | CVaR **-6.72 %** | vol 3.19 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 6.11 % contre 3.01 % aujourd'hui, rapport 2.03)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.88 % vs -9.83 % si l'on extrapolait par √5 _(rapport 0.903 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3439** (β de hausse 1.1049, asymétrie 1.2163) vs GDAXI — 601 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.307× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 115.6043 sur atr_grid (0.5 ATR, 2.592 %) — p(stop avant cible) 0.783 [0.74 ; 0.82], R/R 12.775, perte reelle 2.705 % (gap inclus), CVaR 4.183 %, EV -0.3587 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.4875 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 12.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.783, borne haute 0.824 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **4.9 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.183 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 20.3 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.85 ATR (stop 7.12 %) — p(stop avant cible) 0.4561 [0.40 ; 0.51], R/R 4.512, perte reelle 7.658 % (gap inclus), EV -0.8375 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 11.75 % > budget 4.90 %
      - ⚠ support DETECTE a 0.56 ATR du spot — compartiment <1, mesure a 47.8 % de casse (IC clusterise [0.449 ; 0.507] sur 1237 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.84 %) : P(cible) 0.2 % x 34.55 % + P(rien) 54.2 % x 4.79 % ne couvrent pas P(stop) 45.6 % x 7.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🟢 support a 3.06 ATR (stop 18.572 %) — p(stop avant cible) 0.0234 [0.01 ; 0.04], R/R 1.757, perte reelle 19.669 % (gap inclus), EV 0.6351 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.97 % > budget 4.90 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.296 %) — p(stop avant cible) 0.9134 [0.88 ; 0.94], R/R 25.321, perte reelle 1.365 % (gap inclus), EV -0.3927 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 25.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.913, borne haute 0.940 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 0.1 % x 34.55 % + P(rien) 8.6 % x 9.63 % ne couvrent pas P(stop) 91.3 % x 1.36 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+34.6 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.592 %) — p(stop avant cible) 0.783 [0.74 ; 0.82], R/R 12.775, perte reelle 2.705 % (gap inclus), EV -0.3587 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 12.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.783, borne haute 0.824 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 0.2 % x 34.55 % + P(rien) 21.5 % x 7.91 % ne couvrent pas P(stop) 78.3 % x 2.70 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 grid_snapped a 0.85 ATR (stop 5.948 %) — p(stop avant cible) 0.5155 [0.46 ; 0.57], R/R 5.466, perte reelle 6.321 % (gap inclus), EV -0.626 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 5.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.515, borne haute 0.568 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 9.45 % > budget 4.90 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 0.2 % x 34.55 % + P(rien) 48.3 % x 5.33 % ne couvrent pas P(stop) 51.5 % x 6.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.5 ATR (stop 7.775 %) — p(stop avant cible) 0.4024 [0.35 ; 0.45], R/R 4.12, perte reelle 8.388 % (gap inclus), EV -0.7017 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 4.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.52 % > budget 4.90 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.70 %) : P(cible) 0.2 % x 34.55 % + P(rien) 59.6 % x 4.39 % ne couvrent pas P(stop) 40.2 % x 8.39 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 9.071 %) — p(stop avant cible) 0.3217 [0.27 ; 0.37], R/R 3.56, perte reelle 9.706 % (gap inclus), EV -0.594 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.74 % > budget 4.90 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 0.2 % x 34.55 % + P(rien) 67.7 % x 3.65 % ne couvrent pas P(stop) 32.2 % x 9.71 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 10.366 %) — p(stop avant cible) 0.265 [0.22 ; 0.31], R/R 3.161, perte reelle 10.932 % (gap inclus), EV -0.5183 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 3.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.21 % > budget 4.90 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.52 %) : P(cible) 0.2 % x 34.55 % + P(rien) 73.3 % x 3.16 % ne couvrent pas P(stop) 26.5 % x 10.93 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 11.662 %) — p(stop avant cible) 0.1736 [0.14 ; 0.22], R/R 2.784, perte reelle 12.412 % (gap inclus), EV -0.1366 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.78 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.78 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.14 % > budget 4.90 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.14 %) : P(cible) 0.2 % x 34.55 % + P(rien) 82.5 % x 2.38 % ne couvrent pas P(stop) 17.4 % x 12.41 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 12.958 %) — p(stop avant cible) 0.1211 [0.09 ; 0.16], R/R 2.514, perte reelle 13.746 % (gap inclus), EV 0.2052 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.51 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.51 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.87 % > budget 4.90 %
   - ⚪ atr_grid a 2.75 ATR (stop 14.254 %) — p(stop avant cible) 0.0838 [0.06 ; 0.12], R/R 2.27, perte reelle 15.225 % (gap inclus), EV 0.3214 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.27 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.88 % > budget 4.90 %
   - 🟢 grid_snapped a 3.06 ATR (stop 17.401 %) — p(stop avant cible) 0.027 [0.01 ; 0.05], R/R 1.858, perte reelle 18.597 % (gap inclus), EV 0.6232 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.98 % > budget 4.90 %
   - ⚪ atr_grid a 4.0 ATR (stop 20.733 %) — p(stop avant cible) 0.0072 [0.00 ; 0.02], R/R 1.429, perte reelle 24.186 % (gap inclus), EV 0.7179 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.43 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.21 % > budget 4.90 %
   - ⚪ atr_grid a 4.5 ATR (stop 23.324 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 1.308, perte reelle 26.415 % (gap inclus), EV 0.7497 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.93 % > budget 4.90 %
   - ⚪ atr_grid a 5.0 ATR (stop 25.916 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 1.225, perte reelle 28.219 % (gap inclus), EV 0.7799 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.68 % > budget 4.90 %
   - ⚪ atr_grid a 5.5 ATR (stop 28.508 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 1.165, perte reelle 29.658 % (gap inclus), EV 0.7913 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.17 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.56 % > budget 4.90 %
   - ⚪ atr_grid a 6.0 ATR (stop 31.099 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.059, perte reelle 32.625 % (gap inclus), EV 0.8126 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.13 % > budget 4.90 %
   - ⚪ atr_grid a 6.5 ATR (stop 33.691 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.007, perte reelle 34.318 % (gap inclus), EV 0.8108 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.17 % > budget 4.90 %
   - ⚪ atr_grid a 7.0 ATR (stop 36.282 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.949, perte reelle 36.398 % (gap inclus), EV 0.8079 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.95 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.18 % > budget 4.90 %
   - ⚪ atr_grid a 7.5 ATR (stop 38.874 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 0.889, perte reelle 38.874 % (gap inclus), EV 0.8051 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.23 % > budget 4.90 %
   - ⚪ atr_grid a 8.0 ATR (stop 41.466 %) — p(stop avant cible) 0.0006 [0.00 ; 0.01], R/R 0.833, perte reelle 41.466 % (gap inclus), EV 0.8115 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 0.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.83 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.11 % > budget 4.90 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 118.68, ATR14 6.1514 (5.183 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.369 ATR = 1.913 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.259 % | 118.3724 | 91.42 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.518 % | 118.0649 | 83.73 % | 88.25 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.777 % | 117.7573 | 76.53 % | 82.43 % | 85.97 % | 88.71 % | 91.24 % | 93.37 % |
| 0.2 ATR | 1.037 % | 117.4497 | 70.51 % | 79.07 % | 83.0 % | 86.63 % | 89.45 % | 91.96 % |
| 0.25 ATR | 1.296 % | 117.1421 | 63.81 % | 74.63 % | 79.25 % | 83.37 % | 87.46 % | 90.65 % |
| 0.35 ATR | 1.814 % | 116.527 | 51.97 % | 64.86 % | 70.26 % | 75.94 % | 82.19 % | 86.63 % |
| 0.5 ATR | 2.592 % | 115.6043 | 36.69 % | 51.92 % | 59.49 % | 66.53 % | 74.53 % | 80.5 % |
| 0.75 ATR | 3.887 % | 114.0664 | 19.63 % | 35.83 % | 45.26 % | 54.46 % | 65.37 % | 73.67 % |
| 1.0 ATR | 5.183 % | 112.5286 | 11.05 % | 25.57 % | 34.49 % | 44.36 % | 57.01 % | 65.73 % |
| 1.25 ATR | 6.479 % | 110.9907 | 6.11 % | 17.28 % | 25.0 % | 35.64 % | 48.36 % | 58.19 % |
| 1.5 ATR | 7.775 % | 109.4529 | 2.96 % | 11.15 % | 17.98 % | 27.92 % | 41.29 % | 51.96 % |
| 2.0 ATR | 10.366 % | 106.3771 | 0.79 % | 4.15 % | 8.79 % | 16.44 % | 28.36 % | 40.7 % |
| 2.5 ATR | 12.958 % | 103.3014 | 0.3 % | 2.07 % | 4.15 % | 9.7 % | 19.7 % | 30.95 % |
| 3.0 ATR | 15.55 % | 100.2257 | 0.1 % | 0.89 % | 2.08 % | 5.25 % | 12.74 % | 23.12 % |
| 4.0 ATR | 20.733 % | 94.0743 | 0.1 % | 0.39 % | 1.19 % | 2.48 % | 6.77 % | 12.66 % |
| 6.0 ATR | 31.099 % | 81.7714 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 1.05 ATR | 1.34 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.82 ATR | 1.02 ATR | 1.17 ATR | 1.58 ATR | 1.94 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.04 ATR | 1.25 ATR | 1.43 ATR | 1.93 ATR | 2.41 ATR |
| **5 s.** | 0.36 ATR | 0.86 ATR | 0.98 ATR | 1.33 ATR | 1.63 ATR | 1.84 ATR | 2.48 ATR | 3.09 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.37 ATR | 1.82 ATR | 2.19 ATR | 2.48 ATR | 3.46 ATR | 4.77 ATR |
| **20 s.** | 0.70 ATR | 1.59 ATR | 1.81 ATR | 2.40 ATR | 2.88 ATR | 3.30 ATR | 4.73 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.418–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 23.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.608–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.887 %, prix 114.0669), p(touche) 35.83 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 35.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.756–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.183 %, prix 112.5288), p(touche) 34.49 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (86.2 % des re-echantillons)
- **5 seance(s)** : plage utile 0.984–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (5.183 %, prix 112.5288), p(touche) 44.36 % (en stress 99.01 %)  ✅ optimum identifie (90.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.369–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.775 %, prix 109.4526), p(touche) 41.29 % (en stress 100.0 %)  ✅ optimum identifie (93.0 % des re-echantillons)
- **20 seance(s)** : plage utile 1.809–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (10.366 %, prix 106.3776), p(touche) 40.7 % (en stress 99.0 %)  ✅ optimum identifie (90.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 17.8 | bear 38.2 | side 43.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.728% → cible +2.611% / stop −8.0%, p_fill 79%, n_eff≈83.0) : P(cible|rempli) **14%** · **EV/risk -0.062** (×p_fill ; si rempli -0.63% du capital)
  - **swing** (entrée dip −1.607% → cible +5.938% / stop −5.268%, p_fill 71%, n_eff≈83.4) : P(cible|rempli) **24%** · **EV/risk -0.170** (×p_fill ; si rempli -1.26% du capital)
  - **deep** (entrée dip −2.485% → cible +8.404% / stop −7.973%, p_fill 72%, n_eff≈82.9) : P(cible|rempli) **17%** · **EV/risk -0.206** (×p_fill ; si rempli -2.28% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→62% · +2.0%→34% · +3.0%→15% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.62% (p90 6.06%) · excursion haute méd. +1.37% / basse méd. −1.89%
- Profil de vol intra : ouverture 1.961% vs midi 0.824% vs clôture 1.048% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 87% · range 12% · trend ↑1%/↓0% ; spike-down 61% · recovery-V 24%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; mean-reverting — autocorr -0.032)_ ; drift intra méd. -0.864% ; recovery-V 25%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 59% / bas 83% / whipsaw 42%
- POC intraday (dernière séance, temps-au-prix) : 121.5065 (VA 120.2185–123.5995 ; dernier close 118.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 18% · rebond 57% · **stop −4.86%** sous le fill (sous le bruit) · cible +1.05% · R/R 0.22 (high win-rate)
- Gaps overnight (n=159) : méd. 0.38% · baisse 38% (gap-down >1% 20% · >2% 9%)
- Excursion ouverture 5min (n=160) : bas méd −0.49% (p90 −1.69%) · haut méd +0.49% · range méd 1.14%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.05%) · haut méd +0.58% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.19%) · haut méd +0.62% · range méd 1.69%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.35%) · haut méd +0.68% · range méd 1.81%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 118.68 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 52% · séance 70% (115/159) · gap 30% · délai 0.2min · rebond 48% (59/115) (MFE +0.88%)
   - −1.0% : fill 30min 40% · séance 66% (107/159) · gap 20% · délai 8.6min · rebond 51% (59/107) (MFE +1.04%)
   - −1.5% : fill 30min 29% · séance 53% (88/159) · gap 13% · délai 12.6min · rebond 55% (48/88) (MFE +1.28%)
   - −2.0% : fill 30min 23% · séance 44% (73/159) · gap 9% · délai 20.7min · rebond 50% (41/73) (MFE +1.0%)
   - −3.0% : fill 30min 10% · séance 29% (48/159) · gap 3% · délai 251.6min · rebond 40% (24/48) (MFE +0.66%)
   - −4.0% : fill 30min 6% · séance 18% (32/159) · gap 2% · délai 200.1min · rebond 57% (20/32) (MFE +1.05%)
   - −5.0% : fill 30min 4% · séance 13% (24/159) · gap 0% · délai 397.7min · rebond 38% (11/24) (MFE +0.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.53% (p90 −2.17%) → stop au-delà de −1.55% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.63%) → stop au-delà de −0.96% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.45% (p90 −1.66%) → stop au-delà de −0.95% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=526 jambes) : jambe baissière méd −1.04% (p90 −2.31%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 99% (53/54) · rebond 41% (26/53)
      · −2.0% : fill 84% (41/54) · rebond 49% (20/41)
      · −3.0% : fill 59% (30/54) · rebond 40% (14/30)
      · −4.0% : fill 39% (22/54) · rebond 75% (16/22)
      · −5.0% : fill 30% (18/54) · rebond 47% (10/18)
   - **flat** (18 séances) :
      · −1.0% : fill 59% (13/18) · rebond 64% (9/13)
      · −2.0% : fill 33% (8/18) · rebond 68% (6/8)
      · −3.0% : fill 20% (5/18) · rebond 48% (3/5)
      · −4.0% : fill 6% (3/18) · rebond 59% (2/3)
      · −5.0% : fill 5% (2/18) · rebond 0% (0/2)
   - **gap-up** (87 séances) :
      · −1.0% : fill 46% (41/87) · rebond 61% (24/41)
      · −2.0% : fill 23% (24/87) · rebond 46% (15/24)
      · −3.0% : fill 13% (13/87) · rebond 36% (7/13)
      · −4.0% : fill 9% (7/87) · rebond 11% (2/7)
      · −5.0% : fill 5% (4/87) · rebond 12% (1/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 61% si les 15 1res min sont vertes (71 cas) · 30% si rouges (89 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:31** → P(séance verte=clôture>ouverture) 72% si début vert vs 21% si rouge (base 43% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 290min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **72%** · continue >prix actuel 56% ; creux résiduel méd -1.18% (q20 -2.25%) → **SL/trailing à −2.25%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.08% / q75 +2.1% → **scale +1.08% / runner +2.1%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **21%** (continue à baisser 57%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.96%** (au-delà de la MAE q10 -4.96%), cible rebond +1.06% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.97% .. +1.62%] · haut q95 +2.08% · bas q05 -2.65%
   - 60min (n=160) : retour [-2.5% .. +1.42%] · haut q95 +2.41% · bas q05 -3.07%
   - 2h (n=160) : retour [-2.53% .. +2.22%] · haut q95 +2.56% · bas q05 -3.58%
   - 4h (n=160) : retour [-2.61% .. +2.42%] · haut q95 +3.02% · bas q05 -4.04%
   - 6h (n=160) : retour [-3.22% .. +3.06%] · haut q95 +3.68% · bas q05 -4.31%
   - session (n=160) : retour [-5.78% .. +2.83%] · haut q95 +4.66% · bas q05 -6.21%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.37%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.53 · part idiosyncratique 0.47
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.8  _(survente)_
- **ADX** : 18.7  _(pas de tendance nette)_
- **MACD** : hist -2.123  _(pas de croisement recent)_
- **BB** : %B -0.11 · largeur 23.7%
- **ATR** : 6.15 (38.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.008  _(neutre)_
- **Vol ratio** : 1.78  _(volume au-dessus de la moyenne)_
- **Choppiness** : 35.0  _(marche directionnel)_
- **MA** : MA20 138.6 · MA50 143.0 · MA200 154.32  _(prix < MA20)_
- **Dist MA** : MA20 -14.4% · MA50 -17.0% · MA200 -23.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (784042 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
