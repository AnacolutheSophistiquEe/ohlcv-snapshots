# CAT

**Generated** : 2026-08-22T18:26:39.225209+00:00  
**Santé technique** : 6/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $827.90  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $827.90 (+1.7% vs entrée) · entrée $814.00 · stop $797.78 · T1 $846.42 · R/R 2.0  
> ↳ P(T1 av. stop) 12 % · EV/risk -0.187 · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[LOW]** meta — meta.currency absent — symbole devise déduit du ticker (fallback).


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : — | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $811.38–$816.61 (mid $814.00)
- Spot actuel : $827.90 (+1.7% au-dessus de la zone — repli à attendre)
- Stop : $797.78 (stop swing_plan-based (-7.7%))
- Targets : T1 $846.42 · R/R 2.0 | T2 $849.75 · R/R 2.2 | T3 $853.08 · R/R 2.41
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $797.78


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.68 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (7.7 %)** : le gap seul le franchit 0.08 % des séances (1 fois sur 1254).
   - exécution **1.4 pt plus bas** dans le cas TYPIQUE (médiane), 1.4 au p90, **1.4 au pire**
   - perte réelle **9.1 %** en moyenne _(tirée par la queue)_, jusqu'à **9.1 %** — au lieu des 7.7 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0011 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 1 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.744 % | p01 -3.368 % | pire -9.1 % _(sur 1254 séances)_
- **P(stop avant cible)** _(source : daily, 1255 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0573** [0.0298 ; 0.0995] _(largeur 7.0 pt, n_eff 173.1)_
   - swing : **0.2582** [0.2142 ; 0.3062] _(largeur 9.2 pt, n_eff 345.7)_
   - deep : **0.3846** [0.3345 ; 0.4367] _(largeur 10.2 pt, n_eff 345.7)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-3.79 %** | CVaR **-4.9 %** | vol 2.5 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.39 % contre 2.82 % aujourd'hui, rapport 0.49)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.52 % vs -6.72 % si l'on extrapolait par √5 _(rapport 0.969 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0209** (β de hausse 0.9694, asymétrie 1.0531) vs SPY — 575 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 1.531× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 794.7429 sur atr_grid (1.0 ATR, 4.005 %) — p(stop avant cible) 0.5053 [0.45 ; 0.56], R/R 1.836, perte reelle 5.659 % (gap inclus), CVaR 4.014 %, EV 0.2513 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.3523 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : p_stop_first 0.505, borne haute 0.558 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
   - viole : CVaR 95 % 4.01 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 2.03 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.007 %) — p(stop avant cible) 0.3236 [0.28 ; 0.37], R/R 1.308, perte reelle 7.945 % (gap inclus), EV 0.8469 % — **REFUSE**
      - refuse : R/R 1.31 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 6.01 % > budget 3.00 %
   - ⚪ sr_based a 1.78 ATR (stop 9.725 %) — p(stop avant cible) 0.1392 [0.11 ; 0.18], R/R 1.068, perte reelle 9.725 % (gap inclus), EV 1.6268 % — **REFUSE**
      - refuse : R/R 1.07 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.72 % > budget 3.00 %
   - 🟢 support a 2.3 ATR (stop 11.821 %) — p(stop avant cible) 0.0908 [0.06 ; 0.12], R/R 0.879, perte reelle 11.821 % (gap inclus), EV 1.6283 % — **REFUSE**
      - refuse : R/R 0.88 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.82 % > budget 3.00 %
   - 🟢 support a 10.46 ATR (stop 44.507 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.233, perte reelle 44.507 % (gap inclus), EV 1.9161 % — **REFUSE**
      - refuse : R/R 0.23 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 44.51 % > budget 3.00 %
   - 🟢 support a 12.7 ATR (stop 53.464 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.194, perte reelle 53.464 % (gap inclus), EV 1.9161 % — **REFUSE**
      - refuse : R/R 0.19 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.46 % > budget 3.00 %
   - ⚪ atr_grid a 1.0 ATR (stop 4.005 %) — p(stop avant cible) 0.5053 [0.45 ; 0.56], R/R 1.836, perte reelle 5.659 % (gap inclus), EV 0.2513 % — **REFUSE**
      - refuse : p_stop_first 0.505, borne haute 0.558 > plafond 0.55 (le veto porte sur la BORNE, pas sur le point : un seuil applique a l'estimation serait aleatoire pres de la frontiere)
      - refuse : CVaR 95 % 4.01 % > budget 3.00 %
   - ⚪ grid_snapped a 1.78 ATR (stop 8.319 %) — p(stop avant cible) 0.1804 [0.14 ; 0.22], R/R 1.142, perte reelle 9.1 % (gap inclus), EV 1.5093 % — **REFUSE**
      - refuse : R/R 1.14 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.32 % > budget 3.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 14.017 %) — p(stop avant cible) 0.0208 [0.01 ; 0.04], R/R 0.741, perte reelle 14.017 % (gap inclus), EV 1.8417 % — **REFUSE**
      - refuse : R/R 0.74 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 14.02 % > budget 3.00 %
   - ⚪ atr_grid a 4.0 ATR (stop 16.02 %) — p(stop avant cible) 0.0075 [0.00 ; 0.02], R/R 0.649, perte reelle 16.02 % (gap inclus), EV 1.894 % — **REFUSE**
      - refuse : R/R 0.65 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.02 % > budget 3.00 %
   - ⚪ atr_grid a 4.5 ATR (stop 18.022 %) — p(stop avant cible) 0.0048 [0.00 ; 0.02], R/R 0.577, perte reelle 18.022 % (gap inclus), EV 1.897 % — **REFUSE**
      - refuse : R/R 0.58 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.02 % > budget 3.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 20.025 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 0.519, perte reelle 20.025 % (gap inclus), EV 1.9038 % — **REFUSE**
      - refuse : R/R 0.52 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.03 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 22.027 %) — p(stop avant cible) 0.0016 [0.00 ; 0.01], R/R 0.472, perte reelle 22.027 % (gap inclus), EV 1.9119 % — **REFUSE**
      - refuse : R/R 0.47 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.03 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 24.03 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.432, perte reelle 24.03 % (gap inclus), EV 1.9161 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.03 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 26.032 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.399, perte reelle 26.032 % (gap inclus), EV 1.9161 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.03 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 28.035 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.371, perte reelle 28.035 % (gap inclus), EV 1.9161 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.04 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 30.037 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.346, perte reelle 30.037 % (gap inclus), EV 1.9161 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.04 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 32.04 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.324, perte reelle 32.04 % (gap inclus), EV 1.9161 % — **REFUSE**
      - refuse : R/R 0.32 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 32.04 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.083 | EV/share : $1.337 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 10 % | T2 9 % | T3 6 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈216) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 21.2 | bear 9.3 | side 69.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : normal
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

- **RSI** : 49.5  _(neutre)_
- **ADX** : 13.1  _(pas de tendance nette)_
- **MACD** : hist 0.285  _(pas de croisement recent)_
- **BB** : %B 0.37 · largeur 12.2%
- **ATR** : 33.16 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.365  _(distribution)_
- **Vol ratio** : 0.65  _(volume normal)_
- **Choppiness** : 47.1  _(transition)_
- **MA** : MA20 841.36 · MA50 904.66 · MA200 758.83  _(prix < MA20)_
- **Dist MA** : MA20 -1.6% · MA50 -8.5% · MA200 +9.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (714983 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
