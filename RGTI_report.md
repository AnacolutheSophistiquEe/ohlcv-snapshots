# RGTI

**Generated** : 2026-07-13T00:28:35.856242+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $16.54  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot $16.54 (+3.1% vs entrée) · entrée $16.05 · stop $15.57 · T1 $16.48 · R/R 0.9  
> ↳ P(T1 av. stop) 11 % _(réel 5 s)_ · EV/risk -0.316 _(réel 5 s)_ (GBM 0.086) · ¼-Kelly 0.021 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.96–$16.14 (mid $16.05)
- Spot actuel : $16.54 (+3.1% au-dessus de la zone — repli à attendre)
- Stop : $15.57 (stop swing_plan-based (-9.35%))
- Targets : T1 $16.48 · R/R 0.9 | T2 $16.91 · R/R 1.79 | T3 $17.35 · R/R 2.71
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $15.57


## Edge, scénarios & sizing

- EV/risk : 0.086 | EV/share : $0.042 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 36 % | T3 36 %
- Kelly (position) : f* 0.082 | ¼-Kelly 0.021 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 15.8 | bear 72.8 | side 11.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.969% → cible +2.693% / stop −3.0%, p_fill 48%, n_eff≈20.1) : P(cible|rempli) **11%** · **EV/risk -0.316** (×p_fill ; si rempli -1.99% du capital)
  - **swing** (entrée dip −6.536% → cible +6.023% / stop −3.011%, p_fill 46%, n_eff≈18.6) : P(cible|rempli) **30%** · **EV/risk -0.053** (×p_fill ; si rempli -0.35% du capital)
  - **deep** (entrée dip −10.101% → cible +8.518% / stop −4.259%, p_fill 44%, n_eff≈16.5) : P(cible|rempli) **39%** · **EV/risk +0.059** (×p_fill ; si rempli +0.56% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→89% · +1.0%→82% · +2.0%→70% · +3.0%→56% · +5.0%→39% · +8.0%→16%
- Range intraday médian 8.12% (p90 13.36%) · excursion haute méd. +3.55% / basse méd. −2.93%
- Profil de vol intra : ouverture 5.26% vs midi 1.68% vs clôture 1.907% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 17% · trend ↑0%/↓0% ; spike-down 76% · recovery-V 44%)_
- **Régime intraday** : **chop** _(efficiency 0.123 ; momentum — autocorr 0.042)_ ; drift intra méd. -0.232% ; recovery-V 41%
- **σ réalisé intraday** 5.289% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 53% / whipsaw 18%
- POC intraday (dernière séance, temps-au-prix) : 16.6999 (VA 16.5179–16.7681 ; dernier close 16.54)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 63% · rebond 77% · **stop −7.37%** sous le fill (sous le bruit) · cible +2.64% · R/R 0.36 (high win-rate)
- Gaps overnight (n=159) : méd. -0.54% · baisse 58% (gap-down >1% 45% · >2% 28%)
- Excursion ouverture 5min (n=160) : bas méd −1.3% (p90 −2.95%) · haut méd +1.06% · range méd 2.61%
- Excursion ouverture 15min (n=160) : bas méd −1.54% (p90 −4.41%) · haut méd +1.55% · range méd 3.72%
- Excursion ouverture 30min (n=160) : bas méd −1.8% (p90 −6.02%) · haut méd +2.03% · range méd 4.73%
- Excursion ouverture 60min (n=160) : bas méd −2.09% (p90 −6.57%) · haut méd +2.39% · range méd 5.7%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 16.54 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 79% · séance 87% (137/159) · gap 51% · délai 0.0min · rebond 69% (91/137) (MFE +2.52%)
   - −1.0% : fill 30min 71% · séance 84% (133/159) · gap 45% · délai 0.0min · rebond 68% (88/133) (MFE +2.21%)
   - −1.5% : fill 30min 65% · séance 78% (125/159) · gap 39% · délai 0.0min · rebond 68% (84/125) (MFE +2.41%)
   - −2.0% : fill 30min 60% · séance 72% (115/159) · gap 28% · délai 0.0min · rebond 67% (76/115) (MFE +2.68%)
   - −3.0% : fill 30min 52% · séance 63% (98/159) · gap 12% · délai 1.5min · rebond 77% (73/98) (MFE +2.64%)
   - −4.0% : fill 30min 36% · séance 47% (77/159) · gap 5% · délai 4.7min · rebond 78% (57/77) (MFE +2.41%)
   - −5.0% : fill 30min 24% · séance 41% (65/159) · gap 2% · délai 20.0min · rebond 69% (49/65) (MFE +1.99%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.96%) → stop au-delà de −2.02% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.24% (p90 −4.07%) → stop au-delà de −2.38% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.29% (p90 −4.25%) → stop au-delà de −2.72% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1181 jambes) : jambe baissière méd −1.31% (p90 −3.36%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (84 séances) :
      · −1.0% : fill 98% (83/84) · rebond 65% (51/83)
      · −2.0% : fill 90% (78/84) · rebond 67% (53/78)
      · −3.0% : fill 83% (70/84) · rebond 75% (52/70)
      · −4.0% : fill 63% (56/84) · rebond 78% (42/56)
      · −5.0% : fill 56% (49/84) · rebond 69% (39/49)
   - **flat** (15 séances) :
      · −1.0% : fill 89% (13/15) · rebond 88% (11/13)
      · −2.0% : fill 62% (10/15) · rebond 61% (7/10)
      · −3.0% : fill 44% (5/15) · rebond 75% (3/5)
      · −4.0% : fill 44% (5/15) · rebond 75% (3/5)
      · −5.0% : fill 44% (5/15) · rebond 87% (3/5)
   - **gap-up** (60 séances) :
      · −1.0% : fill 62% (37/60) · rebond 69% (26/37)
      · −2.0% : fill 47% (27/60) · rebond 69% (16/27)
      · −3.0% : fill 37% (23/60) · rebond 86% (18/23)
      · −4.0% : fill 22% (16/60) · rebond 78% (12/16)
      · −5.0% : fill 17% (11/60) · rebond 55% (7/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 63% si les 15 1res min sont vertes (80 cas) · 37% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:32** → P(séance verte=clôture>ouverture) 88% si début vert vs 16% si rouge (base 51% · écart 73 pts) ; prédictivité sature ensuite (plafond brut 93min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=75) : tient le vert **88%** · continue >prix actuel 54% ; creux résiduel méd -2.23% (q20 -3.49%) → **SL/trailing à −3.49%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.75% / q75 +4.27% → **scale +2.75% / runner +4.27%**, sortie à la clôture
  - **si ROUGE au coude** (n=85) : edge inversé — récupère vert seulement **16%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.8%** (au-delà de la MAE q10 -5.8%), cible rebond +2.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.58% .. +5.02%] · haut q95 +7.8% · bas q05 -6.87%
   - 60min (n=160) : retour [-6.09% .. +7.15%] · haut q95 +9.34% · bas q05 -7.22%
   - 2h (n=160) : retour [-7.51% .. +8.21%] · haut q95 +9.47% · bas q05 -8.22%
   - 4h (n=160) : retour [-8.6% .. +6.55%] · haut q95 +9.43% · bas q05 -10.47%
   - 6h (n=160) : retour [-8.68% .. +8.46%] · haut q95 +10.07% · bas q05 -10.47%
   - session (n=160) : retour [-7.92% .. +9.76%] · haut q95 +10.79% · bas q05 -10.47%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.4)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **25%**. Lecture précoce 30 min : signature présente → 10% vs absente 1% (base 6%)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 19.6  _(survente)_
- **ADX** : 19.0  _(pas de tendance nette)_
- **MACD** : hist -0.354  _(pas de croisement recent)_
- **BB** : %B 0.12 · largeur 37.8%
- **ATR** : 1.49 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.173  _(distribution)_
- **Vol ratio** : 0.59  _(volume atone)_
- **Choppiness** : 44.9  _(transition)_
- **MA** : MA20 19.29 · MA50 20.16 · MA200 23.69  _(prix < MA20)_
- **Dist MA** : MA20 -14.3% · MA50 -17.9% · MA200 -30.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (88372 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
