# SOFI

**Generated** : 2026-10-12T00:32:09.708590+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.80  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $15.80 (+1.1% vs entrée) · entrée $15.63 · stop $14.38 · T1 $15.89 · R/R 0.21  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 16.4 < 20 (tendance pas encore confirmée) alors que Choppiness 37.1 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-09 : 15.8 · ATR Wilder 0.564 (3.57 %)_
- **Swing** : plage **15.06 → 14.65** (-4.67 % a -7.25 % sous la cloture, 0.72 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 14.78-14.93 (A) ; 14.42-14.68 (B). stop INDICATIF 14.09 (-3.85 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **14.65 → 13.61** (-7.25 % a -13.84 % sous la cloture, 1.85 ATR) — touchee 45 % → 15 % du temps en 20 seances ; supports reels dans la plage : 14.42-14.68 (B) ; 13.75-13.9 (B). stop INDICATIF 13.14 (-3.5 % sous le bas ; sous le support 13.42-13.6 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.83 ATR sous le plus haut 20 s., RSI(2) 72.8 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 15.2-15.22 (A, -3.67 %) ; 14.78-14.93 (A, -5.51 %) ; 14.42-14.68 (B, -7.09 %) ; 13.75-13.9 (B, -12.03 %) ; 13.42-13.6 (C, -13.92 %) ; 12.86-13.01 (B, -17.66 %)
- Resistances reelles au-dessus : 16.25-16.53 (A, 2.85 %) ; 16.61-16.8 (A, 5.13 %) ; 16.92-17.19 (A, 7.09 %) ; 17.58-17.85 (A, 11.27 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=5.82 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (5.62 %)** : le gap seul le franchit 1.595 % des séances (20 fois sur 1254).
   - exécution **1.3 pt plus bas** dans le cas TYPIQUE (médiane), 4.164 au p90, **5.485 au pire**
   - perte réelle **7.537 %** en moyenne _(tirée par la queue)_, jusqu'à **11.105 %** — au lieu des 5.62 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0306 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.204 % | p01 -6.517 % | pire -11.105 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0114** [0.0024 ; 0.0363] _(largeur 3.4 pt, n_eff 173.1)_
   - swing : **0.571** [0.5184 ; 0.6224] _(largeur 10.4 pt, n_eff 345.7)_
   - deep : **0.5321** [0.4794 ; 0.5842] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 78.9 observations effectives », dont la borne haute a 95 % vaut environ 3.8 %.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-5.8 %** | CVaR **-8.29 %** | vol 3.81 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 5.51 % contre 3.43 % aujourd'hui, rapport 1.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -14.5 % vs -14.19 % si l'on extrapolait par √5 _(rapport 1.022 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8122** (β de hausse 1.7171, asymétrie 1.0554) vs IWM — 604 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.344× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 14.6398 sur atr_grid (2.25 ATR, 7.343 %) — p(stop avant cible) 0.4846 [0.43 ; 0.54], R/R 7.885, perte reelle 7.694 % (gap inclus), CVaR 10.391 %, EV -0.9652 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.72 ATR (stop 4.359 %) — p(stop avant cible) 0.7113 [0.66 ; 0.76], R/R 12.937, perte reelle 4.689 % (gap inclus), EV -0.8895 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 12.94 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.711, borne haute 0.757 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 0.0 % x 60.67 % + P(rien) 28.9 % x 8.48 % ne couvrent pas P(stop) 71.1 % x 4.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ sr_based a 1.41 ATR (stop 6.606 %) — p(stop avant cible) 0.5303 [0.48 ; 0.58], R/R 8.829, perte reelle 6.871 % (gap inclus), EV -0.8289 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 8.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.530, borne haute 0.583 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.83 %) : P(cible) 0.0 % x 60.67 % + P(rien) 47.0 % x 5.99 % ne couvrent pas P(stop) 53.0 % x 6.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - 🟢 support a 1.78 ATR (stop 7.82 %) — p(stop avant cible) 0.452 [0.40 ; 0.50], R/R 7.422, perte reelle 8.174 % (gap inclus), EV -0.9798 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.98 %) : P(cible) 0.0 % x 60.67 % + P(rien) 54.8 % x 4.96 % ne couvrent pas P(stop) 45.2 % x 8.17 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 0.25 ATR (stop 0.816 %) — p(stop avant cible) 0.9449 [0.92 ; 0.97], R/R 69.376, perte reelle 0.874 % (gap inclus), EV -0.0629 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 69.38 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.945, borne haute 0.965 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.06 %) : P(cible) 0.0 % x 60.67 % + P(rien) 5.5 % x 13.85 % ne couvrent pas P(stop) 94.5 % x 0.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 0.72 ATR (stop 3.34 %) — p(stop avant cible) 0.7812 [0.74 ; 0.82], R/R 16.706, perte reelle 3.631 % (gap inclus), EV -0.9347 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 16.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.781, borne haute 0.822 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.93 %) : P(cible) 0.0 % x 60.67 % + P(rien) 21.9 % x 8.69 % ne couvrent pas P(stop) 78.1 % x 3.63 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ grid_snapped a 1.41 ATR (stop 5.587 %) — p(stop avant cible) 0.6126 [0.56 ; 0.66], R/R 10.182, perte reelle 5.958 % (gap inclus), EV -0.8771 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 10.18 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.613, borne haute 0.663 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 0.0 % x 60.67 % + P(rien) 38.7 % x 7.16 % ne couvrent pas P(stop) 61.3 % x 5.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.25 ATR (stop 7.343 %) — p(stop avant cible) 0.4846 [0.43 ; 0.54], R/R 7.885, perte reelle 7.694 % (gap inclus), EV -0.9652 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 7.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.97 %) : P(cible) 0.0 % x 60.67 % + P(rien) 51.5 % x 5.36 % ne couvrent pas P(stop) 48.5 % x 7.69 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 2.75 ATR (stop 8.975 %) — p(stop avant cible) 0.3939 [0.34 ; 0.45], R/R 6.409, perte reelle 9.466 % (gap inclus), EV -1.2122 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 6.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 0.0 % x 60.67 % + P(rien) 60.6 % x 4.15 % ne couvrent pas P(stop) 39.4 % x 9.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.0 ATR (stop 9.791 %) — p(stop avant cible) 0.3447 [0.30 ; 0.40], R/R 5.921, perte reelle 10.246 % (gap inclus), EV -1.2529 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.70 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.0 % x 60.67 % + P(rien) 65.5 % x 3.48 % ne couvrent pas P(stop) 34.5 % x 10.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 3.5 ATR (stop 11.422 %) — p(stop avant cible) 0.258 [0.21 ; 0.31], R/R 5.154, perte reelle 11.77 % (gap inclus), EV -1.037 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 5.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 13.21 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.04 %) : P(cible) 0.0 % x 60.67 % + P(rien) 74.2 % x 2.70 % ne couvrent pas P(stop) 25.8 % x 11.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.0 ATR (stop 13.054 %) — p(stop avant cible) 0.1867 [0.15 ; 0.23], R/R 4.553, perte reelle 13.324 % (gap inclus), EV -0.6736 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.55 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.67 %) : P(cible) 0.0 % x 60.67 % + P(rien) 81.3 % x 2.23 % ne couvrent pas P(stop) 18.7 % x 13.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 4.5 ATR (stop 14.686 %) — p(stop avant cible) 0.121 [0.09 ; 0.16], R/R 4.081, perte reelle 14.867 % (gap inclus), EV -0.5423 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 4.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.12 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.54 %) : P(cible) 0.0 % x 60.67 % + P(rien) 87.9 % x 1.43 % ne couvrent pas P(stop) 12.1 % x 14.87 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.0 ATR (stop 16.318 %) — p(stop avant cible) 0.0788 [0.05 ; 0.11], R/R 3.68, perte reelle 16.483 % (gap inclus), EV -0.3932 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 0.0 % x 60.67 % + P(rien) 92.1 % x 0.98 % ne couvrent pas P(stop) 7.9 % x 16.48 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 5.5 ATR (stop 17.95 %) — p(stop avant cible) 0.057 [0.04 ; 0.09], R/R 3.362, perte reelle 18.044 % (gap inclus), EV -0.3717 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 18.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 0.0 % x 60.67 % + P(rien) 94.3 % x 0.70 % ne couvrent pas P(stop) 5.7 % x 18.04 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.0 ATR (stop 19.581 %) — p(stop avant cible) 0.0475 [0.03 ; 0.07], R/R 3.093, perte reelle 19.612 % (gap inclus), EV -0.3931 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.09 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.49 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.39 %) : P(cible) 0.0 % x 60.67 % + P(rien) 95.2 % x 0.57 % ne couvrent pas P(stop) 4.8 % x 19.61 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 6.5 ATR (stop 21.213 %) — p(stop avant cible) 0.0328 [0.02 ; 0.06], R/R 2.845, perte reelle 21.323 % (gap inclus), EV -0.4152 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.85 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.07 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 0.0 % x 60.67 % + P(rien) 96.7 % x 0.29 % ne couvrent pas P(stop) 3.3 % x 21.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.0 ATR (stop 22.845 %) — p(stop avant cible) 0.0255 [0.01 ; 0.05], R/R 2.638, perte reelle 22.998 % (gap inclus), EV -0.4105 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.64 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.64 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.35 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.41 %) : P(cible) 0.0 % x 60.67 % + P(rien) 97.4 % x 0.18 % ne couvrent pas P(stop) 2.5 % x 23.00 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 7.5 ATR (stop 24.477 %) — p(stop avant cible) 0.0211 [0.01 ; 0.04], R/R 2.461, perte reelle 24.65 % (gap inclus), EV -0.4234 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.46 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.42 %) : P(cible) 0.0 % x 60.67 % + P(rien) 97.9 % x 0.10 % ne couvrent pas P(stop) 2.1 % x 24.65 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
   - ⚪ atr_grid a 8.0 ATR (stop 26.109 %) — p(stop avant cible) 0.0068 [0.00 ; 0.02], R/R 2.31, perte reelle 26.26 % (gap inclus), EV -0.3079 % — **REFUSE**
      - refuse : cible atteinte seulement 0.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.31 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.03 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.31 %) : P(cible) 0.0 % x 60.67 % + P(rien) 99.3 % x -0.13 % ne couvrent pas P(stop) 0.7 % x 26.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon. P(cible) nulle : la cible (+60.7 %) est hors d'atteinte a l'horizon ; verifier la cible avant de conclure.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 15.8, ATR14 0.5156 (3.264 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.378 ATR = 1.234 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.163 % | 15.7742 | 92.96 % | 95.77 % | 97.08 % | 97.47 % | 98.27 % | 98.87 % |
| 0.1 ATR | 0.326 % | 15.7484 | 85.21 % | 89.33 % | 92.04 % | 93.33 % | 95.53 % | 97.13 % |
| 0.15 ATR | 0.49 % | 15.7227 | 78.97 % | 84.59 % | 88.0 % | 90.4 % | 92.89 % | 94.87 % |
| 0.2 ATR | 0.653 % | 15.6969 | 71.73 % | 79.36 % | 83.37 % | 86.87 % | 90.56 % | 93.33 % |
| 0.25 ATR | 0.816 % | 15.6711 | 66.3 % | 75.03 % | 80.14 % | 84.34 % | 89.14 % | 92.1 % |
| 0.35 ATR | 1.142 % | 15.6195 | 52.82 % | 65.36 % | 72.18 % | 78.59 % | 85.69 % | 88.92 % |
| 0.5 ATR | 1.632 % | 15.5422 | 37.53 % | 53.27 % | 61.69 % | 69.39 % | 79.7 % | 84.82 % |
| 0.75 ATR | 2.448 % | 15.4133 | 20.42 % | 36.76 % | 46.88 % | 57.17 % | 70.15 % | 78.26 % |
| 1.0 ATR | 3.264 % | 15.2844 | 8.75 % | 24.47 % | 33.97 % | 45.15 % | 60.0 % | 69.74 % |
| 1.25 ATR | 4.079 % | 15.1554 | 4.23 % | 15.11 % | 24.09 % | 35.76 % | 50.96 % | 63.28 % |
| 1.5 ATR | 4.895 % | 15.0265 | 2.01 % | 9.47 % | 16.63 % | 27.37 % | 43.15 % | 56.92 % |
| 2.0 ATR | 6.527 % | 14.7687 | 0.7 % | 4.43 % | 8.37 % | 15.25 % | 29.64 % | 45.85 % |
| 2.5 ATR | 8.159 % | 14.5109 | 0.3 % | 1.91 % | 3.93 % | 9.49 % | 19.8 % | 36.1 % |
| 3.0 ATR | 9.791 % | 14.2531 | 0.1 % | 0.91 % | 2.82 % | 6.16 % | 13.71 % | 28.31 % |
| 4.0 ATR | 13.054 % | 13.7374 | 0.0 % | 0.3 % | 0.71 % | 2.53 % | 7.41 % | 14.67 % |
| 6.0 ATR | 19.581 % | 12.7061 | 0.0 % | 0.1 % | 0.2 % | 0.2 % | 0.91 % | 3.08 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.18 ATR | 0.38 ATR | 0.43 ATR | 0.57 ATR | 0.68 ATR | 0.76 ATR | 0.97 ATR | 1.21 ATR |
| **2 s.** | 0.25 ATR | 0.55 ATR | 0.62 ATR | 0.83 ATR | 0.99 ATR | 1.12 ATR | 1.48 ATR | 1.94 ATR |
| **3 s.** | 0.32 ATR | 0.70 ATR | 0.79 ATR | 1.02 ATR | 1.23 ATR | 1.39 ATR | 1.90 ATR | 2.38 ATR |
| **5 s.** | 0.41 ATR | 0.90 ATR | 1.00 ATR | 1.33 ATR | 1.60 ATR | 1.80 ATR | 2.46 ATR | 3.32 ATR |
| **10 s.** | 0.62 ATR | 1.28 ATR | 1.44 ATR | 1.88 ATR | 2.24 ATR | 2.49 ATR | 3.59 ATR | 4.74 ATR |
| **20 s.** | 0.85 ATR | 1.81 ATR | 2.04 ATR | 2.70 ATR | 3.24 ATR | 3.61 ATR | 4.81 ATR | 5.67 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.427–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (1.632 %, prix 15.5421), p(touche) 37.53 % (en stress 84.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 25.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.625–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.448 %, prix 15.4132), p(touche) 36.76 % (en stress 91.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 18.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.786–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.264 %, prix 15.2843), p(touche) 33.97 % (en stress 97.0 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 20.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.004–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.079 %, prix 15.1555), p(touche) 35.76 % (en stress 96.97 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 22.6 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.441–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (4.895 %, prix 15.0266), p(touche) 43.15 % (en stress 98.99 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 36.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.044–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.159 %, prix 14.5109), p(touche) 36.1 % (en stress 98.98 %)  ✅ optimum identifie (74.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 7.2 | bear 13.5 | side 79.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.065% → cible +1.649% / stop −8.0%, p_fill 75%, n_eff≈78.9) : P(cible|rempli) **42%** · **EV/risk -0.027** (×p_fill ; si rempli -0.29% du capital)
  - **swing** (entrée dip −2.357% → cible +3.737% / stop −3.342%, p_fill 59%, n_eff≈68.3) : P(cible|rempli) **49%** · **EV/risk +0.030** (×p_fill ; si rempli +0.17% du capital)
  - **deep** (entrée dip −3.634% → cible +5.355% / stop −5.08%, p_fill 59%, n_eff≈65.6) : P(cible|rempli) **48%** · **EV/risk +0.007** (×p_fill ; si rempli +0.06% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→64% · +2.0%→42% · +3.0%→30% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.06% (p90 6.61%) · excursion haute méd. +1.52% / basse méd. −2.06%
- Profil de vol intra : ouverture 2.849% vs midi 0.819% vs clôture 0.934% _(ouverture ~3.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 20% · trend ↑1%/↓0% ; spike-down 62% · recovery-V 23%)_
- **Régime intraday** : **chop** _(efficiency 0.153 ; neutre — autocorr -0.023)_ ; drift intra méd. -0.686% ; recovery-V 22%
- **σ réalisé intraday** 2.273% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 45% / bas 64% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 15.8262 (VA 15.8138–15.9262 ; dernier close 15.75)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 15% · rebond 61% · **stop −2.1%** sous le fill (sous le bruit) · cible +1.97% · R/R 0.94 (high win-rate)
- Gaps overnight (n=159) : méd. 0.17% · baisse 43% (gap-down >1% 22% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.59%) · haut méd +0.65% · range méd 1.42%
- Excursion ouverture 15min (n=160) : bas méd −1.01% (p90 −2.37%) · haut méd +0.79% · range méd 2.05%
- Excursion ouverture 30min (n=160) : bas méd −1.09% (p90 −3.24%) · haut méd +0.86% · range méd 2.37%
- Excursion ouverture 60min (n=160) : bas méd −1.22% (p90 −3.59%) · haut méd +0.99% · range méd 2.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.77 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 76% (120/159) · gap 30% · délai 0.1min · rebond 56% (69/120) (MFE +1.22%)
   - −1.0% : fill 30min 49% · séance 63% (105/159) · gap 22% · délai 1.5min · rebond 49% (57/105) (MFE +0.93%)
   - −1.5% : fill 30min 41% · séance 55% (94/159) · gap 19% · délai 6.8min · rebond 59% (61/94) (MFE +1.3%)
   - −2.0% : fill 30min 30% · séance 43% (73/159) · gap 8% · délai 9.8min · rebond 63% (50/73) (MFE +1.47%)
   - −3.0% : fill 30min 7% · séance 30% (52/159) · gap 2% · délai 78.7min · rebond 49% (32/52) (MFE +1.02%)
   - −4.0% : fill 30min 5% · séance 15% (30/159) · gap 1% · délai 86.8min · rebond 61% (19/30) (MFE +1.97%)
   - −5.0% : fill 30min 2% · séance 7% (15/159) · gap 1% · délai 208.5min · rebond 44% (8/15) (MFE +0.67%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.78%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.49% (p90 −1.87%) → stop au-delà de −1.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.39% (p90 −1.43%) → stop au-delà de −1.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=612 jambes) : jambe baissière méd −1.0% (p90 −2.74%) · ~7.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (64 séances) :
      · −1.0% : fill 98% (63/64) · rebond 49% (35/63)
      · −2.0% : fill 85% (54/64) · rebond 68% (37/54)
      · −3.0% : fill 59% (39/64) · rebond 49% (25/39)
      · −4.0% : fill 35% (25/64) · rebond 69% (17/25)
      · −5.0% : fill 15% (13/64) · rebond 52% (7/13)
   - **flat** (24 séances) :
      · −1.0% : fill 76% (16/24) · rebond 31% (6/16)
      · −2.0% : fill 39% (8/24) · rebond 53% (5/8)
      · −3.0% : fill 33% (7/24) · rebond 44% (3/7)
      · −4.0% : fill 11% (3/24) · rebond 30% (1/3)
      · −5.0% : fill 7% (1/24) · rebond 0% (0/1)
   - **gap-up** (71 séances) :
      · −1.0% : fill 32% (26/71) · rebond 65% (16/26)
      · −2.0% : fill 13% (11/71) · rebond 56% (8/11)
      · −3.0% : fill 7% (6/71) · rebond 60% (4/6)
      · −4.0% : fill 2% (2/71) · rebond 20% (1/2)
      · −5.0% : fill 0% (1/71) · rebond 100% (1/1)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 39% en base · 65% si les 15 1res min sont vertes (72 cas) · 22% si rouges (88 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **36min** → P(séance verte=clôture>ouverture) 71% si début vert vs 19% si rouge (base 39% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=72) : tient le vert **71%** · continue >prix actuel 51% ; creux résiduel méd -1.51% (q20 -2.67%) → **SL/trailing à −2.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.8% / q75 +2.64% → **scale +1.8% / runner +2.64%**, sortie à la clôture
  - **si ROUGE au coude** (n=88) : edge inversé — récupère vert seulement **19%** (continue à baisser 63%) → **RÉDUIRE ~81%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.79%** (au-delà de la MAE q10 -2.79%), cible rebond +1.12% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.96% .. +3.18%] · haut q95 +3.88% · bas q05 -3.58%
   - 60min (n=160) : retour [-3.13% .. +3.65%] · haut q95 +4.44% · bas q05 -3.99%
   - 2h (n=160) : retour [-3.52% .. +3.76%] · haut q95 +4.95% · bas q05 -4.15%
   - 4h (n=160) : retour [-3.89% .. +4.27%] · haut q95 +5.43% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.24% .. +4.07%] · haut q95 +5.44% · bas q05 -5.17%
   - session (n=160) : retour [-4.42% .. +4.63%] · haut q95 +5.47% · bas q05 -5.19%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (3) pour des stats fiables : 1.9% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.73%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.53 · part idiosyncratique 0.47
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 30.3  _(momentum baissier)_
- **ADX** : 16.4  _(pas de tendance nette)_
- **MACD** : hist -0.025  _(pas de croisement recent)_
- **BB** : %B 0.28 · largeur 15.4%
- **ATR** : 0.52 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.281  _(distribution)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 37.1  _(marche directionnel)_
- **MA** : MA20 16.36 · MA50 17.39 · MA200 18.67  _(prix < MA20)_
- **Dist MA** : MA20 -3.4% · MA50 -9.2% · MA200 -15.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (889599 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
