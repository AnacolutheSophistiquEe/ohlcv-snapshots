# SOI

**Generated** : 2026-07-24T00:08:04.258681+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 7.7 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · €117.95  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot €117.95 (+0.6% vs entrée) · entrée €117.28 · stop €114.19 · T1 €122.21 · R/R 1.6  
> ↳ P(T1 av. stop) 32 % _(réel 5 s)_ · EV/risk -0.123 _(réel 5 s)_ (GBM 0.127) · ¼-Kelly 0.034 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.63% cohérent avec le bruit 5 s (EV-optimal ≈ −2.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : up | **H1** : up  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €116.60–€117.95 (mid €117.28)
- Spot actuel : €117.95 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : €114.19 (stop swing_plan-based (-5.75%))
- Targets : T1 €122.21 · R/R 1.6 | T2 €127.15 · R/R 3.19 | T3 €132.09 · R/R 4.79
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €114.19


## Edge, scénarios & sizing

- EV/risk : 0.127 | EV/share : €0.391 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 40 % | T2 38 % | T3 38 %
- Kelly (position) : f* 0.137 | ¼-Kelly 0.034 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 6.8 | bear 35.7 | side 57.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 354.0 (= 3 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.573% → cible +4.21% / stop −2.632%, p_fill 90%, n_eff≈35.7) : P(cible|rempli) **32%** · **EV/risk -0.123** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −1.094% → cible +9.414% / stop −4.707%, p_fill 93%, n_eff≈36.4) : P(cible|rempli) **24%** · **EV/risk -0.277** (×p_fill ; si rempli -1.40% du capital)
  - **deep** (entrée dip −1.482% → cible +13.313% / stop −6.657%, p_fill 95%, n_eff≈36.8) : P(cible|rempli) **15%** · **EV/risk -0.507** (×p_fill ; si rempli -3.56% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→84% · +1.0%→76% · +2.0%→69% · +3.0%→57% · +5.0%→44% · +8.0%→21%
- Range intraday médian 9.09% (p90 17.62%) · excursion haute méd. +3.78% / basse méd. −3.47%
- Profil de vol intra : ouverture 5.787% vs midi 1.693% vs clôture 2.578% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (138 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 15% · trend ↑0%/↓1% ; spike-down 77% · recovery-V 44%)_
- **Régime intraday** : **chop** _(efficiency 0.132 ; mean-reverting — autocorr -0.092)_ ; drift intra méd. -0.253% ; recovery-V 42%
- **σ réalisé intraday** 5.35% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 65% / bas 62% / whipsaw 29%
- POC intraday (dernière séance, temps-au-prix) : 96.0455 (VA 94.9885–96.8005 ; dernier close 96.04)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 44% · rebond 79% · **stop −7.26%** sous le fill (sous le bruit) · cible +2.85% · R/R 0.39 (high win-rate)
- Gaps overnight (n=137) : méd. 0.03% · baisse 50% (gap-down >1% 33% · >2% 25%)
- Excursion ouverture 5min (n=138) : bas méd −1.27% (p90 −3.51%) · haut méd +1.0% · range méd 2.99%
- Excursion ouverture 15min (n=138) : bas méd −1.55% (p90 −4.84%) · haut méd +1.34% · range méd 3.8%
- Excursion ouverture 30min (n=138) : bas méd −1.75% (p90 −5.23%) · haut méd +1.78% · range méd 4.33%
- Excursion ouverture 60min (n=138) : bas méd −1.85% (p90 −5.87%) · haut méd +1.92% · range méd 4.76%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 96.04 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 78% (108/137) · gap 41% · délai 0.0min · rebond 63% (70/108) (MFE +1.93%)
   - −1.0% : fill 30min 63% · séance 75% (103/137) · gap 33% · délai 0.1min · rebond 70% (74/103) (MFE +1.87%)
   - −1.5% : fill 30min 59% · séance 72% (94/137) · gap 31% · délai 0.2min · rebond 73% (69/94) (MFE +2.25%)
   - −2.0% : fill 30min 54% · séance 66% (87/137) · gap 25% · délai 0.2min · rebond 77% (69/87) (MFE +2.72%)
   - −3.0% : fill 30min 42% · séance 57% (72/137) · gap 17% · délai 0.8min · rebond 75% (57/72) (MFE +2.91%)
   - −4.0% : fill 30min 32% · séance 48% (58/137) · gap 7% · délai 2.1min · rebond 75% (46/58) (MFE +2.64%)
   - −5.0% : fill 30min 23% · séance 44% (50/137) · gap 2% · délai 18.3min · rebond 79% (42/50) (MFE +2.85%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −3.78%) → stop au-delà de −2.35% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.94% (p90 −3.1%) → stop au-delà de −2.23% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.9% (p90 −3.19%) → stop au-delà de −2.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1205 jambes) : jambe baissière méd −1.32% (p90 −3.14%) · ~18.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 97% (53/54) · rebond 60% (33/53)
      · −2.0% : fill 94% (51/54) · rebond 73% (40/51)
      · −3.0% : fill 84% (43/54) · rebond 75% (35/43)
      · −4.0% : fill 75% (38/54) · rebond 79% (31/38)
      · −5.0% : fill 67% (33/54) · rebond 85% (28/33)
   - **flat** (17 séances) :
      · −1.0% : fill 100% (17/17) · rebond 79% (14/17)
      · −2.0% : fill 96% (15/17) · rebond 82% (12/15)
      · −3.0% : fill 69% (11/17) · rebond 67% (8/11)
      · −4.0% : fill 57% (8/17) · rebond 65% (6/8)
      · −5.0% : fill 57% (8/17) · rebond 77% (7/8)
   - **gap-up** (66 séances) :
      · −1.0% : fill 46% (33/66) · rebond 84% (27/33)
      · −2.0% : fill 31% (21/66) · rebond 82% (17/21)
      · −3.0% : fill 28% (18/66) · rebond 80% (14/18)
      · −4.0% : fill 19% (12/66) · rebond 68% (9/12)
      · −5.0% : fill 17% (9/66) · rebond 59% (7/9)
