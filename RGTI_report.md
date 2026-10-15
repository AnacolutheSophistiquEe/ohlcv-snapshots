# RGTI

**Generated** : 2026-10-15T00:24:46.752306+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 1/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $11.67  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 22/125 fenêtres (p_fill pondéré 15 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot $11.67 (+7.0% vs entrée) · entrée $10.91 · stop $10.68 · T1 $11.29 · R/R 1.65  
> ↳ ¼-Kelly 0.011 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.1% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +21.3 % ≠ (strike 15.5 − spot 11.67)/spot = +32.8 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 334 % hors [0,100] (R² max 0.90). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 14.8 < 20 (tendance pas encore confirmée) alors que Choppiness 23.5 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-14 : 11.67 · ATR Wilder 0.8505 (7.29 %)_
- **Swing** : plage **10.64 → 10.22** (-8.8 % a -12.44 % sous la cloture, 0.5 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 10.05-10.31 (A). stop INDICATIF 9.07 (-11.19 % sous le bas ; sous le support 9.5-9.74 (- 0,5 ATR)).
- **Deep** : plage **10.22 → 9.18** (-12.44 % a -21.34 % sous la cloture, 1.22 ATR) — touchee 43 % → 15 % du temps en 20 seances ; supports reels dans la plage : 10.05-10.31 (A) ; 9.5-9.74 (C). stop INDICATIF 8.49 (-7.45 % sous le bas ; sous le support 8.92-9.14 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 7.04 ATR sous le plus haut 20 s., RSI(2) 0.0. Limite **11.24** (seance suivante), stop catastrophe 7.84, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 10.71-10.92 (A, -6.43 %) ; 10.05-10.31 (A, -11.65 %) ; 9.5-9.74 (C, -16.54 %) ; 8.92-9.14 (A, -21.68 %) ; 8.35-8.45 (B, -27.59 %) ; 6.86-7.03 (B, -39.8 %)
- Resistances reelles au-dessus : 12.34-12.75 (A, 5.74 %) ; 13.13-13.41 (B, 12.51 %) ; 13.56-13.82 (A, 16.2 %) ; 14.24-14.6 (A, 22.02 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.54 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (19.6 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1253).
   - exécution **11.613 pt plus bas** dans le cas TYPIQUE (médiane), 11.613 au p90, **11.613 au pire**
   - perte réelle **31.213 %** en moyenne _(tirée par la queue)_, jusqu'à **31.213 %** — au lieu des 19.6 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0093 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.113 % | p01 -8.973 % | pire -31.213 % _(sur 1253 séances)_
- **P(stop avant cible)** _(source : daily, 1254 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5101** [0.436 ; 0.5839] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.4766** [0.4243 ; 0.5293] _(largeur 10.5 pt, n_eff 345.7)_
   - deep : **0.4802** [0.4279 ; 0.5328] _(largeur 10.5 pt, n_eff 345.7)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (40.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.94 %** | CVaR **-11.24 %** | vol 6.82 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 19.44 % contre 6.20 % aujourd'hui, rapport 3.14)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -21.76 % vs -22.11 % si l'on extrapolait par √5 _(rapport 0.984 ; < 1 = le √5 surestime)_
- **β de baisse : 1.8333** (β de hausse 2.0008, asymétrie 0.9163) vs IWM — 606 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.53× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 10.5265 sur atr_based (1.5 ATR, 9.799 %) — p(stop avant cible) 0.6189 [0.57 ; 0.67], R/R 2.698, perte reelle 9.964 % (gap inclus), CVaR 11.762 %, EV -1.1357 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3289 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.619, borne haute 0.669 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 2.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel (temoin fige) — ⚠ le budget DERIVE a bien ete calcule, et **il ne differencie plus rien** : 23 des 23 lignes protegeables butent sur une borne. Il est donc CITE mais ne dimensionne pas — une mesure inutilisable ne dimensionne jamais.
   - le noyau permanent preleve 27.9 % de la queue et il ne reste que 13.84 EUR a partager. Prix du risque 0.004 : chaque ligne devrait ramener sa perte de queue a ce multiple — autant dire que c'est hors d'atteinte.
   - **Le geste n'est pas de resserrer les stops, c'est de reduire la TAILLE.** Proposer des stops tres serres ici reviendrait a s'appuyer sur un chiffre qui dit precisement que le probleme est ailleurs.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.799 %) — p(stop avant cible) 0.6189 [0.57 ; 0.67], R/R 2.698, perte reelle 9.964 % (gap inclus), EV -1.1357 % — **REFUSE**
      - refuse : cible atteinte seulement 14.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.70 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.619, borne haute 0.669 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.14 %) : P(cible) 14.8 % x 26.88 % + P(rien) 23.3 % x 4.50 % ne couvrent pas P(stop) 61.9 % x 9.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 1.633 %) — p(stop avant cible) 0.9223 [0.89 ; 0.95], R/R 15.709, perte reelle 1.711 % (gap inclus), EV 0.0606 % — **REFUSE**
      - refuse : cible atteinte seulement 5.3 % du temps (< 15 %) meme a 10 seances : le R/R de 15.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.922, borne haute 0.947 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - ⚪ atr_grid a 0.5 ATR (stop 3.266 %) — p(stop avant cible) 0.8457 [0.80 ; 0.88], R/R 7.948, perte reelle 3.382 % (gap inclus), EV -0.0659 % — **REFUSE**
      - refuse : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 7.95 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.846, borne haute 0.881 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.07 %) : P(cible) 8.5 % x 26.88 % + P(rien) 6.9 % x 7.38 % ne couvrent pas P(stop) 84.6 % x 3.38 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 4.899 %) — p(stop avant cible) 0.7923 [0.75 ; 0.83], R/R 5.408, perte reelle 4.971 % (gap inclus), EV -0.5013 % — **REFUSE**
      - refuse : cible atteinte seulement 9.9 % du temps (< 15 %) meme a 10 seances : le R/R de 5.41 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.792, borne haute 0.833 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.50 %) : P(cible) 9.9 % x 26.88 % + P(rien) 10.9 % x 7.14 % ne couvrent pas P(stop) 79.2 % x 4.97 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.0 ATR (stop 6.533 %) — p(stop avant cible) 0.7181 [0.67 ; 0.76], R/R 4.022, perte reelle 6.683 % (gap inclus), EV -0.4334 % — **REFUSE**
      - refuse : cible atteinte seulement 12.6 % du temps (< 15 %) meme a 10 seances : le R/R de 4.02 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.718, borne haute 0.764 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.43 %) : P(cible) 12.6 % x 26.88 % + P(rien) 15.6 % x 6.27 % ne couvrent pas P(stop) 71.8 % x 6.68 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.25 ATR (stop 8.166 %) — p(stop avant cible) 0.6586 [0.61 ; 0.71], R/R 3.238, perte reelle 8.301 % (gap inclus), EV -0.772 % — **REFUSE**
      - refuse : cible atteinte seulement 13.6 % du temps (< 15 %) meme a 10 seances : le R/R de 3.24 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.659, borne haute 0.707 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.77 %) : P(cible) 13.6 % x 26.88 % + P(rien) 20.6 % x 5.11 % ne couvrent pas P(stop) 65.9 % x 8.30 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 11.432 %) — p(stop avant cible) 0.5504 [0.50 ; 0.60], R/R 2.321, perte reelle 11.582 % (gap inclus), EV -1.2055 % — **REFUSE**
      - refuse : p_stop_first 0.550, borne haute 0.602 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.32 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.08 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.21 %) : P(cible) 15.7 % x 26.88 % + P(rien) 29.3 % x 3.26 % ne couvrent pas P(stop) 55.0 % x 11.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 13.065 %) — p(stop avant cible) 0.4572 [0.41 ; 0.51], R/R 2.03, perte reelle 13.245 % (gap inclus), EV -0.7639 % — **REFUSE**
      - refuse : R/R 2.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.69 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.76 %) : P(cible) 16.2 % x 26.88 % + P(rien) 38.1 % x 2.48 % ne couvrent pas P(stop) 45.7 % x 13.25 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 14.698 %) — p(stop avant cible) 0.3964 [0.35 ; 0.45], R/R 1.799, perte reelle 14.945 % (gap inclus), EV -0.8765 % — **REFUSE**
      - refuse : R/R 1.80 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.65 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.88 %) : P(cible) 16.7 % x 26.88 % + P(rien) 43.7 % x 1.30 % ne couvrent pas P(stop) 39.6 % x 14.94 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 16.332 %) — p(stop avant cible) 0.3241 [0.28 ; 0.37], R/R 1.625, perte reelle 16.545 % (gap inclus), EV -0.5867 % — **REFUSE**
      - refuse : R/R 1.62 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.71 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.59 %) : P(cible) 17.5 % x 26.88 % + P(rien) 50.1 % x 0.15 % ne couvrent pas P(stop) 32.4 % x 16.55 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 17.965 %) — p(stop avant cible) 0.2534 [0.21 ; 0.30], R/R 1.475, perte reelle 18.226 % (gap inclus), EV -0.3597 % — **REFUSE**
      - refuse : R/R 1.47 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.29 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 17.9 % x 26.88 % + P(rien) 56.8 % x -0.97 % ne couvrent pas P(stop) 25.3 % x 18.23 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 19.598 %) — p(stop avant cible) 0.2109 [0.17 ; 0.26], R/R 1.352, perte reelle 19.883 % (gap inclus), EV -0.3237 % — **REFUSE**
      - refuse : R/R 1.35 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.32 %) : P(cible) 18.3 % x 26.88 % + P(rien) 60.6 % x -1.75 % ne couvrent pas P(stop) 21.1 % x 19.88 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 22.864 %) — p(stop avant cible) 0.1231 [0.09 ; 0.16], R/R 1.157, perte reelle 23.225 % (gap inclus), EV -0.0992 % — **REFUSE**
      - refuse : R/R 1.16 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.75 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.10 %) : P(cible) 18.4 % x 26.88 % + P(rien) 69.2 % x -3.17 % ne couvrent pas P(stop) 12.3 % x 23.22 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 26.13 %) — p(stop avant cible) 0.0789 [0.05 ; 0.11], R/R 1.018, perte reelle 26.413 % (gap inclus), EV 0.057 % — **REFUSE**
      - refuse : R/R 1.02 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.58 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 29.397 %) — p(stop avant cible) 0.0587 [0.04 ; 0.09], R/R 0.908, perte reelle 29.607 % (gap inclus), EV 0.0607 % — **REFUSE**
      - refuse : R/R 0.91 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.64 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 32.663 %) — p(stop avant cible) 0.0363 [0.02 ; 0.06], R/R 0.818, perte reelle 32.879 % (gap inclus), EV 0.099 % — **REFUSE**
      - refuse : R/R 0.82 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.34 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 35.929 %) — p(stop avant cible) 0.0224 [0.01 ; 0.04], R/R 0.742, perte reelle 36.208 % (gap inclus), EV 0.1507 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.34 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 39.196 %) — p(stop avant cible) 0.012 [0.00 ; 0.03], R/R 0.682, perte reelle 39.418 % (gap inclus), EV 0.1863 % — **REFUSE**
      - refuse : R/R 0.68 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.60 % > budget 12.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 42.462 %) — p(stop avant cible) 0.0047 [0.00 ; 0.02], R/R 0.633, perte reelle 42.462 % (gap inclus), EV 0.2456 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.30 % > budget 12.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 45.728 %) — p(stop avant cible) 0.0043 [0.00 ; 0.02], R/R 0.583, perte reelle 46.089 % (gap inclus), EV 0.2394 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.53 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 48.995 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.549, perte reelle 48.995 % (gap inclus), EV 0.2389 % — **REFUSE**
      - refuse : R/R 0.55 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.51 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 52.261 %) — p(stop avant cible) 0.0025 [0.00 ; 0.01], R/R 0.504, perte reelle 53.343 % (gap inclus), EV 0.2263 % — **REFUSE**
      - refuse : R/R 0.50 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.72 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 11.67, ATR14 0.7624 (6.533 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.409 ATR = 2.672 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.327 % | 11.6319 | 92.04 % | 94.35 % | 95.56 % | 96.97 % | 97.46 % | 98.56 % |
| 0.1 ATR | 0.653 % | 11.5938 | 86.4 % | 91.03 % | 92.43 % | 94.94 % | 95.93 % | 97.43 % |
| 0.15 ATR | 0.98 % | 11.5556 | 80.87 % | 87.3 % | 89.1 % | 92.01 % | 94.0 % | 96.1 % |
| 0.2 ATR | 1.307 % | 11.5175 | 74.32 % | 82.76 % | 85.57 % | 88.78 % | 91.46 % | 94.46 % |
| 0.25 ATR | 1.633 % | 11.4794 | 68.18 % | 78.53 % | 81.63 % | 85.74 % | 88.92 % | 92.51 % |
| 0.35 ATR | 2.286 % | 11.4032 | 55.69 % | 68.75 % | 74.07 % | 79.68 % | 84.55 % | 89.63 % |
| 0.5 ATR | 3.266 % | 11.2888 | 41.19 % | 57.26 % | 65.09 % | 71.89 % | 79.17 % | 85.32 % |
| 0.75 ATR | 4.899 % | 11.0982 | 21.75 % | 39.11 % | 50.25 % | 59.25 % | 70.83 % | 78.95 % |
| 1.0 ATR | 6.533 % | 10.9076 | 9.77 % | 24.19 % | 33.91 % | 47.02 % | 61.99 % | 72.48 % |
| 1.25 ATR | 8.166 % | 10.7171 | 4.13 % | 14.82 % | 23.92 % | 37.21 % | 52.85 % | 64.99 % |
| 1.5 ATR | 9.799 % | 10.5265 | 1.81 % | 7.16 % | 13.82 % | 25.78 % | 43.09 % | 56.88 % |
| 2.0 ATR | 13.065 % | 10.1453 | 0.4 % | 1.81 % | 4.04 % | 11.02 % | 25.41 % | 40.55 % |
| 2.5 ATR | 16.332 % | 9.7641 | 0.1 % | 0.4 % | 1.21 % | 4.45 % | 14.63 % | 28.23 % |
| 3.0 ATR | 19.598 % | 9.3829 | 0.0 % | 0.2 % | 0.5 % | 1.52 % | 7.32 % | 16.53 % |
| 4.0 ATR | 26.13 % | 8.6206 | 0.0 % | 0.1 % | 0.2 % | 0.61 % | 1.93 % | 3.9 % |
| 6.0 ATR | 39.196 % | 7.0959 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.3 % | 0.62 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.41 ATR | 0.46 ATR | 0.60 ATR | 0.71 ATR | 0.79 ATR | 0.99 ATR | 1.21 ATR |
| **2 s.** | 0.29 ATR | 0.60 ATR | 0.67 ATR | 0.85 ATR | 0.99 ATR | 1.11 ATR | 1.41 ATR | 1.70 ATR |
| **3 s.** | 0.34 ATR | 0.75 ATR | 0.83 ATR | 1.02 ATR | 1.22 ATR | 1.35 ATR | 1.70 ATR | 1.95 ATR |
| **5 s.** | 0.44 ATR | 0.94 ATR | 1.05 ATR | 1.34 ATR | 1.53 ATR | 1.70 ATR | 2.08 ATR | 2.46 ATR |
| **10 s.** | 0.62 ATR | 1.32 ATR | 1.45 ATR | 1.78 ATR | 2.02 ATR | 2.25 ATR | 2.82 ATR | 3.43 ATR |
| **20 s.** | 0.90 ATR | 1.71 ATR | 1.86 ATR | 2.31 ATR | 2.64 ATR | 2.85 ATR | 3.52 ATR | 3.91 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.461–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (3.266 %, prix 11.2889), p(touche) 41.19 % (en stress 86.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.2 % des re-echantillons)
- **2 seance(s)** : plage utile 0.669–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (4.899 %, prix 11.0983), p(touche) 39.11 % (en stress 93.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 40.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.83–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (6.533 %, prix 10.9076), p(touche) 33.91 % (en stress 89.0 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.5 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.051–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (8.166 %, prix 10.717), p(touche) 37.21 % (en stress 94.95 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 34.4 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.451–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (9.799 %, prix 10.5265), p(touche) 43.09 % (en stress 96.97 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.4 % des re-echantillons)
- **20 seance(s)** : plage utile 1.864–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (13.065 %, prix 10.1453), p(touche) 40.55 % (en stress 97.96 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 49.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.033 | EV/share : $0.007 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 — | T3 —
- Kelly (position) : f* 0.044 | ¼-Kelly 0.011 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 27.0 | side 68.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −6.53% → cible +3.495% / stop −2.097%, p_fill 15%, n_eff≈18.7) : P(cible|rempli) **34%** · **EV/risk +0.037** (×p_fill ; si rempli +0.52% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=8, n_eff=8))
  - **deep** : indisponible (échantillon insuffisant (n=4, n_eff=4))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→87% · +1.0%→77% · +2.0%→64% · +3.0%→46% · +5.0%→31% · +8.0%→10%
- Range intraday médian 6.8% (p90 11.03%) · excursion haute méd. +2.76% / basse méd. −2.46%
- Profil de vol intra : ouverture 4.714% vs midi 1.402% vs clôture 1.624% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 79% · range 21% · trend ↑0%/↓0% ; spike-down 65% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; neutre — autocorr -0.001)_ ; drift intra méd. -0.541% ; recovery-V 20%
- **σ réalisé intraday** 3.707% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 62% / whipsaw 20%
- POC intraday (dernière séance, temps-au-prix) : 15.5684 (VA 15.2377–15.7574 ; dernier close 15.26)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 37% · rebond 75% · **stop −5.27%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. -0.2% · baisse 55% (gap-down >1% 36% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.8% (p90 −2.87%) · haut méd +1.18% · range méd 2.39%
- Excursion ouverture 15min (n=160) : bas méd −1.22% (p90 −3.58%) · haut méd +1.56% · range méd 3.3%
- Excursion ouverture 30min (n=160) : bas méd −1.45% (p90 −4.44%) · haut méd +1.84% · range méd 3.8%
- Excursion ouverture 60min (n=160) : bas méd −1.69% (p90 −5.46%) · haut méd +2.09% · range méd 4.51%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 15.25 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 80% (130/159) · gap 44% · délai 0.0min · rebond 63% (83/130) (MFE +1.59%)
   - −1.0% : fill 30min 60% · séance 71% (119/159) · gap 36% · délai 0.0min · rebond 70% (78/119) (MFE +1.68%)
   - −1.5% : fill 30min 54% · séance 63% (111/159) · gap 27% · délai 0.0min · rebond 68% (74/111) (MFE +1.92%)
   - −2.0% : fill 30min 48% · séance 57% (102/159) · gap 22% · délai 0.2min · rebond 67% (68/102) (MFE +2.13%)
   - −3.0% : fill 30min 33% · séance 48% (89/159) · gap 8% · délai 8.9min · rebond 65% (63/89) (MFE +1.87%)
   - −4.0% : fill 30min 24% · séance 37% (67/159) · gap 5% · délai 15.3min · rebond 75% (50/67) (MFE +2.24%)
   - −5.0% : fill 30min 12% · séance 26% (54/159) · gap 1% · délai 32.8min · rebond 57% (35/54) (MFE +1.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.35% (p90 −1.86%) → stop au-delà de −1.47% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.57% (p90 −2.28%) → stop au-delà de −1.73% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −2.38%) → stop au-delà de −1.65% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1068 jambes) : jambe baissière méd −1.27% (p90 −3.0%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 92% (79/83) · rebond 66% (48/79)
      · −2.0% : fill 82% (73/83) · rebond 68% (48/73)
      · −3.0% : fill 70% (66/83) · rebond 62% (45/66)
      · −4.0% : fill 60% (52/83) · rebond 70% (38/52)
      · −5.0% : fill 43% (43/83) · rebond 50% (26/43)
   - **flat** (16 séances) :
      · −1.0% : fill 84% (14/16) · rebond 98% (13/14)
      · −2.0% : fill 48% (10/16) · rebond 90% (9/10)
      · −3.0% : fill 24% (5/16) · rebond 92% (4/5)
      · −4.0% : fill 16% (4/16) · rebond 87% (3/4)
      · −5.0% : fill 10% (3/16) · rebond 100% (3/3)
   - **gap-up** (60 séances) :
      · −1.0% : fill 41% (26/60) · rebond 64% (17/26)
      · −2.0% : fill 30% (19/60) · rebond 53% (11/19)
      · −3.0% : fill 29% (18/60) · rebond 65% (14/18)
      · −4.0% : fill 15% (11/60) · rebond 91% (9/11)
      · −5.0% : fill 10% (8/60) · rebond 78% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 70% si les 15 1res min sont vertes (86 cas) · 21% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:38** → P(séance verte=clôture>ouverture) 86% si début vert vs 10% si rouge (base 47% · écart 76 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=83) : tient le vert **86%** · continue >prix actuel 47% ; creux résiduel méd -1.49% (q20 -2.51%) → **SL/trailing à −2.51%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.67% / q75 +3.2% → **scale +1.67% / runner +3.2%**, sortie à la clôture
  - **si ROUGE au coude** (n=77) : edge inversé — récupère vert seulement **10%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.18%** (au-delà de la MAE q10 -4.18%), cible rebond +1.6% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.03% .. +4.37%] · haut q95 +5.8% · bas q05 -6.04%
   - 60min (n=160) : retour [-6.1% .. +5.82%] · haut q95 +6.56% · bas q05 -7.0%
   - 2h (n=160) : retour [-6.68% .. +5.93%] · haut q95 +6.77% · bas q05 -7.24%
   - 4h (n=160) : retour [-6.76% .. +6.25%] · haut q95 +7.97% · bas q05 -7.75%
   - 6h (n=160) : retour [-6.74% .. +6.96%] · haut q95 +9.18% · bas q05 -8.44%
   - session (n=160) : retour [-7.06% .. +7.17%] · haut q95 +9.19% · bas q05 -8.49%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.2% des séances sont trend-up (mild 0% / strong 6.2%) · base = 10 séances trend-up (n_eff 7.1)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **21%**. Lecture précoce 30 min : signature présente → 10% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 1.66% / p90 2.43%) · ~4.04 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 15.0 min, n=43)
   - −1.0% → **83%** (reprise méd 35.0 min, n=27)
   - −1.5% → **83%** (reprise méd 93.49 min, n=16)
   - −2.0% → **84%** (reprise méd 44.98 min, n=8)
   - −3.0% → **66%** (reprise méd None min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−2.43%** (p90, défaut prudent ; serré/agressif −1.66%) ; extension open→close méd +8.12% (q75 +9.53% / q95 +9.89%), MFE méd +9.52% / q90 +11.18%
   - Échelle scale-out : +9.52% (33%) / +10.45% (33%) / +11.18% (34%)
- **DÉSARMER** : repli > **−2.43%** depuis le plus-haut = décay → P(retournement) **26%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +11.18% : P(retournement après) 0% (mèche méd 1.88%)
- **CONTEXTE** : la dernière heure tient les gains 67% du temps (retour médian dernière heure +0.12%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.54 · part idiosyncratique 0.46
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 3.5  _(survente)_
- **ADX** : 14.7  _(pas de tendance nette)_
- **MACD** : hist -0.367  _(pas de croisement recent)_
- **BB** : %B -0.14 · largeur 35.9%
- **ATR** : 0.76 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.263  _(distribution)_
- **Vol ratio** : 1.38  _(volume normal)_
- **Choppiness** : 23.5  _(marche directionnel)_
- **MA** : MA20 15.15 · MA50 15.94 · MA200 17.92  _(prix < MA20)_
- **Dist MA** : MA20 -23.0% · MA50 -26.8% · MA200 -34.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (894831 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
