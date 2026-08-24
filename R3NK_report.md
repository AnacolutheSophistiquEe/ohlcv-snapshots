# R3NK

**Generated** : 2026-08-22T18:35:35.106114+00:00  
**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $47.81  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $47.81 (+3.6% vs entrée) · entrée $46.16 · stop $45.45 · T1 $46.75 · R/R 0.83  
> ↳ P(T1 av. stop) 43 % · EV/risk -0.051 · ¼-Kelly 0.002 · _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[LOW]** meta — meta.currency absent — symbole devise déduit du ticker (fallback).


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : — | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $46.04–$46.27 (mid $46.16)
- Spot actuel : $47.81 (+3.6% au-dessus de la zone — repli à attendre)
- Stop : $45.45 (stop swing_plan-based (-12.56%))
- Targets : T1 $46.75 · R/R 0.83 | T2 $47.34 · R/R 1.66 | T3 $47.93 · R/R 2.49
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $45.45


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.96 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (12.56 %)** : le gap seul le franchit 0.156 % des séances (1 fois sur 643).
   - exécution **9.316 pt plus bas** dans le cas TYPIQUE (médiane), 9.316 au p90, **9.316 au pire**
   - perte réelle **21.876 %** en moyenne _(tirée par la queue)_, jusqu'à **21.876 %** — au lieu des 12.56 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0145 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.36 % | p01 -5.125 % | pire -21.876 % _(sur 643 séances)_
- **P(stop avant cible)** _(source : daily, 644 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1281** [0.0846 ; 0.184] _(largeur 9.9 pt, n_eff 172.9)_
   - swing : **0.4328** [0.3801 ; 0.4867] _(largeur 10.7 pt, n_eff 329.4)_
   - deep : **0.5186** [0.4646 ; 0.5722] _(largeur 10.8 pt, n_eff 328.9)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 600 séances)** : VaR **-5.47 %** | CVaR **-7.11 %** | vol 3.49 %/j
   - _fenêtre arrêtée : historique epuise — le regime est homogene sur toute la profondeur_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.16 % vs -12.26 % si l'on extrapolait par √5 _(rapport 0.911 ; < 1 = le √5 surestime)_
