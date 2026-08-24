# NVTS

**Generated** : 2026-08-22T18:29:39.522347+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.5 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $12.97  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $12.97 (+0.9% vs entrée) · entrée $12.85 · stop $12.20 · T1 $14.14 · R/R 1.98  
> ↳ P(T1 av. stop) 17 % · EV/risk -0.219 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[LOW]** meta — meta.currency absent — symbole devise déduit du ticker (fallback).


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : — | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.050 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $12.75–$12.94 (mid $12.85)
- Spot actuel : $12.97 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $12.20 (stop swing_plan-based (-10.81%))
- Targets : T1 $14.14 · R/R 1.98 | T2 $14.18 · R/R 2.05 | T3 $14.21 · R/R 2.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $12.20


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=8.90 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.81 %)** : le gap seul le franchit 0.66 % des séances (8 fois sur 1213).
   - exécution **4.209 pt plus bas** dans le cas TYPIQUE (médiane), 11.297 au p90, **11.576 au pire**
   - perte réelle **16.118 %** en moyenne _(tirée par la queue)_, jusqu'à **22.386 %** — au lieu des 10.81 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.035 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 8 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -4.054 % | p01 -8.611 % | pire -22.386 % _(sur 1213 séances)_
- **P(stop avant cible)** _(source : daily, 1214 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3693** [0.3 ; 0.4429] _(largeur 14.3 pt, n_eff 173.1)_
   - swing : **0.5261** [0.4734 ; 0.5783] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.5331** [0.4804 ; 0.5852] _(largeur 10.5 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-9.72 %** | CVaR **-13.19 %** | vol 7.71 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 23.11 % contre 8.49 % aujourd'hui, rapport 2.72)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -19.22 % vs -20.03 % si l'on extrapolait par √5 _(rapport 0.959 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6595** (β de hausse 2.0018, asymétrie 0.829) vs SPY — 556 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.973× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 12.119 sur support (0.48 ATR, 6.561 %) — p(stop avant cible) 0.7228 [0.67 ; 0.77], R/R 2.848, perte reelle 11.812 % (gap inclus), CVaR 6.643 %, EV -2.2136 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.5359 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.723, borne haute 0.768 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 6.64 % > budget 5.83 %
- Budget de queue : **5.83 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.48 ATR (stop 6.561 %) — p(stop avant cible) 0.7228 [0.67 ; 0.77], R/R 2.848, perte reelle 11.812 % (gap inclus), EV -2.2136 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 2.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.723, borne haute 0.768 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 6.64 % > budget 5.83 %
      - ⚠ support DETECTE a 0.48 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-2.21 %) : P(cible) 14.9 % x 33.64 % + P(rien) 12.8 % x 10.24 % ne couvrent pas P(stop) 72.3 % x 11.81 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_based a 1.5 ATR (stop 12.044 %) — p(stop avant cible) 0.5325 [0.48 ; 0.58], R/R 1.787, perte reelle 18.827 % (gap inclus), EV -1.1239 % — **REFUSE**
      - refuse : p_stop_first 0.532, borne haute 0.585 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 12.07 % > budget 5.83 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.12 %) : P(cible) 21.2 % x 33.64 % + P(rien) 25.6 % x 6.94 % ne couvrent pas P(stop) 53.2 % x 18.83 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - 🟢 support a 1.51 ATR (stop 14.85 %) — p(stop avant cible) 0.4627 [0.41 ; 0.52], R/R 1.675, perte reelle 20.086 % (gap inclus), EV -0.3484 % — **REFUSE**
      - refuse : CVaR 95 % 14.87 % > budget 5.83 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.35 %) : P(cible) 21.7 % x 33.64 % + P(rien) 32.0 % x 5.10 % ne couvrent pas P(stop) 46.3 % x 20.09 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ swing_based a 3.6 ATR (stop 31.606 %) — p(stop avant cible) 0.0645 [0.04 ; 0.09], R/R 1.064, perte reelle 31.606 % (gap inclus), EV 3.2795 % — **REFUSE**
      - refuse : R/R 1.06 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 31.61 % > budget 5.83 %
   - 🟢 support a 4.31 ATR (stop 37.325 %) — p(stop avant cible) 0.0334 [0.02 ; 0.06], R/R 0.901, perte reelle 37.325 % (gap inclus), EV 3.1914 % — **REFUSE**
      - refuse : R/R 0.90 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.32 % > budget 5.83 %
   - ⚪ atr_grid a 1.0 ATR (stop 8.029 %) — p(stop avant cible) 0.6686 [0.62 ; 0.72], R/R 2.575, perte reelle 13.062 % (gap inclus), EV -1.3004 % — **REFUSE**
      - refuse : p_stop_first 0.669, borne haute 0.717 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 8.09 % > budget 5.83 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-1.30 %) : P(cible) 17.9 % x 33.64 % + P(rien) 15.3 % x 9.30 % ne couvrent pas P(stop) 66.9 % x 13.06 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 2.25 ATR (stop 18.066 %) — p(stop avant cible) 0.3499 [0.30 ; 0.40], R/R 1.574, perte reelle 21.366 % (gap inclus), EV 1.7344 % — **REFUSE**
      - refuse : R/R 1.57 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.07 % > budget 5.83 %
   - ⚪ atr_grid a 2.75 ATR (stop 22.081 %) — p(stop avant cible) 0.2368 [0.19 ; 0.28], R/R 1.503, perte reelle 22.386 % (gap inclus), EV 3.3594 % — **REFUSE**
      - refuse : R/R 1.50 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.08 % > budget 5.83 %
   - ⚪ atr_grid a 5.0 ATR (stop 40.146 %) — p(stop avant cible) 0.0209 [0.01 ; 0.04], R/R 0.838, perte reelle 40.146 % (gap inclus), EV 3.1694 % — **REFUSE**
      - refuse : R/R 0.84 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 40.15 % > budget 5.83 %
   - ⚪ atr_grid a 5.5 ATR (stop 44.161 %) — p(stop avant cible) 0.0114 [0.00 ; 0.03], R/R 0.762, perte reelle 44.161 % (gap inclus), EV 3.1411 % — **REFUSE**
      - refuse : R/R 0.76 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.16 % > budget 5.83 %
   - ⚪ atr_grid a 6.0 ATR (stop 48.176 %) — p(stop avant cible) 0.0019 [0.00 ; 0.01], R/R 0.698, perte reelle 48.176 % (gap inclus), EV 3.2239 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 48.18 % > budget 5.83 %
   - ⚪ atr_grid a 6.5 ATR (stop 52.19 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.644, perte reelle 52.19 % (gap inclus), EV 3.2275 % — **REFUSE**
      - refuse : R/R 0.64 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 52.19 % > budget 5.83 %
   - ⚪ atr_grid a 7.0 ATR (stop 56.205 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.598, perte reelle 56.205 % (gap inclus), EV 3.2275 % — **REFUSE**
      - refuse : R/R 0.60 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 56.20 % > budget 5.83 %
   - ⚪ atr_grid a 7.5 ATR (stop 60.22 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.559, perte reelle 60.22 % (gap inclus), EV 3.2275 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 60.22 % > budget 5.83 %
   - ⚪ atr_grid a 8.0 ATR (stop 64.234 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.524, perte reelle 64.234 % (gap inclus), EV 3.2275 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 64.23 % > budget 5.83 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.076 | EV/share : $0.049 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 18 % | T2 17 % | T3 17 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 9.5 | bear 5.7 | side 84.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 506.0 (= 39 part(s) × prix) · cible 512.0


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

- **RSI** : 59.5  _(momentum haussier)_
- **ADX** : 15.4  _(pas de tendance nette)_
- **MACD** : hist 0.223  _(pas de croisement recent)_
- **BB** : %B 0.57 · largeur 44.4%
- **ATR** : 1.04 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF -0.054  _(distribution)_
- **Vol ratio** : 0.94  _(volume normal)_
- **Choppiness** : 57.6  _(transition)_
- **MA** : MA20 12.56 · MA50 14.93 · MA200 12.76  _(prix > MA20)_
- **Dist MA** : MA20 +3.3% · MA50 -13.2% · MA200 +1.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (721915 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
