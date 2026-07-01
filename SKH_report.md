# 000660

**Generated** : 2026-07-01T21:45:35.746080+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 9/10 — **Rating** : Strong Buy  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩2560000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩2560000.00 (+3.4% vs entrée) · entrée ₩2475850.00 · stop ₩2364462.05 · T1 ₩2698625.89 · R/R 2.0  
> ↳ P(T1 av. stop) 48 % · EV/risk 0.882 · ¼-Kelly 0.046 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : up (trend-up)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Divergence volume (OBV / CMF)** — OBV rising (accumulation) mais CMF -0.010 < 0 (distribution) — flux acheteur/vendeur en désaccord ; prudence avec une lecture purement haussière.
  - _Le plus parlant — DISTRIBUTION dans la hausse : clôtures en hausse jour après jour (OBV) mais dans le BAS du range intraday (CMF<0) → on achète la force mais il y a vente en séance ; signal baissier de fond._
  - _Gaps d'ouverture : le titre ouvre en gap puis dérive — l'OBV (close-to-close) monte tandis que le CMF (position dans le range) capte la pression vendeuse intra-séance._
  - _Effet de fenêtre : l'OBV est cumulatif (mémoire longue), le CMF sur 20 séances ; un OBV « rising » hérité d'une vieille accumulation peut coexister avec un CMF récemment négatif (divergence temporelle, pas forcément distribution active)._
  - _Vraie incohérence (rare) : volume corrompu/dégradé (flux délayé, volume nul certains jours) fausserait l'un des deux — vérifier la qualité du volume si les valeurs semblent aberrantes._


## Lecture chartiste

Plan privilegie B (swing), composite 9/10, conviction 'Strong Buy'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩2431294.82–₩2520405.18 (mid ₩2475850.00)
- Spot actuel : ₩2560000.00 (+3.4% au-dessus de la zone — repli à attendre)
- Stop : ₩2364462.05 (stop swing_plan-based (-7.64%))
- Targets : T1 ₩2698625.89 · R/R 2.0 | T2 ₩2921401.79 · R/R 4.0 | T3 ₩3144177.68 · R/R 6.0
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2364462.05


## Edge, scénarios & sizing

- EV/risk : 0.882 | EV/share : ₩98277.409 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 21 % | T3 7 %
- Kelly (position) : f* 0.184 | ¼-Kelly 0.046 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 55.1 | bear 17.3 | side 27.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 640.0


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.26 · part idiosyncratique 0.74
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 61.8  _(momentum haussier)_
- **ADX** : 32.5  _(tendance etablie)_
- **MACD** : hist -22352.658  _(bearish_recent)_
- **BB** : %B 0.59 · largeur 48.7%
- **ATR** : 232214.29 (99.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV rising · CMF -0.013  _(neutre)_
- **Vol ratio** : 0.79  _(volume normal)_
- **Choppiness** : 51.4  _(transition)_
- **MA** : MA20 2447800.0 · MA50 2000540.46 · MA200 1007387.62  _(prix > MA20)_
- **Dist MA** : MA20 +4.6% · MA50 +28.0% · MA200 +154.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (20184 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
