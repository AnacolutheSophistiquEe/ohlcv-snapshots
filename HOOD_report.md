# HOOD

**Generated** : 2026-07-22T00:30:37.262887+00:00  
**Santé technique** : 8/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite high · $106.36  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $106.36 (+2.2% vs entrée) · entrée $104.02 · stop $100.90 · T1 $106.62 · R/R 0.83  
> ↳ P(T1 av. stop) 53 % _(réel 5 s)_ · EV/risk 0.071 _(réel 5 s)_ (GBM 0.065) · ¼-Kelly 0.012 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 8/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $103.50–$104.54 (mid $104.02)
- Spot actuel : $106.36 (+2.2% au-dessus de la zone — repli à attendre)
- Stop : $100.90 (stop swing_plan-based (-7.5%))
- Targets : T1 $106.62 · R/R 0.83 | T2 $109.22 · R/R 1.67 | T3 $111.82 · R/R 2.5
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $100.90


## Edge, scénarios & sizing

- EV/risk : 0.065 | EV/share : $0.203 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 21 % | T3 21 %
- Kelly (position) : f* 0.05 | ¼-Kelly 0.012 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 51.7 | bear 9.3 | side 39.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 213.0 (= 2 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.196% → cible +2.498% / stop −3.0%, p_fill 51%, n_eff≈19.7) : P(cible|rempli) **53%** · **EV/risk +0.071** (×p_fill ; si rempli +0.41% du capital)
  - **swing** (entrée dip −4.842% → cible +5.586% / stop −2.793%, p_fill 28%, n_eff≈11.8) : P(cible|rempli) **40%** · **EV/risk +0.049** (×p_fill ; si rempli +0.49% du capital)
  - **deep** (entrée dip −7.475% → cible +7.9% / stop −3.95%, p_fill 22%, n_eff≈10.6) : P(cible|rempli) **57%** · **EV/risk +0.147** (×p_fill ; si rempli +2.58% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→86% · +1.0%→80% · +2.0%→55% · +3.0%→38% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.08% (p90 8.92%) · excursion haute méd. +2.16% / basse méd. −2.34%
- Profil de vol intra : ouverture 3.599% vs midi 1.095% vs clôture 1.059% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 21% · trend ↑1%/↓0% ; spike-down 68% · recovery-V 35%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr 0.008)_ ; drift intra méd. 0.118% ; recovery-V 34%
- **σ réalisé intraday** 3.867% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 61% / bas 43% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 100.9024 (VA 100.1306–101.3311 ; dernier close 99.31)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 21% · rebond 80% · **stop −4.37%** sous le fill (sous le bruit) · cible +2.76% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. -0.06% · baisse 52% (gap-down >1% 34% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −2.14%) · haut méd +0.87% · range méd 2.1%
- Excursion ouverture 15min (n=160) : bas méd −1.16% (p90 −3.27%) · haut méd +1.07% · range méd 2.83%
- Excursion ouverture 30min (n=160) : bas méd −1.48% (p90 −3.84%) · haut méd +1.42% · range méd 3.48%
- Excursion ouverture 60min (n=160) : bas méd −1.87% (p90 −3.9%) · haut méd +1.53% · range méd 3.89%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 99.31 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 80% (123/159) · gap 42% · délai 0.0min · rebond 57% (62/123) (MFE +1.53%)
   - −1.0% : fill 30min 61% · séance 68% (109/159) · gap 34% · délai 0.0min · rebond 61% (62/109) (MFE +1.37%)
   - −1.5% : fill 30min 50% · séance 61% (100/159) · gap 23% · délai 0.2min · rebond 54% (54/100) (MFE +1.35%)
   - −2.0% : fill 30min 43% · séance 54% (89/159) · gap 15% · délai 0.5min · rebond 66% (54/89) (MFE +1.35%)
   - −3.0% : fill 30min 31% · séance 41% (67/159) · gap 8% · délai 9.6min · rebond 73% (45/67) (MFE +1.92%)
   - −4.0% : fill 30min 19% · séance 32% (51/159) · gap 5% · délai 12.0min · rebond 79% (33/51) (MFE +2.32%)
   - −5.0% : fill 30min 11% · séance 21% (32/159) · gap 3% · délai 29.8min · rebond 80% (25/32) (MFE +2.76%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −2.61%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.53%) → stop au-delà de −1.81% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.58%) → stop au-delà de −1.77% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=761 jambes) : jambe baissière méd −1.16% (p90 −2.8%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (71 séances) :
      · −1.0% : fill 96% (68/71) · rebond 57% (36/68)
      · −2.0% : fill 82% (57/71) · rebond 62% (33/57)
      · −3.0% : fill 68% (46/71) · rebond 70% (30/46)
      · −4.0% : fill 55% (37/71) · rebond 83% (26/37)
      · −5.0% : fill 39% (26/71) · rebond 77% (20/26)
   - **flat** (21 séances) :
      · −1.0% : fill 71% (16/21) · rebond 76% (11/16)
      · −2.0% : fill 54% (12/21) · rebond 59% (7/12)
      · −3.0% : fill 19% (6/21) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/21) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/21) · rebond 82% (2/3)
   - **gap-up** (67 séances) :
      · −1.0% : fill 39% (25/67) · rebond 65% (15/25)
      · −2.0% : fill 25% (20/67) · rebond 85% (14/20)
      · −3.0% : fill 20% (15/67) · rebond 96% (13/15)
      · −4.0% : fill 13% (9/67) · rebond 87% (6/9)
      · −5.0% : fill 7% (3/67) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 50% en base · 68% si les 15 1res min sont vertes (70 cas) · 36% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **29min** → P(séance verte=clôture>ouverture) 78% si début vert vs 27% si rouge (base 50% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **78%** · continue >prix actuel 55% ; creux résiduel méd -1.73% (q20 -3.85%) → **SL/trailing à −3.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.65% / q75 +3.69% → **scale +1.65% / runner +3.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **27%** (continue à baisser 46%) → **RÉDUIRE ~73%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.87%** (au-delà de la MAE q10 -3.87%), cible rebond +2.43% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.73% .. +4.45%] · haut q95 +5.02% · bas q05 -4.84%
   - 60min (n=160) : retour [-3.65% .. +4.32%] · haut q95 +6.29% · bas q05 -4.96%
   - 2h (n=160) : retour [-4.42% .. +6.25%] · haut q95 +7.58% · bas q05 -5.63%
   - 4h (n=160) : retour [-5.09% .. +6.54%] · haut q95 +8.37% · bas q05 -6.33%
   - 6h (n=160) : retour [-5.71% .. +6.73%] · haut q95 +8.38% · bas q05 -7.27%
   - session (n=160) : retour [-5.7% .. +6.57%] · haut q95 +8.69% · bas q05 -7.72%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 8.1% des séances sont trend-up (mild 0% / strong 8.1%) · base = 13 séances trend-up (n_eff 9.8)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **40%**. Lecture précoce 30 min : signature présente → 21% vs absente 4% (base 8%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.92% (p75 1.42% / p90 2.12%) · ~4.0 replis/séance, durée méd 36.99 min. P(nouveau plus-haut après repli) :
   - −0.5% → **82%** (reprise méd 20.0 min, n=47)
   - −1.0% → **70%** (reprise méd 32.75 min, n=22)
   - −1.5% → **45%** (reprise méd 52.28 min, n=11)
   - −2.0% → **25%** (reprise méd None min, n=5)
- **RIDER — climb (trail + cibles)** : trail **−2.12%** (p90, défaut prudent ; serré/agressif −1.42%) ; extension open→close méd +6.08% (q75 +9.69% / q95 +13.38%), MFE méd +6.77% / q90 +14.84%
   - Échelle scale-out : +6.77% (33%) / +11.24% (33%) / +14.84% (34%)
- **DÉSARMER** : repli > **−2.12%** depuis le plus-haut = décay → P(retournement) **75%** (préavis méd 165.69 min, n=2) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +14.84% : P(retournement après) 0% (mèche méd 5.8%)
- **CONTEXTE** : la dernière heure tient les gains 78% du temps (retour médian dernière heure +0.61%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 55.2  _(momentum haussier)_
- **ADX** : 23.9  _(pas de tendance nette)_
- **MACD** : hist -1.867  _(pas de croisement recent)_
- **BB** : %B 0.48 · largeur 26.9%
- **ATR** : 7.25 (75.0e pct 1a)  _(volatilite elevee)_
- **OBV/CMF** : OBV falling · CMF -0.05  _(neutre)_
- **Vol ratio** : 0.76  _(volume normal)_
- **Choppiness** : 55.5  _(transition)_
- **MA** : MA20 106.88 · MA50 94.03 · MA200 101.36  _(prix < MA20)_
- **Dist MA** : MA20 -0.5% · MA50 +13.1% · MA200 +4.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (92419 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
