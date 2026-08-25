# 012450

**Generated** : 2026-08-25T22:59:38.288911+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1094000.00  

> 🟡 **WAIT-FOR-DIP** — spot +8.1 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩1094000.00 (+8.1% vs entrée) · entrée ₩1012291.12 · stop ₩942862.55 · T1 ₩1068593.92 · R/R 0.81  
> ↳ P(T1 av. stop) 59 % _(réel 5 s)_ · EV/risk 0.017 _(réel 5 s)_ (GBM 0.03) · ¼-Kelly 0.008 · _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1001030.55–₩1023551.68 (mid ₩1012291.12)
- Spot actuel : ₩1094000.00 (+8.1% au-dessus de la zone — repli à attendre)
- Stop : ₩942862.55 (stop swing_plan-based (-13.82%))
- Targets : T1 ₩1068593.92 · R/R 0.81 | T2 ₩1124896.73 · R/R 1.62 | T3 ₩1181199.54 · R/R 2.43
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩942862.55


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (13.82 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1218).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 13.82 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.81 % | p01 -3.827 % | pire -13.219 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0776** [0.0446 ; 0.1245] _(largeur 8.0 pt, n_eff 173.1)_
   - swing : **0.3748** [0.325 ; 0.4267] _(largeur 10.2 pt, n_eff 345.6)_
   - deep : **0.3219** [0.2743 ; 0.3725] _(largeur 9.8 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (44.2 pt), swing (47.3 pt), deep (47.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-5.52 %** | CVaR **-7.52 %** | vol 3.9 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.67 % contre 4.51 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.29 % vs -12.01 % si l'on extrapolait par √5 _(rapport 0.857 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5212** (β de hausse 0.2949, asymétrie 1.767) vs KS11 — 554 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.312× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : 0.03 | EV/share : ₩2074.492 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 52 % | T2 24 % | T3 16 %
- Kelly (position) : f* 0.03 | ¼-Kelly 0.008 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈209) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 23.4 | bear 71.6 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.391% → cible +2.487% / stop −8.0%, p_fill 40%, n_eff≈17.1) : P(cible|rempli) **45%** · **EV/risk -0.022** (×p_fill ; si rempli -0.44% du capital)
  - **swing** (entrée dip −7.474% → cible +5.562% / stop −6.859%, p_fill 28%, n_eff≈14.1) : P(cible|rempli) **59%** · **EV/risk +0.017** (×p_fill ; si rempli +0.40% du capital)
  - **deep** (entrée dip −11.54% → cible +7.866% / stop −10.762%, p_fill 24%, n_eff≈14.2) : P(cible|rempli) **55%** · **EV/risk -0.002** (×p_fill ; si rempli -0.10% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→65% · +2.0%→45% · +3.0%→31% · +5.0%→19% · +8.0%→4%
- Range intraday médian 6.4% (p90 9.56%) · excursion haute méd. +1.91% / basse méd. −3.17%
- Profil de vol intra : ouverture 4.565% vs midi 1.248% vs clôture 1.311% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 16% · trend ↑0%/↓0% ; spike-down 80% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.125 ; mean-reverting — autocorr -0.035)_ ; drift intra méd. -0.568% ; recovery-V 31%
- **σ réalisé intraday** 4.576% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 51% / bas 50% / whipsaw 13%
- POC intraday (dernière séance, temps-au-prix) : 1089375.0 (VA 1084425.0–1094325.0 ; dernier close 1085000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 24% · rebond 84% · **stop −5.33%** sous le fill (sous le bruit) · cible +1.88% · R/R 0.35 (high win-rate)
- Gaps overnight (n=159) : méd. 0.55% · baisse 33% (gap-down >1% 19% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −1.6% (p90 −4.06%) · haut méd +0.98% · range méd 2.97%
- Excursion ouverture 15min (n=160) : bas méd −2.02% (p90 −5.04%) · haut méd +1.23% · range méd 3.69%
- Excursion ouverture 30min (n=160) : bas méd −2.14% (p90 −5.69%) · haut méd +1.28% · range méd 4.18%
- Excursion ouverture 60min (n=160) : bas méd −2.3% (p90 −5.79%) · haut méd +1.48% · range méd 4.56%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1085000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 74% (119/159) · gap 26% · délai 0.1min · rebond 59% (65/119) (MFE +1.36%)
   - −1.0% : fill 30min 58% · séance 68% (107/159) · gap 19% · délai 0.3min · rebond 58% (58/107) (MFE +1.55%)
   - −1.5% : fill 30min 49% · séance 58% (95/159) · gap 14% · délai 0.9min · rebond 54% (51/95) (MFE +1.25%)
   - −2.0% : fill 30min 43% · séance 54% (85/159) · gap 7% · délai 1.9min · rebond 60% (51/85) (MFE +1.36%)
   - −3.0% : fill 30min 33% · séance 44% (62/159) · gap 4% · délai 4.8min · rebond 70% (40/62) (MFE +1.54%)
   - −4.0% : fill 30min 20% · séance 34% (48/159) · gap 1% · délai 8.4min · rebond 75% (36/48) (MFE +2.12%)
   - −5.0% : fill 30min 14% · séance 24% (35/159) · gap 1% · délai 8.6min · rebond 84% (30/35) (MFE +1.88%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −2.2%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.64% (p90 −2.79%) → stop au-delà de −2.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.71% (p90 −2.83%) → stop au-delà de −2.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=791 jambes) : jambe baissière méd −1.19% (p90 −3.22%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 100% (42/42) · rebond 47% (17/42)
      · −2.0% : fill 90% (38/42) · rebond 52% (20/38)
      · −3.0% : fill 87% (35/42) · rebond 69% (23/35)
      · −4.0% : fill 69% (28/42) · rebond 77% (20/28)
      · −5.0% : fill 50% (22/42) · rebond 82% (19/22)
   - **flat** (25 séances) :
      · −1.0% : fill 66% (21/25) · rebond 72% (13/21)
      · −2.0% : fill 52% (18/25) · rebond 67% (11/18)
      · −3.0% : fill 26% (8/25) · rebond 45% (4/8)
      · −4.0% : fill 24% (7/25) · rebond 68% (5/7)
      · −5.0% : fill 17% (4/25) · rebond 55% (2/4)
   - **gap-up** (92 séances) :
      · −1.0% : fill 51% (44/92) · rebond 64% (28/44)
      · −2.0% : fill 34% (29/92) · rebond 68% (20/29)
      · −3.0% : fill 27% (19/92) · rebond 78% (13/19)
      · −4.0% : fill 18% (13/92) · rebond 74% (11/13)
      · −5.0% : fill 12% (9/92) · rebond 100% (9/9)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 42% en base · 76% si les 15 1res min sont vertes (55 cas) · 18% si rouges (105 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **35min** → P(séance verte=clôture>ouverture) 87% si début vert vs 9% si rouge (base 42% · écart 78 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=56) : tient le vert **87%** · continue >prix actuel 54% ; creux résiduel méd -1.6% (q20 -3.21%) → **SL/trailing à −3.21%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.71% / q75 +4.3% → **scale +2.71% / runner +4.3%**, sortie à la clôture
  - **si ROUGE au coude** (n=104) : edge inversé — récupère vert seulement **9%** (continue à baisser 49%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.75%** (au-delà de la MAE q10 -5.75%), cible rebond +1.88% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.66% .. +3.83%] · haut q95 +5.43% · bas q05 -6.83%
   - 60min (n=160) : retour [-5.23% .. +4.71%] · haut q95 +6.74% · bas q05 -7.21%
   - 2h (n=160) : retour [-6.8% .. +6.07%] · haut q95 +7.16% · bas q05 -8.41%
   - 4h (n=160) : retour [-7.36% .. +5.88%] · haut q95 +7.85% · bas q05 -8.86%
   - 6h (n=160) : retour [-6.81% .. +6.18%] · haut q95 +8.46% · bas q05 -9.1%
   - session (n=160) : retour [-6.92% .. +6.25%] · haut q95 +8.46% · bas q05 -9.1%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.58%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


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
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 59.3  _(momentum haussier)_
- **ADX** : 16.7  _(pas de tendance nette)_
- **MACD** : hist 3002.094  _(pas de croisement recent)_
- **BB** : %B 0.59 · largeur 44.6%
- **ATR** : 69428.57 (50.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.009  _(neutre)_
- **Vol ratio** : 0.41  _(volume atone)_
- **Choppiness** : 50.4  _(transition)_
- **MA** : MA20 1053650.0 · MA50 1041340.0 · MA200 1148260.31  _(prix > MA20)_
- **Dist MA** : MA20 +3.8% · MA50 +5.1% · MA200 -4.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (534365 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
