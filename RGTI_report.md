# RGTI

**Generated** : 2026-07-07T21:53:37.970459+00:00  
> ⚠️ **Données suspectes** : volatilité réalisée 5.4 %/j très élevée — vérifier la qualité des barres avant de se fier au bulletin.  

**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $16.55  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $16.55 (+3.1% vs entrée) · entrée $16.06 · stop $15.54 · T1 $16.54 · R/R 0.92  
> ↳ P(T1 av. stop) 23 % _(réel 5 s)_ · EV/risk -0.216 _(réel 5 s)_ (GBM 0.052) · ¼-Kelly 0.02 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.19% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.96–$16.15 (mid $16.06)
- Spot actuel : $16.55 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : $15.54 (stop swing_plan-based (-9.68%))
- Targets : T1 $16.54 · R/R 0.92 | T2 $17.01 · R/R 1.83 | T3 $17.49 · R/R 2.75
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.54


## Edge, scénarios & sizing

- EV/risk : 0.052 | EV/share : $0.026 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.08 | ¼-Kelly 0.02 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.4 | bear 72.7 | side 10.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.986% → cible +2.984% / stop −3.189%, p_fill 46%, n_eff≈19.6) : P(cible|rempli) **23%** · **EV/risk -0.216** (×p_fill ; si rempli -1.50% du capital)
  - **swing** (entrée dip −6.563% → cible +6.672% / stop −3.336%, p_fill 45%, n_eff≈18.6) : P(cible|rempli) **25%** · **EV/risk -0.100** (×p_fill ; si rempli -0.75% du capital)
  - **deep** (entrée dip −10.151% → cible +9.435% / stop −4.718%, p_fill 43%, n_eff≈15.5) : P(cible|rempli) **36%** · **EV/risk +0.027** (×p_fill ; si rempli +0.29% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→84% · +2.0%→69% · +3.0%→55% · +5.0%→39% · +8.0%→16%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.44% / basse méd. −2.93%
- Profil de vol intra : ouverture 5.183% vs midi 1.693% vs clôture 1.954% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 47%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; momentum — autocorr 0.057)_ ; drift intra méd. -0.026% ; recovery-V 48%
- **σ réalisé intraday** 5.554% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 49% / whipsaw 22%
- POC intraday (dernière séance, temps-au-prix) : 18.1352 (VA 18.0484–18.5472 ; dernier close 17.96)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 64% · rebond 79% · **stop −7.38%** sous le fill (sous le bruit) · cible +2.73% · R/R 0.37 (high win-rate)
- Gaps overnight (n=159) : méd. -0.54% · baisse 58% (gap-down >1% 44% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.36% (p90 −2.97%) · haut méd +1.06% · range méd 2.62%
- Excursion ouverture 15min (n=160) : bas méd −1.54% (p90 −4.49%) · haut méd +1.55% · range méd 3.71%
- Excursion ouverture 30min (n=160) : bas méd −1.81% (p90 −6.02%) · haut méd +2.08% · range méd 4.71%
- Excursion ouverture 60min (n=160) : bas méd −2.1% (p90 −6.48%) · haut méd +2.48% · range méd 5.72%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 17.96 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 79% · séance 86% (137/159) · gap 51% · délai 0.0min · rebond 71% (92/137) (MFE +2.45%)
   - −1.0% : fill 30min 71% · séance 83% (133/159) · gap 44% · délai 0.0min · rebond 70% (89/133) (MFE +2.21%)
   - −1.5% : fill 30min 64% · séance 78% (124/159) · gap 38% · délai 0.0min · rebond 68% (83/124) (MFE +2.53%)
   - −2.0% : fill 30min 59% · séance 72% (114/159) · gap 28% · délai 0.0min · rebond 67% (75/114) (MFE +2.72%)
   - −3.0% : fill 30min 52% · séance 64% (98/159) · gap 13% · délai 1.4min · rebond 79% (73/98) (MFE +2.73%)
   - −4.0% : fill 30min 37% · séance 48% (77/159) · gap 5% · délai 5.5min · rebond 77% (57/77) (MFE +2.48%)
   - −5.0% : fill 30min 24% · séance 42% (65/159) · gap 2% · délai 16.8min · rebond 72% (50/65) (MFE +2.3%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −1.03% (p90 −3.02%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.3% (p90 −4.12%) → stop au-delà de −2.42% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.3% (p90 −4.26%) → stop au-delà de −2.74% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1188 jambes) : jambe baissière méd −1.32% (p90 −3.37%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (83 séances) :
      · −1.0% : fill 98% (82/83) · rebond 66% (50/82)
      · −2.0% : fill 89% (77/83) · rebond 68% (52/77)
      · −3.0% : fill 85% (70/83) · rebond 78% (52/70)
      · −4.0% : fill 64% (56/83) · rebond 77% (42/56)
      · −5.0% : fill 56% (49/83) · rebond 74% (40/49)
   - **flat** (15 séances) :
      · −1.0% : fill 89% (13/15) · rebond 88% (11/13)
      · −2.0% : fill 62% (10/15) · rebond 61% (7/10)
      · −3.0% : fill 44% (5/15) · rebond 75% (3/5)
      · −4.0% : fill 44% (5/15) · rebond 75% (3/5)
      · −5.0% : fill 44% (5/15) · rebond 87% (3/5)
   - **gap-up** (61 séances) :
      · −1.0% : fill 58% (38/61) · rebond 73% (28/38)
      · −2.0% : fill 46% (27/61) · rebond 65% (16/27)
      · −3.0% : fill 36% (23/61) · rebond 83% (18/23)
      · −4.0% : fill 24% (16/61) · rebond 78% (12/16)
      · −5.0% : fill 18% (11/61) · rebond 55% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 53% en base · 64% si les 15 1res min sont vertes (78 cas) · 40% si rouges (82 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 91% si début vert vs 17% si rouge (base 53% · écart 74 pts) ; prédictivité sature ensuite (plafond brut 93min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=74) : tient le vert **91%** · continue >prix actuel 54% ; creux résiduel méd -2.48% (q20 -3.58%) → **SL/trailing à −3.58%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.95% / q75 +4.34% → **scale +2.95% / runner +4.34%**, sortie à la clôture
  - **si ROUGE au coude** (n=86) : edge inversé — récupère vert seulement **17%** (continue à baisser 55%) → **RÉDUIRE ~83%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.82%** (au-delà de la MAE q10 -5.82%), cible rebond +1.88% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.79% .. +5.49%] · haut q95 +8.14% · bas q05 -7.01%
   - 60min (n=160) : retour [-5.73% .. +7.16%] · haut q95 +9.59% · bas q05 -7.31%
   - 2h (n=160) : retour [-7.56% .. +8.52%] · haut q95 +9.84% · bas q05 -8.31%
   - 4h (n=160) : retour [-8.81% .. +6.6%] · haut q95 +10.02% · bas q05 -10.49%
   - 6h (n=160) : retour [-8.81% .. +8.53%] · haut q95 +10.68% · bas q05 -10.49%
   - session (n=160) : retour [-7.99% .. +9.88%] · haut q95 +11.06% · bas q05 -10.49%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 11% vs absente 2% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.26% (p75 1.86% / p90 2.7%) · ~4.0 replis/séance, durée méd 40.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **93%** (reprise méd 11.1 min, n=44)
   - −1.0% → **90%** (reprise méd 30.5 min, n=27)
   - −1.5% → **81%** (reprise méd 43.22 min, n=12)
   - −2.0% → **70%** (reprise méd 138.94 min, n=8)
   - −3.0% → **26%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.7%** (p90, défaut prudent ; serré/agressif −1.86%) ; extension open→close méd +8.33% (q75 +9.92% / q95 +12.86%), MFE méd +9.1% / q90 +12.37%
   - Échelle scale-out : +9.1% (33%) / +10.39% (33%) / +12.37% (34%)
- **DÉSARMER** : repli > **−2.7%** depuis le plus-haut = décay → P(retournement) **74%** (préavis méd 141.49 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +12.37% : P(retournement après) 0% (mèche méd 0.52%)
- **CONTEXTE** : la dernière heure tient les gains 100% du temps (retour médian dernière heure +0.96%)


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 21.0  _(survente)_
- **ADX** : 16.8  _(pas de tendance nette)_
- **MACD** : hist -0.431  _(pas de croisement recent)_
- **BB** : %B -0.03 · largeur 31.3%
- **ATR** : 1.71 (46.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.231  _(distribution)_
- **Vol ratio** : 0.8  _(volume normal)_
- **Choppiness** : 50.3  _(transition)_
- **MA** : MA20 19.82 · MA50 20.15 · MA200 23.84  _(prix < MA20)_
- **Dist MA** : MA20 -16.5% · MA50 -17.9% · MA200 -30.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88115 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
