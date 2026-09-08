# 012450

**Generated** : 2026-09-08T00:29:18.974460+00:00  
**Santé technique** : 6/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1039000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)  
> ↳ spot ₩1039000.00 (+3.8% vs entrée) · entrée ₩1001265.57 · stop ₩921164.33 · T1 ₩1020790.04 · R/R 0.24  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk -0.021 _(réel 5 s)_ (GBM -0.11) · ¼-Kelly 0.033 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩997360.68–₩1005170.47 (mid ₩1001265.57)
- Spot actuel : ₩1039000.00 (+3.8% au-dessus de la zone — repli à attendre)
- Stop : ₩921164.33 (stop swing_plan-based (-14.01%))
- Targets : T1 ₩1020790.04 · R/R 0.24 | T2 ₩1040314.50 · R/R 0.49 | T3 ₩1059838.96 · R/R 0.73
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩921164.33


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (14.01 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 14.01 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.81 % | p01 -3.828 % | pire -13.219 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0626** [0.0335 ; 0.1061] _(largeur 7.3 pt, n_eff 173.1)_
   - swing : **0.3729** [0.3231 ; 0.4248] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.322** [0.2744 ; 0.3726] _(largeur 9.8 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 16.0 observations effectives », dont la borne haute a 95 % vaut environ 18.8 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.8 pt), swing (51.7 pt), deep (47.4 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1140 séances)** : VaR **-5.39 %** | CVaR **-7.3 %** | vol 3.65 %/j
   - _fenêtre arrêtée : rupture de regime a 1200 seances en arriere (volatilite 2.33 % contre 4.04 % aujourd'hui, rapport 0.58)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.3 % vs -12.01 % si l'on extrapolait par √5 _(rapport 0.858 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5236** (β de hausse 0.3024, asymétrie 1.7317) vs KS11 — 552 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.312× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.11 | EV/share : ₩-8825.112 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 48 % | T2 29 % | T3 19 %
- Kelly (position) : f* 0.132 | ¼-Kelly 0.033 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 16.7 | bear 6.4 | side 77.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.63% → cible +1.95% / stop −8.0%, p_fill 36%, n_eff≈16.0) : P(cible|rempli) **40%** · **EV/risk -0.021** (×p_fill ; si rempli -0.47% du capital)
  - **swing** (entrée dip −7.988% → cible +4.36% / stop −6.545%, p_fill 28%, n_eff≈11.8) : P(cible|rempli) **49%** · **EV/risk +0.017** (×p_fill ; si rempli +0.39% du capital)
  - **deep** (entrée dip −12.346% → cible +6.166% / stop −10.306%, p_fill 18%, n_eff≈10.1) : P(cible|rempli) **77%** · **EV/risk +0.041** (×p_fill ; si rempli +2.29% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→68% · +2.0%→46% · +3.0%→35% · +5.0%→19% · +8.0%→4%
- Range intraday médian 6.4% (p90 9.56%) · excursion haute méd. +1.92% / basse méd. −3.01%
- Profil de vol intra : ouverture 4.469% vs midi 1.242% vs clôture 1.324% _(ouverture ~3.6× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 85% · range 15% · trend ↑0%/↓0% ; spike-down 78% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.118 ; mean-reverting — autocorr -0.044)_ ; drift intra méd. -0.645% ; recovery-V 33%
- **σ réalisé intraday** 3.92% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 55% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 1044912.5 (VA 1043362.5–1050337.5 ; dernier close 1056000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 35% · rebond 80% · **stop −4.3%** sous le fill (sous le bruit) · cible +1.74% · R/R 0.4 (high win-rate)
- Gaps overnight (n=159) : méd. 0.55% · baisse 33% (gap-down >1% 16% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −1.42% (p90 −4.05%) · haut méd +0.95% · range méd 2.83%
- Excursion ouverture 15min (n=160) : bas méd −1.89% (p90 −4.88%) · haut méd +1.08% · range méd 3.63%
- Excursion ouverture 30min (n=160) : bas méd −2.1% (p90 −5.22%) · haut méd +1.08% · range méd 3.95%
- Excursion ouverture 60min (n=160) : bas méd −2.17% (p90 −5.42%) · haut méd +1.29% · range méd 4.26%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1055000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 75% (119/159) · gap 25% · délai 0.0min · rebond 60% (66/119) (MFE +1.37%)
   - −1.0% : fill 30min 60% · séance 70% (108/159) · gap 16% · délai 0.3min · rebond 61% (60/108) (MFE +1.62%)
   - −1.5% : fill 30min 49% · séance 57% (94/159) · gap 12% · délai 0.7min · rebond 57% (50/94) (MFE +1.25%)
   - −2.0% : fill 30min 43% · séance 53% (84/159) · gap 6% · délai 2.3min · rebond 63% (50/84) (MFE +1.36%)
   - −3.0% : fill 30min 32% · séance 46% (65/159) · gap 3% · délai 12.5min · rebond 64% (40/65) (MFE +1.47%)
   - −4.0% : fill 30min 16% · séance 35% (51/159) · gap 1% · délai 35.1min · rebond 80% (39/51) (MFE +1.74%)
   - −5.0% : fill 30min 12% · séance 22% (36/159) · gap 1% · délai 8.9min · rebond 77% (30/36) (MFE +1.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.74% (p90 −2.26%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.79% (p90 −2.69%) → stop au-delà de −2.28% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.02% (p90 −2.69%) → stop au-delà de −2.44% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=782 jambes) : jambe baissière méd −1.19% (p90 −3.22%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (43 séances) :
      · −1.0% : fill 100% (43/43) · rebond 50% (18/43)
      · −2.0% : fill 86% (38/43) · rebond 58% (20/38)
      · −3.0% : fill 83% (35/43) · rebond 66% (22/35)
      · −4.0% : fill 63% (28/43) · rebond 79% (20/28)
      · −5.0% : fill 42% (22/43) · rebond 82% (19/22)
   - **flat** (25 séances) :
      · −1.0% : fill 72% (21/25) · rebond 80% (14/21)
      · −2.0% : fill 61% (18/25) · rebond 77% (11/18)
      · −3.0% : fill 40% (10/25) · rebond 47% (5/10)
      · −4.0% : fill 39% (9/25) · rebond 84% (7/9)
      · −5.0% : fill 24% (5/25) · rebond 32% (2/5)
   - **gap-up** (91 séances) :
      · −1.0% : fill 53% (44/91) · rebond 65% (28/44)
      · −2.0% : fill 32% (28/91) · rebond 61% (19/28)
      · −3.0% : fill 26% (20/91) · rebond 69% (13/20)
      · −4.0% : fill 19% (14/91) · rebond 79% (12/14)
      · −5.0% : fill 10% (9/91) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 69% si les 15 1res min sont vertes (55 cas) · 22% si rouges (105 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 82% si début vert vs 16% si rouge (base 40% · écart 67 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=53) : tient le vert **82%** · continue >prix actuel 50% ; creux résiduel méd -1.81% (q20 -3.0%) → **SL/trailing à −3.0%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.3% / q75 +3.88% → **scale +2.3% / runner +3.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=107) : edge inversé — récupère vert seulement **16%** (continue à baisser 49%) → **RÉDUIRE ~84%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.6%** (au-delà de la MAE q10 -5.6%), cible rebond +1.48% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.25% .. +3.69%] · haut q95 +5.04% · bas q05 -6.3%
   - 60min (n=160) : retour [-5.14% .. +4.23%] · haut q95 +6.05% · bas q05 -6.65%
   - 2h (n=160) : retour [-6.67% .. +4.71%] · haut q95 +7.01% · bas q05 -8.38%
   - 4h (n=160) : retour [-7.34% .. +5.72%] · haut q95 +7.55% · bas q05 -8.66%
   - 6h (n=160) : retour [-6.78% .. +5.63%] · haut q95 +7.9% · bas q05 -8.91%
   - session (n=160) : retour [-6.79% .. +5.55%] · haut q95 +7.9% · bas q05 -8.91%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.54%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.9  _(momentum baissier)_
- **ADX** : 11.5  _(pas de tendance nette)_
- **MACD** : hist -13960.608  _(pas de croisement recent)_
- **BB** : %B 0.13 · largeur 18.1%
- **ATR** : 62571.43 (36.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.108  _(distribution)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 48.3  _(transition)_
- **MA** : MA20 1112650.0 · MA50 1032640.0 · MA200 1153517.2  _(prix < MA20)_
- **Dist MA** : MA20 -6.6% · MA50 +0.6% · MA200 -9.9%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (483236 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
