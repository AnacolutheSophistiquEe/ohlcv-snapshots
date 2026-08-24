# NNE

**Generated** : 2026-08-22T18:36:35.824463+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.8 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $18.85  

> 🟡 **WAIT-FOR-DIP** — spot +5.2 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $18.85 (+5.2% vs entrée) · entrée $17.91 · stop $17.10 · T1 $19.52 · R/R 1.99  
> ↳ P(T1 av. stop) 24 % · EV/risk 0.019 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[LOW]** meta — meta.currency absent — symbole devise déduit du ticker (fallback).


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : — | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $17.79–$18.02 (mid $17.91)
- Spot actuel : $18.85 (+5.2% au-dessus de la zone — repli à attendre)
- Stop : $17.10 (stop swing_plan-based (-17.39%))
- Targets : T1 $19.52 · R/R 1.99 | T2 $19.57 · R/R 2.05 | T3 $19.61 · R/R 2.1
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $17.10


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=11.87 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (17.39 %)** : le gap seul le franchit 0.349 % des séances (2 fois sur 573).
   - exécution **2.327 pt plus bas** dans le cas TYPIQUE (médiane), 2.77 au p90, **2.88 au pire**
   - perte réelle **19.717 %** en moyenne _(tirée par la queue)_, jusqu'à **20.27 %** — au lieu des 17.39 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0081 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.795 % | p01 -9.117 % | pire -20.27 % _(sur 573 séances)_
