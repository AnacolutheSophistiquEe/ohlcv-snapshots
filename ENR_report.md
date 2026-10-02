# ENR

**Generated** : 2026-10-02T00:08:17.581062+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €143.16  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)  
> ↳ spot €143.16 (+2.6% vs entrée) · entrée €139.54 · stop €128.38 · T1 €142.14 · R/R 0.23  
> ↳ _probas brutes, non calibrées · n=0_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €139.12–€139.97 (mid €139.54)
- Spot actuel : €143.16 (+2.6% au-dessus de la zone — repli à attendre)
- Stop : €128.38 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 €142.14 · R/R 0.23 | T2 €144.74 · R/R 0.47 | T3 €147.34 · R/R 0.7
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €128.38


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.59 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.19 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **6.98 pt plus bas** dans le cas TYPIQUE (médiane), 22.65 au p90, **26.567 au pire**
   - perte réelle **21.854 %** en moyenne _(tirée par la queue)_, jusqu'à **35.757 %** — au lieu des 9.19 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0298 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.33 % | p01 -5.088 % | pire -35.757 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0076** [0.0011 ; 0.0299] _(largeur 2.9 pt, n_eff 173.1)_
   - swing : **0.4965** [0.444 ; 0.549] _(largeur 10.5 pt, n_eff 345.8)_
   - deep : **0.468** [0.4159 ; 0.5207] _(largeur 10.5 pt, n_eff 345.8)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 41.5 observations effectives », dont la borne haute a 95 % vaut environ 7.2 %.
