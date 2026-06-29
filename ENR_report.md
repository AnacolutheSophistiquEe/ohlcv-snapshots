# ENR

**Generated** : 2026-06-29T21:40:30.716960+00:00  
**Santé technique** : 5/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · €157.06  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié  
> ↳ spot €157.06 (+8.1% vs entrée) · entrée €145.25 · stop €133.63 · T1 €148.07 · R/R 0.24  
> ↳ P(T1 av. stop) 49 % · EV/risk -0.021 · ¼-Kelly 0.081 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 5/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : €144.68–€145.81 (mid €145.25)
- Spot actuel : €157.06 (+8.1% au-dessus de la zone — repli à attendre)
- Stop : €133.63 (stop swing_plan-based (-18.36%))
- Targets : T1 €148.07 · R/R 0.24 | T2 €150.89 · R/R 0.49 | T3 €153.72 · R/R 0.73
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous €133.63


## Edge, scénarios & sizing

- EV/risk : -0.021 | EV/share : €-0.244 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 20 % | T3 10 %
- Kelly (position) : f* 0.325 | ¼-Kelly 0.081 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 13.0 | bear 56.3 | side 30.7  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 157.0 (= 1 part(s) × prix) · cible 288.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **swing** : indisponible (échantillon insuffisant (n=0, n_eff=0))
  - **deep** : indisponible (échantillon insuffisant (n=0, n_eff=0))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→75% · +1.0%→65% · +2.0%→49% · +3.0%→28% · +5.0%→10% · +8.0%→1%
