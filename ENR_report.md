# ENR

**Generated** : 2026-10-27T21:44:20.703287+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €128.58  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot €128.58 (+0.8% vs entrée) · entrée €127.52 · stop €117.31 · T1 €130.53 · R/R 0.29  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-27 : 128.58 · ATR Wilder 5.88 (4.57 %)_
- **Swing** : plage **121.64 → 116.8** (-5.39 % a -9.16 % sous la cloture, 0.82 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 110.53 (-5.37 % sous le bas ; sous le support 113.47-114.51 (- 0,5 ATR)).
- **Deep** : plage **116.8 → 108.32** (-9.16 % a -15.76 % sous la cloture, 1.44 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 113.47-114.51 (A) ; 109.88-110.08 (C). stop INDICATIF 100.27 (-7.43 % sous le bas ; sous le support 103.21-104.4 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.81 ATR sous le plus haut 20 s., RSI(2) 76.2 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 122.83-124.46 (B, -3.2 %) ; 113.47-114.51 (A, -10.94 %) ; 109.88-110.08 (C, -14.39 %) ; 103.21-104.4 (B, -18.8 %) ; 98.56-100.32 (A, -21.98 %) ; 92.27-94.76 (A, -26.31 %)
- Resistances reelles au-dessus : 130.89-133.3 (A, 1.8 %) ; 133.85-135.72 (A, 4.1 %) ; 137.46-140.18 (A, 6.91 %) ; 143.38-146.08 (B, 11.51 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.67 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.51 %)** : le gap seul le franchit 0.549 % des séances (7 fois sur 1274).
   - exécution **2.238 pt plus bas** dans le cas TYPIQUE (médiane), 17.495 au p90, **29.247 au pire**
   - perte réelle **13.645 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 6.51 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0392 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.376 % | p01 -5.39 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0061** [0.0007 ; 0.0273] _(largeur 2.7 pt, n_eff 173.1)_
   - swing : **0.4592** [0.4072 ; 0.5119] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.437** [0.3854 ; 0.4896] _(largeur 10.4 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 81.3 observations effectives », dont la borne haute a 95 % vaut environ 3.7 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.75 %** | CVaR **-6.72 %** | vol 3.2 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 6.10 % contre 3.03 % aujourd'hui, rapport 2.02)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.88 % vs -9.83 % si l'on extrapolait par √5 _(rapport 0.903 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3426** (β de hausse 1.1036, asymétrie 1.2167) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.297× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 127.0739 sur atr_grid (0.25 ATR, 1.171 %) — p(stop avant cible) 0.9186 [0.89 ; 0.94], R/R 37.186, perte reelle 1.232 % (gap inclus), CVaR 2.287 %, EV -0.3227 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.7164 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 37.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.919, borne haute 0.944 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **4.18 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.155 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 21.3 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.71 ATR (stop 5.431 %) — p(stop avant cible) 0.5721 [0.52 ; 0.62], R/R 7.982, perte reelle 5.738 % (gap inclus), EV -0.6433 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.572, borne haute 0.624 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 8.64 % > budget 4.18 %
      - ⚠ support DETECTE a 0.71 ATR du spot — compartiment <1, mesure a 47.8 % de casse (IC clusterise [0.444 ; 0.509] sur 1198 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.64 %) : P(cible) 0.1 % x 45.80 % + P(rien) 42.7 % x 6.11 % ne couvrent pas P(stop) 57.2 % x 5.74 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_based a 1.5 ATR (stop 7.028 %) — p(stop avant cible) 0.4687 [0.42 ; 0.52], R/R 5.936, perte reelle 7.716 % (gap inclus), EV -1.0302 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.69 % > budget 4.18 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.03 %) : P(cible) 0.1 % x 45.80 % + P(rien) 53.1 % x 4.82 % ne couvrent pas P(stop) 46.9 % x 7.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 2.51 ATR (stop 13.872 %) — p(stop avant cible) 0.1042 [0.08 ; 0.14], R/R 3.101, perte reelle 14.77 % (gap inclus), EV 0.1007 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.74 % > budget 4.18 %
   - 🟢 support a 4.77 ATR (stop 24.443 %) — p(stop avant cible) 0.0041 [0.00 ; 0.02], R/R 1.682, perte reelle 27.236 % (gap inclus), EV 0.57 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.96 % > budget 4.18 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.171 %) — p(stop avant cible) 0.9186 [0.89 ; 0.94], R/R 37.186, perte reelle 1.232 % (gap inclus), EV -0.3227 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 37.19 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.919, borne haute 0.944 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 0.0 % x 45.80 % + P(rien) 8.1 % x 9.94 % ne couvrent pas P(stop) 91.9 % x 1.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🔴 grid_snapped a 0.71 ATR (stop 4.719 %) — p(stop avant cible) 0.6178 [0.57 ; 0.67], R/R 9.325, perte reelle 4.912 % (gap inclus), EV -0.5113 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 9.32 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.618, borne haute 0.668 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.99 % > budget 4.18 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 0.1 % x 45.80 % + P(rien) 38.2 % x 6.54 % ne couvrent pas P(stop) 61.8 % x 4.91 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 1.75 ATR (stop 8.199 %) — p(stop avant cible) 0.388 [0.34 ; 0.44], R/R 5.1, perte reelle 8.98 % (gap inclus), EV -0.8793 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.25 % > budget 4.18 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 0.1 % x 45.80 % + P(rien) 61.1 % x 4.22 % ne couvrent pas P(stop) 38.8 % x 8.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 9.37 %) — p(stop avant cible) 0.317 [0.27 ; 0.37], R/R 4.542, perte reelle 10.085 % (gap inclus), EV -0.7069 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.54 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.27 % > budget 4.18 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.71 %) : P(cible) 0.1 % x 45.80 % + P(rien) 68.2 % x 3.61 % ne couvrent pas P(stop) 31.7 % x 10.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 10.542 %) — p(stop avant cible) 0.2557 [0.21 ; 0.30], R/R 4.089, perte reelle 11.202 % (gap inclus), EV -0.5609 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.56 % > budget 4.18 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.56 %) : P(cible) 0.1 % x 45.80 % + P(rien) 74.4 % x 3.06 % ne couvrent pas P(stop) 25.6 % x 11.20 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+45.8 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 grid_snapped a 2.51 ATR (stop 13.16 %) — p(stop avant cible) 0.1226 [0.09 ; 0.16], R/R 3.265, perte reelle 14.027 % (gap inclus), EV 0.0572 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.26 % > budget 4.18 %
   - ⚪ atr_grid a 3.5 ATR (stop 16.398 %) — p(stop avant cible) 0.0429 [0.03 ; 0.07], R/R 2.611, perte reelle 17.543 % (gap inclus), EV 0.408 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.07 % > budget 4.18 %
   - ⚪ atr_grid a 4.0 ATR (stop 18.741 %) — p(stop avant cible) 0.0324 [0.02 ; 0.06], R/R 2.351, perte reelle 19.48 % (gap inclus), EV 0.4311 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.25 % > budget 4.18 %
   - ⚪ atr_grid a 4.5 ATR (stop 21.084 %) — p(stop avant cible) 0.0066 [0.00 ; 0.02], R/R 1.864, perte reelle 24.565 % (gap inclus), EV 0.526 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.27 % > budget 4.18 %
   - 🟢 grid_snapped a 4.77 ATR (stop 23.731 %) — p(stop avant cible) 0.0047 [0.00 ; 0.02], R/R 1.723, perte reelle 26.583 % (gap inclus), EV 0.5546 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.09 % > budget 4.18 %
   - ⚪ atr_grid a 5.5 ATR (stop 25.769 %) — p(stop avant cible) 0.0035 [0.00 ; 0.01], R/R 1.626, perte reelle 28.163 % (gap inclus), EV 0.586 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.63 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.84 % > budget 4.18 %
   - ⚪ atr_grid a 6.0 ATR (stop 28.111 %) — p(stop avant cible) 0.0029 [0.00 ; 0.01], R/R 1.554, perte reelle 29.476 % (gap inclus), EV 0.595 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.72 % > budget 4.18 %
   - ⚪ atr_grid a 6.5 ATR (stop 30.454 %) — p(stop avant cible) 0.0017 [0.00 ; 0.01], R/R 1.449, perte reelle 31.6 % (gap inclus), EV 0.6075 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.45 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.47 % > budget 4.18 %
   - ⚪ atr_grid a 7.0 ATR (stop 32.797 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.358, perte reelle 33.73 % (gap inclus), EV 0.615 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.33 % > budget 4.18 %
   - ⚪ atr_grid a 7.5 ATR (stop 35.139 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.293, perte reelle 35.428 % (gap inclus), EV 0.6131 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.29 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.37 % > budget 4.18 %
   - ⚪ atr_grid a 8.0 ATR (stop 37.482 %) — p(stop avant cible) 0.0011 [0.00 ; 0.01], R/R 1.222, perte reelle 37.482 % (gap inclus), EV 0.6102 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.37 % > budget 4.18 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 128.58, ATR14 6.0243 (4.685 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.37 ATR = 1.734 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.234 % | 128.2788 | 91.42 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.469 % | 127.9776 | 83.63 % | 88.25 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.703 % | 127.6764 | 76.43 % | 82.43 % | 85.97 % | 88.71 % | 91.24 % | 93.37 % |
| 0.2 ATR | 0.937 % | 127.3751 | 70.41 % | 79.07 % | 83.0 % | 86.63 % | 89.45 % | 91.96 % |
| 0.25 ATR | 1.171 % | 127.0739 | 63.71 % | 74.63 % | 79.25 % | 83.37 % | 87.46 % | 90.65 % |
| 0.35 ATR | 1.64 % | 126.4715 | 52.07 % | 65.05 % | 70.45 % | 76.04 % | 82.29 % | 86.73 % |
| 0.5 ATR | 2.343 % | 125.5679 | 36.79 % | 52.12 % | 59.68 % | 66.73 % | 74.73 % | 80.7 % |
| 0.75 ATR | 3.514 % | 124.0618 | 19.72 % | 36.03 % | 45.45 % | 54.65 % | 65.57 % | 73.87 % |
| 1.0 ATR | 4.685 % | 122.5557 | 11.14 % | 25.77 % | 34.68 % | 44.55 % | 57.21 % | 65.93 % |
| 1.25 ATR | 5.857 % | 121.0496 | 6.11 % | 17.37 % | 25.2 % | 35.84 % | 48.56 % | 58.39 % |
| 1.5 ATR | 7.028 % | 119.5436 | 2.96 % | 11.25 % | 18.18 % | 28.12 % | 41.49 % | 52.16 % |
| 2.0 ATR | 9.37 % | 116.5314 | 0.79 % | 4.24 % | 8.99 % | 16.63 % | 28.56 % | 40.9 % |
| 2.5 ATR | 11.713 % | 113.5193 | 0.3 % | 2.07 % | 4.25 % | 9.9 % | 19.9 % | 31.16 % |
| 3.0 ATR | 14.056 % | 110.5071 | 0.1 % | 0.89 % | 2.08 % | 5.35 % | 12.94 % | 23.32 % |
| 4.0 ATR | 18.741 % | 104.4829 | 0.1 % | 0.39 % | 1.19 % | 2.48 % | 6.97 % | 12.86 % |
| 6.0 ATR | 28.111 % | 92.4343 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.56 ATR | 0.67 ATR | 0.75 ATR | 1.06 ATR | 1.34 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.61 ATR | 0.82 ATR | 1.02 ATR | 1.17 ATR | 1.59 ATR | 1.95 ATR |
| **3 s.** | 0.30 ATR | 0.67 ATR | 0.76 ATR | 1.04 ATR | 1.26 ATR | 1.44 ATR | 1.95 ATR | 2.42 ATR |
| **5 s.** | 0.37 ATR | 0.86 ATR | 0.99 ATR | 1.34 ATR | 1.64 ATR | 1.85 ATR | 2.49 ATR | 3.12 ATR |
| **10 s.** | 0.49 ATR | 1.21 ATR | 1.38 ATR | 1.83 ATR | 2.21 ATR | 2.49 ATR | 3.49 ATR | 4.82 ATR |
| **20 s.** | 0.71 ATR | 1.60 ATR | 1.82 ATR | 2.41 ATR | 2.89 ATR | 3.32 ATR | 4.76 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.419–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.611–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.514 %, prix 124.0617), p(touche) 36.03 % (en stress 90.2 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.76–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.685 %, prix 122.556), p(touche) 34.68 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (86.1 % des re-echantillons)
- **5 seance(s)** : plage utile 0.989–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.685 %, prix 122.556), p(touche) 44.55 % (en stress 99.01 %)  ✅ optimum identifie (90.6 % des re-echantillons)
- **10 seance(s)** : plage utile 1.376–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (7.028 %, prix 119.5434), p(touche) 41.49 % (en stress 100.0 %)  ✅ optimum identifie (92.9 % des re-echantillons)
- **20 seance(s)** : plage utile 1.818–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (9.37 %, prix 116.5321), p(touche) 40.9 % (en stress 99.0 %)  ✅ optimum identifie (90.8 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.058 | EV/share : €-0.587 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 26 % | T2 6 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 17.4 | bear 47.5 | side 35.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.826% → cible +2.362% / stop −8.0%, p_fill 77%, n_eff≈81.3) : P(cible|rempli) **21%** · **EV/risk -0.053** (×p_fill ; si rempli -0.55% du capital)
  - **swing** (entrée dip −1.825% → cible +7.564% / stop −4.772%, p_fill 69%, n_eff≈80.6) : P(cible|rempli) **11%** · **EV/risk -0.211** (×p_fill ; si rempli -1.47% du capital)
  - **deep** (entrée dip −2.812% → cible +8.664% / stop −7.231%, p_fill 67%, n_eff≈76.3) : P(cible|rempli) **15%** · **EV/risk -0.198** (×p_fill ; si rempli -2.13% du capital)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.58 · part idiosyncratique 0.42
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.4  _(momentum baissier)_
- **ADX** : 21.1  _(pas de tendance nette)_
- **MACD** : hist -1.42  _(pas de croisement recent)_
- **BB** : %B 0.27 · largeur 26.0%
- **ATR** : 6.02 (37.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.073  _(accumulation)_
- **Vol ratio** : 1.08  _(volume normal)_
- **Choppiness** : 37.2  _(marche directionnel)_
- **MA** : MA20 136.85 · MA50 141.69 · MA200 154.31  _(prix < MA20)_
- **Dist MA** : MA20 -6.0% · MA50 -9.3% · MA200 -16.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (800595 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
