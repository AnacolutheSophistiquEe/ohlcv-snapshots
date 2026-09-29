# RHM

**Generated** : 2026-09-29T00:02:40.271402+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · €967.40  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)  
> ↳ spot €967.40 (+0.5% vs entrée) · entrée €962.30 · stop €943.05 · T1 €973.75 · R/R 0.59  
> ↳ P(T1 av. stop) 48 % _(réel 5 s)_ · EV/risk -0.156 _(réel 5 s)_ (GBM 0.06) · ¼-Kelly 0.03 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.0% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €960.01–€964.59 (mid €962.30)
- Spot actuel : €967.40 (+0.5% au-dessus de la zone — repli à attendre)
- Stop : €943.05 (plancher anti-bruit 5 s — stop EV-optimal −2% (first-passage 5 s réel) ; -2.00 % depuis l'entree)
- Targets : T1 €973.75 · R/R 0.59 | T2 €985.20 · R/R 1.19 | T3 €996.65 · R/R 1.78
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €943.05


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.73 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (4.53 %)** : le gap seul le franchit 0.549 % des séances (7 fois sur 1274).
   - exécution **0.501 pt plus bas** dans le cas TYPIQUE (médiane), 9.153 au p90, **17.899 au pire**
   - perte réelle **7.856 %** en moyenne _(tirée par la queue)_, jusqu'à **22.429 %** — au lieu des 4.53 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0183 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 7 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.574 % | p01 -3.746 % | pire -22.429 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3456** [0.2778 ; 0.4185] _(largeur 14.1 pt, n_eff 173.1)_
   - swing : **0.44** [0.3884 ; 0.4926] _(largeur 10.4 pt, n_eff 345.8)_
   - deep : **0.4557** [0.4038 ; 0.5084] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / swing : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 27.5 observations effectives », dont la borne haute a 95 % vaut environ 10.9 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.7 pt), swing (35.8 pt), deep (34.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 480 séances)** : VaR **-4.86 %** | CVaR **-6.85 %** | vol 3.08 %/j
   - _fenêtre arrêtée : rupture de regime a 540 seances en arriere (volatilite 1.79 % contre 3.10 % aujourd'hui, rapport 0.58)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.83 % vs -8.98 % si l'on extrapolait par √5 _(rapport 0.871 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5312** (β de hausse 0.5878, asymétrie 0.9038) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.127× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 933.9657 sur grid_snapped (0.73 ATR, 3.456 %) — p(stop avant cible) 0.7126 [0.66 ; 0.76], R/R 4.745, perte reelle 5.656 % (gap inclus), CVaR 3.484 %, EV -1.6997 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3789 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.713, borne haute 0.758 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
- Budget de queue : **3.49 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.18 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 47.6 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ role de queue **non etabli** pour cette ligne (l'intervalle contient zero) : le budget vient de son NOTIONNEL seul, pas d'une mesure de co-mouvement.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.73 ATR (stop 4.659 %) — p(stop avant cible) 0.6321 [0.58 ; 0.68], R/R 2.595, perte reelle 10.343 % (gap inclus), EV -3.9295 % — **REFUSE**
      - refuse : cible atteinte seulement 0.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.59 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.632, borne haute 0.682 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 2.59 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 4.68 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.93 %) : P(cible) 0.6 % x 26.84 % + P(rien) 36.2 % x 6.78 % ne couvrent pas P(stop) 63.2 % x 10.34 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - 🔴 support a 1.18 ATR (stop 6.203 %) — p(stop avant cible) 0.5208 [0.47 ; 0.57], R/R 1.772, perte reelle 15.141 % (gap inclus), EV -5.2468 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.521, borne haute 0.573 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 6.22 % > budget 3.49 %
      - ⚠ support DETECTE a 0.63 ATR du spot — compartiment <1, mesure a 47.5 % de casse (IC clusterise [0.441 ; 0.507] sur 1150 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.25 %) : P(cible) 0.9 % x 26.84 % + P(rien) 47.0 % x 5.11 % ne couvrent pas P(stop) 52.1 % x 15.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.25 ATR (stop 0.842 %) — p(stop avant cible) 0.9361 [0.91 ; 0.96], R/R 12.719, perte reelle 2.11 % (gap inclus), EV -1.2529 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 12.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.936, borne haute 0.958 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.25 %) : P(cible) 0.2 % x 26.84 % + P(rien) 6.2 % x 10.75 % ne couvrent pas P(stop) 93.6 % x 2.11 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.73 ATR (stop 3.456 %) — p(stop avant cible) 0.7126 [0.66 ; 0.76], R/R 4.745, perte reelle 5.656 % (gap inclus), EV -1.6997 % — **REFUSE**
      - refuse : cible atteinte seulement 0.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.713, borne haute 0.758 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.70 %) : P(cible) 0.5 % x 26.84 % + P(rien) 28.2 % x 7.78 % ne couvrent pas P(stop) 71.3 % x 5.66 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 6.737 %) — p(stop avant cible) 0.4802 [0.43 ; 0.53], R/R 1.772, perte reelle 15.141 % (gap inclus), EV -4.6215 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 6.75 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.62 %) : P(cible) 0.9 % x 26.84 % + P(rien) 51.0 % x 4.70 % ne couvrent pas P(stop) 48.0 % x 15.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 7.579 %) — p(stop avant cible) 0.4293 [0.38 ; 0.48], R/R 1.772, perte reelle 15.141 % (gap inclus), EV -3.9265 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.77 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 7.59 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.93 %) : P(cible) 0.9 % x 26.84 % + P(rien) 56.1 % x 4.14 % ne couvrent pas P(stop) 42.9 % x 15.14 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 8.421 %) — p(stop avant cible) 0.4067 [0.36 ; 0.46], R/R 1.197, perte reelle 22.429 % (gap inclus), EV -6.6169 % — **REFUSE**
      - refuse : cible atteinte seulement 0.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.43 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-6.62 %) : P(cible) 0.9 % x 26.84 % + P(rien) 58.4 % x 3.86 % ne couvrent pas P(stop) 40.7 % x 22.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.75 ATR (stop 9.263 %) — p(stop avant cible) 0.3461 [0.30 ; 0.40], R/R 1.197, perte reelle 22.429 % (gap inclus), EV -5.4513 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.27 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.45 %) : P(cible) 1.1 % x 26.84 % + P(rien) 64.3 % x 3.15 % ne couvrent pas P(stop) 34.6 % x 22.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.0 ATR (stop 10.105 %) — p(stop avant cible) 0.2951 [0.25 ; 0.34], R/R 1.197, perte reelle 22.429 % (gap inclus), EV -4.5816 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 10.11 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.58 %) : P(cible) 1.1 % x 26.84 % + P(rien) 69.4 % x 2.53 % ne couvrent pas P(stop) 29.5 % x 22.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 3.5 ATR (stop 11.789 %) — p(stop avant cible) 0.2231 [0.18 ; 0.27], R/R 1.197, perte reelle 22.429 % (gap inclus), EV -3.3576 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.80 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.36 %) : P(cible) 1.1 % x 26.84 % + P(rien) 76.6 % x 1.78 % ne couvrent pas P(stop) 22.3 % x 22.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.0 ATR (stop 13.474 %) — p(stop avant cible) 0.1652 [0.13 ; 0.21], R/R 1.197, perte reelle 22.429 % (gap inclus), EV -2.5589 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.48 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.56 %) : P(cible) 1.1 % x 26.84 % + P(rien) 82.4 % x 1.05 % ne couvrent pas P(stop) 16.5 % x 22.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 4.5 ATR (stop 15.158 %) — p(stop avant cible) 0.129 [0.10 ; 0.17], R/R 1.197, perte reelle 22.429 % (gap inclus), EV -2.0051 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.16 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.01 %) : P(cible) 1.1 % x 26.84 % + P(rien) 86.1 % x 0.70 % ne couvrent pas P(stop) 12.9 % x 22.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.0 ATR (stop 16.842 %) — p(stop avant cible) 0.0947 [0.07 ; 0.13], R/R 1.197, perte reelle 22.429 % (gap inclus), EV -1.6568 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.85 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.66 %) : P(cible) 1.1 % x 26.84 % + P(rien) 89.5 % x 0.21 % ne couvrent pas P(stop) 9.5 % x 22.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 5.5 ATR (stop 18.526 %) — p(stop avant cible) 0.0607 [0.04 ; 0.09], R/R 1.197, perte reelle 22.429 % (gap inclus), EV -1.3136 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.53 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.31 %) : P(cible) 1.1 % x 26.84 % + P(rien) 92.9 % x -0.25 % ne couvrent pas P(stop) 6.1 % x 22.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.0 ATR (stop 20.21 %) — p(stop avant cible) 0.0443 [0.03 ; 0.07], R/R 1.197, perte reelle 22.429 % (gap inclus), EV -1.2023 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.21 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.20 %) : P(cible) 1.1 % x 26.84 % + P(rien) 94.5 % x -0.52 % ne couvrent pas P(stop) 4.4 % x 22.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 6.5 ATR (stop 21.894 %) — p(stop avant cible) 0.0329 [0.02 ; 0.06], R/R 1.197, perte reelle 22.429 % (gap inclus), EV -1.0746 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.20 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.20 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 21.89 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.07 %) : P(cible) 1.1 % x 26.84 % + P(rien) 95.7 % x -0.65 % ne couvrent pas P(stop) 3.3 % x 22.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.0 ATR (stop 23.579 %) — p(stop avant cible) 0.0101 [0.00 ; 0.03], R/R 1.138, perte reelle 23.579 % (gap inclus), EV -0.8918 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.14 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.14 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.58 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.89 %) : P(cible) 1.1 % x 26.84 % + P(rien) 97.9 % x -0.96 % ne couvrent pas P(stop) 1.0 % x 23.58 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 7.5 ATR (stop 25.263 %) — p(stop avant cible) 0.0062 [0.00 ; 0.02], R/R 1.062, perte reelle 25.263 % (gap inclus), EV -0.9022 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.06 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.06 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 25.26 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.90 %) : P(cible) 1.1 % x 26.84 % + P(rien) 98.3 % x -1.04 % ne couvrent pas P(stop) 0.6 % x 25.26 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 8.0 ATR (stop 26.947 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 0.996, perte reelle 26.947 % (gap inclus), EV -0.8586 % — **REFUSE**
      - refuse : cible atteinte seulement 1.1 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.95 % > budget 3.49 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.86 %) : P(cible) 1.1 % x 26.84 % + P(rien) 98.5 % x -1.03 % ne couvrent pas P(stop) 0.5 % x 26.95 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 967.4, ATR14 32.5857 (3.368 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.394 ATR = 1.327 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.168 % | 965.7707 | 89.45 % | 92.2 % | 93.38 % | 94.55 % | 97.01 % | 97.69 % |
| 0.1 ATR | 0.337 % | 964.1415 | 83.43 % | 87.96 % | 89.82 % | 91.39 % | 95.22 % | 96.28 % |
| 0.15 ATR | 0.505 % | 962.5122 | 76.53 % | 83.22 % | 85.87 % | 88.32 % | 92.94 % | 94.77 % |
| 0.2 ATR | 0.674 % | 960.8829 | 70.02 % | 78.78 % | 81.82 % | 85.25 % | 90.95 % | 93.17 % |
| 0.25 ATR | 0.842 % | 959.2536 | 62.52 % | 73.05 % | 76.88 % | 81.19 % | 88.46 % | 91.36 % |
| 0.35 ATR | 1.179 % | 955.995 | 53.94 % | 66.04 % | 71.44 % | 76.73 % | 85.87 % | 89.25 % |
| 0.5 ATR | 1.684 % | 951.1072 | 40.53 % | 54.99 % | 61.86 % | 69.21 % | 80.3 % | 83.82 % |
| 0.75 ATR | 2.526 % | 942.9607 | 23.57 % | 39.09 % | 47.33 % | 57.62 % | 70.45 % | 77.09 % |
| 1.0 ATR | 3.368 % | 934.8143 | 13.02 % | 26.65 % | 36.26 % | 48.51 % | 62.39 % | 70.55 % |
| 1.25 ATR | 4.21 % | 926.6679 | 7.4 % | 17.97 % | 26.19 % | 39.11 % | 54.23 % | 64.22 % |
| 1.5 ATR | 5.053 % | 918.5215 | 3.94 % | 13.13 % | 20.55 % | 31.78 % | 45.97 % | 57.09 % |
| 2.0 ATR | 6.737 % | 902.2286 | 1.78 % | 7.01 % | 12.15 % | 20.99 % | 34.33 % | 47.34 % |
| 2.5 ATR | 8.421 % | 885.9357 | 0.49 % | 3.36 % | 6.32 % | 12.48 % | 24.98 % | 37.99 % |
| 3.0 ATR | 10.105 % | 869.6429 | 0.1 % | 1.38 % | 3.85 % | 7.72 % | 17.41 % | 32.16 % |
| 4.0 ATR | 13.474 % | 837.0572 | 0.0 % | 0.3 % | 1.28 % | 3.27 % | 8.66 % | 20.5 % |
| 6.0 ATR | 20.21 % | 771.8858 | 0.0 % | 0.0 % | 0.0 % | 0.2 % | 0.8 % | 3.52 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.39 ATR | 0.45 ATR | 0.61 ATR | 0.73 ATR | 0.83 ATR | 1.13 ATR | 1.42 ATR |
| **2 s.** | 0.23 ATR | 0.58 ATR | 0.66 ATR | 0.87 ATR | 1.05 ATR | 1.19 ATR | 1.76 ATR | 2.27 ATR |
| **3 s.** | 0.28 ATR | 0.70 ATR | 0.80 ATR | 1.08 ATR | 1.30 ATR | 1.53 ATR | 2.18 ATR | 2.77 ATR |
| **5 s.** | 0.39 ATR | 0.96 ATR | 1.09 ATR | 1.46 ATR | 1.81 ATR | 2.06 ATR | 2.76 ATR | 3.61 ATR |
| **10 s.** | 0.64 ATR | 1.38 ATR | 1.54 ATR | 2.07 ATR | 2.50 ATR | 2.83 ATR | 3.85 ATR | 4.93 ATR |
| **20 s.** | 0.83 ATR | 1.86 ATR | 2.12 ATR | 2.93 ATR | 3.61 ATR | 4.06 ATR | 5.24 ATR | 5.83 ATR |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.45–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 46.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.657–1.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.526 %, prix 942.9635), p(touche) 39.09 % (en stress 91.18 %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 41.9 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.803–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.368 %, prix 934.818), p(touche) 36.26 % (en stress 95.1 %)  ✅ optimum identifie (60.0 % des re-echantillons)
- **5 seance(s)** : plage utile 1.093–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.25 ATR (4.21 %, prix 926.6725), p(touche) 39.11 % (en stress 98.02 %)  ✅ optimum identifie (86.9 % des re-echantillons)
- **10 seance(s)** : plage utile 1.542–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (6.737 %, prix 902.2263), p(touche) 34.33 % (en stress 96.04 %)  ✅ optimum identifie (98.6 % des re-echantillons)
- **20 seance(s)** : plage utile 2.125–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.5 ATR (8.421 %, prix 885.9353), p(touche) 37.99 % (en stress 98.0 %)  ✅ optimum identifie (99.1 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- EV/risk : 0.06 | EV/share : €1.146 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 62 % | T2 38 % | T3 21 %
- Kelly (position) : f* 0.119 | ¼-Kelly 0.03 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.3 | bear 6.0 | side 10.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.531% → cible +1.19% / stop −2.0%, p_fill 90%, n_eff≈35.8) : P(cible|rempli) **48%** · **EV/risk -0.156** (×p_fill ; si rempli -0.35% du capital)
  - **swing** (entrée dip −1.162% → cible +2.66% / stop −3.408%, p_fill 69%, n_eff≈27.5) : P(cible|rempli) **49%** · **EV/risk -0.126** (×p_fill ; si rempli -0.62% du capital)
  - **deep** (entrée dip −1.798% → cible +3.762% / stop −5.145%, p_fill 71%, n_eff≈26.7) : P(cible|rempli) **67%** · **EV/risk +0.091** (×p_fill ; si rempli +0.66% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→69% · +2.0%→48% · +3.0%→30% · +5.0%→5% · +8.0%→1%
- Range intraday médian 3.92% (p90 6.55%) · excursion haute méd. +1.95% / basse méd. −1.64%
- Profil de vol intra : ouverture 2.505% vs midi 0.939% vs clôture 1.046% _(ouverture ~2.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 91% · range 9% · trend ↑0%/↓0% ; spike-down 55% · recovery-V 30%)_
- **Régime intraday** : **chop** _(efficiency 0.116 ; mean-reverting — autocorr -0.052)_ ; drift intra méd. -0.593% ; recovery-V 19%
- **σ réalisé intraday** 2.514% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 53% / bas 61% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 1053.3925 (VA 1037.4725–1057.3725 ; dernier close 1033.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 26% · rebond 47% · **stop −2.28%** sous le fill (sous le bruit) · cible +0.96% · R/R 0.42 (high win-rate)
- Gaps overnight (n=159) : méd. 0.52% · baisse 30% (gap-down >1% 8% · >2% 3%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −1.97%) · haut méd +0.43% · range méd 1.33%
- Excursion ouverture 15min (n=160) : bas méd −0.94% (p90 −2.06%) · haut méd +0.57% · range méd 1.69%
- Excursion ouverture 30min (n=160) : bas méd −1.02% (p90 −2.22%) · haut méd +0.72% · range méd 1.95%
- Excursion ouverture 60min (n=160) : bas méd −1.08% (p90 −2.63%) · haut méd +0.86% · range méd 2.13%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1034.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 55% · séance 71% (105/159) · gap 18% · délai 0.9min · rebond 51% (54/105) (MFE +1.01%)
   - −1.0% : fill 30min 42% · séance 65% (93/159) · gap 8% · délai 5.7min · rebond 59% (55/93) (MFE +1.18%)
   - −1.5% : fill 30min 23% · séance 50% (76/159) · gap 6% · délai 33.2min · rebond 53% (42/76) (MFE +1.15%)
   - −2.0% : fill 30min 16% · séance 43% (65/159) · gap 3% · délai 65.8min · rebond 57% (38/65) (MFE +1.2%)
   - −3.0% : fill 30min 6% · séance 26% (35/159) · gap 3% · délai 224.3min · rebond 47% (17/35) (MFE +0.96%)
   - −4.0% : fill 30min 3% · séance 12% (22/159) · gap 2% · délai 170.8min · rebond 69% (13/22) (MFE +1.66%)
   - −5.0% : fill 30min 1% · séance 7% (12/159) · gap 1% · délai 301.9min · rebond 92% (11/12) (MFE +2.4%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.66% (p90 −1.47%) → stop au-delà de −1.18% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.71%) → stop au-delà de −1.31% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.33% (p90 −1.74%) → stop au-delà de −1.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=539 jambes) : jambe baissière méd −1.07% (p90 −2.47%) · ~7.5 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (33 séances) :
      · −1.0% : fill 96% (32/33) · rebond 73% (23/32)
      · −2.0% : fill 78% (27/33) · rebond 58% (17/27)
      · −3.0% : fill 45% (13/33) · rebond 48% (7/13)
      · −4.0% : fill 31% (10/33) · rebond 72% (7/10)
      · −5.0% : fill 21% (7/33) · rebond 100% (7/7)
   - **flat** (21 séances) :
      · −1.0% : fill 86% (15/21) · rebond 64% (11/15)
      · −2.0% : fill 47% (8/21) · rebond 71% (6/8)
      · −3.0% : fill 26% (4/21) · rebond 37% (1/4)
      · −4.0% : fill 8% (2/21) · rebond 62% (1/2)
      · −5.0% : fill 8% (2/21) · rebond 62% (1/2)
   - **gap-up** (105 séances) :
      · −1.0% : fill 48% (46/105) · rebond 46% (21/46)
      · −2.0% : fill 30% (30/105) · rebond 49% (15/30)
      · −3.0% : fill 19% (18/105) · rebond 50% (9/18)
      · −4.0% : fill 7% (10/105) · rebond 67% (5/10)
      · −5.0% : fill 2% (3/105) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 57% si les 15 1res min sont vertes (73 cas) · 34% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **47min** → P(séance verte=clôture>ouverture) 66% si début vert vs 25% si rouge (base 44% · écart 41 pts) ; prédictivité sature ensuite (plafond brut 259min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **66%** · continue >prix actuel 45% ; creux résiduel méd -1.28% (q20 -2.47%) → **SL/trailing à −2.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.65% / q75 +2.23% → **scale +1.65% / runner +2.23%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **25%** (continue à baisser 58%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.83%** (au-delà de la MAE q10 -3.83%), cible rebond +1.11% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.58% .. +3.13%] · haut q95 +3.42% · bas q05 -2.96%
   - 60min (n=160) : retour [-2.7% .. +3.15%] · haut q95 +4.2% · bas q05 -3.67%
   - 2h (n=160) : retour [-3.26% .. +2.84%] · haut q95 +4.34% · bas q05 -4.04%
   - 4h (n=160) : retour [-3.25% .. +2.99%] · haut q95 +4.73% · bas q05 -4.52%
   - 6h (n=160) : retour [-3.97% .. +3.17%] · haut q95 +4.8% · bas q05 -4.76%
   - session (n=160) : retour [-4.23% .. +3.53%] · haut q95 +4.94% · bas q05 -5.45%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — RHM = **plat / peu volatil** (vol intra méd 2.31%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-30 — US PCE Price Index (headline) — Personal Income & Outlays (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.6  _(momentum baissier)_
- **ADX** : 26.3  _(tendance etablie)_
- **MACD** : hist -1.838  _(pas de croisement recent)_
- **BB** : %B 0.09 · largeur 12.7%
- **ATR** : 32.59 (0.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.244  _(distribution)_
- **Vol ratio** : 0.52  _(volume atone)_
- **Choppiness** : 67.1  _(marche en range (choppy))_
- **MA** : MA20 1019.98 · MA50 1089.47 · MA200 1346.58  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 -11.2% · MA200 -28.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (861725 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