- ⚠ **5 s — échantillon insuffisant sur : swing (36.5 pt), deep (34.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-4.63 %** | CVaR **-6.59 %** | vol 3.19 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 5.94 % contre 3.01 % aujourd'hui, rapport 1.97)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.81 % vs -9.75 % si l'on extrapolait par √5 _(rapport 0.904 ; < 1 = le √5 surestime)_
- **β de baisse : 1.3571** (β de hausse 1.084, asymétrie 1.2519) vs GDAXI — 600 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.34× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — rien n'y coupe la baisse avant la perte du notionnel investi ; un stop ne borne pas la perte (un gap l'execute sous son seuil), il la limite en esperance.**
- **Couple retenu** : stop 130.1707 sur atr_grid (2.5 ATR, 9.073 %) — p(stop avant cible) 0.3154 [0.27 ; 0.37], R/R 3.33, perte reelle 9.348 % (gap inclus), CVaR 10.806 %, EV -0.1809 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9767 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
- Budget de queue : **12.0 %** du notionnel — ⚠ VALEUR FIGEE (valeur de repli (ligne absente de l'allocation)), PAS une mesure. L'allocation derivee de la contrainte du compte n'etait pas disponible.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.97 ATR (stop 5.4 %) — p(stop avant cible) 0.5816 [0.53 ; 0.63], R/R 5.561, perte reelle 5.597 % (gap inclus), EV -0.3825 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 5.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.582, borne haute 0.633 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.38 %) : P(cible) 0.4 % x 31.13 % + P(rien) 41.5 % x 6.66 % ne couvrent pas P(stop) 58.2 % x 5.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ sr_based a 2.88 ATR (stop 12.35 %) — p(stop avant cible) 0.129 [0.10 ; 0.17], R/R 2.402, perte reelle 12.96 % (gap inclus), EV 0.452 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.40 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.40 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.92 % > budget 12.00 %
   - 🟢 support a 6.37 ATR (stop 24.987 %) — p(stop avant cible) 0.0039 [0.00 ; 0.02], R/R 1.117, perte reelle 27.866 % (gap inclus), EV 1.1889 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.57 % > budget 12.00 %
   - 🟢 support a 9.46 ATR (stop 36.22 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.856, perte reelle 36.347 % (gap inclus), EV 1.2173 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 0.86 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.86 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.04 % > budget 12.00 %
   - ⚪ atr_grid a 0.25 ATR (stop 0.907 %) — p(stop avant cible) 0.9233 [0.89 ; 0.95], R/R 32.345, perte reelle 0.962 % (gap inclus), EV -0.1232 % — **REFUSE**
      - refuse : cible atteinte seulement 0.1 % du temps (< 15 %) meme a 10 seances : le R/R de 32.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.923, borne haute 0.948 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 0.1 % x 31.13 % + P(rien) 7.5 % x 9.61 % ne couvrent pas P(stop) 92.3 % x 0.96 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 0.5 ATR (stop 1.815 %) — p(stop avant cible) 0.847 [0.81 ; 0.88], R/R 16.25, perte reelle 1.916 % (gap inclus), EV -0.2209 % — **REFUSE**
      - refuse : cible atteinte seulement 0.2 % du temps (< 15 %) meme a 10 seances : le R/R de 16.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.847, borne haute 0.882 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.22 %) : P(cible) 0.2 % x 31.13 % + P(rien) 15.1 % x 8.88 % ne couvrent pas P(stop) 84.7 % x 1.92 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 0.97 ATR (stop 4.609 %) — p(stop avant cible) 0.6243 [0.57 ; 0.67], R/R 6.522, perte reelle 4.773 % (gap inclus), EV -0.2274 % — **REFUSE**
      - refuse : cible atteinte seulement 0.3 % du temps (< 15 %) meme a 10 seances : le R/R de 6.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.624, borne haute 0.674 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.23 %) : P(cible) 0.3 % x 31.13 % + P(rien) 37.2 % x 7.11 % ne couvrent pas P(stop) 62.4 % x 4.77 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 1.75 ATR (stop 6.351 %) — p(stop avant cible) 0.5158 [0.46 ; 0.57], R/R 4.715, perte reelle 6.601 % (gap inclus), EV -0.5138 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.72 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.516, borne haute 0.568 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.51 %) : P(cible) 0.4 % x 31.13 % + P(rien) 48.1 % x 5.79 % ne couvrent pas P(stop) 51.6 % x 6.60 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.0 ATR (stop 7.259 %) — p(stop avant cible) 0.4525 [0.40 ; 0.51], R/R 4.167, perte reelle 7.469 % (gap inclus), EV -0.4521 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 4.17 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.45 %) : P(cible) 0.4 % x 31.13 % + P(rien) 54.4 % x 5.18 % ne couvrent pas P(stop) 45.2 % x 7.47 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.25 ATR (stop 8.166 %) — p(stop avant cible) 0.3817 [0.33 ; 0.43], R/R 3.69, perte reelle 8.435 % (gap inclus), EV -0.3423 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.34 %) : P(cible) 0.4 % x 31.13 % + P(rien) 61.5 % x 4.50 % ne couvrent pas P(stop) 38.2 % x 8.43 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ atr_grid a 2.5 ATR (stop 9.073 %) — p(stop avant cible) 0.3154 [0.27 ; 0.37], R/R 3.33, perte reelle 9.348 % (gap inclus), EV -0.1809 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 3.33 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.18 %) : P(cible) 0.4 % x 31.13 % + P(rien) 68.1 % x 3.90 % ne couvrent pas P(stop) 31.5 % x 9.35 %.
        -> ligne DETENUE : l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne, a remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes. Ligne NON detenue : ne pas l'ouvrir sur ce couple stop / cible a cet horizon.
   - ⚪ grid_snapped a 2.88 ATR (stop 11.559 %) — p(stop avant cible) 0.1666 [0.13 ; 0.21], R/R 2.578, perte reelle 12.073 % (gap inclus), EV 0.2259 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.58 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 2.58 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.27 % > budget 12.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 14.517 %) — p(stop avant cible) 0.0732 [0.05 ; 0.10], R/R 1.991, perte reelle 15.633 % (gap inclus), EV 0.7453 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.99 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.99 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.15 % > budget 12.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 16.332 %) — p(stop avant cible) 0.0349 [0.02 ; 0.06], R/R 1.736, perte reelle 17.935 % (gap inclus), EV 0.9882 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.74 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.74 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.28 % > budget 12.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.147 %) — p(stop avant cible) 0.0257 [0.01 ; 0.05], R/R 1.604, perte reelle 19.404 % (gap inclus), EV 1.0338 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.60 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.60 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.89 % > budget 12.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 19.961 %) — p(stop avant cible) 0.0126 [0.00 ; 0.03], R/R 1.416, perte reelle 21.977 % (gap inclus), EV 1.1202 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.42 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.06 % > budget 12.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 21.776 %) — p(stop avant cible) 0.0073 [0.00 ; 0.02], R/R 1.253, perte reelle 24.84 % (gap inclus), EV 1.1201 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.13 % > budget 12.00 %
   - 🟢 grid_snapped a 6.37 ATR (stop 24.195 %) — p(stop avant cible) 0.0046 [0.00 ; 0.02], R/R 1.146, perte reelle 27.155 % (gap inclus), EV 1.1696 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.73 % > budget 12.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 27.22 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 1.071, perte reelle 29.069 % (gap inclus), EV 1.2 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.42 % > budget 12.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 29.034 %) — p(stop avant cible) 0.0026 [0.00 ; 0.01], R/R 1.03, perte reelle 30.225 % (gap inclus), EV 1.2057 % — **REFUSE**
      - refuse : cible atteinte seulement 0.4 % du temps (< 15 %) meme a 10 seances : le R/R de 1.03 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.03 < plancher 3.00 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.27 % > budget 12.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Distances ATR x horizon — p(touche) a 1 / 5 / 20 seances