- Range intraday médian 4.41% (p90 6.24%) · excursion haute méd. +1.69% / basse méd. −1.81%
- Profil de vol intra : ouverture 2.191% vs midi 1.017% vs clôture 1.217% _(ouverture ~2.2× plus volatile → privilégier/éviter selon le setup)_
- **Carte d'identité** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 14% · trend ↑0%/↓0% ; spike-down 58% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; neutre — autocorr -0.014)_ ; drift intra méd. -0.529% ; recovery-V 9%
- **σ réalisé intraday** 2.651% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 69% / whipsaw 30%
- POC intraday (dernière séance, temps-au-prix) : 157.6338 (VA 154.9363–158.0487 ; dernier close 154.42)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 75% · **stop −1.48%** sous le fill (sous le bruit) · cible +1.49% · R/R 1.01 (high win-rate)
- Gaps overnight (n=159) : méd. 0.44% · baisse 40% (gap-down >1% 22% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −0.62% (p90 −1.83%) · haut méd +0.47% · range méd 1.22%
- Excursion ouverture 15min (n=160) : bas méd −0.74% (p90 −2.21%) · haut méd +0.6% · range méd 1.53%
- Excursion ouverture 30min (n=160) : bas méd −0.93% (p90 −2.42%) · haut méd +0.63% · range méd 1.81%
- Excursion ouverture 60min (n=160) : bas méd −0.99% (p90 −2.57%) · haut méd +0.8% · range méd 2.01%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 154.42 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 56% · séance 72% (112/159) · gap 28% · délai 0.3min · rebond 48% (54/112) (MFE +0.92%)
   - −1.0% : fill 30min 48% · séance 66% (100/159) · gap 22% · délai 1.7min · rebond 52% (57/100) (MFE +1.05%)
   - −1.5% : fill 30min 36% · séance 60% (87/159) · gap 18% · délai 13.7min · rebond 60% (54/87) (MFE +1.44%)
   - −2.0% : fill 30min 24% · séance 44% (64/159) · gap 11% · délai 16.1min · rebond 58% (38/64) (MFE +1.18%)
   - −3.0% : fill 30min 18% · séance 36% (50/159) · gap 5% · délai 124.3min · rebond 70% (37/50) (MFE +1.6%)
   - −4.0% : fill 30min 9% · séance 27% (38/159) · gap 2% · délai 302.8min · rebond 64% (25/38) (MFE +1.66%)
   - −5.0% : fill 30min 2% · séance 18% (22/159) · gap 1% · délai 370.7min · rebond 75% (15/22) (MFE +1.49%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −2.07%) → stop au-delà de −1.02% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.58% (p90 −2.46%) → stop au-delà de −1.46% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.54% (p90 −1.54%) → stop au-delà de −0.91% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=506 jambes) : jambe baissière méd −1.08% (p90 −2.55%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (46 séances) :
      · −1.0% : fill 95% (45/46) · rebond 55% (25/45)
      · −2.0% : fill 70% (33/46) · rebond 65% (22/33)
      · −3.0% : fill 63% (29/46) · rebond 67% (21/29)
      · −4.0% : fill 52% (24/46) · rebond 61% (16/24)
      · −5.0% : fill 37% (16/46) · rebond 74% (11/16)
   - **flat** (27 séances) :
      · −1.0% : fill 62% (18/27) · rebond 55% (12/18)
      · −2.0% : fill 30% (8/27) · rebond 35% (3/8)
      · −3.0% : fill 23% (5/27) · rebond 80% (3/5)
      · −4.0% : fill 20% (4/27) · rebond 76% (2/4)
      · −5.0% : fill 12% (2/27) · rebond 74% (1/2)
   - **gap-up** (86 séances) :
      · −1.0% : fill 49% (37/86) · rebond 48% (20/37)
      · −2.0% : fill 32% (23/86) · rebond 56% (13/23)
      · −3.0% : fill 24% (16/86) · rebond 74% (13/16)
      · −4.0% : fill 14% (10/86) · rebond 67% (7/10)
      · −5.0% : fill 7% (4/86) · rebond 78% (3/4)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 47% en base · 85% si les 15 1res min sont vertes (79 cas) · 17% si rouges (81 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→306min, n=160) : COUDE à **17min** → P(séance verte=clôture>ouverture) 84% si début vert vs 21% si rouge (base 47% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 245min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=77) : tient le vert **84%** · continue >prix actuel 67% ; creux résiduel méd -1.19% (q20 -2.47%) → **SL/trailing à −2.47%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.04% / q75 +3.08% → **scale +2.04% / runner +3.08%**, sortie à la clôture
  - **si ROUGE au coude** (n=83) : edge inversé — récupère vert seulement **21%** (continue à baisser 64%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.05%** (au-delà de la MAE q10 -5.05%), cible rebond +1.25% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.26% .. +2.15%] · haut q95 +2.77% · bas q05 -2.76%
   - 60min (n=160) : retour [-2.44% .. +2.2%] · haut q95 +2.96% · bas q05 -3.29%
   - 2h (n=160) : retour [-3.15% .. +2.61%] · haut q95 +3.57% · bas q05 -3.75%
   - 4h (n=160) : retour [-3.05% .. +2.83%] · haut q95 +4.29% · bas q05 -3.9%
   - 6h (n=160) : retour [-3.23% .. +4.12%] · haut q95 +4.9% · bas q05 -4.49%
   - session (n=160) : retour [-5.02% .. +4.46%] · haut q95 +5.88% · bas q05 -6.08%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — ENR = **plat / peu volatil** (vol intra méd 2.46%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.64 · part idiosyncratique 0.36
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-07-02 — US Employment Situation (NFP / unemployment / earnings) (J-2 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 56.6  _(momentum haussier)_
- **ADX** : 18.1  _(pas de tendance nette)_
- **MACD** : hist 0.34  _(pas de croisement recent)_
- **BB** : %B 0.47 · largeur 19.1%
- **ATR** : 7.57 (74.0e pct 1a)  _(volatilite au-dessus de la moyenne (tiers haut))_
- **OBV/CMF** : OBV falling · CMF -0.102  _(distribution)_
- **Vol ratio** : 0.69  _(volume normal)_
- **Choppiness** : 41.5  _(transition)_
- **MA** : MA20 157.98 · MA50 168.28 · MA200 138.13  _(prix < MA20)_
- **Dist MA** : MA20 -0.6% · MA50 -6.7% · MA200 +13.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (90853 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
