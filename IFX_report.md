# IFX

**Generated** : 2026-08-22T18:18:57.036473+00:00  
**Santé technique** : 3/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $55.97  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $55.97 (+0.9% vs entrée) · entrée $55.49 · stop $54.68 · T1 $56.73 · R/R 1.53  
> ↳ P(T1 av. stop) 31 % · EV/risk -0.29 · ¼-Kelly 0.007 · _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (2, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -22 % hors [0,100] (R² max 0.49). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.
>   - **[LOW]** meta — meta.currency absent — symbole devise déduit du ticker (fallback).


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : — | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $55.24–$55.74 (mid $55.49)
- Spot actuel : $55.97 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $54.68 (stop swing_plan-based (-6.69%))
- Targets : T1 $56.73 · R/R 1.53 | T2 $57.97 · R/R 3.06 | T3 $59.21 · R/R 4.59
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $54.68


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=2.59 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (6.69 %)** : le gap seul le franchit 0.235 % des séances (3 fois sur 1274).
   - exécution **2.342 pt plus bas** dans le cas TYPIQUE (médiane), 2.957 au p90, **3.111 au pire**
   - perte réelle **8.542 %** en moyenne _(tirée par la queue)_, jusqu'à **9.801 %** — au lieu des 6.69 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0044 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -2.238 % | p01 -4.029 % | pire -9.801 % _(sur 1274 séances)_
- **P(stop avant cible)** _(source : daily, 1275 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1147** [0.0737 ; 0.1685] _(largeur 9.5 pt, n_eff 173.1)_
   - swing : **0.3666** [0.3171 ; 0.4183] _(largeur 10.1 pt, n_eff 345.8)_
   - deep : **0.4327** [0.3812 ; 0.4853] _(largeur 10.4 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-5.31 %** | CVaR **-6.71 %** | vol 3.24 %/j
   - _fenêtre arrêtée : rupture de regime a 180 seances en arriere (volatilite 2.16 % contre 4.07 % aujourd'hui, rapport 0.53)_
   - ⚠ le regime n'est homogene que sur 120 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.09 % vs -8.88 % si l'on extrapolait par √5 _(rapport 1.024 ; < 1 = le √5 surestime)_
- **β de baisse : 0.8469** (β de hausse 0.7323, asymétrie 1.1565) vs SPY — 567 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 2.264× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 52.6466 sur support (0.71 ATR, 5.938 %) — p(stop avant cible) 0.451 [0.40 ; 0.50], R/R 1.624, perte reelle 7.901 % (gap inclus), CVaR 5.944 %, EV 0.4344 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 0.9425 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : CVaR 95 % 5.94 % > budget 3.06 %
- Budget de queue : **3.06 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - 🔴 support a 0.71 ATR (stop 5.938 %) — p(stop avant cible) 0.451 [0.40 ; 0.50], R/R 1.624, perte reelle 7.901 % (gap inclus), EV 0.4344 % — **REFUSE**
      - refuse : CVaR 95 % 5.94 % > budget 3.06 %
      - ⚠ support DETECTE a 0.71 ATR du spot — compartiment <1, mesure a 51.0 % de casse (IC clusterise [0.478 ; 0.541] sur 1127 touches, registre point-in-time). C'est un pile ou face : l'ancrage n'apporte rien de plus qu'une distance arbitraire et rapproche le stop du bruit. Si c'est le seul disponible, la ligne n'est pas ancrable et le levier redevient la TAILLE.
   - ⚪ atr_based a 1.5 ATR (stop 7.215 %) — p(stop avant cible) 0.3725 [0.32 ; 0.42], R/R 1.362, perte reelle 9.417 % (gap inclus), EV 0.5758 % — **REFUSE**
      - refuse : R/R 1.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 7.22 % > budget 3.06 %
   - 🟢 support a 2.88 ATR (stop 16.354 %) — p(stop avant cible) 0.0831 [0.06 ; 0.12], R/R 0.784, perte reelle 16.354 % (gap inclus), EV 1.0457 % — **REFUSE**
      - refuse : R/R 0.78 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 16.35 % > budget 3.06 %
   - 🟢 support a 4.98 ATR (stop 26.48 %) — p(stop avant cible) 0.0031 [0.00 ; 0.01], R/R 0.484, perte reelle 26.48 % (gap inclus), EV 1.3416 % — **REFUSE**
      - refuse : R/R 0.48 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 26.48 % > budget 3.06 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.157 | EV/share : $0.127 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 37 % | T2 17 % | T3 6 %
- Kelly (position) : f* 0.026 | ¼-Kelly 0.007 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈218) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 14.7 | bear 35.0 | side 50.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


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

- **RSI** : 35.1  _(momentum baissier)_
- **ADX** : 23.1  _(pas de tendance nette)_
- **MACD** : hist -0.244  _(bearish_recent)_
- **BB** : %B 0.16 · largeur 19.8%
- **ATR** : 2.69 (70.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.432  _(distribution)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 46.5  _(transition)_
- **MA** : MA20 60.04 · MA50 68.66 · MA200 52.2  _(prix < MA20)_
- **Dist MA** : MA20 -6.8% · MA50 -18.5% · MA200 +7.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (687962 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
