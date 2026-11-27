# 000660

**Generated** : 2026-11-27T21:51:51.205955+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 6/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1103000.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (25 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩1103000.00 (+1.0% vs entrée) · entrée ₩1092214.67 · stop ₩1065544.52 · T1 ₩1139868.74 · R/R 1.79  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.44% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-27 : 1103000.0 · ATR Wilder 96393.49 (8.74 %)_
- **Swing** : plage **991263.06 → 910055.25** (-10.13 % a -17.49 % sous la cloture, 0.84 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 866876.93-970823.65 (B). stop INDICATIF 813661.76 (-10.59 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **910055.25 → 726023.2** (-17.49 % a -34.18 % sous la cloture, 1.91 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 866876.93-970823.65 (B) ; 757609.55-792349.05 (A). stop INDICATIF 660471.72 (-9.03 % sous le bas ; sous le support 708668.47-717477.87 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.8 ATR sous le plus haut 20 s., RSI(2) 71.9 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 1021816.42-1068316.22 (A, -3.14 %) ; 866876.93-970823.65 (B, -11.98 %) ; 757609.55-792349.05 (A, -28.16 %) ; 708668.47-717477.87 (B, -34.95 %) ; 580442.51-611764.89 (B, -44.54 %) ; 490039.76-520361.64 (A, -52.82 %)
- Resistances reelles au-dessus : 1148758.79-1188979.98 (A, 4.15 %) ; 1222069.2-1222069.2 (C, 10.8 %) ; 1291985.66-1303757.86 (B, 17.13 %) ; 1346630.09-1346630.09 (B, 22.09 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.30 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (10.21 %)** : le gap seul le franchit 0.246 % des séances (3 fois sur 1219).
   - exécution **0.65 pt plus bas** dans le cas TYPIQUE (médiane), 3.038 au p90, **3.635 au pire**
   - perte réelle **11.681 %** en moyenne _(tirée par la queue)_, jusqu'à **13.845 %** — au lieu des 10.21 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0036 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 3 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.723 % | p01 -7.63 % | pire -13.845 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.455** [0.3821 ; 0.5294] _(largeur 14.7 pt, n_eff 173.1)_
   - swing : **0.3496** [0.3007 ; 0.401] _(largeur 10.0 pt, n_eff 345.6)_
   - deep : **0.319** [0.2715 ; 0.3695] _(largeur 9.8 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-9.69 %** | CVaR **-11.75 %** | vol 5.91 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 4.18 % contre 6.75 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.02 % vs -11.45 % si l'on extrapolait par √5 _(rapport 0.875 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4355** (β de hausse 1.6093, asymétrie 0.892) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.121 | EV/share : ₩-3231.031 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 19 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 52.3 | bear 42.7 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.982% → cible +4.363% / stop −2.442%, p_fill 72%, n_eff≈78.2) : P(cible|rempli) **16%** · **EV/risk -0.322** (×p_fill ; si rempli -1.09% du capital)
  - **swing** (entrée dip −2.15% → cible +12.407% / stop −8.237%, p_fill 68%, n_eff≈78.2) : P(cible|rempli) **23%** · **EV/risk -0.145** (×p_fill ; si rempli -1.76% du capital)
  - **deep** (entrée dip −3.32% → cible +13.771% / stop −12.506%, p_fill 68%, n_eff≈74.9) : P(cible|rempli) **34%** · **EV/risk -0.132** (×p_fill ; si rempli -2.44% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→78% · +2.0%→55% · +3.0%→38% · +5.0%→23% · +8.0%→8%
- Range intraday médian 6.05% (p90 10.45%) · excursion haute méd. +2.31% / basse méd. −2.61%
- Profil de vol intra : ouverture 3.003% vs midi 1.225% vs clôture 1.446% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 62% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; neutre — autocorr -0.023)_ ; drift intra méd. -0.404% ; recovery-V 17%
- **σ réalisé intraday** 3.303% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 65% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 1222800.0 (VA 1186400.0–1253600.0 ; dernier close 1281000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 57% · **stop −6.13%** sous le fill (sous le bruit) · cible +1.66% · R/R 0.27 (high win-rate)
- Gaps overnight (n=152) : méd. 1.13% · baisse 34% (gap-down >1% 28% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −0.48% (p90 −1.95%) · haut méd +0.82% · range méd 1.36%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.42%) · haut méd +1.01% · range méd 2.04%
- Excursion ouverture 30min (n=160) : bas méd −0.97% (p90 −3.27%) · haut méd +1.34% · range méd 2.54%
- Excursion ouverture 60min (n=160) : bas méd −1.28% (p90 −3.8%) · haut méd +1.49% · range méd 3.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1281000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 42% · séance 55% (79/152) · gap 29% · délai 0.0min · rebond 54% (46/79) (MFE +1.12%)
   - −1.0% : fill 30min 40% · séance 52% (76/152) · gap 28% · délai 0.0min · rebond 64% (50/76) (MFE +1.36%)
   - −1.5% : fill 30min 36% · séance 50% (71/152) · gap 25% · délai 0.9min · rebond 61% (45/71) (MFE +1.52%)
   - −2.0% : fill 30min 34% · séance 47% (67/152) · gap 19% · délai 0.9min · rebond 62% (44/67) (MFE +1.91%)
   - −3.0% : fill 30min 23% · séance 32% (51/152) · gap 11% · délai 3.0min · rebond 52% (30/51) (MFE +1.44%)
   - −4.0% : fill 30min 12% · séance 26% (39/152) · gap 7% · délai 39.7min · rebond 49% (23/39) (MFE +0.94%)
   - −5.0% : fill 30min 9% · séance 25% (37/152) · gap 6% · délai 62.9min · rebond 57% (23/37) (MFE +1.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −2.29%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.35% (p90 −2.6%) → stop au-delà de −2.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −2.56%) → stop au-delà de −2.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=848 jambes) : jambe baissière méd −1.25% (p90 −3.37%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 100% (49/49) · rebond 60% (29/49)
      · −2.0% : fill 96% (46/49) · rebond 60% (29/46)
      · −3.0% : fill 69% (38/49) · rebond 46% (21/38)
      · −4.0% : fill 56% (30/49) · rebond 44% (17/30)
      · −5.0% : fill 54% (28/49) · rebond 44% (16/28)
   - **gap-up** (97 séances) :
      · −1.0% : fill 24% (22/97) · rebond 74% (17/22)
      · −2.0% : fill 18% (16/97) · rebond 67% (11/16)
      · −3.0% : fill 12% (11/97) · rebond 80% (8/11)
      · −4.0% : fill 9% (8/97) · rebond 84% (6/8)
      · −5.0% : fill 9% (8/97) · rebond 84% (6/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 56% si les 15 1res min sont vertes (87 cas) · 21% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 65% si début vert vs 9% si rouge (base 40% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 223min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=88) : tient le vert **65%** · continue >prix actuel 49% ; creux résiduel méd -1.45% (q20 -3.7%) → **SL/trailing à −3.7%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +2.94% → **scale +1.46% / runner +2.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=72) : edge inversé — récupère vert seulement **9%** (continue à baisser 68%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.01%** (au-delà de la MAE q10 -5.01%), cible rebond +1.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.0% .. +2.65%] · haut q95 +3.82% · bas q05 -4.01%
   - 60min (n=160) : retour [-3.6% .. +3.81%] · haut q95 +4.68% · bas q05 -5.02%
   - 2h (n=160) : retour [-4.69% .. +4.46%] · haut q95 +5.68% · bas q05 -6.5%
   - 4h (n=160) : retour [-5.25% .. +4.7%] · haut q95 +6.4% · bas q05 -7.14%
   - 6h (n=160) : retour [-6.42% .. +5.56%] · haut q95 +7.17% · bas q05 -7.45%
   - session (n=160) : retour [-6.55% .. +6.05%] · haut q95 +7.17% · bas q05 -7.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — 000660 = **volatil sans tendance propre (choppy)** (vol intra méd 3.34%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.22 · part idiosyncratique 0.78
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 49.3  _(neutre)_
- **ADX** : 24.2  _(pas de tendance nette)_
- **MACD** : hist 2790.281  _(bullish_recent)_
- **BB** : %B 0.36 · largeur 40.1%
- **ATR** : 88900.5 (51.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.237  _(distribution)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 55.9  _(transition)_
- **MA** : MA20 1170603.57 · MA50 1392800.93 · MA200 1505470.2  _(prix < MA20)_
- **Dist MA** : MA20 -5.8% · MA50 -20.8% · MA200 -26.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (390888 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
