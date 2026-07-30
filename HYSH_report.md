# 298040

**Generated** : 2026-07-30T21:52:12.418279+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 6.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · ₩1894000.00  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot ₩1894000.00 (+4.5% vs entrée) · entrée ₩1813155.88 · stop ₩1609733.82 · T1 ₩2220000.00 · R/R 2.0  
> ↳ P(T1 av. stop) 7 % _(réel 5 s)_ · EV/risk -0.106 _(réel 5 s)_ (GBM 0.092) · ¼-Kelly 0.0 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -134 % hors [0,100] (R² max 0.98). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie B (swing), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1784696.75–₩1841615.01 (mid ₩1813155.88)
- Spot actuel : ₩1894000.00 (+4.5% au-dessus de la zone — repli à attendre)
- Stop : ₩1609733.82 (stop swing_plan-based (-15.01%))
- Targets : T1 ₩2220000.00 · R/R 2.0 | T2 ₩2229374.60 · R/R 2.05 | T3 ₩2238749.20 · R/R 2.09
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1609733.82


## Edge, scénarios & sizing

- EV/risk : 0.092 | EV/share : ₩18801.596 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 5 % | T2 5 % | T3 5 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 21.5 | bear 64.5 | side 14.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.935% → cible +3.499% / stop −8.0%, p_fill 84%, n_eff≈34.1) : P(cible|rempli) **33%** · **EV/risk -0.130** (×p_fill ; si rempli -1.24% du capital)
  - **swing** (entrée dip −4.27% → cible +22.438% / stop −11.219%, p_fill 57%, n_eff≈24.9) : P(cible|rempli) **7%** · **EV/risk -0.106** (×p_fill ; si rempli -2.08% du capital)
  - **deep** (entrée dip −6.592% → cible +11.065% / stop −5.533%, p_fill 72%, n_eff≈26.8) : P(cible|rempli) **18%** · **EV/risk -0.368** (×p_fill ; si rempli -2.82% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→79% · +1.0%→61% · +2.0%→51% · +3.0%→38% · +5.0%→21% · +8.0%→6%
- Range intraday médian 6.97% (p90 10.06%) · excursion haute méd. +2.1% / basse méd. −3.94%
- Profil de vol intra : ouverture 4.293% vs midi 1.102% vs clôture 1.176% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (143 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 75% · range 24% · trend ↑0%/↓1% ; spike-down 78% · recovery-V 26%)_
- **Régime intraday** : **chop** _(efficiency 0.144 ; mean-reverting — autocorr -0.09)_ ; drift intra méd. -2.432% ; recovery-V 26%
- **σ réalisé intraday** 5.247% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 69% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 1966625.0 (VA 1885775.0–2082125.0 ; dernier close 1988000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 36% · rebond 83% · **stop −5.72%** sous le fill (sous le bruit) · cible +2.29% · R/R 0.4 (high win-rate)
- Gaps overnight (n=142) : méd. 0.51% · baisse 38% (gap-down >1% 24% · >2% 17%)
- Excursion ouverture 5min (n=143) : bas méd −1.29% (p90 −3.43%) · haut méd +0.81% · range méd 2.72%
- Excursion ouverture 15min (n=143) : bas méd −2.09% (p90 −4.43%) · haut méd +0.97% · range méd 3.74%
- Excursion ouverture 30min (n=143) : bas méd −2.51% (p90 −5.07%) · haut méd +1.09% · range méd 4.23%
- Excursion ouverture 60min (n=143) : bas méd −2.82% (p90 −5.32%) · haut méd +1.22% · range méd 4.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1988000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 72% (98/142) · gap 32% · délai 0.0min · rebond 59% (60/98) (MFE +1.27%)
   - −1.0% : fill 30min 58% · séance 69% (90/142) · gap 24% · délai 0.9min · rebond 58% (55/90) (MFE +1.54%)
   - −1.5% : fill 30min 51% · séance 62% (81/142) · gap 21% · délai 1.5min · rebond 50% (48/81) (MFE +1.06%)
   - −2.0% : fill 30min 46% · séance 59% (72/142) · gap 17% · délai 3.4min · rebond 52% (39/72) (MFE +1.27%)
   - −3.0% : fill 30min 35% · séance 50% (59/142) · gap 8% · délai 7.9min · rebond 51% (32/59) (MFE +1.0%)
   - −4.0% : fill 30min 24% · séance 46% (51/142) · gap 6% · délai 25.2min · rebond 68% (37/51) (MFE +1.77%)
   - −5.0% : fill 30min 21% · séance 36% (38/142) · gap 5% · délai 26.8min · rebond 83% (31/38) (MFE +2.29%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.68% (p90 −3.19%) → stop au-delà de −2.13% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.72% (p90 −4.17%) → stop au-delà de −2.47% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.76% (p90 −4.2%) → stop au-delà de −2.14% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=769 jambes) : jambe baissière méd −1.42% (p90 −3.57%) · ~13.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (49 séances) :
      · −1.0% : fill 100% (49/49) · rebond 56% (30/49)
      · −2.0% : fill 88% (41/49) · rebond 51% (22/41)
      · −3.0% : fill 84% (39/49) · rebond 51% (21/39)
      · −4.0% : fill 80% (34/49) · rebond 74% (25/34)
      · −5.0% : fill 68% (28/49) · rebond 83% (22/28)
   - **flat** (16 séances) :
      · −1.0% : fill 85% (11/16) · rebond 66% (8/11)
      · −2.0% : fill 76% (8/16) · rebond 57% (5/8)
      · −3.0% : fill 52% (5/16) · rebond 68% (4/5)
      · −4.0% : fill 52% (5/16) · rebond 43% (3/5)
      · −5.0% : fill 43% (3/16) · rebond 61% (2/3)
   - **gap-up** (77 séances) :
      · −1.0% : fill 46% (30/77) · rebond 58% (17/30)
      · −2.0% : fill 36% (23/77) · rebond 53% (12/23)
      · −3.0% : fill 27% (15/77) · rebond 45% (7/15)
      · −4.0% : fill 22% (12/77) · rebond 64% (9/12)
      · −5.0% : fill 14% (7/77) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=143) : 37% en base · 61% si les 15 1res min sont vertes (57 cas) · 25% si rouges (86 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=143) : COUDE à **1:21** → P(séance verte=clôture>ouverture) 78% si début vert vs 12% si rouge (base 37% · écart 66 pts) ; prédictivité sature ensuite (plafond brut 226min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -1.65% (q20 -3.5%) → **SL/trailing à −3.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.7% / q75 +3.18% → **scale +1.7% / runner +3.18%**, sortie à la clôture
  - **si ROUGE au coude** (n=80) : edge inversé — récupère vert seulement **12%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.31%** (au-delà de la MAE q10 -6.31%), cible rebond +1.35% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=143) : retour [-4.78% .. +4.22%] · haut q95 +6.03% · bas q05 -5.33%
   - 60min (n=143) : retour [-5.25% .. +4.75%] · haut q95 +6.2% · bas q05 -6.28%
   - 2h (n=143) : retour [-7.59% .. +4.29%] · haut q95 +6.62% · bas q05 -8.89%
   - 4h (n=143) : retour [-8.01% .. +5.27%] · haut q95 +7.04% · bas q05 -10.28%
   - 6h (n=143) : retour [-8.14% .. +5.24%] · haut q95 +7.92% · bas q05 -10.28%
   - session (n=143) : retour [-7.06% .. +5.51%] · haut q95 +7.92% · bas q05 -10.28%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **72%**. Lecture précoce 30 min : signature présente → 24% vs absente 0% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.53% / p90 2.47%) · ~4.0 replis/séance, durée méd 54.79 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 26.87 min, n=28)
   - −1.0% → **83%** (reprise méd 56.82 min, n=12)
   - −1.5% → **67%** (reprise méd 61.26 min, n=6)
   - −2.0% → **67%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.47%** (p90, défaut prudent ; serré/agressif −1.53%) ; extension open→close méd +5.76% (q75 +7.39% / q95 +8.29%), MFE méd +6.29% / q90 +9.17%
   - Échelle scale-out : +6.29% (33%) / +8.55% (33%) / +9.17% (34%)
- **DÉSARMER** : repli > **−2.47%** depuis le plus-haut = décay → P(retournement) **25%** (préavis méd 180.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.17% : P(retournement après) 0% (mèche méd 0.97%)
- **CONTEXTE** : la dernière heure tient les gains 57% du temps (retour médian dernière heure +0.24%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : extreme
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

- **RSI** : 30.5  _(momentum baissier)_
- **ADX** : 17.9  _(pas de tendance nette)_
- **MACD** : hist -63415.29  _(pas de croisement recent)_
- **BB** : %B -0.06 · largeur 54.2%
- **ATR** : 261357.14 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.247  _(distribution)_
- **Vol ratio** : 2.07  _(volume au-dessus de la moyenne)_
- **Choppiness** : 43.7  _(transition)_
- **MA** : MA20 2717450.0 · MA50 3237900.0 · MA200 2638811.73  _(prix < MA20)_
- **Dist MA** : MA20 -30.3% · MA50 -41.5% · MA200 -28.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (87782 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