- Reference : spot 143.16, ATR14 5.1957 (3.629 % du cours). **Les prix ci-dessous sont ancres sur ce spot de cloture : les REANCRER sur le prix vivant avant de poser.**
- **Horizon = consigne operateur.** intraday -> 1 seance ; SANS PRECISION -> swing, 5 seances ; positionnel/long -> 20.
- **Bornes appliquees d'office par le calculateur** : aucune tranche touchee plus de **45.0 %** du temps a l'horizon retenu ; aucune sous le **bruit journalier** du titre (0.367 ATR = 1.332 % du cours, soit l'excursion adverse mediane d'une seance) ; deux tranches jamais separees par moins que ce bruit. Ce sont des DEFAUTS DU MODULE : ils cedent avant toute consigne, et le rapport le dit.

| distance | % du cours | prix (spot ref) | p(touche) 1s | p(touche) 2s | p(touche) 3s | p(touche) 5s | p(touche) 10s | p(touche) 20s |
|---|---|---|---|---|---|---|---|---|
| 0.05 ATR | 0.181 % | 142.9002 | 91.52 % | 94.08 % | 95.55 % | 96.14 % | 97.21 % | 97.89 % |
| 0.1 ATR | 0.363 % | 142.6404 | 83.83 % | 88.15 % | 90.61 % | 92.67 % | 94.63 % | 95.68 % |
| 0.15 ATR | 0.544 % | 142.3806 | 76.33 % | 82.23 % | 85.87 % | 88.51 % | 91.04 % | 93.27 % |
| 0.2 ATR | 0.726 % | 142.1209 | 70.41 % | 78.97 % | 83.0 % | 86.34 % | 89.25 % | 91.86 % |
| 0.25 ATR | 0.907 % | 141.8611 | 63.91 % | 74.63 % | 79.35 % | 83.17 % | 87.16 % | 90.45 % |
| 0.35 ATR | 1.27 % | 141.3415 | 51.78 % | 64.76 % | 70.36 % | 75.74 % | 81.79 % | 86.33 % |
| 0.5 ATR | 1.815 % | 140.5621 | 36.39 % | 51.63 % | 59.49 % | 66.24 % | 74.13 % | 80.2 % |
| 0.75 ATR | 2.722 % | 139.2632 | 19.63 % | 35.64 % | 45.06 % | 54.26 % | 65.07 % | 73.27 % |
| 1.0 ATR | 3.629 % | 137.9643 | 10.95 % | 25.27 % | 34.09 % | 43.76 % | 56.42 % | 64.92 % |
| 1.25 ATR | 4.537 % | 136.6654 | 6.02 % | 17.18 % | 24.8 % | 35.45 % | 47.96 % | 57.29 % |
| 1.5 ATR | 5.444 % | 135.3664 | 2.76 % | 10.96 % | 17.69 % | 27.62 % | 40.7 % | 50.95 % |
| 2.0 ATR | 7.259 % | 132.7686 | 0.79 % | 3.95 % | 8.5 % | 16.04 % | 27.86 % | 39.6 % |
| 2.5 ATR | 9.073 % | 130.1707 | 0.3 % | 1.97 % | 3.95 % | 9.31 % | 19.2 % | 29.95 % |
| 3.0 ATR | 10.888 % | 127.5729 | 0.1 % | 0.79 % | 1.88 % | 4.85 % | 12.14 % | 22.21 % |
| 4.0 ATR | 14.517 % | 122.3771 | 0.1 % | 0.39 % | 1.09 % | 2.28 % | 6.27 % | 12.46 % |
| 6.0 ATR | 21.776 % | 111.9857 | 0.0 % | 0.2 % | 0.4 % | 0.89 % | 2.19 % | 5.33 % |

