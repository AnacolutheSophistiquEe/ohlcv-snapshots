# 012450

**Generated** : 2026-09-10T00:28:49.105171+00:00  
**Santé technique** : 7/10 — **Rating** : Pass (negative EV)  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1047000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-11 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩1047000.00 (+0.3% vs entrée) · entrée ₩1043572.79 · stop ₩960086.97 · T1 ₩1062078.56 · R/R 0.22  
> ↳ P(T1 av. stop) 53 % _(réel 5 s)_ · EV/risk -0.1 _(réel 5 s)_ (GBM -0.106) · ¼-Kelly 0.039 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : up  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Pass (negative EV)'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1040145.58–₩1047000.00 (mid ₩1043572.79)
- Spot actuel : ₩1047000.00 (+0.3% au-dessus de la zone — repli à attendre)
- Stop : ₩960086.97 (stop swing_plan-based (-5.88%))
- Targets : T1 ₩1062078.56 · R/R 0.22 | T2 ₩1080584.34 · R/R 0.44 | T3 ₩1099090.11 · R/R 0.66
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩960086.97


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (5.88 %)** : le gap seul le franchit 0.411 % des séances (5 fois sur 1217).
   - exécution **3.081 pt plus bas** dans le cas TYPIQUE (médiane), 7.314 au p90, **7.339 au pire**
   - perte réelle **9.925 %** en moyenne _(tirée par la queue)_, jusqu'à **13.219 %** — au lieu des 5.88 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0166 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 5 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.81 % | p01 -3.828 % | pire -13.219 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.057** [0.0295 ; 0.0991] _(largeur 7.0 pt, n_eff 173.1)_
   - swing : **0.4028** [0.3521 ; 0.4551] _(largeur 10.3 pt, n_eff 345.6)_
   - deep : **0.4273** [0.3759 ; 0.4799] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.5 pt), swing (31.1 pt), deep (31.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1140 séances)** : VaR **-5.39 %** | CVaR **-7.3 %** | vol 3.65 %/j
   - _fenêtre arrêtée : rupture de regime a 1200 seances en arriere (volatilite 2.31 % contre 4.02 % aujourd'hui, rapport 0.57)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.3 % vs -12.01 % si l'on extrapolait par √5 _(rapport 0.858 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5227** (β de hausse 0.2925, asymétrie 1.7872) vs KS11 — 552 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.311× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.106 | EV/share : ₩-8840.335 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 33 % | T3 19 %
- Kelly (position) : f* 0.155 | ¼-Kelly 0.039 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 27.0 | bear 5.2 | side 67.8  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.326% → cible +1.773% / stop −8.0%, p_fill 90%, n_eff≈36.2) : P(cible|rempli) **53%** · **EV/risk -0.100** (×p_fill ; si rempli -0.89% du capital)
  - **swing** (entrée dip −0.545% → cible +3.965% / stop −5.364%, p_fill 90%, n_eff≈36.7) : P(cible|rempli) **56%** · **EV/risk -0.051** (×p_fill ; si rempli -0.30% du capital)
  - **deep** (entrée dip −0.758% → cible +5.608% / stop −8.063%, p_fill 91%, n_eff≈36.6) : P(cible|rempli) **52%** · **EV/risk -0.104** (×p_fill ; si rempli -0.92% du capital)
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
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-11 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-11 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-11 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 35.0  _(momentum baissier)_
- **ADX** : 10.3  _(pas de tendance nette)_
- **MACD** : hist -12823.287  _(pas de croisement recent)_
- **BB** : %B 0.24 · largeur 19.8%
- **ATR** : 55857.14 (29.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.143  _(distribution)_
- **Vol ratio** : 0.62  _(volume normal)_
- **Choppiness** : 60.4  _(transition)_
- **MA** : MA20 1103850.0 · MA50 1033500.0 · MA200 1154409.08  _(prix < MA20)_
- **Dist MA** : MA20 -5.2% · MA50 +1.3% · MA200 -9.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (482350 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
