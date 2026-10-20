# ENR

**Generated** : 2026-10-20T21:43:31.275278+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €130.32  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (12 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot €130.32 (+1.2% vs entrée) · entrée €128.82 · stop €118.51 · T1 €131.47 · R/R 0.26  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-20 : 130.32 · ATR Wilder 5.37 (4.12 %)_
- **Swing** : plage **124.28 → 119.74** (-4.63 % a -8.12 % sous la cloture, 0.85 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 122.83-124.46 (A). stop INDICATIF 110.78 (-7.48 % sous le bas ; sous le support 113.47-114.51 (- 0,5 ATR)).
- **Deep** : plage **119.74 → 112.3** (-8.12 % a -13.83 % sous la cloture, 1.39 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 113.47-114.51 (A). stop INDICATIF 107.2 (-4.54 % sous le bas ; sous le support 109.88-110.08 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.85 ATR sous le plus haut 20 s., RSI(2) 13.0 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 122.83-124.46 (A, -4.5 %) ; 113.47-114.51 (A, -12.13 %) ; 109.88-110.08 (C, -15.53 %) ; 103.21-104.4 (B, -19.89 %) ; 98.56-100.32 (A, -23.02 %) ; 92.27-94.76 (A, -27.29 %)
- Resistances reelles au-dessus : 133.85-135.72 (A, 2.71 %) ; 137.46-139.16 (A, 5.48 %) ; 146.08-148.4 (A, 12.09 %) ; 150.58-151.76 (A, 15.55 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.67 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.59 %)** : le gap seul le franchit 0.549 % des séances (7 fois sur 1274).
   - exécution **2.158 pt plus bas** dans le cas TYPIQUE (médiane), 17.415 au p90, **29.167 au pire**
   - perte réelle **13.645 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 6.59 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0388 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.368 % | p01 -5.39 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0065** [0.0008 ; 0.028] _(largeur 2.7 pt, n_eff 173.1)_
   - swing : **0.4817** [0.4294 ; 0.5343] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.4757** [0.4234 ; 0.5284] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 69.1 observations effectives », dont la borne haute a 95 % vaut environ 4.3 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.65 %** | CVaR **-6.61 %** | vol 3.18 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 6.12 % contre 2.90 % aujourd'hui, rapport 2.11)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.86 % vs -9.76 % si l'on extrapolait par √5 _(rapport 0.908 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3379** (β de hausse 1.108, asymétrie 1.2075) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.281× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 122.7316 sur grid_snapped (1.13 ATR, 5.823 %) — p(stop avant cible) 0.5203 [0.47 ; 0.57], R/R 7.231, perte reelle 6.088 % (gap inclus), CVaR 8.333 %, EV -0.4895 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.3965 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.520, borne haute 0.573 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 8.33 % > budget 6.13 %
- Budget de queue : **6.13 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.264 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 36.1 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🟢 support a 1.13 ATR (stop 6.737 %) — p(stop avant cible) 0.4673 [0.42 ; 0.52], R/R 6.26, perte reelle 7.032 % (gap inclus), EV -0.6267 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 6.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 9.39 % > budget 6.13 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.63 %) : P(cible) 0.1 % x 44.02 % + P(rien) 53.2 % x 4.95 % ne couvrent pas P(stop) 46.7 % x 7.03 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 3.18 ATR (stop 15.066 %) — p(stop avant cible) 0.0567 [0.04 ; 0.08], R/R 2.717, perte reelle 16.2 % (gap inclus), EV 0.6329 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.72 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.35 % > budget 6.13 %
   - 🟢 support a 5.75 ATR (stop 25.495 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 1.569, perte reelle 28.059 % (gap inclus), EV 0.9723 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.57 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.32 % > budget 6.13 %
   - ⚪ atr_grid a 0.25 ATR (stop 1.016 %) — p(stop avant cible) 0.9182 [0.89 ; 0.94], R/R 40.918, perte reelle 1.076 % (gap inclus), EV -0.1768 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 40.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.918, borne haute 0.944 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 0.0 % x 44.02 % + P(rien) 8.2 % x 9.92 % ne couvrent pas P(stop) 91.8 % x 1.08 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.5 ATR (stop 2.031 %) — p(stop avant cible) 0.8296 [0.79 ; 0.87], R/R 20.671, perte reelle 2.13 % (gap inclus), EV -0.3252 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 20.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.830, borne haute 0.866 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.33 %) : P(cible) 0.0 % x 44.02 % + P(rien) 17.0 % x 8.46 % ne couvrent pas P(stop) 83.0 % x 2.13 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.75 ATR (stop 3.047 %) — p(stop avant cible) 0.7476 [0.70 ; 0.79], R/R 13.879, perte reelle 3.172 % (gap inclus), EV -0.2786 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 13.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.748, borne haute 0.791 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.28 %) : P(cible) 0.1 % x 44.02 % + P(rien) 25.2 % x 8.21 % ne couvrent pas P(stop) 74.8 % x 3.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 grid_snapped a 1.13 ATR (stop 5.823 %) — p(stop avant cible) 0.5203 [0.47 ; 0.57], R/R 7.231, perte reelle 6.088 % (gap inclus), EV -0.4895 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 7.23 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.520, borne haute 0.573 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 8.33 % > budget 6.13 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.49 %) : P(cible) 0.1 % x 44.02 % + P(rien) 47.9 % x 5.54 % ne couvrent pas P(stop) 52.0 % x 6.09 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.0 ATR (stop 8.125 %) — p(stop avant cible) 0.3713 [0.32 ; 0.42], R/R 5.101, perte reelle 8.631 % (gap inclus), EV -0.5278 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 5.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 11.83 % > budget 6.13 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.53 %) : P(cible) 0.1 % x 44.02 % + P(rien) 62.8 % x 4.22 % ne couvrent pas P(stop) 37.1 % x 8.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 9.141 %) — p(stop avant cible) 0.307 [0.26 ; 0.36], R/R 4.57, perte reelle 9.633 % (gap inclus), EV -0.3655 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.13 % > budget 6.13 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 0.1 % x 44.02 % + P(rien) 69.2 % x 3.71 % ne couvrent pas P(stop) 30.7 % x 9.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.5 ATR (stop 10.156 %) — p(stop avant cible) 0.262 [0.22 ; 0.31], R/R 4.142, perte reelle 10.628 % (gap inclus), EV -0.2955 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 4.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.61 % > budget 6.13 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.30 %) : P(cible) 0.1 % x 44.02 % + P(rien) 73.7 % x 3.34 % ne couvrent pas P(stop) 26.2 % x 10.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 11.172 %) — p(stop avant cible) 0.1936 [0.15 ; 0.24], R/R 3.723, perte reelle 11.826 % (gap inclus), EV -0.0918 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 3.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.66 % > budget 6.13 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.09 %) : P(cible) 0.1 % x 44.02 % + P(rien) 80.6 % x 2.69 % ne couvrent pas P(stop) 19.4 % x 11.83 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+44.0 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 grid_snapped a 3.18 ATR (stop 14.151 %) — p(stop avant cible) 0.0794 [0.05 ; 0.11], R/R 2.89, perte reelle 15.232 % (gap inclus), EV 0.507 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.89 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.89 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.87 % > budget 6.13 %
   - ⚪ atr_grid a 4.0 ATR (stop 16.25 %) — p(stop avant cible) 0.0324 [0.02 ; 0.06], R/R 2.459, perte reelle 17.902 % (gap inclus), EV 0.7868 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.93 % > budget 6.13 %
   - ⚪ atr_grid a 4.5 ATR (stop 18.281 %) — p(stop avant cible) 0.0238 [0.01 ; 0.04], R/R 2.259, perte reelle 19.486 % (gap inclus), EV 0.8273 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.26 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.26 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.61 % > budget 6.13 %
   - ⚪ atr_grid a 5.0 ATR (stop 20.313 %) — p(stop avant cible) 0.0117 [0.00 ; 0.03], R/R 1.984, perte reelle 22.186 % (gap inclus), EV 0.906 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.98 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.98 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.82 % > budget 6.13 %
   - ⚪ atr_grid a 5.5 ATR (stop 22.344 %) — p(stop avant cible) 0.0067 [0.00 ; 0.02], R/R 1.756, perte reelle 25.074 % (gap inclus), EV 0.9085 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.76 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.76 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.87 % > budget 6.13 %
   - 🟢 grid_snapped a 5.75 ATR (stop 24.581 %) — p(stop avant cible) 0.0042 [0.00 ; 0.02], R/R 1.614, perte reelle 27.281 % (gap inclus), EV 0.9558 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.61 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.47 % > budget 6.13 %
   - ⚪ atr_grid a 6.5 ATR (stop 26.406 %) — p(stop avant cible) 0.0036 [0.00 ; 0.01], R/R 1.55, perte reelle 28.405 % (gap inclus), EV 0.971 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.34 % > budget 6.13 %
   - ⚪ atr_grid a 7.0 ATR (stop 28.438 %) — p(stop avant cible) 0.003 [0.00 ; 0.01], R/R 1.486, perte reelle 29.626 % (gap inclus), EV 0.9803 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.20 % > budget 6.13 %
   - ⚪ atr_grid a 7.5 ATR (stop 30.469 %) — p(stop avant cible) 0.0018 [0.00 ; 0.01], R/R 1.393, perte reelle 31.612 % (gap inclus), EV 0.9925 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.39 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.94 % > budget 6.13 %
   - ⚪ atr_grid a 8.0 ATR (stop 32.5 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 1.313, perte reelle 33.537 % (gap inclus), EV 0.9996 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.78 % > budget 6.13 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 130.32, ATR14 5.2943 (4.063 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.369 ATR = 1.499 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.203 % | 130.0553 | 91.42 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.406 % | 129.7906 | 83.73 % | 88.25 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.609 % | 129.5259 | 76.43 % | 82.33 % | 85.87 % | 88.61 % | 91.14 % | 93.27 % |
| 0.2 ATR | 0.813 % | 129.2612 | 70.41 % | 78.97 % | 82.91 % | 86.53 % | 89.35 % | 91.86 % |
| 0.25 ATR | 1.016 % | 128.9964 | 63.81 % | 74.53 % | 79.15 % | 83.37 % | 87.36 % | 90.55 % |
| 0.35 ATR | 1.422 % | 128.467 | 51.97 % | 64.76 % | 70.16 % | 75.94 % | 82.09 % | 86.53 % |
| 0.5 ATR | 2.031 % | 127.6729 | 36.69 % | 51.83 % | 59.39 % | 66.53 % | 74.43 % | 80.4 % |
| 0.75 ATR | 3.047 % | 126.3493 | 19.63 % | 35.74 % | 45.06 % | 54.36 % | 65.17 % | 73.47 % |
| 1.0 ATR | 4.063 % | 125.0257 | 11.05 % | 25.47 % | 34.29 % | 44.26 % | 56.82 % | 65.53 % |
| 1.25 ATR | 5.078 % | 123.7022 | 6.11 % | 17.28 % | 24.9 % | 35.54 % | 48.16 % | 57.99 % |
| 1.5 ATR | 6.094 % | 122.3786 | 2.86 % | 11.06 % | 17.89 % | 27.72 % | 41.0 % | 51.66 % |
| 2.0 ATR | 8.125 % | 119.7314 | 0.79 % | 4.15 % | 8.79 % | 16.24 % | 28.06 % | 40.4 % |
| 2.5 ATR | 10.156 % | 117.0843 | 0.3 % | 2.07 % | 4.15 % | 9.5 % | 19.4 % | 30.65 % |
| 3.0 ATR | 12.188 % | 114.4372 | 0.1 % | 0.89 % | 2.08 % | 5.15 % | 12.44 % | 22.81 % |
| 4.0 ATR | 16.25 % | 109.1429 | 0.1 % | 0.39 % | 1.19 % | 2.48 % | 6.57 % | 12.46 % |
| 6.0 ATR | 24.375 % | 98.5543 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 1.05 ATR | 1.33 ATR |
| **2 s.** | 0.24 ATR | 0.53 ATR | 0.61 ATR | 0.82 ATR | 1.01 ATR | 1.17 ATR | 1.58 ATR | 1.94 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.03 ATR | 1.25 ATR | 1.43 ATR | 1.93 ATR | 2.41 ATR |
| **5 s.** | 0.36 ATR | 0.86 ATR | 0.98 ATR | 1.33 ATR | 1.62 ATR | 1.84 ATR | 2.46 ATR | 3.06 ATR |
| **10 s.** | 0.49 ATR | 1.20 ATR | 1.36 ATR | 1.81 ATR | 2.18 ATR | 2.46 ATR | 3.42 ATR | 4.72 ATR |
| **20 s.** | 0.69 ATR | 1.57 ATR | 1.80 ATR | 2.38 ATR | 2.86 ATR | 3.27 ATR | 4.69 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.418–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 24.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.606–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (3.047 %, prix 126.3492), p(touche) 35.74 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.0 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.751–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.063 %, prix 125.0251), p(touche) 34.29 % (en stress 91.18 %)  ✅ optimum identifie (84.9 % des re-echantillons)
- **5 seance(s)** : plage utile 0.982–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (4.063 %, prix 125.0251), p(touche) 44.26 % (en stress 99.01 %)  ✅ optimum identifie (88.6 % des re-echantillons)
- **10 seance(s)** : plage utile 1.36–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (6.094 %, prix 122.3783), p(touche) 41.0 % (en stress 100.0 %)  ✅ optimum identifie (91.5 % des re-echantillons)
- **20 seance(s)** : plage utile 1.796–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (8.125 %, prix 119.7315), p(touche) 40.4 % (en stress 99.0 %)  ✅ optimum identifie (89.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : -0.045 | EV/share : €-0.463 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 10 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 56.8 | side 38.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.152% → cible +2.055% / stop −8.0%, p_fill 65%, n_eff≈69.1) : P(cible|rempli) **26%** · **EV/risk -0.032** (×p_fill ; si rempli -0.40% du capital)
  - **swing** (entrée dip −2.527% → cible +6.958% / stop −4.168%, p_fill 52%, n_eff≈62.8) : P(cible|rempli) **23%** · **EV/risk -0.075** (×p_fill ; si rempli -0.60% du capital)
  - **deep** (entrée dip −3.916% → cible +8.496% / stop −6.342%, p_fill 59%, n_eff≈66.9) : P(cible|rempli) **26%** · **EV/risk -0.076** (×p_fill ; si rempli -0.82% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→77% · +1.0%→62% · +2.0%→38% · +3.0%→18% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.7% (p90 6.11%) · excursion haute méd. +1.52% / basse méd. −1.74%
- Profil de vol intra : ouverture 1.958% vs midi 0.866% vs clôture 1.062% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 90% · range 10% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.108 ; mean-reverting — autocorr -0.038)_ ; drift intra méd. -0.357% ; recovery-V 20%
- **σ réalisé intraday** 2.187% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 67% / bas 72% / whipsaw 38%
- POC intraday (dernière séance, temps-au-prix) : 146.1558 (VA 145.4312–146.3972 ; dernier close 145.44)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 49% · rebond 59% · **stop −3.83%** sous le fill (sous le bruit) · cible +1.48% · R/R 0.39 (high win-rate)
- Gaps overnight (n=159) : méd. 0.47% · baisse 33% (gap-down >1% 15% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.53% (p90 −1.67%) · haut méd +0.44% · range méd 1.12%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.17%) · haut méd +0.59% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.23%) · haut méd +0.62% · range méd 1.68%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.44%) · haut méd +0.73% · range méd 1.79%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 145.42 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 49% · séance 69% (116/159) · gap 24% · délai 0.5min · rebond 58% (62/116) (MFE +1.2%)
   - −1.0% : fill 30min 38% · séance 64% (108/159) · gap 15% · délai 10.3min · rebond 61% (62/108) (MFE +1.36%)
   - −1.5% : fill 30min 25% · séance 49% (88/159) · gap 11% · délai 22.9min · rebond 59% (50/88) (MFE +1.48%)
   - −2.0% : fill 30min 17% · séance 40% (73/159) · gap 8% · délai 62.1min · rebond 54% (44/73) (MFE +1.08%)
   - −3.0% : fill 30min 9% · séance 22% (46/159) · gap 2% · délai 189.8min · rebond 44% (26/46) (MFE +0.86%)
   - −4.0% : fill 30min 6% · séance 14% (33/159) · gap 1% · délai 76.7min · rebond 58% (22/33) (MFE +1.12%)
   - −5.0% : fill 30min 2% · séance 11% (24/159) · gap 0% · délai 388.5min · rebond 43% (12/24) (MFE +0.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.46% (p90 −1.72%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.33% (p90 −1.32%) → stop au-delà de −0.83% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −0.95%) → stop au-delà de −0.7% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=521 jambes) : jambe baissière méd −1.02% (p90 −2.33%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (53 séances) :
      · −1.0% : fill 98% (52/53) · rebond 55% (28/52)
      · −2.0% : fill 75% (39/53) · rebond 44% (20/39)
      · −3.0% : fill 45% (27/53) · rebond 33% (14/27)
      · −4.0% : fill 37% (22/53) · rebond 60% (16/22)
      · −5.0% : fill 31% (18/53) · rebond 49% (11/18)
   - **flat** (17 séances) :
      · −1.0% : fill 78% (14/17) · rebond 65% (10/14)
      · −2.0% : fill 44% (9/17) · rebond 67% (6/9)
      · −3.0% : fill 27% (6/17) · rebond 46% (3/6)
      · −4.0% : fill 9% (4/17) · rebond 52% (2/4)
      · −5.0% : fill 7% (3/17) · rebond 0% (0/3)
   - **gap-up** (89 séances) :
      · −1.0% : fill 43% (42/89) · rebond 66% (24/42)
      · −2.0% : fill 21% (25/89) · rebond 65% (18/25)
      · −3.0% : fill 8% (13/89) · rebond 72% (9/13)
      · −4.0% : fill 4% (7/89) · rebond 47% (4/7)
      · −5.0% : fill 2% (3/89) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 66% si les 15 1res min sont vertes (75 cas) · 24% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:29** → P(séance verte=clôture>ouverture) 73% si début vert vs 22% si rouge (base 44% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 219min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **73%** · continue >prix actuel 54% ; creux résiduel méd -1.07% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.24% / q75 +2.25% → **scale +1.24% / runner +2.25%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 59%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.65%** (au-delà de la MAE q10 -3.65%), cible rebond +1.13% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.93% .. +1.69%] · haut q95 +2.36% · bas q05 -2.59%
   - 60min (n=160) : retour [-2.46% .. +1.94%] · haut q95 +2.55% · bas q05 -2.86%
   - 2h (n=160) : retour [-2.78% .. +2.36%] · haut q95 +2.76% · bas q05 -3.56%
   - 4h (n=160) : retour [-3.15% .. +2.63%] · haut q95 +3.22% · bas q05 -3.93%
   - 6h (n=160) : retour [-3.69% .. +3.35%] · haut q95 +4.15% · bas q05 -4.56%
   - session (n=160) : retour [-4.9% .. +3.08%] · haut q95 +4.77% · bas q05 -6.18%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.53 · part idiosyncratique 0.47
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 32.9  _(momentum baissier)_
- **ADX** : 14.0  _(pas de tendance nette)_
- **MACD** : hist -1.284  _(pas de croisement recent)_
- **BB** : %B -0.03 · largeur 14.6%
- **ATR** : 5.29 (30.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.02  _(neutre)_
- **Vol ratio** : 1.04  _(volume normal)_
- **Choppiness** : 38.9  _(transition)_
- **MA** : MA20 141.34 · MA50 145.17 · MA200 154.36  _(prix < MA20)_
- **Dist MA** : MA20 -7.8% · MA50 -10.2% · MA200 -15.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (781455 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
