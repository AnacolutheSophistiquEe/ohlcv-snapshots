# SMR

**Generated** : 2026-09-29T00:43:42.735318+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $7.90  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot $7.90 (+1.7% vs entrée) · entrée $7.77 · stop $7.57 · T1 $8.04 · R/R 1.35  
> ↳ P(T1 av. stop) 33 % _(réel 5 s)_ · EV/risk 0.001 _(réel 5 s)_ (GBM 0.168) · ¼-Kelly 0.039 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.52% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §12 Options — Max-pain gap affiché +6.9 % ≠ (strike 9.0 − spot 7.90)/spot = +13.9 %. Probable spot d'options périmé vs spot courant.
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -46 % hors [0,100] (R² max 0.54). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 13.8 < 20 (tendance pas encore confirmée) alors que Choppiness 37.9 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $7.71–$7.82 (mid $7.77)
- Spot actuel : $7.90 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : $7.57 (plancher anti-bruit (R/R<2) ; -2.57 % depuis l'entree)
- Targets : T1 $8.04 · R/R 1.35 | T2 $8.32 · R/R 2.75 | T3 $8.59 · R/R 4.1
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $7.57


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.45 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.92 %)** : le gap seul le franchit 0.436 % des séances (5 fois sur 1148).
   - exécution **2.865 pt plus bas** dans le cas TYPIQUE (médiane), 13.167 au p90, **18.403 au pire**
   - perte réelle **17.667 %** en moyenne _(tirée par la queue)_, jusqu'à **30.323 %** — au lieu des 11.92 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.025 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.48 % | p01 -6.959 % | pire -30.323 % _(sur 1148 séances)_