- **P(clôture VERTE) selon le drive 15min** (n=138) : 53% en base · 72% si les 15 1res min sont vertes (64 cas) · 32% si rouges (74 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=138) : COUDE à **36min** → P(séance verte=clôture>ouverture) 80% si début vert vs 25% si rouge (base 53% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 276min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **80%** · continue >prix actuel 60% ; creux résiduel méd -2.23% (q20 -5.47%) → **SL/trailing à −5.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +3.02% / q75 +5.88% → **scale +3.02% / runner +5.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=75) : edge inversé — récupère vert seulement **25%** (continue à baisser 61%) → **RÉDUIRE ~75%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −8.63%** (au-delà de la MAE q10 -8.63%), cible rebond +2.09% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=138) : retour [-5.33% .. +6.79%] · haut q95 +7.2% · bas q05 -6.33%
   - 60min (n=138) : retour [-6.09% .. +7.4%] · haut q95 +8.55% · bas q05 -6.76%
   - 2h (n=138) : retour [-6.73% .. +10.16%] · haut q95 +12.02% · bas q05 -8.18%
   - 4h (n=138) : retour [-7.2% .. +11.09%] · haut q95 +13.05% · bas q05 -8.47%
   - 6h (n=138) : retour [-8.66% .. +12.01%] · haut q95 +14.09% · bas q05 -10.44%
   - session (n=138) : retour [-11.95% .. +13.89%] · haut q95 +16.44% · bas q05 -13.98%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 6.5% des séances sont trend-up (mild 0% / strong 6.5%) · base = 9 séances trend-up (n_eff 5.7)
- **ARMER** : fenêtre la + prédictive = **60 min** → P(reste trend-up à la clôture) **14%**. Lecture précoce 30 min : signature présente → 6% vs absente 6% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.08% (p75 1.67% / p90 2.95%) · ~6.0 replis/séance, durée méd 38.95 min. P(nouveau plus-haut après repli) :
   - −0.5% → **94%** (reprise méd 20.0 min, n=57)
   - −1.0% → **92%** (reprise méd 34.22 min, n=33)
   - −1.5% → **88%** (reprise méd 46.1 min, n=17)
   - −2.0% → **87%** (reprise méd 49.44 min, n=15)
   - −3.0% → **100%** (reprise méd 61.76 min, n=6)
- **RIDER — climb (trail + cibles)** : trail **−2.95%** (p90, défaut prudent ; serré/agressif −1.67%) ; extension open→close méd +10.12% (q75 +13.85% / q95 +17.31%), MFE méd +10.12% / q90 +18.28%
   - Échelle scale-out : +10.12% (33%) / +16.57% (33%) / +18.28% (34%)
- **DÉSARMER** : repli > **−2.95%** depuis le plus-haut = décay → P(retournement) **0%** (préavis méd None min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.28% : P(retournement après) 0% (mèche méd 1.42%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +3.01%)


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
- **swing** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-29 — US FOMC Rate Decision (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 50.4  _(neutre)_
- **ADX** : 18.8  _(pas de tendance nette)_
- **MACD** : hist 1.886  _(bullish_recent)_
- **BB** : %B 0.82 · largeur 42.2%
- **ATR** : 10.29 (78.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.021  _(neutre)_
- **Vol ratio** : 1.14  _(volume normal)_
- **Choppiness** : 43.0  _(transition)_
- **MA** : MA20 104.01 · MA50 128.68 · MA200 69.11  _(prix > MA20)_
- **Dist MA** : MA20 +13.4% · MA50 -8.3% · MA200 +70.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (98900 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
