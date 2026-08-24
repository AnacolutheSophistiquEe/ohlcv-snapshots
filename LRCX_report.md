# LRCX

**Generated** : 2026-08-22T18:32:37.339009+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.6 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $314.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $314.00 (+0.7% vs entrée) · entrée $311.69 · stop $306.47 · T1 $321.23 · R/R 1.83  
> ↳ P(T1 av. stop) 20 % · EV/risk -0.491 · ¼-Kelly 0.013 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[LOW]** meta — meta.currency absent — symbole devise déduit du ticker (fallback).


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : — | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.120 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $309.78–$313.60 (mid $311.69)
- Spot actuel : $314.00 (+0.7% au-dessus de la zone — repli à attendre)
- Stop : $306.47 (stop swing_plan-based (-7.16%))
- Targets : T1 $321.23 · R/R 1.83 | T2 $330.77 · R/R 3.66 | T3 $340.31 · R/R 5.48
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $306.47


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.47 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.16 %)** : le gap seul le franchit 0.319 % des séances (4 fois sur 1254).
   - exécution **0.88 pt plus bas** dans le cas TYPIQUE (médiane), 2.091 au p90, **2.566 au pire**
   - perte réelle **8.256 %** en moyenne _(tirée par la queue)_, jusqu'à **9.726 %** — au lieu des 7.16 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0035 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 4 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.812 % | p01 -4.795 % | pire -9.726 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1454** [0.0989 ; 0.2036] _(largeur 10.5 pt, n_eff 173.1)_
   - swing : **0.3963** [0.3458 ; 0.4485] _(largeur 10.3 pt, n_eff 345.7)_
   - deep : **0.4599** [0.4079 ; 0.5126] _(largeur 10.5 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.08 %** | CVaR **-8.04 %** | vol 4.02 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.08 % contre 4.74 % aujourd'hui, rapport 0.44)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.73 % vs -11.22 % si l'on extrapolait par √5 _(rapport 0.868 ; < 1 = le √5 surestime)_
- **β de baisse : 1.6164** (β de hausse 1.95, asymétrie 0.8289) vs SPY — 575 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.482× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 293.8907 sur sr_based (0.63 ATR, 6.404 %) — p(stop avant cible) 0.4712 [0.42 ; 0.52], R/R 2.469, perte reelle 7.526 % (gap inclus), CVaR 6.41 %, EV 1.2288 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.8854 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 6.41 % > budget 3.40 %
- Budget de queue : **3.4 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.63 ATR (stop 6.404 %) — p(stop avant cible) 0.4712 [0.42 ; 0.52], R/R 2.469, perte reelle 7.526 % (gap inclus), EV 1.2288 % — **REFUSE**
      - refuse : cible atteinte seulement 13.2 % du temps (< 15 %) meme a 10 seances : le R/R de 2.47 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 6.41 % > budget 3.40 %
   - 🔴 support a 0.88 ATR (stop 7.796 %) — p(stop avant cible) 0.4069 [0.36 ; 0.46], R/R 2.16, perte reelle 8.602 % (gap inclus), EV 1.5158 % — **REFUSE**
      - refuse : cible atteinte seulement 14.0 % du temps (< 15 %) meme a 10 seances : le R/R de 2.16 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 7.80 % > budget 3.40 %
      - ⚠ support DETECTE a 0.53 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ swing_based a 3.85 ATR (stop 24.238 %) — p(stop avant cible) 0.0145 [0.01 ; 0.03], R/R 0.766, perte reelle 24.238 % (gap inclus), EV 3.413 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.77 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.77 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.24 % > budget 3.40 %
   - 🟢 support a 4.19 ATR (stop 26.092 %) — p(stop avant cible) 0.0068 [0.00 ; 0.02], R/R 0.712, perte reelle 26.092 % (gap inclus), EV 3.4642 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.71 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.71 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.09 % > budget 3.40 %
   - 🟢 support a 6.9 ATR (stop 41.142 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.452, perte reelle 41.142 % (gap inclus), EV 3.4797 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.45 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 41.14 % > budget 3.40 %
   - ⚪ atr_grid a 1.75 ATR (stop 9.691 %) — p(stop avant cible) 0.2951 [0.25 ; 0.34], R/R 1.91, perte reelle 9.726 % (gap inclus), EV 2.4538 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.91 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 9.69 % > budget 3.40 %
   - ⚪ atr_grid a 2.0 ATR (stop 11.076 %) — p(stop avant cible) 0.2362 [0.19 ; 0.28], R/R 1.677, perte reelle 11.076 % (gap inclus), EV 2.7319 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 11.08 % > budget 3.40 %
   - ⚪ atr_grid a 2.25 ATR (stop 12.46 %) — p(stop avant cible) 0.1995 [0.16 ; 0.24], R/R 1.491, perte reelle 12.46 % (gap inclus), EV 2.8562 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.49 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.49 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 12.46 % > budget 3.40 %
   - ⚪ atr_grid a 2.75 ATR (stop 15.229 %) — p(stop avant cible) 0.1467 [0.11 ; 0.19], R/R 1.22, perte reelle 15.229 % (gap inclus), EV 2.7825 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.23 % > budget 3.40 %
   - ⚪ atr_grid a 3.0 ATR (stop 16.614 %) — p(stop avant cible) 0.1279 [0.10 ; 0.17], R/R 1.118, perte reelle 16.614 % (gap inclus), EV 2.8049 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 1.12 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.12 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.61 % > budget 3.40 %
   - ⚪ atr_grid a 3.5 ATR (stop 19.383 %) — p(stop avant cible) 0.076 [0.05 ; 0.11], R/R 0.958, perte reelle 19.383 % (gap inclus), EV 3.0366 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.96 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.96 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.38 % > budget 3.40 %
   - ⚪ atr_grid a 5.0 ATR (stop 27.69 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.671, perte reelle 27.69 % (gap inclus), EV 3.4797 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.67 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.67 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.69 % > budget 3.40 %
   - ⚪ atr_grid a 5.5 ATR (stop 30.459 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.61, perte reelle 30.459 % (gap inclus), EV 3.4797 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.61 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.61 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.46 % > budget 3.40 %
   - ⚪ atr_grid a 6.0 ATR (stop 33.228 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.559, perte reelle 33.228 % (gap inclus), EV 3.4797 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 33.23 % > budget 3.40 %
   - ⚪ atr_grid a 6.5 ATR (stop 35.997 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.516, perte reelle 35.997 % (gap inclus), EV 3.4797 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.52 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 36.00 % > budget 3.40 %
   - ⚪ atr_grid a 8.0 ATR (stop 44.304 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.419, perte reelle 44.304 % (gap inclus), EV 3.4797 % — **REFUSE**
      - refuse : cible atteinte seulement 14.9 % du temps (< 15 %) meme a 10 seances : le R/R de 0.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.30 % > budget 3.40 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.35 | EV/share : $1.824 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 36 % | T2 15 % | T3 4 %
- Kelly (position) : f* 0.053 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 19.4 | bear 5.0 | side 75.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 314.0 (= 1 part(s) × prix) · cible 512.0


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
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 57.1  _(momentum haussier)_
- **ADX** : 10.4  _(pas de tendance nette)_
- **MACD** : hist 1.545  _(pas de croisement recent)_
- **BB** : %B 0.57 · largeur 28.2%
- **ATR** : 17.39 (79.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.12  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 58.8  _(transition)_
- **MA** : MA20 307.9 · MA50 337.26 · MA200 253.35  _(prix > MA20)_
- **Dist MA** : MA20 +2.0% · MA50 -6.9% · MA200 +23.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (722589 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