**A quelle distance poser pour n'etre sorti que p % du temps** (lecture INVERSE — c'est elle qui sert a arbitrer) :

| horizon | p=75 % | p=50 % | p=45 % | p=33 % | p=25 % | p=20 % | p=10 % | p=5 % |
|---|---|---|---|---|---|---|---|---|
| **1 s.** | 0.16 ATR | 0.37 ATR | 0.42 ATR | 0.55 ATR | 0.67 ATR | 0.74 ATR | 1.05 ATR | 1.33 ATR |
| **2 s.** | 0.25 ATR | 0.53 ATR | 0.60 ATR | 0.81 ATR | 1.01 ATR | 1.16 ATR | 1.57 ATR | 1.93 ATR |
| **3 s.** | 0.30 ATR | 0.66 ATR | 0.75 ATR | 1.03 ATR | 1.25 ATR | 1.42 ATR | 1.92 ATR | 2.38 ATR |
| **5 s.** | 0.36 ATR | 0.85 ATR | 0.97 ATR | 1.33 ATR | 1.61 ATR | 1.83 ATR | 2.45 ATR | 2.98 ATR |
| **10 s.** | 0.48 ATR | 1.19 ATR | 1.35 ATR | 1.80 ATR | 2.17 ATR | 2.45 ATR | 3.37 ATR | 4.62 ATR |
| **20 s.** | 0.69 ATR | 1.54 ATR | 1.76 ATR | 2.34 ATR | 2.82 ATR | 3.23 ATR | 4.69 ATR | hors grille |

**Distance optimale par horizon** (plage utile mesuree, puis meilleur point unique de cette plage) :
- **1 seance(s)** : plage utile 0.416–0.35 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum — ATR (— %, prix —), p(touche) — % (en stress — %)  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 26.8 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **2 seance(s)** : plage utile 0.604–0.75 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 0.75 ATR (2.722 %, prix 139.2632), p(touche) 35.64 % (en stress 91.18 %)  ⚠ **SOLUTION DE COIN** — l'optimum est sur une borne, l'objectif est monotone : ce n'est PAS un arbitrage. Trancher avec la lecture inverse ci-dessus.  ⚠ **OPTIMUM NON IDENTIFIE** — au bootstrap par blocs, le vainqueur ne gagne que 39.2 % des re-echantillons : le rendement ne distingue pas les distances de cette zone. Trancher par la tolerance de sortie ou par un niveau structurel ne coute donc rien.
- **3 seance(s)** : plage utile 0.751–1.25 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.629 %, prix 137.9647), p(touche) 34.09 % (en stress 91.18 %)  ✅ optimum identifie (86.1 % des re-echantillons)
- **5 seance(s)** : plage utile 0.97–1.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.0 ATR (3.629 %, prix 137.9647), p(touche) 43.76 % (en stress 99.01 %)  ✅ optimum identifie (91.1 % des re-echantillons)
- **10 seance(s)** : plage utile 1.352–2.5 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 1.5 ATR (5.444 %, prix 135.3664), p(touche) 40.7 % (en stress 100.0 %)  ✅ optimum identifie (92.1 % des re-echantillons)
- **20 seance(s)** : plage utile 1.762–3.0 ATR _(borne basse : tolerance de sortie par defaut (45 %))_ — optimum 2.0 ATR (7.259 %, prix 132.768), p(touche) 39.6 % (en stress 99.0 %)  ✅ optimum identifie (88.9 % des re-echantillons)

