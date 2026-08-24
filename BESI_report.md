# BESI

**Generated** : 2026-08-22T18:20:49.181616+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $212.80  

> 🟡 **WAIT-FOR-DIP** — spot +8.0 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $212.80 (+8.0% vs entrée) · entrée $197.02 · stop $187.50 · T1 $206.74 · R/R 1.02  
> ↳ P(T1 av. stop) 67 % · EV/risk 0.207 · ¼-Kelly 0.013 · _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[LOW]** meta — meta.currency absent — symbole devise déduit du ticker (fallback).


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : — | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : $195.08–$198.97 (mid $197.02)
- Spot actuel : $212.80 (+8.0% au-dessus de la zone — repli à attendre)
- Stop : $187.50 (stop swing_plan-based (-11.89%))
- Targets : T1 $206.74 · R/R 1.02 | T2 $216.45 · R/R 2.04 | T3 $226.16 · R/R 3.06
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $187.50


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.52 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (11.89 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1280).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 11.89 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.524 % | p01 -4.997 % | pire -10.843 % _(sur 1280 séances)_
- **P(stop avant cible)** _(source : daily, 1281 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.1004** [0.0623 ; 0.1518] _(largeur 9.0 pt, n_eff 173.1)_
   - swing : **0.3874** [0.3372 ; 0.4395] _(largeur 10.2 pt, n_eff 345.8)_
   - deep : **0.4794** [0.4271 ; 0.532] _(largeur 10.5 pt, n_eff 345.8)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.85 %** | CVaR **-7.58 %** | vol 3.23 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 2.27 % contre 3.83 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.9 % vs -10.28 % si l'on extrapolait par √5 _(rapport 1.061 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0357** (β de hausse 0.5674, asymétrie 1.8253) vs SPY — 570 séances de repli, historique complet


## Echelle Warden — OU poser le stop

- **Verdict : AUCUN couple (stop, cible) ne tient les contraintes. Ce n'est pas un defaut du calcul : la structure est trop loin sous le spot pour qu'un stop structurel soit rentable a ces cibles. Le levier de fond n'est PAS la distance du stop mais la TAILLE de la ligne — voir `min_target_for_rr` pour savoir a partir de quelle cible chaque stop redeviendrait defendable. **MAIS ON POSE QUAND MEME** : `best_effort` porte le moins mauvais couple, non conforme et marque comme tel. Laisser la ligne NUE est pire — la perte y est non bornee.**
- **Couple retenu** : stop 198.5179 sur atr_based (1.5 ATR, 6.712 %) — p(stop avant cible) 0.4515 [0.40 ; 0.50], R/R 2.206, perte reelle 8.783 % (gap inclus), CVaR 6.723 %, EV 0.615 % — **NON CONFORME (best_effort — proposition de derniere main)**
   - severite des violations : 1.0687 (somme des depassements RELATIFS a chaque seuil ; c'est elle qui a departage, l'esperance ne tranchant qu'a severites egales)
   - viole : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
   - viole : CVaR 95 % 6.72 % > budget 3.25 %
- Budget de queue : **3.25 %** du notionnel (temoin fige : 12.0 %) — DERIVE de la contrainte JOINTE d'appel de marge par allocation d'Euler : c'est la part de CETTE ligne dans la queue du portefeuille, pas un pourcentage choisi.
   - prix du risque 0.212 : chaque ligne protegeable doit ramener sa perte de queue a ce multiple de ce qu'elle coute aujourd'hui — le noyau permanent preleve 42.8 % de la queue AVANT le partage, ce qui durcit le budget de toutes les autres.
- Candidats (la structure propose, la statistique elimine) :
   - ⚪ atr_based a 1.5 ATR (stop 6.712 %) — p(stop avant cible) 0.4515 [0.40 ; 0.50], R/R 2.206, perte reelle 8.783 % (gap inclus), EV 0.615 % — **REFUSE**
      - refuse : cible atteinte seulement 8.5 % du temps (< 15 %) meme a 10 seances : le R/R de 2.21 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : CVaR 95 % 6.72 % > budget 3.25 %
   - ⚪ swing_based a 2.87 ATR (stop 15.204 %) — p(stop avant cible) 0.1531 [0.12 ; 0.19], R/R 1.275, perte reelle 15.204 % (gap inclus), EV 1.372 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 1.27 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 1.27 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 15.20 % > budget 3.25 %
   - 🟢 support a 4.83 ATR (stop 23.966 %) — p(stop avant cible) 0.0198 [0.01 ; 0.04], R/R 0.809, perte reelle 23.966 % (gap inclus), EV 1.6491 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.81 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.81 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 23.97 % > budget 3.25 %
   - 🟢 support a 9.81 ATR (stop 46.241 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.419, perte reelle 46.241 % (gap inclus), EV 1.8393 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.42 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.42 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 46.24 % > budget 3.25 %
   - 🟢 support a 11.35 ATR (stop 53.129 %) — p(stop avant cible) 0.0 [0.00 ; 0.01], R/R 0.365, perte reelle 53.129 % (gap inclus), EV 1.8393 % — **REFUSE**
      - refuse : cible atteinte seulement 8.6 % du temps (< 15 %) meme a 10 seances : le R/R de 0.36 est un rapport de distances, pas une esperance — viser si loin revient a n'avoir pas de cible
      - refuse : R/R 0.36 < plancher 1.60 (mesure vs SPOT, gap inclus)
      - refuse : CVaR 95 % 53.13 % > budget 3.25 %
- ⚠ **Un ancrage marque `faible` est un support DETECTE a moins de 1 ATR du spot : mesure a 51 % de casse (pile ou face, IC clusterise [0,474 ; 0,545]) contre ~35 % au-dela. Il est GARDE comme candidat, jamais refuse en silence — mais si c est le seul disponible, la ligne n est pas ancrable et le levier redevient la TAILLE.**
- ⚠ `anchor_quality: non mesure` ne veut PAS dire mauvais : la mesure porte sur les supports DETECTES, pas sur un multiple d ATR ni sur un bas de canal.


## Edge, scénarios & sizing

- EV/risk : 0.144 | EV/share : $1.371 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 21 % | T3 6 %
- Kelly (position) : f* 0.052 | ¼-Kelly 0.013 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈217) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 85.3 | bear 9.1 | side 5.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 213.0 (= 1 part(s) × prix) · cible 288.0


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

- **RSI** : 57.5  _(momentum haussier)_
- **ADX** : 16.7  _(pas de tendance nette)_
- **MACD** : hist 1.078  _(pas de croisement recent)_
- **BB** : %B 0.46 · largeur 25.7%
- **ATR** : 9.52 (53.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.114  _(distribution)_
- **Vol ratio** : 0.53  _(volume atone)_
- **Choppiness** : 51.1  _(transition)_
- **MA** : MA20 215.13 · MA50 246.83 · MA200 203.63  _(prix < MA20)_
- **Dist MA** : MA20 -1.1% · MA50 -13.8% · MA200 +4.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (694399 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