- **P(stop avant cible)** _(source : daily, 1149 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.5228** [0.4485 ; 0.5963] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.477** [0.4247 ; 0.5297] _(largeur 10.5 pt, n_eff 345.3)_
   - deep : **0.4457** [0.3939 ; 0.4984] _(largeur 10.4 pt, n_eff 345.3)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (33.9 pt), swing (34.6 pt), deep (32.5 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-9.52 %** | CVaR **-12.13 %** | vol 6.99 %/j
   - _fenêtre arrêtée : rupture de regime a 660 seances en arriere (volatilite 10.78 % contre 6.23 % aujourd'hui, rapport 1.73)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.19 % vs -18.73 % si l'on extrapolait par √5 _(rapport 1.024 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6036** (β de hausse 1.3752, asymétrie 1.1661) vs IWM — 547 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.896× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 6.9854 sur support (1.06 ATR, 11.577 %) — p(stop avant cible) 0.5164 [0.46 ; 0.57], R/R 1.086, perte reelle 17.667 % (gap inclus), CVaR 11.604 %, EV -3.7934 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.0342 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.516, borne haute 0.569 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 1.06 ATR (stop 11.577 %) — p(stop avant cible) 0.5164 [0.46 ; 0.57], R/R 1.086, perte reelle 17.667 % (gap inclus), EV -3.7934 % — **REFUSE**
      - refuse : p_stop_first 0.516, borne haute 0.569 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.09 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - ⚠ support DETECTE a 0.80 ATR du spot — compartiment <1, mesure a 47.5 % de casse (IC clusterise [0.441 ; 0.507] sur 1150 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.79 %) : P(cible) 27.0 % x 19.19 % + P(rien) 21.4 % x 0.70 % ne couvrent pas P(stop) 51.6 % x 17.67 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 2.066 %) — p(stop avant cible) 0.897 [0.86 ; 0.93], R/R 4.718, perte reelle 4.067 % (gap inclus), EV -1.9087 % — **REFUSE**
      - refuse : cible atteinte seulement 8.8 % du temps (< 15 %) meme a 10 seances : le R/R de 4.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.897, borne haute 0.926 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.91 %) : P(cible) 8.8 % x 19.19 % + P(rien) 1.5 % x 2.84 % ne couvrent pas P(stop) 89.7 % x 4.07 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 4.132 %) — p(stop avant cible) 0.8221 [0.78 ; 0.86], R/R 2.557, perte reelle 7.506 % (gap inclus), EV -3.3203 % — **REFUSE**
      - refuse : cible atteinte seulement 14.1 % du temps (< 15 %) meme a 10 seances : le R/R de 2.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.822, borne haute 0.860 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.56 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.32 %) : P(cible) 14.1 % x 19.19 % + P(rien) 3.7 % x 3.84 % ne couvrent pas P(stop) 82.2 % x 7.51 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.75 ATR (stop 6.198 %) — p(stop avant cible) 0.7462 [0.70 ; 0.79], R/R 1.701, perte reelle 11.281 % (gap inclus), EV -4.4303 % — **REFUSE**
      - refuse : p_stop_first 0.746, borne haute 0.790 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.70 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.43 %) : P(cible) 19.6 % x 19.19 % + P(rien) 5.8 % x 4.02 % ne couvrent pas P(stop) 74.6 % x 11.28 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 14.462 %) — p(stop avant cible) 0.4281 [0.38 ; 0.48], R/R 0.923, perte reelle 20.78 % (gap inclus), EV -3.285 % — **REFUSE**
      - refuse : R/R 0.92 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.48 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.28 %) : P(cible) 28.9 % x 19.19 % + P(rien) 28.3 % x 0.24 % ne couvrent pas P(stop) 42.8 % x 20.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 16.528 %) — p(stop avant cible) 0.3514 [0.30 ; 0.40], R/R 0.807, perte reelle 23.778 % (gap inclus), EV -3.1704 % — **REFUSE**
      - refuse : R/R 0.81 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.54 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.17 %) : P(cible) 29.4 % x 19.19 % + P(rien) 35.4 % x -1.29 % ne couvrent pas P(stop) 35.1 % x 23.78 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 18.594 %) — p(stop avant cible) 0.2851 [0.24 ; 0.33], R/R 0.633, perte reelle 30.323 % (gap inclus), EV -4.0231 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.60 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.02 %) : P(cible) 29.5 % x 19.19 % + P(rien) 42.0 % x -2.49 % ne couvrent pas P(stop) 28.5 % x 30.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 20.66 %) — p(stop avant cible) 0.2173 [0.18 ; 0.26], R/R 0.633, perte reelle 30.323 % (gap inclus), EV -2.6598 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.67 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.66 %) : P(cible) 29.7 % x 19.19 % + P(rien) 48.6 % x -3.64 % ne couvrent pas P(stop) 21.7 % x 30.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 22.726 %) — p(stop avant cible) 0.1701 [0.13 ; 0.21], R/R 0.633, perte reelle 30.323 % (gap inclus), EV -1.797 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.73 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.80 %) : P(cible) 29.7 % x 19.19 % + P(rien) 53.3 % x -4.40 % ne couvrent pas P(stop) 17.0 % x 30.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 24.792 %) — p(stop avant cible) 0.1299 [0.10 ; 0.17], R/R 0.633, perte reelle 30.323 % (gap inclus), EV -1.1794 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.80 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.18 %) : P(cible) 29.8 % x 19.19 % + P(rien) 57.2 % x -5.16 % ne couvrent pas P(stop) 13.0 % x 30.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 28.924 %) — p(stop avant cible) 0.0653 [0.04 ; 0.10], R/R 0.633, perte reelle 30.323 % (gap inclus), EV -0.3565 % — **REFUSE**
      - refuse : R/R 0.63 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.93 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 29.8 % x 19.19 % + P(rien) 63.7 % x -6.42 % ne couvrent pas P(stop) 6.5 % x 30.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 33.056 %) — p(stop avant cible) 0.035 [0.02 ; 0.06], R/R 0.581, perte reelle 33.056 % (gap inclus), EV -0.2266 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.06 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 29.8 % x 19.19 % + P(rien) 66.7 % x -7.17 % ne couvrent pas P(stop) 3.5 % x 33.06 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 37.188 %) — p(stop avant cible) 0.0261 [0.01 ; 0.05], R/R 0.516, perte reelle 37.188 % (gap inclus), EV -0.2598 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.19 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 29.8 % x 19.19 % + P(rien) 67.6 % x -7.40 % ne couvrent pas P(stop) 2.6 % x 37.19 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 41.32 %) — p(stop avant cible) 0.0144 [0.01 ; 0.03], R/R 0.464, perte reelle 41.32 % (gap inclus), EV -0.2709 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.32 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 29.8 % x 19.19 % + P(rien) 68.8 % x -7.84 % ne couvrent pas P(stop) 1.4 % x 41.32 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 45.452 %) — p(stop avant cible) 0.0093 [0.00 ; 0.02], R/R 0.422, perte reelle 45.452 % (gap inclus), EV -0.266 % — **REFUSE**
      - refuse : R/R 0.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 45.45 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.27 %) : P(cible) 29.8 % x 19.19 % + P(rien) 69.3 % x -8.02 % ne couvrent pas P(stop) 0.9 % x 45.45 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 49.584 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.387, perte reelle 49.584 % (gap inclus), EV -0.262 % — **REFUSE**
      - refuse : R/R 0.39 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.58 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 29.8 % x 19.19 % + P(rien) 70.0 % x -8.40 % ne couvrent pas P(stop) 0.2 % x 49.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 53.716 %) — p(stop avant cible) 0.0002 [0.00 ; 0.01], R/R 0.357, perte reelle 53.716 % (gap inclus), EV -0.2633 % — **REFUSE**
      - refuse : R/R 0.36 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.72 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 29.8 % x 19.19 % + P(rien) 70.2 % x -8.50 % ne couvrent pas P(stop) 0.0 % x 53.72 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 57.848 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.332, perte reelle 57.848 % (gap inclus), EV -0.2576 % — **REFUSE**
      - refuse : R/R 0.33 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 57.85 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 29.8 % x 19.19 % + P(rien) 70.2 % x -8.51 % ne couvrent pas P(stop) 0.0 % x 57.85 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 61.98 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.31, perte reelle 61.98 % (gap inclus), EV -0.2576 % — **REFUSE**
      - refuse : R/R 0.31 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 61.98 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 29.8 % x 19.19 % + P(rien) 70.2 % x -8.51 % ne couvrent pas P(stop) 0.0 % x 61.98 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 66.112 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.29, perte reelle 66.112 % (gap inclus), EV -0.2576 % — **REFUSE**
      - refuse : R/R 0.29 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 66.11 % > budget 12.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.26 %) : P(cible) 29.8 % x 19.19 % + P(rien) 70.2 % x -8.51 % ne couvrent pas P(stop) 0.0 % x 66.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 7.9, ATR14 0.6529 (8.264 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.426 ATR = 3.52 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.413 % | 7.8674 | 92.45 % | 95.04 % | 96.28 % | 97.06 % | 97.95 % | 98.39 % |
| 0.1 ATR | 0.826 % | 7.8347 | 86.71 % | 91.21 % | 93.23 % | 94.68 % | 96.25 % | 97.47 % |
| 0.15 ATR | 1.24 % | 7.8021 | 80.74 % | 86.92 % | 89.62 % | 91.74 % | 93.97 % | 96.09 % |
| 0.2 ATR | 1.653 % | 7.7694 | 75.0 % | 82.64 % | 86.34 % | 89.25 % | 92.38 % | 95.05 % |
| 0.25 ATR | 2.066 % | 7.7368 | 69.82 % | 79.59 % | 83.75 % | 87.1 % | 90.67 % | 93.9 % |
| 0.35 ATR | 2.892 % | 7.6715 | 58.11 % | 72.04 % | 77.31 % | 82.69 % | 87.6 % | 91.48 % |
| 0.5 ATR | 4.132 % | 7.5736 | 42.0 % | 58.74 % | 66.93 % | 73.98 % | 83.16 % | 88.49 % |
| 0.75 ATR | 6.198 % | 7.4104 | 20.61 % | 37.2 % | 47.52 % | 59.5 % | 72.35 % | 81.01 % |
| 1.0 ATR | 8.264 % | 7.2471 | 11.37 % | 25.82 % | 35.78 % | 49.21 % | 64.51 % | 75.14 % |
| 1.25 ATR | 10.33 % | 7.0839 | 4.73 % | 16.01 % | 25.06 % | 38.46 % | 54.95 % | 68.7 % |
| 1.5 ATR | 12.396 % | 6.9207 | 2.25 % | 9.81 % | 16.25 % | 28.39 % | 45.51 % | 61.91 % |
| 2.0 ATR | 16.528 % | 6.5943 | 0.34 % | 3.27 % | 6.55 % | 14.71 % | 31.4 % | 48.91 % |
| 2.5 ATR | 20.66 % | 6.2679 | 0.11 % | 1.35 % | 2.93 % | 6.9 % | 20.71 % | 38.09 % |
| 3.0 ATR | 24.792 % | 5.9414 | 0.11 % | 0.56 % | 1.92 % | 3.85 % | 11.83 % | 28.19 % |
| 4.0 ATR | 33.056 % | 5.2886 | 0.0 % | 0.23 % | 0.34 % | 1.13 % | 4.55 % | 13.58 % |
| 6.0 ATR | 49.584 % | 3.9829 | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.34 % | 1.61 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.20 ATR | 0.43 ATR | 0.47 ATR | 0.60 ATR | 0.70 ATR | 0.77 ATR | 1.05 ATR | 1.24 ATR |
| **2 s.** | 0.31 ATR | 0.60 ATR | 0.66 ATR | 0.84 ATR | 1.02 ATR | 1.15 ATR | 1.49 ATR | 1.87 ATR |
| **3 s.** | 0.38 ATR | 0.72 ATR | 0.80 ATR | 1.06 ATR | 1.25 ATR | 1.39 ATR | 1.82 ATR | 2.21 ATR |
| **5 s.** | 0.48 ATR | 0.98 ATR | 1.10 ATR | 1.39 ATR | 1.62 ATR | 1.81 ATR | 2.30 ATR | 2.81 ATR |
| **10 s.** | 0.69 ATR | 1.38 ATR | 1.52 ATR | 1.94 ATR | 2.30 ATR | 2.54 ATR | 3.25 ATR | 3.94 ATR |
| **20 s.** | 1.00 ATR | 1.96 ATR | 2.18 ATR | 2.76 ATR | 3.22 ATR | 3.56 ATR | 4.60 ATR | 5.43 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.472–0.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.5 ATR (4.132 %, prix 7.5736), p(touche) 42.0 % (en stress 82.02 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (60.1 % des re-echantillons)
- **2 seance(s)** : plage utile 0.659–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (6.198 %, prix 7.4104), p(touche) 37.2 % (en stress 88.76 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ✅ optimum identifie (69.0 % des re-echantillons)
- **3 seance(s)** : plage utile 0.804–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (8.264 %, prix 7.2471), p(touche) 35.78 % (en stress 89.89 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 52.1 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **5 seance(s)** : plage utile 1.098–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (10.33 %, prix 7.0839), p(touche) 38.46 % (en stress 95.51 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **10 seance(s)** : plage utile 1.518–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (16.528 %, prix 6.5943), p(touche) 31.4 % (en stress 96.59 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **20 seance(s)** : plage utile 2.181–2.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 32.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.168 | EV/share : $0.033 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 35 % | T3 35 %
- Kelly (position) : f* 0.155 | ¼-Kelly 0.039 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 32.7 | bear 13.1 | side 54.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.66% → cible +3.555% / stop −2.522%, p_fill 72%, n_eff≈30.8) : P(cible|rempli) **33%** · **EV/risk +0.001** (×p_fill ; si rempli +0.00% du capital)
  - **swing** (entrée dip −3.656% → cible +16.222% / stop −8.578%, p_fill 64%, n_eff≈25.3) : P(cible|rempli) **5%** · **EV/risk +0.123** (×p_fill ; si rempli +1.65% du capital)
  - **deep** (entrée dip −5.648% → cible +27.854% / stop −13.928%, p_fill 51%, n_eff≈25.5) : P(cible|rempli) **8%** · **EV/risk +0.139** (×p_fill ; si rempli +3.84% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→92% · +1.0%→81% · +2.0%→70% · +3.0%→64% · +5.0%→39% · +8.0%→10%
- Range intraday médian 7.03% (p90 12.01%) · excursion haute méd. +3.75% / basse méd. −2.71%
- Profil de vol intra : ouverture 4.625% vs midi 1.437% vs clôture 1.737% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 41%)_
- **Régime intraday** : **chop** _(efficiency 0.121 ; mean-reverting — autocorr -0.074)_ ; drift intra méd. 0.451% ; recovery-V 48%
- **σ réalisé intraday** 4.311% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 60% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 9.4737 (VA 9.4479–9.5856 ; dernier close 9.695)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 40% · rebond 76% · **stop −4.13%** sous le fill (sous le bruit) · cible +2.5% · R/R 0.61 (high win-rate)
- Gaps overnight (n=159) : méd. -0.56% · baisse 58% (gap-down >1% 36% · >2% 23%)
- Excursion ouverture 5min (n=160) : bas méd −1.01% (p90 −2.93%) · haut méd +1.22% · range méd 2.66%
- Excursion ouverture 15min (n=160) : bas méd −1.29% (p90 −3.78%) · haut méd +1.87% · range méd 3.52%
- Excursion ouverture 30min (n=160) : bas méd −1.55% (p90 −4.61%) · haut méd +2.23% · range méd 4.13%
- Excursion ouverture 60min (n=160) : bas méd −2.06% (p90 −5.35%) · haut méd +2.64% · range méd 5.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 9.7 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 79% (130/159) · gap 52% · délai 0.0min · rebond 64% (82/130) (MFE +1.62%)
   - −1.0% : fill 30min 63% · séance 75% (123/159) · gap 37% · délai 0.0min · rebond 65% (77/123) (MFE +2.03%)
   - −1.5% : fill 30min 59% · séance 70% (116/159) · gap 27% · délai 0.0min · rebond 71% (83/116) (MFE +1.99%)
   - −2.0% : fill 30min 51% · séance 62% (107/159) · gap 23% · délai 0.7min · rebond 68% (73/107) (MFE +1.98%)
   - −3.0% : fill 30min 39% · séance 53% (93/159) · gap 10% · délai 4.6min · rebond 76% (74/93) (MFE +2.31%)
   - −4.0% : fill 30min 32% · séance 46% (83/159) · gap 4% · délai 8.7min · rebond 76% (63/83) (MFE +2.53%)
   - −5.0% : fill 30min 23% · séance 40% (65/159) · gap 2% · délai 22.3min · rebond 76% (49/65) (MFE +2.5%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.7% (p90 −2.66%) → stop au-delà de −1.93% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.71% (p90 −2.68%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.05% (p90 −2.75%) → stop au-delà de −2.16% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1137 jambes) : jambe baissière méd −1.34% (p90 −3.08%) · ~13.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (89 séances) :
      · −1.0% : fill 96% (87/89) · rebond 63% (55/87)
      · −2.0% : fill 86% (81/89) · rebond 74% (60/81)
      · −3.0% : fill 78% (75/89) · rebond 82% (63/75)
      · −4.0% : fill 69% (67/89) · rebond 82% (54/67)
      · −5.0% : fill 58% (51/89) · rebond 83% (42/51)
   - **flat** (10 séances) :
      · −1.0% : fill 92% (8/10) · rebond 48% (4/8)
      · −2.0% : fill 80% (6/10) · rebond 40% (2/6)
      · −3.0% : fill 80% (6/10) · rebond 50% (3/6)
      · −4.0% : fill 80% (6/10) · rebond 62% (4/6)
      · −5.0% : fill 60% (4/10) · rebond 79% (3/4)
   - **gap-up** (60 séances) :
      · −1.0% : fill 44% (28/60) · rebond 74% (18/28)
      · −2.0% : fill 27% (20/60) · rebond 51% (11/20)
      · −3.0% : fill 14% (12/60) · rebond 49% (8/12)
      · −4.0% : fill 11% (10/60) · rebond 33% (5/10)
      · −5.0% : fill 11% (10/60) · rebond 26% (4/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 52% en base · 65% si les 15 1res min sont vertes (74 cas) · 38% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:15** → P(séance verte=clôture>ouverture) 85% si début vert vs 20% si rouge (base 52% · écart 65 pts) ; prédictivité sature ensuite (plafond brut 197min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=80) : tient le vert **85%** · continue >prix actuel 58% ; creux résiduel méd -1.67% (q20 -3.41%) → **SL/trailing à −3.41%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.07% / q75 +4.06% → **scale +3.07% / runner +4.06%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **20%** (continue à baisser 55%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.4%** (au-delà de la MAE q10 -5.4%), cible rebond +1.42% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.92% .. +4.46%] · haut q95 +6.13% · bas q05 -5.65%
   - 60min (n=160) : retour [-4.99% .. +4.69%] · haut q95 +6.67% · bas q05 -6.2%
   - 2h (n=160) : retour [-6.22% .. +5.43%] · haut q95 +7.83% · bas q05 -7.86%
   - 4h (n=160) : retour [-7.13% .. +7.01%] · haut q95 +8.38% · bas q05 -7.96%
   - 6h (n=160) : retour [-6.87% .. +8.08%] · haut q95 +9.95% · bas q05 -8.33%
   - session (n=160) : retour [-6.95% .. +8.67%] · haut q95 +10.49% · bas q05 -8.41%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — SMR = **volatil sans tendance propre (choppy)** (vol intra méd 4.83%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 22.7  _(survente)_
- **ADX** : 13.8  _(pas de tendance nette)_
- **MACD** : hist -0.118  _(pas de croisement recent)_
- **BB** : %B 0.16 · largeur 38.4%
- **ATR** : 0.65 (5.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.155  _(distribution)_
- **Vol ratio** : 0.82  _(volume normal)_
- **Choppiness** : 37.9  _(marche directionnel)_
- **MA** : MA20 9.1 · MA50 9.07 · MA200 12.18  _(prix < MA20)_
- **Dist MA** : MA20 -13.2% · MA50 -12.9% · MA200 -35.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (857634 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
