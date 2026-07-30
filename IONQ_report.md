# IONQ

**Generated** : 2026-07-30T22:01:56.326466+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.1 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · $35.77  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $35.77 (+0.9% vs entrée) · entrée $35.45 · stop $34.62 · T1 $36.45 · R/R 1.2  
> ↳ P(T1 av. stop) 28 % _(réel 5 s)_ · EV/risk -0.153 _(réel 5 s)_ (GBM 0.031) · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.32% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -67 % hors [0,100] (R² max 0.05). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : up | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $35.25–$35.65 (mid $35.45)
- Spot actuel : $35.77 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $34.62 (stop swing_plan-based (-5.08%))
- Targets : T1 $36.45 · R/R 1.2 | T2 $37.45 · R/R 2.41 | T3 $38.45 · R/R 3.61
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $34.62


## Edge, scénarios & sizing

- EV/risk : 0.031 | EV/share : $0.025 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 27 % | T3 27 %
- Kelly (position) : f* 0.06 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 42.6 | bear 45.4 | side 12.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.909% → cible +2.822% / stop −2.322%, p_fill 85%, n_eff≈35.5) : P(cible|rempli) **28%** · **EV/risk -0.153** (×p_fill ; si rempli -0.42% du capital)
  - **swing** (entrée dip −1.987% → cible +6.31% / stop −3.155%, p_fill 89%, n_eff≈34.7) : P(cible|rempli) **21%** · **EV/risk -0.290** (×p_fill ; si rempli -1.03% du capital)
  - **deep** (entrée dip −3.075% → cible +8.924% / stop −4.462%, p_fill 91%, n_eff≈34.8) : P(cible|rempli) **23%** · **EV/risk -0.238** (×p_fill ; si rempli -1.17% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→80% · +2.0%→65% · +3.0%→61% · +5.0%→31% · +8.0%→15%
- Range intraday médian 7.68% (p90 12.54%) · excursion haute méd. +3.72% / basse méd. −3.27%
- Profil de vol intra : ouverture 5.21% vs midi 1.572% vs clôture 1.683% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 14% · trend ↑0%/↓0% ; spike-down 73% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.107 ; momentum — autocorr 0.032)_ ; drift intra méd. -1.237% ; recovery-V 28%
- **σ réalisé intraday** 4.734% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 71% / whipsaw 21%
- POC intraday (dernière séance, temps-au-prix) : 32.6604 (VA 32.2869–33.2829 ; dernier close 32.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 41% · rebond 83% · **stop −5.16%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.4% · baisse 56% (gap-down >1% 39% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.27% (p90 −2.93%) · haut méd +1.01% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.83% (p90 −4.27%) · haut méd +1.33% · range méd 3.64%
- Excursion ouverture 30min (n=160) : bas méd −1.92% (p90 −5.29%) · haut méd +1.66% · range méd 4.51%
- Excursion ouverture 60min (n=160) : bas méd −2.52% (p90 −5.96%) · haut méd +1.91% · range méd 5.34%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 32.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 75% · séance 83% (133/159) · gap 46% · délai 0.0min · rebond 67% (91/133) (MFE +1.87%)
   - −1.0% : fill 30min 72% · séance 80% (127/159) · gap 39% · délai 0.0min · rebond 73% (93/127) (MFE +2.35%)
   - −1.5% : fill 30min 69% · séance 78% (122/159) · gap 32% · délai 0.0min · rebond 66% (83/122) (MFE +2.51%)
   - −2.0% : fill 30min 60% · séance 70% (112/159) · gap 20% · délai 0.3min · rebond 66% (76/112) (MFE +2.53%)
   - −3.0% : fill 30min 49% · séance 61% (93/159) · gap 10% · délai 7.7min · rebond 72% (67/93) (MFE +2.8%)
   - −4.0% : fill 30min 31% · séance 47% (74/159) · gap 6% · délai 16.7min · rebond 72% (55/74) (MFE +2.19%)
   - −5.0% : fill 30min 20% · séance 41% (64/159) · gap 2% · délai 31.1min · rebond 83% (55/64) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −2.89%) → stop au-delà de −2.01% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.04% (p90 −3.63%) → stop au-delà de −2.55% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.04% (p90 −2.99%) → stop au-delà de −2.36% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1122 jambes) : jambe baissière méd −1.34% (p90 −3.31%) · ~14.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (75 séances) :
      · −1.0% : fill 100% (75/75) · rebond 73% (56/75)
      · −2.0% : fill 95% (71/75) · rebond 71% (53/71)
      · −3.0% : fill 83% (61/75) · rebond 70% (45/61)
      · −4.0% : fill 63% (46/75) · rebond 69% (34/46)
      · −5.0% : fill 56% (40/75) · rebond 77% (32/40)
   - **flat** (16 séances) :
      · −1.0% : fill 71% (13/16) · rebond 87% (9/13)
      · −2.0% : fill 58% (12/16) · rebond 64% (6/12)
      · −3.0% : fill 48% (9/16) · rebond 69% (5/9)
      · −4.0% : fill 47% (8/16) · rebond 81% (4/8)
      · −5.0% : fill 27% (7/16) · rebond 91% (6/7)
   - **gap-up** (68 séances) :
      · −1.0% : fill 56% (39/68) · rebond 71% (28/39)
      · −2.0% : fill 40% (29/68) · rebond 52% (17/29)
      · −3.0% : fill 34% (23/68) · rebond 78% (17/23)
      · −4.0% : fill 27% (20/68) · rebond 79% (17/20)
      · −5.0% : fill 24% (17/68) · rebond 100% (17/17)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 51% si les 15 1res min sont vertes (79 cas) · 32% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 76% si début vert vs 17% si rouge (base 42% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **76%** · continue >prix actuel 53% ; creux résiduel méd -2.29% (q20 -3.85%) → **SL/trailing à −3.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.84% / q75 +2.8% → **scale +1.84% / runner +2.8%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **17%** (continue à baisser 56%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.29%** (au-delà de la MAE q10 -4.29%), cible rebond +2.15% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.23% .. +6.73%] · haut q95 +7.84% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.19% .. +5.41%] · haut q95 +8.36% · bas q05 -6.74%
   - 2h (n=160) : retour [-6.42% .. +7.84%] · haut q95 +8.92% · bas q05 -7.33%
   - 4h (n=160) : retour [-7.26% .. +7.13%] · haut q95 +10.14% · bas q05 -8.33%
   - 6h (n=160) : retour [-7.51% .. +7.47%] · haut q95 +10.14% · bas q05 -8.61%
   - session (n=160) : retour [-7.36% .. +8.1%] · haut q95 +10.14% · bas q05 -8.61%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 7.3)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 9% vs absente 2% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.25% (p75 1.89% / p90 2.79%) · ~4.04 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 15.0 min, n=39)
   - −1.0% → **74%** (reprise méd 20.0 min, n=24)
   - −1.5% → **59%** (reprise méd 38.13 min, n=12)
   - −2.0% → **51%** (reprise méd 31.37 min, n=8)
   - −3.0% → **25%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.79%** (p90, défaut prudent ; serré/agressif −1.89%) ; extension open→close méd +7.79% (q75 +10.75% / q95 +18.2%), MFE méd +9.27% / q90 +19.18%
   - Échelle scale-out : +9.27% (33%) / +12.82% (33%) / +19.18% (34%)
- **DÉSARMER** : repli > **−2.79%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 168.41 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +19.18% : P(retournement après) 0% (mèche méd 3.41%)
- **CONTEXTE** : la dernière heure tient les gains 95% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : bullish


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-4 sess · earnings)
- **deep** : ❄️ GELÉ jusqu'au 2026-08-05 — IONQ earnings (J-4 sess · earnings)


## Indicateurs (résumé)

- **RSI** : 35.3  _(momentum baissier)_
- **ADX** : 40.3  _(tendance tres forte)_
- **MACD** : hist 0.233  _(bullish_recent)_
- **BB** : %B 0.37 · largeur 56.7%
- **ATR** : 2.74 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.364  _(distribution)_
- **Vol ratio** : 0.95  _(volume normal)_
- **Choppiness** : 49.6  _(transition)_
- **MA** : MA20 38.53 · MA50 50.9 · MA200 46.52  _(prix < MA20)_
- **Dist MA** : MA20 -7.2% · MA50 -29.7% · MA200 -23.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88991 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
