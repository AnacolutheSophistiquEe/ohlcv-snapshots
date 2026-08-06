# 000660

**Generated** : 2026-08-06T21:48:58.836827+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite high · ₩1507000.00  

> 🟡 **WAIT-FOR-DIP** — spot +4.5 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩1507000.00 (+4.5% vs entrée) · entrée ₩1441750.00 · stop ₩1383957.14 · T1 ₩1521317.54 · R/R 1.38  
> ↳ P(T1 av. stop) 24 % _(réel 5 s)_ · EV/risk 0.039 _(réel 5 s)_ (GBM -0.108) · ¼-Kelly 0.016 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.01% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1425836.49–₩1457663.51 (mid ₩1441750.00)
- Spot actuel : ₩1507000.00 (+4.5% au-dessus de la zone — repli à attendre)
- Stop : ₩1383957.14 (stop swing_plan-based (-20.38%))
- Targets : T1 ₩1521317.54 · R/R 1.38 | T2 ₩1600885.08 · R/R 2.75 | T3 ₩1680452.62 · R/R 4.13
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1383957.14


## Edge, scénarios & sizing

- EV/risk : -0.108 | EV/share : ₩-6260.960 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 25 % | T3 25 %
- Kelly (position) : f* 0.064 | ¼-Kelly 0.016 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.3 | bear 62.1 | side 30.6  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −4.325% → cible +5.519% / stop −4.009%, p_fill 59%, n_eff≈21.0) : P(cible|rempli) **24%** · **EV/risk +0.039** (×p_fill ; si rempli +0.27% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=14, n_eff=11))
  - **deep** : indisponible (échantillon insuffisant (n=12, n_eff=10))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→78% · +2.0%→52% · +3.0%→38% · +5.0%→28% · +8.0%→14%
- Range intraday médian 6.91% (p90 11.62%) · excursion haute méd. +2.08% / basse méd. −2.94%
- Profil de vol intra : ouverture 3.235% vs midi 1.396% vs clôture 1.598% _(ouverture ~2.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (152 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 81% · range 17% · trend ↑2%/↓0% ; spike-down 73% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; mean-reverting — autocorr -0.032)_ ; drift intra méd. -1.67% ; recovery-V 24%
- **σ réalisé intraday** 5.471% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 52% / bas 76% / whipsaw 34%
- POC intraday (dernière séance, temps-au-prix) : 1681425.0 (VA 1670625.0–1694925.0 ; dernier close 1682000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 72% · **stop −8.45%** sous le fill (sous le bruit) · cible +2.8% · R/R 0.33 (high win-rate)
- Gaps overnight (n=151) : méd. 0.04% · baisse 48% (gap-down >1% 35% · >2% 29%)
- Excursion ouverture 5min (n=152) : bas méd −0.73% (p90 −2.12%) · haut méd +0.85% · range méd 1.65%
- Excursion ouverture 15min (n=152) : bas méd −0.85% (p90 −2.86%) · haut méd +1.05% · range méd 2.34%
- Excursion ouverture 30min (n=152) : bas méd −1.39% (p90 −4.15%) · haut méd +1.23% · range méd 2.93%
- Excursion ouverture 60min (n=152) : bas méd −1.75% (p90 −4.92%) · haut méd +1.49% · range méd 3.73%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1682000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 59% · séance 68% (96/151) · gap 41% · délai 0.0min · rebond 56% (51/96) (MFE +1.35%)
   - −1.0% : fill 30min 54% · séance 64% (88/151) · gap 35% · délai 0.0min · rebond 65% (55/88) (MFE +1.85%)
   - −1.5% : fill 30min 48% · séance 60% (79/151) · gap 33% · délai 0.0min · rebond 66% (50/79) (MFE +2.24%)
   - −2.0% : fill 30min 42% · séance 55% (72/151) · gap 29% · délai 0.0min · rebond 64% (47/72) (MFE +2.12%)
   - −3.0% : fill 30min 39% · séance 49% (62/151) · gap 25% · délai 0.1min · rebond 70% (44/62) (MFE +2.33%)
   - −4.0% : fill 30min 30% · séance 42% (49/151) · gap 14% · délai 3.4min · rebond 74% (37/49) (MFE +2.5%)
   - −5.0% : fill 30min 17% · séance 36% (40/151) · gap 10% · délai 30.3min · rebond 72% (30/40) (MFE +2.8%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.41% (p90 −2.75%) → stop au-delà de −1.63% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.56% (p90 −3.29%) → stop au-delà de −2.4% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −4.01%) → stop au-delà de −2.6% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=818 jambes) : jambe baissière méd −1.34% (p90 −3.56%) · ~14.0 jambes/séance
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
   - **gap-up** (74 séances) :
      · −1.0% : fill 30% (16/74) · rebond 99% (15/16)
      · −2.0% : fill 21% (11/74) · rebond 88% (10/11)
      · −3.0% : fill 16% (8/74) · rebond 74% (6/8)
      · −4.0% : fill 13% (5/74) · rebond 100% (5/5)
      · −5.0% : fill 11% (4/74) · rebond 100% (4/4)
- **P(clôture VERTE) selon le drive 15min** (n=152) : 42% en base · 50% si les 15 1res min sont vertes (79 cas) · 34% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=152) : COUDE à **1:03** → P(séance verte=clôture>ouverture) 72% si début vert vs 20% si rouge (base 42% · écart 52 pts) ; prédictivité sature ensuite (plafond brut 204min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **72%** · continue >prix actuel 47% ; creux résiduel méd -1.96% (q20 -6.18%) → **SL/trailing à −6.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.31% / q75 +3.36% → **scale +1.31% / runner +3.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=78) : edge inversé — récupère vert seulement **20%** (continue à baisser 60%) → **RÉDUIRE ~80%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −7.23%** (au-delà de la MAE q10 -7.23%), cible rebond +1.85% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=152) : retour [-3.75% .. +3.09%] · haut q95 +3.73% · bas q05 -4.75%
   - 60min (n=152) : retour [-3.62% .. +5.37%] · haut q95 +5.85% · bas q05 -5.94%
   - 2h (n=152) : retour [-4.97% .. +5.34%] · haut q95 +8.08% · bas q05 -7.26%
   - 4h (n=152) : retour [-6.7% .. +6.78%] · haut q95 +8.45% · bas q05 -8.36%
   - 6h (n=152) : retour [-7.67% .. +7.55%] · haut q95 +9.14% · bas q05 -9.41%
   - session (n=152) : retour [-7.53% .. +7.92%] · haut q95 +9.14% · bas q05 -9.41%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.9% des séances sont trend-up (mild 0% / strong 5.9%) · base = 9 séances trend-up (n_eff 7.5)
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
- **swing** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-12 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 40.5  _(momentum baissier)_
- **ADX** : 31.5  _(tendance etablie)_
- **MACD** : hist -7780.067  _(pas de croisement recent)_
- **BB** : %B 0.23 · largeur 53.2%
- **ATR** : 192642.86 (86.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.226  _(distribution)_
- **Vol ratio** : 0.66  _(volume normal)_
- **Choppiness** : 48.0  _(transition)_
- **MA** : MA20 1764100.0 · MA50 2141152.5 · MA200 1198054.53  _(prix < MA20)_
- **Dist MA** : MA20 -14.6% · MA50 -29.6% · MA200 +25.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (86658 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
