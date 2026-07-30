# SOFI

**Generated** : 2026-07-30T00:31:13.511573+00:00  
**Santé technique** : 2/10 — **Rating** : Strong Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · $15.25  

> ⛔ **STAND-DOWN** — EV/risque ≤ 0 — pas d'engagement statistiquement justifié (vérité terrain 5 s)  
> ↳ spot $15.25 (+0.3% vs entrée) · entrée $15.20 · stop $14.67 · T1 $15.48 · R/R 0.53  
> ↳ P(T1 av. stop) 35 % _(réel 5 s)_ · EV/risk -0.142 _(réel 5 s)_ (GBM -0.016) · ¼-Kelly 0.027 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −3.5% cohérent avec le bruit 5 s (EV-optimal ≈ −3.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal 207 % hors [0,100] (R² max 0.85). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 16.8 < 20 (tendance pas encore confirmée) alors que Choppiness 36.0 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Strong Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : $15.15–$15.25 (mid $15.20)
- Spot actuel : $15.25 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : $14.67 (stop swing_plan-based (-2.62%))
- Targets : T1 $15.48 · R/R 0.53 | T2 $15.76 · R/R 1.06 | T3 $16.04 · R/R 1.58
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous $14.67


## Edge, scénarios & sizing

- EV/risk : -0.016 | EV/share : $-0.009 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 50 % | T2 22 % | T3 10 %
- Kelly (position) : f* 0.11 | ¼-Kelly 0.027 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 19.1 | bear 29.0 | side 51.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.331% → cible +1.851% / stop −3.5%, p_fill 86%, n_eff≈35.0) : P(cible|rempli) **35%** · **EV/risk -0.142** (×p_fill ; si rempli -0.58% du capital)
  - **swing** (entrée dip −0.562% → cible +4.139% / stop −2.069%, p_fill 91%, n_eff≈36.7) : P(cible|rempli) **26%** · **EV/risk -0.266** (×p_fill ; si rempli -0.60% du capital)
  - **deep** (entrée dip −0.734% → cible +5.853% / stop −2.927%, p_fill 89%, n_eff≈36.4) : P(cible|rempli) **33%** · **EV/risk -0.068** (×p_fill ; si rempli -0.22% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→91% · +1.0%→69% · +2.0%→48% · +3.0%→35% · +5.0%→10% · +8.0%→0%
- Range intraday médian 4.39% (p90 6.91%) · excursion haute méd. +1.89% / basse méd. −2.18%
- Profil de vol intra : ouverture 3.064% vs midi 0.911% vs clôture 0.996% _(ouverture ~3.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 67% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.134 ; neutre — autocorr 0.001)_ ; drift intra méd. -0.247% ; recovery-V 25%
- **σ réalisé intraday** 2.883% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 54% / bas 61% / whipsaw 15%
- POC intraday (dernière séance, temps-au-prix) : 16.7244 (VA 16.5736–16.8081 ; dernier close 16.72)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−2.0%** sous le close veille · fill 51% · rebond 73% · **stop −2.96%** sous le fill (sous le bruit) · cible +1.89% · R/R 0.64 (high win-rate)
- Gaps overnight (n=159) : méd. 0.13% · baisse 47% (gap-down >1% 27% · >2% 10%)
- Excursion ouverture 5min (n=160) : bas méd −0.66% (p90 −1.66%) · haut méd +0.72% · range méd 1.68%
- Excursion ouverture 15min (n=160) : bas méd −1.07% (p90 −2.93%) · haut méd +0.96% · range méd 2.3%
- Excursion ouverture 30min (n=160) : bas méd −1.19% (p90 −3.25%) · haut méd +1.15% · range méd 2.82%
- Excursion ouverture 60min (n=160) : bas méd −1.48% (p90 −3.68%) · haut méd +1.3% · range méd 3.43%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 16.72 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 75% (122/159) · gap 34% · délai 0.0min · rebond 54% (65/122) (MFE +1.2%)
   - −1.0% : fill 30min 54% · séance 68% (111/159) · gap 27% · délai 0.5min · rebond 61% (69/111) (MFE +1.31%)
   - −1.5% : fill 30min 49% · séance 64% (101/159) · gap 18% · délai 7.2min · rebond 68% (65/101) (MFE +1.68%)
   - −2.0% : fill 30min 40% · séance 51% (75/159) · gap 10% · délai 3.3min · rebond 73% (52/75) (MFE +1.89%)
   - −3.0% : fill 30min 18% · séance 38% (56/159) · gap 2% · délai 31.4min · rebond 68% (39/56) (MFE +1.57%)
   - −4.0% : fill 30min 10% · séance 23% (38/159) · gap 1% · délai 45.3min · rebond 62% (25/38) (MFE +1.91%)
   - −5.0% : fill 30min 3% · séance 8% (17/159) · gap 1% · délai 56.3min · rebond 49% (10/17) (MFE +0.96%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.16%) → stop au-delà de −1.43% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.47% (p90 −1.93%) → stop au-delà de −1.44% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.41% (p90 −1.99%) → stop au-delà de −1.17% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=660 jambes) : jambe baissière méd −1.13% (p90 −2.77%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (66 séances) :
      · −1.0% : fill 97% (65/66) · rebond 63% (41/65)
      · −2.0% : fill 84% (53/66) · rebond 75% (39/53)
      · −3.0% : fill 69% (43/66) · rebond 78% (33/43)
      · −4.0% : fill 39% (28/66) · rebond 72% (21/28)
      · −5.0% : fill 17% (13/66) · rebond 47% (8/13)
   - **flat** (23 séances) :
      · −1.0% : fill 47% (13/23) · rebond 29% (6/13)
      · −2.0% : fill 30% (7/23) · rebond 37% (3/7)
      · −3.0% : fill 23% (5/23) · rebond 29% (2/5)
      · −4.0% : fill 16% (3/23) · rebond 67% (1/3)
      · −5.0% : fill 1% (1/23) · rebond 0% (0/1)
   - **gap-up** (70 séances) :
      · −1.0% : fill 48% (33/70) · rebond 67% (22/33)
      · −2.0% : fill 25% (15/70) · rebond 78% (10/15)
      · −3.0% : fill 13% (8/70) · rebond 39% (4/8)
      · −4.0% : fill 10% (7/70) · rebond 20% (3/7)
      · −5.0% : fill 2% (3/70) · rebond 70% (2/3)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 53% si les 15 1res min sont vertes (73 cas) · 32% si rouges (87 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **38min** → P(séance verte=clôture>ouverture) 76% si début vert vs 14% si rouge (base 42% · écart 61 pts) ; prédictivité sature ensuite (plafond brut 230min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=68) : tient le vert **76%** · continue >prix actuel 52% ; creux résiduel méd -1.56% (q20 -3.39%) → **SL/trailing à −3.39%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.72% / q75 +2.76% → **scale +1.72% / runner +2.76%**, sortie à la clôture
  - **si ROUGE au coude** (n=92) : edge inversé — récupère vert seulement **14%** (continue à baisser 60%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.29%** (au-delà de la MAE q10 -3.29%), cible rebond +1.14% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.93% .. +3.44%] · haut q95 +3.8% · bas q05 -3.52%
   - 60min (n=160) : retour [-3.15% .. +3.36%] · haut q95 +4.01% · bas q05 -3.99%
   - 2h (n=160) : retour [-3.58% .. +3.61%] · haut q95 +4.5% · bas q05 -4.75%
   - 4h (n=160) : retour [-3.91% .. +4.24%] · haut q95 +5.62% · bas q05 -5.08%
   - 6h (n=160) : retour [-4.62% .. +3.87%] · haut q95 +5.68% · bas q05 -5.09%
   - session (n=160) : retour [-4.55% .. +4.81%] · haut q95 +5.68% · bas q05 -5.29%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (4) pour des stats fiables : 2.5% des séances seulement sont des jours de hausse propre — SOFI = **volatil sans tendance propre (choppy)** (vol intra méd 2.9%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict sell_bias_strong
**Options** : favorable


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 24.6  _(survente)_
- **ADX** : 16.8  _(pas de tendance nette)_
- **MACD** : hist -0.256  _(pas de croisement recent)_
- **BB** : %B -0.13 · largeur 20.7%
- **ATR** : 0.9 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.165  _(distribution)_
- **Vol ratio** : 2.17  _(volume au-dessus de la moyenne)_
- **Choppiness** : 36.0  _(marche directionnel)_
- **MA** : MA20 17.55 · MA50 17.15 · MA200 21.41  _(prix < MA20)_
- **Dist MA** : MA20 -13.1% · MA50 -11.1% · MA200 -28.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (84565 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