- p(touche) = part des fenetres de N seances ou le prix est venu chercher un stop pose a cette distance SOUS le prix d'entree de la fenetre. Mesure sur les barres reelles du titre, pas modelisee.

- **Ce que la mesure permet** : CE QUE LA MESURE PERMET, ET CE QU'ELLE NE PERMET PAS. Un bootstrap par blocs (800 re-echantillons, blocs de 20 seances) demande si l'optimum de croissance survit au re-echantillonnage. Resultat du 26/08 : A 1 SEANCE, NON — sur RHM le vainqueur ne gagne que 45,8 % des re-echantillons, sur MSTR 31,6 %. Il n'existe donc PAS d'arbitrage purement calculatoire de la distance intraday : le rendement ne distingue pas les distances proches. C'est un resultat, pas une lacune — il dit que d'autres criteres (tolerance de sortie via `inverse_by_horizon`, niveau structurel, marge) peuvent trancher SANS RIEN COUTER en rendement mesure. A 5 et 20 seances sur RHM l'optimum EST identifie, et il est au maximum de la grille : le rendement pur veut le stop le plus large, et ce qui l'en empeche est le PORTEFEUILLE (cash rendu, marge), pas la ligne.
- **Comment choisir** : LE CHOIX DE LA DISTANCE EST UN ARBITRAGE, PAS UNE LECTURE. 1) L'horizon vient de la consigne. 2) Fixer une TOLERANCE DE SORTIE — combien de fois sur dix accepte-t-on d'etre stoppe a cet horizon ? 3) Lire `inverse_by_horizon[<H>].p<XX>` : c'est la distance qui realise cette tolerance SUR CE TITRE. 4) Croiser avec la plage utile (`optimal_by_horizon[<H>].range_atr`) et avec `ordinary_pct`, qui dit ce que la distance rapporte. 5) Si `best_is_corner` est vrai, ne PAS citer `best_atr` comme un optimum : l'objectif est monotone, il n'y a pas de point interieur, et c'est la tolerance qui doit trancher. 6) Annoncer la distance retenue AVEC sa p(touche) : c'est le seul chiffre qui permet a l'operateur de contester le choix.


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 84.0 | side 11.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 143.0 (= 1 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.522% → cible +1.862% / stop −8.0%, p_fill 35%, n_eff≈41.5) : P(cible|rempli) **22%** · **EV/risk -0.010** (×p_fill ; si rempli -0.24% du capital)
  - **swing** (entrée dip −5.561% → cible +4.297% / stop −3.843%, p_fill 22%, n_eff≈26.3) : P(cible|rempli) **53%** · **EV/risk +0.042** (×p_fill ; si rempli +0.74% du capital)
  - **deep** (entrée dip −8.596% → cible +6.278% / stop −5.956%, p_fill 18%, n_eff≈20.4) : P(cible|rempli) **78%** · **EV/risk +0.101** (×p_fill ; si rempli +3.41% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→77% · +1.0%→63% · +2.0%→38% · +3.0%→19% · +5.0%→6% · +8.0%→1%
- Range intraday médian 3.7% (p90 6.11%) · excursion haute méd. +1.54% / basse méd. −1.74%
- Profil de vol intra : ouverture 1.96% vs midi 0.867% vs clôture 1.072% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 89% · range 10% · trend ↑1%/↓0% ; spike-down 55% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.114 ; mean-reverting — autocorr -0.036)_ ; drift intra méd. -0.421% ; recovery-V 22%
- **σ réalisé intraday** 2.178% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 63% / bas 74% / whipsaw 37%
- POC intraday (dernière séance, temps-au-prix) : 144.949 (VA 144.011–146.021 ; dernier close 142.5)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−1.5%** sous le close veille · fill 50% · rebond 59% · **stop −3.82%** sous le fill (sous le bruit) · cible +1.47% · R/R 0.38 (high win-rate)
- Gaps overnight (n=159) : méd. 0.45% · baisse 34% (gap-down >1% 16% · >2% 8%)
- Excursion ouverture 5min (n=160) : bas méd −0.53% (p90 −1.67%) · haut méd +0.44% · range méd 1.11%
- Excursion ouverture 15min (n=160) : bas méd −0.67% (p90 −2.18%) · haut méd +0.59% · range méd 1.45%
- Excursion ouverture 30min (n=160) : bas méd −0.83% (p90 −2.23%) · haut méd +0.62% · range méd 1.67%
- Excursion ouverture 60min (n=160) : bas méd −0.92% (p90 −2.49%) · haut méd +0.73% · range méd 1.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 142.6 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 49% · séance 70% (116/159) · gap 25% · délai 0.4min · rebond 57% (61/116) (MFE +1.19%)
   - −1.0% : fill 30min 39% · séance 64% (108/159) · gap 16% · délai 8.9min · rebond 60% (61/108) (MFE +1.3%)
   - −1.5% : fill 30min 26% · séance 50% (89/159) · gap 11% · délai 22.9min · rebond 59% (50/89) (MFE +1.47%)
   - −2.0% : fill 30min 18% · séance 41% (74/159) · gap 8% · délai 62.1min · rebond 53% (44/74) (MFE +1.08%)
   - −3.0% : fill 30min 9% · séance 22% (47/159) · gap 2% · délai 200.8min · rebond 44% (27/47) (MFE +0.88%)
   - −4.0% : fill 30min 6% · séance 14% (33/159) · gap 1% · délai 76.7min · rebond 58% (22/33) (MFE +1.12%)
   - −5.0% : fill 30min 3% · séance 11% (24/159) · gap 0% · délai 388.5min · rebond 43% (12/24) (MFE +0.87%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.48% (p90 −1.75%) → stop au-delà de −1.19% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.39% (p90 −1.49%) → stop au-delà de −0.86% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.26% (p90 −0.95%) → stop au-delà de −0.7% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=522 jambes) : jambe baissière méd −1.03% (p90 −2.34%) · ~7.0 jambes/séance
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
      · −1.0% : fill 42% (42/89) · rebond 63% (23/42)
      · −2.0% : fill 22% (26/89) · rebond 64% (18/26)
      · −3.0% : fill 9% (14/89) · rebond 73% (10/14)
      · −4.0% : fill 4% (7/89) · rebond 47% (4/7)
      · −5.0% : fill 2% (3/89) · rebond 35% (1/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 44% en base · 64% si les 15 1res min sont vertes (75 cas) · 25% si rouges (85 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **1:29** → P(séance verte=clôture>ouverture) 72% si début vert vs 22% si rouge (base 44% · écart 49 pts) ; prédictivité sature ensuite (plafond brut 219min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **72%** · continue >prix actuel 56% ; creux résiduel méd -1.05% (q20 -2.14%) → **SL/trailing à −2.14%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.34% / q75 +2.29% → **scale +1.34% / runner +2.29%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **22%** (continue à baisser 61%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.72%** (au-delà de la MAE q10 -3.72%), cible rebond +1.04% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-1.93% .. +1.71%] · haut q95 +2.41% · bas q05 -2.6%
   - 60min (n=160) : retour [-2.47% .. +1.96%] · haut q95 +2.57% · bas q05 -2.91%
   - 2h (n=160) : retour [-2.8% .. +2.38%] · haut q95 +2.77% · bas q05 -3.56%
   - 4h (n=160) : retour [-3.17% .. +2.66%] · haut q95 +3.26% · bas q05 -4.01%
   - 6h (n=160) : retour [-3.71% .. +3.45%] · haut q95 +4.22% · bas q05 -4.59%
   - session (n=160) : retour [-4.9% .. +3.12%] · haut q95 +4.79% · bas q05 -6.19%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.43%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : entrée acceptable (proche d'une zone support/confluence)
- Proximité zone : 1.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.55 · part idiosyncratique 0.45
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.7  _(neutre)_
- **ADX** : 9.1  _(pas de tendance nette)_
- **MACD** : hist 0.656  _(pas de croisement recent)_
- **BB** : %B 0.54 · largeur 12.2%
- **ATR** : 5.2 (30.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.228  _(distribution)_
- **Vol ratio** : 0.38  _(volume atone)_
- **Choppiness** : 55.6  _(transition)_
- **MA** : MA20 142.48 · MA50 147.39 · MA200 153.13  _(prix > MA20)_
- **Dist MA** : MA20 +0.5% · MA50 -2.9% · MA200 -6.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (847353 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
