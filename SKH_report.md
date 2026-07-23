# 000660

**Generated** : 2026-07-23T00:11:43.939492+00:00  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite extreme · ₩1830000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot ₩1830000.00 (+2.0% vs entrée) · entrée ₩1794253.35 · stop ₩1720453.35 · T1 ₩1855000.00 · R/R 0.82  
> ↳ P(T1 av. stop) 39 % _(réel 5 s)_ · EV/risk -0.072 _(réel 5 s)_ (GBM -0.004) · ¼-Kelly 0.025 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −4.11% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -23 % hors [0,100] (R² max 0.96). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1782104.03–₩1806402.68 (mid ₩1794253.35)
- Spot actuel : ₩1830000.00 (+2.0% au-dessus de la zone — repli à attendre)
- Stop : ₩1720453.35 (stop swing_plan-based (-11.63%))
- Targets : T1 ₩1855000.00 · R/R 0.82 | T2 ₩2019833.22 · R/R 3.06 | T3 ₩2026030.80 · R/R 3.14
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩1720453.35


## Edge, scénarios & sizing

- EV/risk : -0.004 | EV/share : ₩-297.712 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 35 % | T2 25 % | T3 25 %
- Kelly (position) : f* 0.099 | ¼-Kelly 0.025 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.5 | bear 62.2 | side 29.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −1.957% → cible +3.386% / stop −4.113%, p_fill 73%, n_eff≈27.5) : P(cible|rempli) **39%** · **EV/risk -0.072** (×p_fill ; si rempli -0.40% du capital)
  - **swing** (entrée dip −4.294% → cible +15.33% / stop −7.665%, p_fill 65%, n_eff≈21.9) : P(cible|rempli) **20%** · **EV/risk -0.233** (×p_fill ; si rempli -2.73% du capital)
  - **deep** (entrée dip −6.644% → cible +13.617% / stop −6.808%, p_fill 57%, n_eff≈17.5) : P(cible|rempli) **16%** · **EV/risk -0.326** (×p_fill ; si rempli -3.89% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→95% · +1.0%→81% · +2.0%→57% · +3.0%→39% · +5.0%→26% · +8.0%→14%
- Range intraday médian 6.19% (p90 11.16%) · excursion haute méd. +2.33% / basse méd. −2.5%
- Profil de vol intra : ouverture 3.02% vs midi 1.22% vs clôture 1.497% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (141 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 15% · trend ↑2%/↓0% ; spike-down 66% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr -0.024)_ ; drift intra méd. -0.38% ; recovery-V 30%
- **σ réalisé intraday** 5.104% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 56% / bas 66% / whipsaw 32%
- POC intraday (dernière séance, temps-au-prix) : 1844437.5 (VA 1809562.5–1871562.5 ; dernier close 1847000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 48% · rebond 79% · **stop −8.68%** sous le fill (sous le bruit) · cible +2.69% · R/R 0.31 (high win-rate)
- Gaps overnight (n=140) : méd. -0.04% · baisse 50% (gap-down >1% 37% · >2% 30%)
- Excursion ouverture 5min (n=141) : bas méd −0.58% (p90 −1.75%) · haut méd +0.94% · range méd 1.52%
- Excursion ouverture 15min (n=141) : bas méd −0.79% (p90 −2.41%) · haut méd +1.17% · range méd 2.1%
- Excursion ouverture 30min (n=141) : bas méd −1.3% (p90 −3.03%) · haut méd +1.34% · range méd 2.76%
- Excursion ouverture 60min (n=141) : bas méd −1.34% (p90 −3.78%) · haut méd +1.7% · range méd 3.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1847000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 60% · séance 67% (88/140) · gap 42% · délai 0.0min · rebond 58% (47/88) (MFE +1.7%)
   - −1.0% : fill 30min 56% · séance 64% (81/140) · gap 37% · délai 0.0min · rebond 66% (51/81) (MFE +2.11%)
   - −1.5% : fill 30min 51% · séance 59% (72/140) · gap 34% · délai 0.0min · rebond 68% (46/72) (MFE +2.18%)
   - −2.0% : fill 30min 43% · séance 53% (65/140) · gap 30% · délai 0.0min · rebond 66% (43/65) (MFE +2.04%)
   - −3.0% : fill 30min 40% · séance 48% (56/140) · gap 24% · délai 0.0min · rebond 79% (42/56) (MFE +2.69%)
   - −4.0% : fill 30min 29% · séance 39% (43/140) · gap 14% · délai 3.5min · rebond 77% (33/43) (MFE +2.78%)
   - −5.0% : fill 30min 15% · séance 31% (34/140) · gap 11% · délai 30.4min · rebond 74% (26/34) (MFE +2.65%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.37% (p90 −2.53%) → stop au-delà de −1.63% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.6% (p90 −3.41%) → stop au-delà de −2.45% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −3.64%) → stop au-delà de −2.46% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=720 jambes) : jambe baissière méd −1.31% (p90 −3.32%) · ~13.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (61 séances) :
      · −1.0% : fill 97% (59/61) · rebond 55% (32/59)
      · −2.0% : fill 87% (50/61) · rebond 62% (30/50)
      · −3.0% : fill 82% (45/61) · rebond 76% (32/45)
      · −4.0% : fill 72% (38/61) · rebond 73% (28/38)
      · −5.0% : fill 60% (31/61) · rebond 71% (23/31)
   - **flat** (12 séances) :
      · −1.0% : fill 91% (9/12) · rebond 86% (7/9)
      · −2.0% : fill 77% (7/12) · rebond 86% (6/7)
      · −3.0% : fill 45% (5/12) · rebond 100% (5/5)
      · −4.0% : fill 24% (2/12) · rebond 100% (2/2)
      · −5.0% : fill 11% (1/12) · rebond 100% (1/1)
   - **gap-up** (67 séances) :
      · −1.0% : fill 26% (13/67) · rebond 98% (12/13)
      · −2.0% : fill 14% (8/67) · rebond 75% (7/8)
      · −3.0% : fill 12% (6/67) · rebond 91% (5/6)
      · −4.0% : fill 8% (3/67) · rebond 100% (3/3)
      · −5.0% : fill 4% (2/67) · rebond 100% (2/2)
- **P(clôture VERTE) selon le drive 15min** (n=141) : 47% en base · 55% si les 15 1res min sont vertes (76 cas) · 37% si rouges (65 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=141) : COUDE à **1:36** → P(séance verte=clôture>ouverture) 75% si début vert vs 17% si rouge (base 47% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 211min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **75%** · continue >prix actuel 50% ; creux résiduel méd -1.7% (q20 -5.5%) → **SL/trailing à −5.5%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.48% / q75 +3.3% → **scale +1.48% / runner +3.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=64) : edge inversé — récupère vert seulement **17%** (continue à baisser 63%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.75%** (au-delà de la MAE q10 -6.75%), cible rebond +1.71% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=141) : retour [-2.81% .. +3.5%] · haut q95 +4.18% · bas q05 -3.66%
   - 60min (n=141) : retour [-3.51% .. +5.7%] · haut q95 +6.71% · bas q05 -5.12%
   - 2h (n=141) : retour [-4.56% .. +5.59%] · haut q95 +8.33% · bas q05 -6.35%
   - 4h (n=141) : retour [-5.7% .. +7.08%] · haut q95 +8.51% · bas q05 -8.1%
   - 6h (n=141) : retour [-7.12% .. +7.77%] · haut q95 +9.72% · bas q05 -8.96%
   - session (n=141) : retour [-6.4% .. +8.09%] · haut q95 +9.72% · bas q05 -8.96%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.4% des séances sont trend-up (mild 0% / strong 6.4%) · base = 9 séances trend-up (n_eff 7.5)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **33%**. Lecture précoce 30 min : signature présente → 19% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.94% (p75 1.08% / p90 1.73%) · ~3.08 replis/séance, durée méd 45.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **86%** (reprise méd 23.01 min, n=33)
   - −1.0% → **88%** (reprise méd 32.85 min, n=12)
   - −1.5% → **67%** (reprise méd 29.94 min, n=4)
- **RIDER — climb (trail + cibles)** : trail **−1.73%** (p90, défaut prudent ; serré/agressif −1.08%) ; extension open→close méd +7.9% (q75 +8.22% / q95 +11.4%), MFE méd +8.29% / q90 +10.64%
   - Échelle scale-out : +8.29% (33%) / +8.54% (33%) / +10.64% (34%)
- **DÉSARMER** : repli > **−1.73%** depuis le plus-haut = décay → P(retournement) **48%** (préavis méd 275.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +10.64% : P(retournement après) 0% (mèche méd 0.34%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +1.03%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.25/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 32.1  _(momentum baissier)_
- **ADX** : 28.3  _(tendance etablie)_
- **MACD** : hist -68314.247  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 62.2%
- **ATR** : 246000.0 (95.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.207  _(distribution)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 54.4  _(transition)_
- **MA** : MA20 2237950.0 · MA50 2199863.14 · MA200 1129568.47  _(prix < MA20)_
- **Dist MA** : MA20 -18.2% · MA50 -16.8% · MA200 +62.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88580 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
