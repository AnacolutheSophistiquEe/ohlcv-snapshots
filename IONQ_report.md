# IONQ

**Generated** : 2026-07-23T00:23:56.798871+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · $34.68  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)  
> ↳ spot $34.68 (+0.4% vs entrée) · entrée $34.55 · stop $33.68 · T1 $35.35 · R/R 0.92  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.121 _(réel 5 s)_ (GBM 0.012) · ¼-Kelly 0.008 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.52% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -26 % hors [0,100] (R² max 0.79). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $34.41–$34.68 (mid $34.55)
- Spot actuel : $34.68 (+0.4% au-dessus de la zone — repli à attendre)
- Stop : $33.68 (stop swing_plan-based (-8.35%))
- Targets : T1 $35.35 · R/R 0.92 | T2 $36.15 · R/R 1.84 | T3 $36.95 · R/R 2.76
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $33.68


## Edge, scénarios & sizing

- EV/risk : 0.012 | EV/share : $0.010 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 33 % | T3 30 %
- Kelly (position) : f* 0.033 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 12.3 | bear 31.0 | side 56.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.387% → cible +2.321% / stop −2.523%, p_fill 97%, n_eff≈38.9) : P(cible|rempli) **40%** · **EV/risk -0.121** (×p_fill ; si rempli -0.32% du capital)
  - **swing** (entrée dip −0.678% → cible +15.449% / stop −7.724%, p_fill 96%, n_eff≈38.2) : P(cible|rempli) **8%** · **EV/risk -0.608** (×p_fill ; si rempli -4.88% du capital)
  - **deep** (entrée dip −0.987% → cible +7.338% / stop −3.669%, p_fill 95%, n_eff≈37.1) : P(cible|rempli) **34%** · **EV/risk -0.033** (×p_fill ; si rempli -0.12% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→79% · +2.0%→65% · +3.0%→61% · +5.0%→32% · +8.0%→18%
- Range intraday médian 7.87% (p90 12.54%) · excursion haute méd. +3.72% / basse méd. −3.27%
- Profil de vol intra : ouverture 5.119% vs midi 1.566% vs clôture 1.656% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; neutre — autocorr 0.028)_ ; drift intra méd. -1.287% ; recovery-V 29%
- **σ réalisé intraday** 4.741% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 50% / bas 68% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 35.6077 (VA 35.3397–35.8423 ; dernier close 35.52)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 42% · rebond 81% · **stop −5.1%** sous le fill (sous le bruit) · cible +2.66% · R/R 0.52 (high win-rate)
- Gaps overnight (n=159) : méd. -0.27% · baisse 53% (gap-down >1% 38% · >2% 20%)
- Excursion ouverture 5min (n=160) : bas méd −1.27% (p90 −2.94%) · haut méd +0.96% · range méd 2.51%
- Excursion ouverture 15min (n=160) : bas méd −1.83% (p90 −4.29%) · haut méd +1.23% · range méd 3.64%
- Excursion ouverture 30min (n=160) : bas méd −1.92% (p90 −5.26%) · haut méd +1.67% · range méd 4.41%
- Excursion ouverture 60min (n=160) : bas méd −2.51% (p90 −5.92%) · haut méd +1.91% · range méd 5.49%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 35.52 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 74% · séance 83% (132/159) · gap 46% · délai 0.0min · rebond 68% (91/132) (MFE +1.89%)
   - −1.0% : fill 30min 70% · séance 80% (126/159) · gap 38% · délai 0.0min · rebond 73% (92/126) (MFE +2.4%)
   - −1.5% : fill 30min 67% · séance 78% (121/159) · gap 30% · délai 0.0min · rebond 67% (83/121) (MFE +2.46%)
   - −2.0% : fill 30min 59% · séance 69% (111/159) · gap 20% · délai 0.3min · rebond 67% (75/111) (MFE +2.59%)
   - −3.0% : fill 30min 49% · séance 60% (93/159) · gap 9% · délai 6.0min · rebond 71% (67/93) (MFE +3.05%)
   - −4.0% : fill 30min 31% · séance 47% (75/159) · gap 4% · délai 15.5min · rebond 73% (55/75) (MFE +2.01%)
   - −5.0% : fill 30min 20% · séance 42% (66/159) · gap 2% · délai 31.1min · rebond 81% (56/66) (MFE +2.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.95% (p90 −2.85%) → stop au-delà de −2.0% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.08% (p90 −3.79%) → stop au-delà de −2.65% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.08% (p90 −3.39%) → stop au-delà de −2.55% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1125 jambes) : jambe baissière méd −1.34% (p90 −3.34%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 100% (72/72) · rebond 72% (54/72)
      · −2.0% : fill 94% (68/72) · rebond 74% (52/68)
      · −3.0% : fill 84% (59/72) · rebond 71% (44/59)
      · −4.0% : fill 64% (45/72) · rebond 71% (34/45)
      · −5.0% : fill 57% (39/72) · rebond 74% (31/39)
   - **flat** (15 séances) :
      · −1.0% : fill 64% (12/15) · rebond 82% (8/12)
      · −2.0% : fill 48% (11/15) · rebond 46% (5/11)
      · −3.0% : fill 36% (8/15) · rebond 48% (4/8)
      · −4.0% : fill 34% (7/15) · rebond 67% (3/7)
      · −5.0% : fill 34% (7/15) · rebond 91% (6/7)
   - **gap-up** (72 séances) :
      · −1.0% : fill 59% (42/72) · rebond 71% (30/42)
      · −2.0% : fill 42% (32/72) · rebond 51% (18/32)
      · −3.0% : fill 36% (26/72) · rebond 78% (19/26)
      · −4.0% : fill 29% (23/72) · rebond 78% (18/23)
      · −5.0% : fill 25% (20/72) · rebond 99% (19/20)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 43% en base · 51% si les 15 1res min sont vertes (78 cas) · 34% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 79% si début vert vs 16% si rouge (base 43% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=70) : tient le vert **79%** · continue >prix actuel 53% ; creux résiduel méd -2.07% (q20 -4.22%) → **SL/trailing à −4.22%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.84% / q75 +3.01% → **scale +1.84% / runner +3.01%**, sortie à la clôture
  - **si ROUGE au coude** (n=90) : edge inversé — récupère vert seulement **16%** (continue à baisser 57%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.5%** (au-delà de la MAE q10 -4.5%), cible rebond +1.96% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.18% .. +6.61%] · haut q95 +7.51% · bas q05 -5.83%
   - 60min (n=160) : retour [-5.35% .. +5.62%] · haut q95 +8.46% · bas q05 -6.83%
   - 2h (n=160) : retour [-6.5% .. +8.19%] · haut q95 +9.12% · bas q05 -7.45%
   - 4h (n=160) : retour [-7.38% .. +7.43%] · haut q95 +10.3% · bas q05 -8.4%
   - 6h (n=160) : retour [-7.66% .. +7.56%] · haut q95 +11.04% · bas q05 -8.77%
   - session (n=160) : retour [-7.47% .. +8.66%] · haut q95 +11.04% · bas q05 -8.79%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 7.3)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 11% vs absente 2% (base 5%)
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 0.5 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 8.4  _(survente)_
- **ADX** : 37.3  _(tendance etablie)_
- **MACD** : hist -0.865  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 64.9%
- **ATR** : 2.91 (23.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.457  _(distribution)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 24.9  _(marche directionnel)_
- **MA** : MA20 43.9 · MA50 53.35 · MA200 47.77  _(prix < MA20)_
- **Dist MA** : MA20 -21.0% · MA50 -35.0% · MA200 -27.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89557 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
