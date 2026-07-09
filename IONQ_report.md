# IONQ

**Generated** : 2026-07-09T00:20:25.512629+00:00  
**Santé technique** : 5/10 — **Rating** : Neutral  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · $45.08  

> 🟡 **WAIT-FOR-DIP** — spot +0.9 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot $45.08 (+0.9% vs entrée) · entrée $44.66 · stop $43.37 · T1 $45.86 · R/R 0.93  
> ↳ P(T1 av. stop) 59 % _(réel 5 s)_ · EV/risk 0.101 _(réel 5 s)_ (GBM 0.099) · ¼-Kelly 0.029 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.89% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -51 % hors [0,100] (R² max 0.81). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Neutral'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $44.42–$44.90 (mid $44.66)
- Spot actuel : $45.08 (+0.9% au-dessus de la zone — repli à attendre)
- Stop : $43.37 (stop swing_plan-based (-5.01%))
- Targets : T1 $45.86 · R/R 0.93 | T2 $47.06 · R/R 1.86 | T3 $48.27 · R/R 2.8
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $43.37


## Edge, scénarios & sizing

- EV/risk : 0.099 | EV/share : $0.128 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 57 % | T2 33 % | T3 33 %
- Kelly (position) : f* 0.115 | ¼-Kelly 0.029 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 8.1 | bear 15.9 | side 76.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.932% → cible +2.694% / stop −2.885%, p_fill 84%, n_eff≈34.6) : P(cible|rempli) **59%** · **EV/risk +0.101** (×p_fill ; si rempli +0.35% du capital)
  - **swing** (entrée dip −2.06% → cible +6.024% / stop −3.012%, p_fill 82%, n_eff≈32.8) : P(cible|rempli) **42%** · **EV/risk +0.179** (×p_fill ; si rempli +0.66% du capital)
  - **deep** (entrée dip −3.186% → cible +8.519% / stop −4.259%, p_fill 86%, n_eff≈31.9) : P(cible|rempli) **40%** · **EV/risk +0.135** (×p_fill ; si rempli +0.67% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→82% · +2.0%→69% · +3.0%→64% · +5.0%→35% · +8.0%→18%
- Range intraday médian 7.84% (p90 12.54%) · excursion haute méd. +3.78% / basse méd. −2.97%
- Profil de vol intra : ouverture 4.974% vs midi 1.604% vs clôture 1.687% _(ouverture ~3.1× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑0%/↓1% ; spike-down 73% · recovery-V 40%)_
- **Régime intraday** : **chop** _(efficiency 0.112 ; momentum — autocorr 0.044)_ ; drift intra méd. -0.328% ; recovery-V 36%
- **σ réalisé intraday** 5.197% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 66% / bas 62% / whipsaw 35%
- POC intraday (dernière séance, temps-au-prix) : 45.6481 (VA 44.8781–46.3219 ; dernier close 45.37)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−3.0%** sous le close veille · fill 60% · rebond 76% · **stop −5.93%** sous le fill (sous le bruit) · cible +3.35% · R/R 0.56 (high win-rate)
- Gaps overnight (n=159) : méd. -0.41% · baisse 55% (gap-down >1% 39% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −1.25% (p90 −2.98%) · haut méd +1.0% · range méd 2.57%
- Excursion ouverture 15min (n=160) : bas méd −1.63% (p90 −3.9%) · haut méd +1.34% · range méd 3.58%
- Excursion ouverture 30min (n=160) : bas méd −1.87% (p90 −5.18%) · haut méd +1.96% · range méd 4.49%
- Excursion ouverture 60min (n=160) : bas méd −2.17% (p90 −6.13%) · haut méd +2.59% · range méd 5.74%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 45.37 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 76% · séance 84% (133/159) · gap 49% · délai 0.0min · rebond 72% (93/133) (MFE +2.26%)
   - −1.0% : fill 30min 72% · séance 80% (125/159) · gap 39% · délai 0.0min · rebond 77% (92/125) (MFE +2.75%)
   - −1.5% : fill 30min 68% · séance 77% (120/159) · gap 32% · délai 0.0min · rebond 73% (84/120) (MFE +2.58%)
   - −2.0% : fill 30min 58% · séance 71% (112/159) · gap 22% · délai 0.2min · rebond 73% (79/112) (MFE +2.7%)
   - −3.0% : fill 30min 48% · séance 60% (91/159) · gap 10% · délai 4.5min · rebond 76% (68/91) (MFE +3.35%)
   - −4.0% : fill 30min 29% · séance 46% (73/159) · gap 5% · délai 17.5min · rebond 76% (55/73) (MFE +2.38%)
   - −5.0% : fill 30min 20% · séance 40% (64/159) · gap 3% · délai 28.4min · rebond 82% (55/64) (MFE +3.02%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.99% (p90 −2.89%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.08% (p90 −3.44%) → stop au-delà de −2.57% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.13% (p90 −3.49%) → stop au-delà de −2.61% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=1112 jambes) : jambe baissière méd −1.33% (p90 −3.32%) · ~15.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 100% (72/72) · rebond 76% (53/72)
      · −2.0% : fill 94% (68/72) · rebond 78% (53/68)
      · −3.0% : fill 82% (58/72) · rebond 75% (45/58)
      · −4.0% : fill 63% (45/72) · rebond 72% (35/45)
      · −5.0% : fill 54% (39/72) · rebond 76% (32/39)
   - **flat** (17 séances) :
      · −1.0% : fill 64% (13/17) · rebond 83% (9/13)
      · −2.0% : fill 48% (12/17) · rebond 48% (6/12)
      · −3.0% : fill 36% (9/17) · rebond 50% (5/9)
      · −4.0% : fill 33% (7/17) · rebond 67% (3/7)
      · −5.0% : fill 33% (7/17) · rebond 91% (6/7)
   - **gap-up** (70 séances) :
      · −1.0% : fill 57% (40/70) · rebond 78% (30/40)
      · −2.0% : fill 45% (32/70) · rebond 64% (20/32)
      · −3.0% : fill 36% (24/70) · rebond 86% (18/24)
      · −4.0% : fill 28% (21/70) · rebond 89% (17/21)
      · −5.0% : fill 23% (18/70) · rebond 98% (17/18)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 48% en base · 55% si les 15 1res min sont vertes (80 cas) · 39% si rouges (80 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **1:46** → P(séance verte=clôture>ouverture) 77% si début vert vs 22% si rouge (base 48% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 198min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **77%** · continue >prix actuel 54% ; creux résiduel méd -2.22% (q20 -4.24%) → **SL/trailing à −4.24%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.91% / q75 +3.36% → **scale +1.91% / runner +3.36%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **22%** (continue à baisser 51%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.26%** (au-delà de la MAE q10 -5.26%), cible rebond +2.19% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.09% .. +7.16%] · haut q95 +7.98% · bas q05 -5.87%
   - 60min (n=160) : retour [-5.54% .. +6.05%] · haut q95 +9.69% · bas q05 -7.14%
   - 2h (n=160) : retour [-6.6% .. +8.49%] · haut q95 +10.49% · bas q05 -7.54%
   - 4h (n=160) : retour [-7.65% .. +7.67%] · haut q95 +11.9% · bas q05 -8.48%
   - 6h (n=160) : retour [-7.51% .. +7.64%] · haut q95 +12.22% · bas q05 -9.14%
   - session (n=160) : retour [-7.35% .. +9.34%] · haut q95 +12.23% · bas q05 -8.88%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.6% des séances sont trend-up (mild 0% / strong 5.6%) · base = 9 séances trend-up (n_eff 7.6)
- **ARMER** : fenêtre la + prédictive = **90 min** → P(reste trend-up à la clôture) **26%**. Lecture précoce 30 min : signature présente → 11% vs absente 3% (base 6%)
- **RIDER — replis (autoloop)** : profondeur médiane 1.24% (p75 1.9% / p90 2.72%) · ~4.11 replis/séance, durée méd 30.0 min. P(nouveau plus-haut après repli) :
   - −0.5% → **83%** (reprise méd 15.0 min, n=44)
   - −1.0% → **74%** (reprise méd 20.47 min, n=27)
   - −1.5% → **60%** (reprise méd 38.13 min, n=14)
   - −2.0% → **51%** (reprise méd 31.37 min, n=8)
   - −3.0% → **25%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.72%** (p90, défaut prudent ; serré/agressif −1.9%) ; extension open→close méd +7.82% (q75 +12.53% / q95 +18.2%), MFE méd +9.35% / q90 +18.66%
   - Échelle scale-out : +9.35% (33%) / +13.03% (33%) / +18.66% (34%)
- **DÉSARMER** : repli > **−2.72%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 168.41 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +18.66% : P(retournement après) 0% (mèche méd 3.41%)
- **CONTEXTE** : la dernière heure tient les gains 94% du temps (retour médian dernière heure +0.99%)


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : neutral_cautious


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 29.9  _(survente)_
- **ADX** : 21.9  _(pas de tendance nette)_
- **MACD** : hist -1.295  _(pas de croisement recent)_
- **BB** : %B 0.02 · largeur 33.5%
- **ATR** : 4.3 (61.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.361  _(distribution)_
- **Vol ratio** : 0.63  _(volume normal)_
- **Choppiness** : 45.1  _(transition)_
- **MA** : MA20 53.71 · MA50 55.07 · MA200 49.32  _(prix < MA20)_
- **Dist MA** : MA20 -16.1% · MA50 -18.1% · MA200 -8.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89231 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