- **β de baisse : 0.2456** (β de hausse -0.0551, asymétrie -4.4556) vs SPY — 269 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.322× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 44.7976 sur swing_based (0.76 ATR, 6.311 %) — p(stop avant cible) 0.5514 [0.50 ; 0.60], R/R 3.617, perte reelle 11.049 % (gap inclus), CVaR 6.34 %, EV -2.2221 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.2126 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.551, borne haute 0.605 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 6.34 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 1.2 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ swing_based a 0.76 ATR (stop 6.311 %) — p(stop avant cible) 0.5514 [0.50 ; 0.60], R/R 3.617, perte reelle 11.049 % (gap inclus), EV -2.2221 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 3.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.551, borne haute 0.605 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.34 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.22 %) : P(cible) 0.8 % x 39.97 % + P(rien) 44.0 % x 8.05 % ne couvrent pas P(stop) 55.1 % x 11.05 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ sr_based a 2.92 ATR (stop 16.957 %) — p(stop avant cible) 0.115 [0.08 ; 0.15], R/R 1.827, perte reelle 21.876 % (gap inclus), EV -0.1553 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 16.96 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.16 %) : P(cible) 0.8 % x 39.97 % + P(rien) 87.7 % x 2.31 % ne couvrent pas P(stop) 11.5 % x 21.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 3.17 ATR (stop 18.219 %) — p(stop avant cible) 0.0933 [0.07 ; 0.13], R/R 1.827, perte reelle 21.876 % (gap inclus), EV 0.0849 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 18.22 % > budget 3.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 8.619 %) — p(stop avant cible) 0.4343 [0.38 ; 0.49], R/R 2.618, perte reelle 15.263 % (gap inclus), EV -2.613 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 2.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 8.64 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.61 %) : P(cible) 0.8 % x 39.97 % + P(rien) 55.7 % x 6.61 % ne couvrent pas P(stop) 43.4 % x 15.26 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.0 ATR (stop 9.85 %) — p(stop avant cible) 0.4028 [0.35 ; 0.46], R/R 1.827, perte reelle 21.876 % (gap inclus), EV -4.7833 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 9.87 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-4.78 %) : P(cible) 0.8 % x 39.97 % + P(rien) 58.9 % x 6.28 % ne couvrent pas P(stop) 40.3 % x 21.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 11.082 %) — p(stop avant cible) 0.3184 [0.27 ; 0.37], R/R 1.827, perte reelle 21.876 % (gap inclus), EV -3.1782 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 11.10 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-3.18 %) : P(cible) 0.8 % x 39.97 % + P(rien) 67.3 % x 5.13 % ne couvrent pas P(stop) 31.8 % x 21.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.5 ATR (stop 12.313 %) — p(stop avant cible) 0.2736 [0.23 ; 0.32], R/R 1.827, perte reelle 21.876 % (gap inclus), EV -2.3311 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 12.33 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.33 %) : P(cible) 0.8 % x 39.97 % + P(rien) 71.8 % x 4.63 % ne couvrent pas P(stop) 27.4 % x 21.88 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 4.0 ATR (stop 19.701 %) — p(stop avant cible) 0.0671 [0.04 ; 0.10], R/R 1.827, perte reelle 21.876 % (gap inclus), EV 0.2945 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.83 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 19.70 % > budget 3.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 22.164 %) — p(stop avant cible) 0.0509 [0.03 ; 0.08], R/R 1.803, perte reelle 22.164 % (gap inclus), EV 0.3669 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.80 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 22.16 % > budget 3.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 24.626 %) — p(stop avant cible) 0.0308 [0.02 ; 0.05], R/R 1.623, perte reelle 24.626 % (gap inclus), EV 0.3609 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.62 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 24.63 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.089 %) — p(stop avant cible) 0.0141 [0.01 ; 0.03], R/R 1.475, perte reelle 27.089 % (gap inclus), EV 0.4254 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.48 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.48 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.09 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 29.551 %) — p(stop avant cible) 0.0058 [0.00 ; 0.02], R/R 1.352, perte reelle 29.551 % (gap inclus), EV 0.5104 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.35 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.35 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.55 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 32.014 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 1.248, perte reelle 32.014 % (gap inclus), EV 0.587 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.25 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.25 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.01 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 34.477 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.159, perte reelle 34.477 % (gap inclus), EV 0.6475 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.16 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.48 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 36.939 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.082, perte reelle 36.939 % (gap inclus), EV 0.6475 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.08 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.08 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.94 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 39.402 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 1.014, perte reelle 39.402 % (gap inclus), EV 0.6475 % — **REFUSE**
      - refuse : cible atteinte seulement 0.8 % du temps (< 15 %) meme a 10 seances : le R/R de 1.01 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.01 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.40 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : -0.093 | EV/share : $-0.066 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 36 % | T3 19 %
- Kelly (position) : f* 0.009 | ¼-Kelly 0.002 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.5 | bear 66.4 | side 17.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 143.0 (= 3 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 44.9  _(momentum baissier)_
- **ADX** : 25.6  _(tendance etablie)_
- **MACD** : hist -0.303  _(bearish_recent)_
- **BB** : %B 0.22 · largeur 11.0%
- **ATR** : 2.35 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.107  _(distribution)_
- **Vol ratio** : 0.61  _(volume normal)_
- **Choppiness** : 58.3  _(transition)_
- **MA** : MA20 49.32 · MA50 46.59 · MA200 52.3  _(prix < MA20)_
- **Dist MA** : MA20 -3.1% · MA50 +2.6% · MA200 -8.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (722957 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
