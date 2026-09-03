# 012450

**Generated** : 2026-09-03T00:19:23.690805+00:00  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1025000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)  
> ↳ spot ₩1025000.00 (+7.9% vs entrée) · entrée ₩949684.26 · stop ₩885969.98 · T1 ₩993660.96 · R/R 0.69  
> ↳ P(T1 av. stop) 61 % _(réel 5 s)_ · EV/risk 0.037 _(réel 5 s)_ (GBM 0.012) · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 4/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩940888.92–₩958479.60 (mid ₩949684.26)
- Spot actuel : ₩1025000.00 (+7.9% au-dessus de la zone — repli à attendre)
- Stop : ₩885969.98 (stop swing_plan-based (-13.56%))
- Targets : T1 ₩993660.96 · R/R 0.69 | T2 ₩1037637.65 · R/R 1.38 | T3 ₩1081614.34 · R/R 2.07
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩885969.98


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (13.56 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 13.56 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.81 % | p01 -3.828 % | pire -13.219 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0648** [0.0351 ; 0.1088] _(largeur 7.4 pt, n_eff 173.1)_
   - swing : **0.3756** [0.3258 ; 0.4275] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.3225** [0.2749 ; 0.3731] _(largeur 9.8 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.9 pt), swing (48.2 pt), deep (52.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 1020 séances)** : VaR **-5.4 %** | CVaR **-7.32 %** | vol 3.74 %/j
   - _fenêtre arrêtée : rupture de regime a 1080 seances en arriere (volatilite 2.48 % contre 4.06 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.3 % vs -12.01 % si l'on extrapolait par √5 _(rapport 0.858 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5205** (β de hausse 0.3035, asymétrie 1.7148) vs KS11 — 553 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.308× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : 0.012 | EV/share : ₩744.838 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 58 % | T2 31 % | T3 19 %
- Kelly (position) : f* 0.035 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 26.7 | bear 68.3 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 160.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.337% → cible +2.071% / stop −8.0%, p_fill 42%, n_eff≈16.5) : P(cible|rempli) **43%** · **EV/risk -0.030** (×p_fill ; si rempli -0.57% du capital)
  - **swing** (entrée dip −7.344% → cible +4.631% / stop −6.709%, p_fill 28%, n_eff≈13.2) : P(cible|rempli) **61%** · **EV/risk +0.037** (×p_fill ; si rempli +0.89% du capital)
  - **deep** (entrée dip −11.356% → cible +6.549% / stop −10.519%, p_fill 22%, n_eff≈11.2) : P(cible|rempli) **49%** · **EV/risk -0.017** (×p_fill ; si rempli -0.80% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→80% · +1.0%→68% · +2.0%→45% · +3.0%→34% · +5.0%→19% · +8.0%→4%
- Range intraday médian 6.44% (p90 9.56%) · excursion haute méd. +1.91% / basse méd. −3.17%
- Profil de vol intra : ouverture 4.556% vs midi 1.238% vs clôture 1.331% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 77% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.124 ; mean-reverting — autocorr -0.048)_ ; drift intra méd. -0.698% ; recovery-V 32%
- **σ réalisé intraday** 4.133% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 49% / bas 53% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 1060762.5 (VA 1057212.5–1064312.5 ; dernier close 1060000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 35% · rebond 79% · **stop −4.37%** sous le fill (sous le bruit) · cible +1.9% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. 0.47% · baisse 33% (gap-down >1% 17% · >2% 6%)
- Excursion ouverture 5min (n=160) : bas méd −1.51% (p90 −4.05%) · haut méd +1.01% · range méd 2.9%
- Excursion ouverture 15min (n=160) : bas méd −1.94% (p90 −4.92%) · haut méd +1.09% · range méd 3.64%
- Excursion ouverture 30min (n=160) : bas méd −2.13% (p90 −5.3%) · haut méd +1.11% · range méd 4.09%
- Excursion ouverture 60min (n=160) : bas méd −2.19% (p90 −5.51%) · haut méd +1.29% · range méd 4.45%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1058000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 67% · séance 74% (119/159) · gap 24% · délai 0.0min · rebond 59% (65/119) (MFE +1.28%)
   - −1.0% : fill 30min 60% · séance 68% (108/159) · gap 17% · délai 0.3min · rebond 61% (60/108) (MFE +1.6%)
   - −1.5% : fill 30min 50% · séance 59% (96/159) · gap 13% · délai 0.9min · rebond 56% (52/96) (MFE +1.25%)
   - −2.0% : fill 30min 44% · séance 54% (86/159) · gap 6% · délai 1.9min · rebond 62% (52/86) (MFE +1.36%)
   - −3.0% : fill 30min 34% · séance 46% (66/159) · gap 3% · délai 11.6min · rebond 67% (42/66) (MFE +1.54%)
   - −4.0% : fill 30min 17% · séance 35% (51/159) · gap 1% · délai 28.1min · rebond 79% (39/51) (MFE +1.9%)
   - −5.0% : fill 30min 12% · séance 23% (36/159) · gap 1% · délai 8.9min · rebond 77% (30/36) (MFE +1.78%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.67% (p90 −2.26%) → stop au-delà de −2.02% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.7% (p90 −2.69%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.89% (p90 −2.74%) → stop au-delà de −2.41% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=788 jambes) : jambe baissière méd −1.19% (p90 −3.22%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (44 séances) :
      · −1.0% : fill 100% (44/44) · rebond 53% (19/44)
      · −2.0% : fill 86% (39/44) · rebond 55% (21/39)
      · −3.0% : fill 82% (36/44) · rebond 72% (24/36)
      · −4.0% : fill 61% (28/44) · rebond 77% (20/28)
      · −5.0% : fill 44% (22/44) · rebond 82% (19/22)
   - **flat** (26 séances) :
      · −1.0% : fill 72% (22/26) · rebond 80% (15/22)
      · −2.0% : fill 61% (19/26) · rebond 77% (12/19)
      · −3.0% : fill 40% (10/26) · rebond 47% (5/10)
      · −4.0% : fill 39% (9/26) · rebond 84% (7/9)
      · −5.0% : fill 23% (5/26) · rebond 32% (2/5)
   - **gap-up** (89 séances) :
      · −1.0% : fill 49% (42/89) · rebond 59% (26/42)
      · −2.0% : fill 34% (28/89) · rebond 61% (19/28)
      · −3.0% : fill 28% (20/89) · rebond 69% (13/20)
      · −4.0% : fill 20% (14/89) · rebond 79% (12/14)
      · −5.0% : fill 11% (9/89) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 69% si les 15 1res min sont vertes (55 cas) · 22% si rouges (105 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 82% si début vert vs 14% si rouge (base 40% · écart 68 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=54) : tient le vert **82%** · continue >prix actuel 50% ; creux résiduel méd -1.8% (q20 -3.0%) → **SL/trailing à −3.0%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.29% / q75 +3.88% → **scale +2.29% / runner +3.88%**, sortie à la clôture
  - **si ROUGE au coude** (n=106) : edge inversé — récupère vert seulement **14%** (continue à baisser 51%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.65%** (au-delà de la MAE q10 -5.65%), cible rebond +1.47% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.38% .. +3.71%] · haut q95 +5.21% · bas q05 -6.3%
   - 60min (n=160) : retour [-5.17% .. +4.45%] · haut q95 +6.32% · bas q05 -6.92%
   - 2h (n=160) : retour [-6.68% .. +4.98%] · haut q95 +7.06% · bas q05 -8.39%
   - 4h (n=160) : retour [-7.34% .. +5.77%] · haut q95 +7.81% · bas q05 -8.85%
   - 6h (n=160) : retour [-6.8% .. +5.8%] · haut q95 +8.08% · bas q05 -8.97%
   - session (n=160) : retour [-6.83% .. +5.72%] · haut q95 +8.08% · bas q05 -8.97%


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
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-10 — ECB Monetary Policy Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 34.8  _(momentum baissier)_
- **ADX** : 13.8  _(pas de tendance nette)_
- **MACD** : hist -12098.452  _(bearish_recent)_
- **BB** : %B 0.07 · largeur 18.4%
- **ATR** : 63714.29 (39.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.028  _(neutre)_
- **Vol ratio** : 0.51  _(volume atone)_
- **Choppiness** : 49.0  _(transition)_
- **MA** : MA20 1113500.0 · MA50 1034540.0 · MA200 1152061.62  _(prix < MA20)_
- **Dist MA** : MA20 -7.9% · MA50 -0.9% · MA200 -11.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (213282 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
