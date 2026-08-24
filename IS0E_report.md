# IS0E

**Generated** : 2026-08-22T18:25:11.660378+00:00  
**Santé technique** : 10/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite high · $40.81  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $40.81 (+0.9% vs entrée) · entrée $40.46 · stop $40.00 · T1 $41.22 · R/R 1.65  
> ↳ P(T1 av. stop) 28 % · EV/risk -0.243 · ¼-Kelly 0.007 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 959 % hors [0,100] (R² max 0.93). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.
>   - **[LOW]** meta — meta.currency absent — symbole devise déduit du ticker (fallback).


## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : — | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🔴 **Santé haussière vs sur-extension** — Santé technique 10/10 élevée alors que : RSI 84.3 > 70 (surachat) ; %B 1.02 (collé à la bande haute) ; extension extrême (≥3×ATR, confluence MA20/50) — le score mesure la santé durable, PAS le timing ; entrée au prix actuel défavorable.
  - _Par DESIGN (le plus courant) : le score mesure la santé technique DURABLE (structure de tendance), pas le timing. Un uptrend sain mais étiré score haut ET flag surachat — c'est attendu ; le flag empêche de lire « score élevé = acheter maintenant »._
  - _Momentum parabolique : RSI > 70 + %B > 0,95 + extension extrême = phase d'accélération qui peut soit continuer (trend-following) soit se retourner brutalement → forte asymétrie de risque à l'entrée._
  - _Point de calcul à vérifier (≠ ce que disait l'audit §3.4) : le malus d'over-extension (ex-T_penalty, −2 si « extreme ») a été SORTI du score lors de la refonte §A3 — le score = santé pure, le malus vit dans le bloc TIMING (d'où le « étendu »). Donc le « score plafond + surachat » est normal, pas un poids mal calibré. Le seul vrai risque de calcul ici est la CLASSIFICATION d'over-extension elle-même (compute_overextension) : qu'« extreme » se déclenche au bon seuil._


## Lecture chartiste

Plan privilegie A (intraday), composite 10/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $40.31–$40.61 (mid $40.46)
- Spot actuel : $40.81 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $40.00 (stop swing_plan-based (-5.66%))
- Targets : T1 $41.22 · R/R 1.65 | T2 $41.98 · R/R 3.3 | T3 $42.74 · R/R 4.96
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $40.00


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.34 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.66 %)** : le gap seul le franchit 0.393 % des séances (5 fois sur 1272).
   - exécution **0.985 pt plus bas** dans le cas TYPIQUE (médiane), 6.421 au p90, **9.319 au pire**
   - perte réelle **8.165 %** en moyenne _(tirée par la queue)_, jusqu'à **14.979 %** — au lieu des 5.66 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0098 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.618 % | p01 -3.444 % | pire -14.979 % _(sur 1272 séances)_
- **P(stop avant cible)** _(source : daily, 1273 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0274** [0.0102 ; 0.0601] _(largeur 5.0 pt, n_eff 173.1)_
   - swing : **0.2869** [0.2411 ; 0.3362] _(largeur 9.5 pt, n_eff 345.8)_
   - deep : **0.4032** [0.3525 ; 0.4555] _(largeur 10.3 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-4.57 %** | CVaR **-7.35 %** | vol 3.36 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 1.64 % contre 3.31 % aujourd'hui, rapport 0.50)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -6.77 % vs -7.48 % si l'on extrapolait par √5 _(rapport 0.905 ; < 1 = le √5 surestime)_
- **β de baisse : 0.3038** (β de hausse 0.0415, asymétrie 7.3154) vs SPY — 567 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.184× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 38.7872 sur grid_snapped (1.02 ATR, 4.968 %) — p(stop avant cible) 0.454 [0.40 ; 0.51], R/R 1.416, perte reelle 7.367 % (gap inclus), CVaR 4.981 %, EV 0.1131 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.6604 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : R/R 1.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
   - viole : CVaR 95 % 4.98 % > budget 3.00 %
- Budget de queue : **3.0 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
   - ⚠ budget **borne** (brut 1.59 %) : les bornes sont un choix declare, pas une mesure.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ sr_based a 1.02 ATR (stop 6.286 %) — p(stop avant cible) 0.3514 [0.30 ; 0.40], R/R 1.066, perte reelle 9.786 % (gap inclus), EV 0.1828 % — **REFUSE**
      - refuse : R/R 1.07 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 6.29 % > budget 3.00 %
   - 🔴 support a 1.89 ATR (stop 9.524 %) — p(stop avant cible) 0.2217 [0.18 ; 0.27], R/R 0.697, perte reelle 14.979 % (gap inclus), EV 0.113 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 9.53 % > budget 3.00 %
      - ⚠ support DETECTE a 0.92 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ swing_based a 3.89 ATR (stop 17.05 %) — p(stop avant cible) 0.0512 [0.03 ; 0.08], R/R 0.612, perte reelle 17.05 % (gap inclus), EV 1.4382 % — **REFUSE**
      - refuse : R/R 0.61 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 17.05 % > budget 3.00 %
   - 🟢 support a 9.54 ATR (stop 38.252 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.273, perte reelle 38.252 % (gap inclus), EV 1.6384 % — **REFUSE**
      - refuse : R/R 0.27 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 38.25 % > budget 3.00 %
   - ⚪ grid_snapped a 1.02 ATR (stop 4.968 %) — p(stop avant cible) 0.454 [0.40 ; 0.51], R/R 1.416, perte reelle 7.367 % (gap inclus), EV 0.1131 % — **REFUSE**
      - refuse : R/R 1.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 4.98 % > budget 3.00 %
   - 🔴 grid_snapped a 1.89 ATR (stop 8.207 %) — p(stop avant cible) 0.2653 [0.22 ; 0.31], R/R 0.697, perte reelle 14.979 % (gap inclus), EV -0.3666 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 8.21 % > budget 3.00 %
      - 🚩 **LIGNE_EV_NEGATIVE** — le meilleur bracket disponible perd de l'argent en esperance (-0.37 %) : P(cible) 25.4 % x 10.43 % + P(rien) 48.1 % x 1.99 % ne couvrent pas P(stop) 26.5 % x 14.98 %.
        -> l'alternative dominante n'est pas un autre stop mais la REDUCTION ou la CLOTURE de la ligne. A remonter a l'etage portefeuille, pas a traiter en assouplissant les contraintes.
   - ⚪ atr_grid a 3.0 ATR (stop 11.262 %) — p(stop avant cible) 0.1724 [0.14 ; 0.21], R/R 0.697, perte reelle 14.979 % (gap inclus), EV 0.6282 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 11.26 % > budget 3.00 %
   - ⚪ atr_grid a 3.5 ATR (stop 13.139 %) — p(stop avant cible) 0.1081 [0.08 ; 0.14], R/R 0.697, perte reelle 14.979 % (gap inclus), EV 1.158 % — **REFUSE**
      - refuse : R/R 0.70 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 13.14 % > budget 3.00 %
   - ⚪ grid_snapped a 3.89 ATR (stop 15.732 %) — p(stop avant cible) 0.0593 [0.04 ; 0.09], R/R 0.663, perte reelle 15.732 % (gap inclus), EV 1.4384 % — **REFUSE**
      - refuse : R/R 0.66 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.73 % > budget 3.00 %
   - ⚪ atr_grid a 5.0 ATR (stop 18.769 %) — p(stop avant cible) 0.0378 [0.02 ; 0.06], R/R 0.556, perte reelle 18.769 % (gap inclus), EV 1.4277 % — **REFUSE**
      - refuse : R/R 0.56 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 18.77 % > budget 3.00 %
   - ⚪ atr_grid a 5.5 ATR (stop 20.646 %) — p(stop avant cible) 0.0268 [0.01 ; 0.05], R/R 0.505, perte reelle 20.646 % (gap inclus), EV 1.4966 % — **REFUSE**
      - refuse : R/R 0.51 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 20.65 % > budget 3.00 %
   - ⚪ atr_grid a 6.0 ATR (stop 22.523 %) — p(stop avant cible) 0.0159 [0.01 ; 0.03], R/R 0.463, perte reelle 22.523 % (gap inclus), EV 1.5591 % — **REFUSE**
      - refuse : R/R 0.46 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 22.52 % > budget 3.00 %
   - ⚪ atr_grid a 6.5 ATR (stop 24.4 %) — p(stop avant cible) 0.0095 [0.00 ; 0.02], R/R 0.428, perte reelle 24.4 % (gap inclus), EV 1.5708 % — **REFUSE**
      - refuse : R/R 0.43 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 24.40 % > budget 3.00 %
   - ⚪ atr_grid a 7.0 ATR (stop 26.277 %) — p(stop avant cible) 0.0032 [0.00 ; 0.01], R/R 0.397, perte reelle 26.277 % (gap inclus), EV 1.6137 % — **REFUSE**
      - refuse : R/R 0.40 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.28 % > budget 3.00 %
   - ⚪ atr_grid a 7.5 ATR (stop 28.154 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.371, perte reelle 28.154 % (gap inclus), EV 1.6384 % — **REFUSE**
      - refuse : R/R 0.37 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 28.15 % > budget 3.00 %
   - ⚪ atr_grid a 8.0 ATR (stop 30.031 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.347, perte reelle 30.031 % (gap inclus), EV 1.6384 % — **REFUSE**
      - refuse : R/R 0.35 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 30.03 % > budget 3.00 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.206 | EV/share : $0.095 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 17 % | T3 7 %
- Kelly (position) : f* 0.029 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 33.7 | bear 40.1 | side 26.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 612.0 (= 15 part(s) × prix) · cible 640.0


## Timing d'entrée (observe-only)

- **Verdict timing** : étendu — attendre un repli vers une zone
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : extreme
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

- **RSI** : 84.3  _(surachat)_
- **ADX** : 30.2  _(tendance etablie)_
- **MACD** : hist 0.623  _(pas de croisement recent)_
- **BB** : %B 1.02 · largeur 39.0%
- **ATR** : 1.53 (75.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF 0.324  _(accumulation)_
- **Vol ratio** : 1.63  _(volume au-dessus de la moyenne)_
- **Choppiness** : 24.7  _(marche directionnel)_
- **MA** : MA20 33.95 · MA50 32.29 · MA200 34.86  _(prix > MA20)_
- **Dist MA** : MA20 +20.2% · MA50 +26.4% · MA200 +17.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (716660 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