- **P(stop avant cible)** _(source : daily, 574 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.31** [0.2446 ; 0.3817] _(largeur 13.7 pt, n_eff 172.7)_
   - swing : **0.5589** [0.5043 ; 0.6125] _(largeur 10.8 pt, n_eff 321.3)_
   - deep : **0.5697** [0.5151 ; 0.6231] _(largeur 10.8 pt, n_eff 320.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 420 séances)** : VaR **-8.46 %** | CVaR **-11.57 %** | vol 6.65 %/j
   - _fenêtre arrêtée : rupture de regime a 480 seances en arriere (volatilite 11.09 % contre 6.20 % aujourd'hui, rapport 1.79)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -20.54 % vs -25.34 % si l'on extrapolait par √5 _(rapport 0.811 ; < 1 = le √5 surestime)_
- **β de baisse : 2.485** (β de hausse 1.9711, asymétrie 1.2607) vs SPY — 244 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 17.6474 sur atr_grid (1.0 ATR, 6.38 %) — p(stop avant cible) 0.7838 [0.74 ; 0.83], R/R 4.706, perte reelle 10.132 % (gap inclus), CVaR 6.478 %, EV -4.1728 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5471 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.784, borne haute 0.826 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 6.48 % > budget 6.20 %
- Budget de queue : **6.2 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 9.57 %) — p(stop avant cible) 0.6455 [0.59 ; 0.70], R/R 3.434, perte reelle 13.887 % (gap inclus), EV -3.8178 % — **REFUSE**
      - refuse : cible atteinte seulement 3.0 % du temps (< 15 %) meme a 10 seances : le R/R de 3.43 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.645, borne haute 0.696 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 9.62 % > budget 6.20 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.82 %) : P(cible) 3.0 % x 47.68 % + P(rien) 32.5 % x 11.47 % ne couvrent pas P(stop) 64.5 % x 13.89 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.44 ATR (stop 25.312 %) — p(stop avant cible) 0.1049 [0.07 ; 0.14], R/R 1.884, perte reelle 25.312 % (gap inclus), EV -0.5844 % — **REFUSE**
      - refuse : cible atteinte seulement 3.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.88 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 25.31 % > budget 6.20 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.58 %) : P(cible) 3.8 % x 47.68 % + P(rien) 85.7 % x 0.29 % ne couvrent pas P(stop) 10.5 % x 25.31 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 1.0 ATR (stop 6.38 %) — p(stop avant cible) 0.7838 [0.74 ; 0.83], R/R 4.706, perte reelle 10.132 % (gap inclus), EV -4.1728 % — **REFUSE**
      - refuse : cible atteinte seulement 2.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.784, borne haute 0.826 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.48 % > budget 6.20 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.17 %) : P(cible) 2.5 % x 47.68 % + P(rien) 19.2 % x 13.55 % ne couvrent pas P(stop) 78.4 % x 10.13 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 12.76 %) — p(stop avant cible) 0.5379 [0.48 ; 0.59], R/R 2.418, perte reelle 19.717 % (gap inclus), EV -5.1428 % — **REFUSE**
      - refuse : cible atteinte seulement 3.3 % du temps (< 15 %) meme a 10 seances : le R/R de 2.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.538, borne haute 0.592 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.78 % > budget 6.20 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-5.14 %) : P(cible) 3.3 % x 47.68 % + P(rien) 42.9 % x 9.06 % ne couvrent pas P(stop) 53.8 % x 19.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 15.95 %) — p(stop avant cible) 0.4246 [0.37 ; 0.48], R/R 2.418, perte reelle 19.717 % (gap inclus), EV -3.2402 % — **REFUSE**
      - refuse : cible atteinte seulement 3.4 % du temps (< 15 %) meme a 10 seances : le R/R de 2.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 15.96 % > budget 6.20 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.24 %) : P(cible) 3.4 % x 47.68 % + P(rien) 54.1 % x 6.46 % ne couvrent pas P(stop) 42.5 % x 19.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 19.14 %) — p(stop avant cible) 0.3003 [0.25 ; 0.35], R/R 2.418, perte reelle 19.717 % (gap inclus), EV -1.794 % — **REFUSE**
      - refuse : cible atteinte seulement 3.6 % du temps (< 15 %) meme a 10 seances : le R/R de 2.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.14 % > budget 6.20 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.79 %) : P(cible) 3.6 % x 47.68 % + P(rien) 66.4 % x 3.65 % ne couvrent pas P(stop) 30.0 % x 19.72 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.5 ATR (stop 28.709 %) — p(stop avant cible) 0.0461 [0.03 ; 0.07], R/R 1.661, perte reelle 28.709 % (gap inclus), EV -0.3578 % — **REFUSE**
      - refuse : cible atteinte seulement 3.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.66 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 28.71 % > budget 6.20 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.36 %) : P(cible) 3.9 % x 47.68 % + P(rien) 91.5 % x -0.99 % ne couvrent pas P(stop) 4.6 % x 28.71 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.0 ATR (stop 31.899 %) — p(stop avant cible) 0.024 [0.01 ; 0.05], R/R 1.495, perte reelle 31.899 % (gap inclus), EV -0.1246 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.90 % > budget 6.20 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.12 %) : P(cible) 4.0 % x 47.68 % + P(rien) 93.6 % x -1.36 % ne couvrent pas P(stop) 2.4 % x 31.90 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 5.5 ATR (stop 35.089 %) — p(stop avant cible) 0.0144 [0.01 ; 0.03], R/R 1.359, perte reelle 35.089 % (gap inclus), EV -0.0806 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 35.09 % > budget 6.20 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.08 %) : P(cible) 4.0 % x 47.68 % + P(rien) 94.5 % x -1.58 % ne couvrent pas P(stop) 1.4 % x 35.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.0 ATR (stop 38.279 %) — p(stop avant cible) 0.0106 [0.00 ; 0.03], R/R 1.246, perte reelle 38.279 % (gap inclus), EV -0.0509 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.28 % > budget 6.20 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.05 %) : P(cible) 4.0 % x 47.68 % + P(rien) 94.9 % x -1.66 % ne couvrent pas P(stop) 1.1 % x 38.28 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 6.5 ATR (stop 41.469 %) — p(stop avant cible) 0.0065 [0.00 ; 0.02], R/R 1.15, perte reelle 41.469 % (gap inclus), EV 0.0232 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.15 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.15 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.47 % > budget 6.20 %
   - ⚪ atr_grid a 7.0 ATR (stop 44.659 %) — p(stop avant cible) 0.0055 [0.00 ; 0.02], R/R 1.068, perte reelle 44.659 % (gap inclus), EV 0.0189 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.07 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.07 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.66 % > budget 6.20 %
   - ⚪ atr_grid a 7.5 ATR (stop 47.849 %) — p(stop avant cible) 0.004 [0.00 ; 0.02], R/R 0.997, perte reelle 47.849 % (gap inclus), EV 0.0058 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 47.85 % > budget 6.20 %
   - ⚪ atr_grid a 8.0 ATR (stop 51.039 %) — p(stop avant cible) 0.0012 [0.00 ; 0.01], R/R 0.934, perte reelle 51.039 % (gap inclus), EV 0.0228 % — **REFUSE**
      - refuse : cible atteinte seulement 4.0 % du temps (< 15 %) meme a 10 seances : le R/R de 0.93 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.93 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 51.04 % > budget 6.20 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.052 | EV/share : $-0.042 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 14 % | T2 12 % | T3 12 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.3 | bear 24.6 | side 70.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 151.0 (= 8 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 56.3  _(momentum haussier)_
- **ADX** : 15.2  _(pas de tendance nette)_
- **MACD** : hist 0.184  _(pas de croisement recent)_
- **BB** : %B 0.63 · largeur 31.7%
- **ATR** : 1.2 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF 0.03  _(neutre)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 55.9  _(transition)_
- **MA** : MA20 18.08 · MA50 19.47 · MA200 25.94  _(prix > MA20)_
- **Dist MA** : MA20 +4.3% · MA50 -3.2% · MA200 -27.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (721873 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
