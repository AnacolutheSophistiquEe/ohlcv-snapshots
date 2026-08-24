# NOK

**Generated** : 2026-08-22T18:39:46.946259+00:00  
**Santé technique** : 7/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $10.21  

> 🟡 **WAIT-FOR-DIP** — spot +0.8 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $10.21 (+0.8% vs entrée) · entrée $10.13 · stop $9.62 · T1 $10.61 · R/R 0.94  
> ↳ P(T1 av. stop) 46 % · EV/risk 0.094 · ¼-Kelly 0.025 · _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -112 % hors [0,100] (R² max 0.77). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.
>   - **[LOW]** meta — meta.currency absent — symbole devise déduit du ticker (fallback).


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : — | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.160 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $10.04–$10.21 (mid $10.13)
- Spot actuel : $10.21 (+0.8% au-dessus de la zone — repli à attendre)
- Stop : $9.62 (stop swing_plan-based (-5.79%))
- Targets : T1 $10.61 · R/R 0.94 | T2 $11.10 · R/R 1.9 | T3 $11.58 · R/R 2.84
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $9.62


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.51 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (5.79 %)** : le gap seul le franchit 0.797 % des séances (10 fois sur 1254).
   - exécution **1.269 pt plus bas** dans le cas TYPIQUE (médiane), 2.046 au p90, **2.946 au pire**
   - perte réelle **7.104 %** en moyenne _(tirée par la queue)_, jusqu'à **8.736 %** — au lieu des 5.79 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0105 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.595 % | p01 -5.36 % | pire -8.736 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1312** [0.0871 ; 0.1875] _(largeur 10.0 pt, n_eff 173.1)_
   - swing : **0.3417** [0.2932 ; 0.3929] _(largeur 10.0 pt, n_eff 345.7)_
   - deep : **0.404** [0.3533 ; 0.4563] _(largeur 10.3 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-5.37 %** | CVaR **-7.16 %** | vol 3.79 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 2.43 % contre 4.39 % aujourd'hui, rapport 0.55)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -7.99 % vs -7.95 % si l'on extrapolait par √5 _(rapport 1.004 ; < 1 = le √5 surestime)_
- **β de baisse : 0.8826** (β de hausse 0.7788, asymétrie 1.1334) vs SPY — 575 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.008× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 9.7649 sur sr_based (0.35 ATR, 4.359 %) — p(stop avant cible) 0.5121 [0.46 ; 0.56], R/R 4.336, perte reelle 6.308 % (gap inclus), CVaR 4.385 %, EV 0.5925 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.4882 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : p_stop_first 0.512, borne haute 0.565 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 4.39 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 2.24 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 0.35 ATR (stop 4.359 %) — p(stop avant cible) 0.5121 [0.46 ; 0.56], R/R 4.336, perte reelle 6.308 % (gap inclus), EV 0.5925 % — **REFUSE**
      - refuse : cible atteinte seulement 4.5 % du temps (< 15 %) meme a 10 seances : le R/R de 4.34 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : p_stop_first 0.512, borne haute 0.565 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 4.39 % > budget 3.00 %
   - 🔴 support a 0.83 ATR (stop 6.725 %) — p(stop avant cible) 0.366 [0.32 ; 0.42], R/R 3.684, perte reelle 7.424 % (gap inclus), EV 2.1358 % — **REFUSE**
      - refuse : cible atteinte seulement 6.3 % du temps (< 15 %) meme a 10 seances : le R/R de 3.68 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 6.73 % > budget 3.00 %
      - ⚠ support DETECTE a 0.25 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ swing_based a 2.35 ATR (stop 14.282 %) — p(stop avant cible) 0.1597 [0.12 ; 0.20], R/R 1.915, perte reelle 14.282 % (gap inclus), EV 2.3416 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 14.28 % > budget 3.00 %
   - 🟢 support a 9.37 ATR (stop 49.232 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.556, perte reelle 49.232 % (gap inclus), EV 2.3841 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.56 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 49.23 % > budget 3.00 %
   - 🟢 support a 11.78 ATR (stop 61.181 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.447, perte reelle 61.181 % (gap inclus), EV 2.3841 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.45 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.45 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 61.18 % > budget 3.00 %
   - ⚪ atr_grid a 1.75 ATR (stop 8.704 %) — p(stop avant cible) 0.2937 [0.25 ; 0.34], R/R 3.131, perte reelle 8.736 % (gap inclus), EV 2.6562 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 3.13 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 8.70 % > budget 3.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 17.409 %) — p(stop avant cible) 0.0897 [0.06 ; 0.12], R/R 1.571, perte reelle 17.409 % (gap inclus), EV 2.249 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.57 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.57 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.41 % > budget 3.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 19.896 %) — p(stop avant cible) 0.0503 [0.03 ; 0.08], R/R 1.375, perte reelle 19.896 % (gap inclus), EV 2.3598 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.37 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.37 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 19.90 % > budget 3.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 22.383 %) — p(stop avant cible) 0.0304 [0.02 ; 0.05], R/R 1.222, perte reelle 22.383 % (gap inclus), EV 2.394 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.22 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.22 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.38 % > budget 3.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 24.87 %) — p(stop avant cible) 0.0156 [0.01 ; 0.03], R/R 1.1, perte reelle 24.87 % (gap inclus), EV 2.3783 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.10 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.10 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.87 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 27.357 %) — p(stop avant cible) 0.0052 [0.00 ; 0.02], R/R 1.0, perte reelle 27.357 % (gap inclus), EV 2.3771 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 1.00 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.00 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 27.36 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 29.844 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.916, perte reelle 29.844 % (gap inclus), EV 2.3841 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.92 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.92 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 29.84 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 32.331 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.846, perte reelle 32.331 % (gap inclus), EV 2.3841 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.85 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.85 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.33 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 34.818 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.786, perte reelle 34.818 % (gap inclus), EV 2.3841 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.79 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.79 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 34.82 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 37.305 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.733, perte reelle 37.305 % (gap inclus), EV 2.3841 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.73 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.73 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 37.30 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 39.792 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.687, perte reelle 39.792 % (gap inclus), EV 2.3841 % — **REFUSE**
      - refuse : cible atteinte seulement 6.7 % du temps (< 15 %) meme a 10 seances : le R/R de 0.69 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.69 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 39.79 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.188 | EV/share : $0.095 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 27 % | T3 14 %
- Kelly (position) : f* 0.099 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈214) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.8 | bear 7.0 | side 7.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 510.0 (= 50 part(s) × prix) · cible 512.0


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

- **RSI** : 61.4  _(momentum haussier)_
- **ADX** : 19.0  _(pas de tendance nette)_
- **MACD** : hist 0.19  _(pas de croisement recent)_
- **BB** : %B 0.68 · largeur 27.4%
- **ATR** : 0.51 (65.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV rising · CMF -0.164  _(distribution)_
- **Vol ratio** : 0.55  _(volume atone)_
- **Choppiness** : 47.9  _(transition)_
- **MA** : MA20 9.72 · MA50 11.32 · MA200 9.44  _(prix > MA20)_
- **Dist MA** : MA20 +5.1% · MA50 -9.8% · MA200 +8.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (724674 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
