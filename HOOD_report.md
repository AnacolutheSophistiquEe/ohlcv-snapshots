# HOOD

**Generated** : 2026-07-21T00:30:11.781433+00:00  
**Santé technique** : 4/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite normal · $99.28  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-07-23 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot $99.28 (+0.6% vs entrée) · entrée $98.71 · stop $95.75 · T1 $101.03 · R/R 0.78  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.049 _(réel 5 s)_ (GBM 0.061) · ¼-Kelly 0.015 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.0% cohérent avec le bruit 5 s (EV-optimal ≈ −3.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $98.25–$99.17 (mid $98.71)
- Spot actuel : $99.28 (+0.6% au-dessus de la zone — repli à attendre)
- Stop : $95.75 (stop swing_plan-based (-3.85%))
- Targets : T1 $101.03 · R/R 0.78 | T2 $103.35 · R/R 1.57 | T3 $105.67 · R/R 2.35
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $95.75


## Edge, scénarios & sizing

- EV/risk : 0.061 | EV/share : $0.182 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 43 % | T2 24 % | T3 21 %
- Kelly (position) : f* 0.061 | ¼-Kelly 0.015 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 36.1 | bear 8.0 | side 56.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.577% → cible +2.348% / stop −3.0%, p_fill 82%, n_eff≈33.7) : P(cible|rempli) **40%** · **EV/risk -0.049** (×p_fill ; si rempli -0.18% du capital)
  - **swing** (entrée dip −1.257% → cible +5.251% / stop −2.626%, p_fill 84%, n_eff≈34.2) : P(cible|rempli) **45%** · **EV/risk +0.441** (×p_fill ; si rempli +1.38% du capital)
  - **deep** (entrée dip −1.949% → cible +7.426% / stop −3.713%, p_fill 75%, n_eff≈31.3) : P(cible|rempli) **46%** · **EV/risk +0.282** (×p_fill ; si rempli +1.40% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→88% · +1.0%→81% · +2.0%→55% · +3.0%→38% · +5.0%→21% · +8.0%→6%
- Range intraday médian 5.12% (p90 8.92%) · excursion haute méd. +2.16% / basse méd. −2.34%
- Profil de vol intra : ouverture 3.587% vs midi 1.099% vs clôture 1.068% _(ouverture ~3.3× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 21% · trend ↑1%/↓0% ; spike-down 68% · recovery-V 36%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; neutre — autocorr 0.014)_ ; drift intra méd. 0.272% ; recovery-V 36%
- **σ réalisé intraday** 3.91% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 64% / bas 45% / whipsaw 17%
- POC intraday (dernière séance, temps-au-prix) : 100.6536 (VA 99.9106–102.6969 ; dernier close 99.97)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 22% · rebond 80% · **stop −4.37%** sous le fill (sous le bruit) · cible +2.76% · R/R 0.63 (high win-rate)
- Gaps overnight (n=159) : méd. -0.08% · baisse 53% (gap-down >1% 35% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −0.76% (p90 −2.06%) · haut méd +0.93% · range méd 2.08%
- Excursion ouverture 15min (n=160) : bas méd −1.14% (p90 −3.33%) · haut méd +1.07% · range méd 2.82%
- Excursion ouverture 30min (n=160) : bas méd −1.37% (p90 −3.84%) · haut méd +1.44% · range méd 3.44%
- Excursion ouverture 60min (n=160) : bas méd −1.83% (p90 −3.9%) · haut méd +1.65% · range méd 3.9%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 99.97 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 70% · séance 79% (123/159) · gap 43% · délai 0.0min · rebond 57% (62/123) (MFE +1.49%)
   - −1.0% : fill 30min 60% · séance 68% (109/159) · gap 35% · délai 0.0min · rebond 60% (62/109) (MFE +1.32%)
   - −1.5% : fill 30min 51% · séance 62% (101/159) · gap 23% · délai 0.2min · rebond 54% (55/101) (MFE +1.36%)
   - −2.0% : fill 30min 44% · séance 55% (90/159) · gap 15% · délai 0.5min · rebond 66% (55/90) (MFE +1.35%)
   - −3.0% : fill 30min 32% · séance 42% (67/159) · gap 8% · délai 9.6min · rebond 73% (45/67) (MFE +1.92%)
   - −4.0% : fill 30min 20% · séance 33% (51/159) · gap 5% · délai 12.0min · rebond 79% (33/51) (MFE +2.32%)
   - −5.0% : fill 30min 11% · séance 22% (32/159) · gap 3% · délai 29.8min · rebond 80% (25/32) (MFE +2.76%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.59% (p90 −2.61%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.62% (p90 −2.53%) → stop au-delà de −1.81% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.58% (p90 −2.58%) → stop au-delà de −1.77% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=761 jambes) : jambe baissière méd −1.17% (p90 −2.8%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (72 séances) :
      · −1.0% : fill 96% (69/72) · rebond 57% (37/69)
      · −2.0% : fill 82% (58/72) · rebond 62% (34/58)
      · −3.0% : fill 67% (46/72) · rebond 70% (30/46)
      · −4.0% : fill 55% (37/72) · rebond 83% (26/37)
      · −5.0% : fill 39% (26/72) · rebond 77% (20/26)
   - **flat** (21 séances) :
      · −1.0% : fill 71% (16/21) · rebond 76% (11/16)
      · −2.0% : fill 54% (12/21) · rebond 59% (7/12)
      · −3.0% : fill 19% (6/21) · rebond 23% (2/6)
      · −4.0% : fill 17% (5/21) · rebond 16% (1/5)
      · −5.0% : fill 8% (3/21) · rebond 82% (2/3)
   - **gap-up** (66 séances) :
      · −1.0% : fill 36% (24/66) · rebond 61% (14/24)
      · −2.0% : fill 26% (20/66) · rebond 85% (14/20)
      · −3.0% : fill 21% (15/66) · rebond 96% (13/15)
      · −4.0% : fill 14% (9/66) · rebond 87% (6/9)
      · −5.0% : fill 7% (3/66) · rebond 100% (3/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 51% en base · 68% si les 15 1res min sont vertes (70 cas) · 37% si rouges (90 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **29min** → P(séance verte=clôture>ouverture) 78% si début vert vs 28% si rouge (base 51% · écart 50 pts) ; prédictivité sature ensuite (plafond brut 232min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=71) : tient le vert **78%** · continue >prix actuel 55% ; creux résiduel méd -1.73% (q20 -3.85%) → **SL/trailing à −3.85%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.65% / q75 +3.69% → **scale +1.65% / runner +3.69%**, sortie à la clôture
  - **si ROUGE au coude** (n=89) : edge inversé — récupère vert seulement **28%** (continue à baisser 48%) → **RÉDUIRE ~72%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.87%** (au-delà de la MAE q10 -3.87%), cible rebond +2.41% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.77% .. +4.49%] · haut q95 +5.05% · bas q05 -4.88%
   - 60min (n=160) : retour [-3.66% .. +4.33%] · haut q95 +6.32% · bas q05 -4.97%
   - 2h (n=160) : retour [-4.43% .. +6.39%] · haut q95 +7.59% · bas q05 -5.73%
   - 4h (n=160) : retour [-5.1% .. +6.84%] · haut q95 +8.39% · bas q05 -6.37%
   - 6h (n=160) : retour [-5.72% .. +6.74%] · haut q95 +8.4% · bas q05 -7.33%
   - session (n=160) : retour [-5.73% .. +6.8%] · haut q95 +8.7% · bas q05 -7.75%


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

- **Verdict timing** : neutre
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
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

- **RSI** : 47.6  _(neutre)_
- **ADX** : 25.4  _(tendance etablie)_
- **MACD** : hist -2.04  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 26.9%
- **ATR** : 6.84 (68.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.113  _(distribution)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 53.3  _(transition)_
- **MA** : MA20 106.85 · MA50 93.43 · MA200 101.53  _(prix < MA20)_
- **Dist MA** : MA20 -7.1% · MA50 +6.3% · MA200 -2.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (89226 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
