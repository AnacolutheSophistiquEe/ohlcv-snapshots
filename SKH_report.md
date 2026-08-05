# 000660

**Generated** : 2026-08-05T00:13:09.282684+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 4/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1577000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)  
> ↳ spot ₩1577000.00 (+21.0% vs entrée) · entrée ₩1303275.75 · stop ₩1146882.66 · T1 ₩1460373.28 · R/R 1.0  
> ↳ P(T1 av. stop) 38 % · EV/risk 0.229 · ¼-Kelly 0.016 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1271856.24–₩1334695.25 (mid ₩1303275.75)
- Spot actuel : ₩1577000.00 (+21.0% au-dessus de la zone — repli à attendre)
- Stop : ₩1146882.66 (stop swing_plan-based (-27.27%))
- Targets : T1 ₩1460373.28 · R/R 1.0 | T2 ₩1617470.80 · R/R 2.01 | T3 ₩1774568.33 · R/R 3.01
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1146882.66


## Edge, scénarios & sizing

- EV/risk : 0.229 | EV/share : ₩35783.516 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 38 % | T2 8 % | T3 1 %
- Kelly (position) : f* 0.066 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 11.0 | bear 62.8 | side 26.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=7, n_eff=5))
  - **swing** : indisponible (échantillon insuffisant (n=4, n_eff=4))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→92% · +1.0%→79% · +2.0%→54% · +3.0%→39% · +5.0%→28% · +8.0%→14%
- Range intraday médian 6.8% (p90 11.62%) · excursion haute méd. +2.16% / basse méd. −2.93%
- Profil de vol intra : ouverture 3.206% vs midi 1.368% vs clôture 1.59% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (150 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 80% · range 18% · trend ↑2%/↓0% ; spike-down 72% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.127 ; neutre — autocorr -0.028)_ ; drift intra méd. -1.666% ; recovery-V 27%
- **σ réalisé intraday** 5.526% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 74% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 1591275.0 (VA 1579575.0–1599075.0 ; dernier close 1568000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 35% · rebond 70% · **stop −8.49%** sous le fill (sous le bruit) · cible +2.72% · R/R 0.32 (high win-rate)
- Gaps overnight (n=149) : méd. -0.02% · baisse 50% (gap-down >1% 36% · >2% 30%)
- Excursion ouverture 5min (n=150) : bas méd −0.7% (p90 −2.17%) · haut méd +0.9% · range méd 1.7%
- Excursion ouverture 15min (n=150) : bas méd −0.83% (p90 −2.96%) · haut méd +1.13% · range méd 2.34%
- Excursion ouverture 30min (n=150) : bas méd −1.34% (p90 −3.77%) · haut méd +1.27% · range méd 2.93%
- Excursion ouverture 60min (n=150) : bas méd −1.63% (p90 −4.86%) · haut méd +1.56% · range méd 3.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1568000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 69% (95/149) · gap 42% · délai 0.0min · rebond 55% (50/95) (MFE +1.28%)
   - −1.0% : fill 30min 54% · séance 65% (87/149) · gap 36% · délai 0.0min · rebond 64% (54/87) (MFE +1.78%)
   - −1.5% : fill 30min 50% · séance 60% (78/149) · gap 34% · délai 0.0min · rebond 65% (49/78) (MFE +2.16%)
   - −2.0% : fill 30min 43% · séance 55% (71/149) · gap 30% · délai 0.0min · rebond 63% (46/71) (MFE +2.04%)
   - −3.0% : fill 30min 41% · séance 49% (61/149) · gap 26% · délai 0.0min · rebond 68% (43/61) (MFE +2.25%)
   - −4.0% : fill 30min 31% · séance 42% (48/149) · gap 15% · délai 2.5min · rebond 73% (36/48) (MFE +2.45%)
   - −5.0% : fill 30min 18% · séance 35% (39/149) · gap 11% · délai 26.4min · rebond 70% (29/39) (MFE +2.72%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.75%) → stop au-delà de −1.63% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −3.29%) → stop au-delà de −2.4% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −4.01%) → stop au-delà de −2.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=802 jambes) : jambe baissière méd −1.34% (p90 −3.58%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 98% (63/65) · rebond 51% (33/63)
      · −2.0% : fill 89% (54/65) · rebond 55% (31/54)
      · −3.0% : fill 85% (49/65) · rebond 67% (33/49)
      · −4.0% : fill 77% (42/65) · rebond 68% (30/42)
      · −5.0% : fill 66% (35/65) · rebond 66% (25/35)
   - **flat** (12 séances) :
      · −1.0% : fill 91% (9/12) · rebond 86% (7/9)
      · −2.0% : fill 77% (7/12) · rebond 86% (6/7)
      · −3.0% : fill 45% (5/12) · rebond 100% (5/5)
      · −4.0% : fill 24% (2/12) · rebond 100% (2/2)
      · −5.0% : fill 11% (1/12) · rebond 100% (1/1)
   - **gap-up** (72 séances) :
      · −1.0% : fill 28% (15/72) · rebond 99% (14/15)
      · −2.0% : fill 19% (10/72) · rebond 85% (9/10)
      · −3.0% : fill 14% (7/72) · rebond 66% (5/7)
      · −4.0% : fill 10% (4/72) · rebond 100% (4/4)
      · −5.0% : fill 7% (3/72) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=150) : 44% en base · 50% si les 15 1res min sont vertes (79 cas) · 36% si rouges (71 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=150) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 72% si début vert vs 21% si rouge (base 44% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 204min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **72%** · continue >prix actuel 47% ; creux résiduel méd -1.96% (q20 -6.18%) → **SL/trailing à −6.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +3.36% → **scale +1.31% / runner +3.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=76) : edge inversé — récupère vert seulement **21%** (continue à baisser 64%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.24%** (au-delà de la MAE q10 -7.24%), cible rebond +1.82% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=150) : retour [-3.34% .. +3.13%] · haut q95 +3.77% · bas q05 -4.8%
   - 60min (n=150) : retour [-3.38% .. +5.43%] · haut q95 +5.87% · bas q05 -5.5%
   - 2h (n=150) : retour [-4.99% .. +5.38%] · haut q95 +8.15% · bas q05 -6.91%
   - 4h (n=150) : retour [-6.71% .. +6.84%] · haut q95 +8.47% · bas q05 -8.2%
   - 6h (n=150) : retour [-7.88% .. +7.6%] · haut q95 +9.3% · bas q05 -9.66%
   - session (n=150) : retour [-7.65% .. +7.96%] · haut q95 +9.3% · bas q05 -9.66%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.0% des séances sont trend-up (mild 0% / strong 6.0%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 19% vs absente 1% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 41.3  _(momentum baissier)_
- **ADX** : 31.8  _(tendance etablie)_
- **MACD** : hist -23472.493  _(pas de croisement recent)_
- **BB** : %B 0.26 · largeur 55.2%
- **ATR** : 208428.57 (88.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.242  _(distribution)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 43.5  _(transition)_
- **MA** : MA20 1819200.0 · MA50 2157499.15 · MA200 1186300.78  _(prix < MA20)_
- **Dist MA** : MA20 -13.3% · MA50 -26.9% · MA200 +32.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86059 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
