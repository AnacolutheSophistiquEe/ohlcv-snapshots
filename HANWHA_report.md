# 012450

**Generated** : 2026-08-25T00:19:12.102251+00:00  
**Santé technique** : 7/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1105000.00  

> 🟡 **WAIT-FOR-DIP** — spot +8.6 % au-dessus de la zone d'entrée — attendre le repli  
> ↳ spot ₩1105000.00 (+8.6% vs entrée) · entrée ₩1017241.12 · stop ₩943526.83 · T1 ₩1079576.24 · R/R 0.85  
> ↳ P(T1 av. stop) 59 % _(réel 5 s)_ · EV/risk 0.02 _(réel 5 s)_ (GBM 0.032) · ¼-Kelly 0.009 · _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie B (swing), composite 7/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan B — swing** (order_type LMT)
- Entry (zone de repli) : ₩1004774.09–₩1029708.14 (mid ₩1017241.12)
- Spot actuel : ₩1105000.00 (+8.6% au-dessus de la zone — repli à attendre)
- Stop : ₩943526.83 (stop swing_plan-based (-14.61%))
- Targets : T1 ₩1079576.24 · R/R 0.85 | T2 ₩1141911.37 · R/R 1.69 | T3 ₩1204246.49 · R/R 2.54
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩943526.83


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (14.61 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 14.61 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.81 % | p01 -3.828 % | pire -13.219 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.2478** [0.188 ; 0.3159] _(largeur 12.8 pt, n_eff 173.1)_
   - swing : **0.4732** [0.421 ; 0.5259] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.5209** [0.4682 ; 0.5732] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 16.5 observations effectives », dont la borne haute a 95 % vaut environ 18.2 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (43.8 pt), swing (49.4 pt), deep (50.1 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 780 séances)** : VaR **-5.52 %** | CVaR **-7.52 %** | vol 3.9 %/j
   - _fenêtre arrêtée : rupture de regime a 840 seances en arriere (volatilite 2.66 % contre 4.51 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.3 % vs -12.01 % si l'on extrapolait par √5 _(rapport 0.858 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5263** (β de hausse 0.2949, asymétrie 1.7845) vs KS11 — 553 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.312× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : 0.032 | EV/share : ₩2329.967 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 49 % | T2 21 % | T3 12 %
- Kelly (position) : f* 0.035 | ¼-Kelly 0.009 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage empirique daily (historique réel, n≈208) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, swing) : bull 21.5 | bear 73.5 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 512.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.609% → cible +2.74% / stop −8.0%, p_fill 40%, n_eff≈16.5) : P(cible|rempli) **38%** · **EV/risk -0.018** (×p_fill ; si rempli -0.36% du capital)
  - **swing** (entrée dip −7.939% → cible +6.128% / stop −7.246%, p_fill 27%, n_eff≈12.7) : P(cible|rempli) **59%** · **EV/risk +0.020** (×p_fill ; si rempli +0.53% du capital)
  - **deep** (entrée dip −12.273% → cible +8.666% / stop −11.406%, p_fill 23%, n_eff≈12.6) : P(cible|rempli) **55%** · **EV/risk +0.013** (×p_fill ; si rempli +0.65% du capital)
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
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 24% · rebond 74% · **stop −5.09%** sous le fill (sous le bruit) · cible +2.18% · R/R 0.43 (high win-rate)
- Gaps overnight (n=159) : méd. 0.61% · baisse 34% (gap-down >1% 20% · >2% 11%)
- Excursion ouverture 5min (n=160) : bas méd −1.6% (p90 −4.06%) · haut méd +0.98% · range méd 2.97%
- Excursion ouverture 15min (n=160) : bas méd −2.02% (p90 −5.04%) · haut méd +1.23% · range méd 3.69%
- Excursion ouverture 30min (n=160) : bas méd −2.14% (p90 −5.69%) · haut méd +1.28% · range méd 4.18%
- Excursion ouverture 60min (n=160) : bas méd −2.3% (p90 −5.79%) · haut méd +1.48% · range méd 4.56%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1085000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 62% · séance 70% (114/159) · gap 22% · délai 0.1min · rebond 52% (58/114) (MFE +1.09%)
   - −1.0% : fill 30min 56% · séance 66% (109/159) · gap 20% · délai 0.8min · rebond 56% (64/109) (MFE +1.01%)
   - −1.5% : fill 30min 51% · séance 60% (100/159) · gap 13% · délai 1.3min · rebond 59% (57/100) (MFE +1.26%)
   - −2.0% : fill 30min 44% · séance 53% (83/159) · gap 11% · délai 3.5min · rebond 64% (51/83) (MFE +1.58%)
   - −3.0% : fill 30min 30% · séance 44% (62/159) · gap 4% · délai 4.3min · rebond 73% (43/62) (MFE +1.83%)
   - −4.0% : fill 30min 19% · séance 33% (47/159) · gap 1% · délai 14.7min · rebond 74% (37/47) (MFE +1.98%)
   - −5.0% : fill 30min 13% · séance 24% (34/159) · gap 1% · délai 7.8min · rebond 74% (27/34) (MFE +2.18%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.57% (p90 −2.2%) → stop au-delà de −2.04% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.64% (p90 −2.79%) → stop au-delà de −2.61% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.71% (p90 −2.83%) → stop au-delà de −2.63% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=791 jambes) : jambe baissière méd −1.19% (p90 −3.22%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (38 séances) :
      · −1.0% : fill 89% (36/38) · rebond 46% (16/36)
      · −2.0% : fill 84% (33/38) · rebond 59% (19/33)
      · −3.0% : fill 82% (30/38) · rebond 72% (21/30)
      · −4.0% : fill 66% (26/38) · rebond 81% (21/26)
      · −5.0% : fill 41% (17/38) · rebond 73% (14/17)
   - **flat** (20 séances) :
      · −1.0% : fill 90% (19/20) · rebond 49% (10/19)
      · −2.0% : fill 69% (15/20) · rebond 48% (7/15)
      · −3.0% : fill 53% (9/20) · rebond 37% (3/9)
      · −4.0% : fill 53% (9/20) · rebond 48% (5/9)
      · −5.0% : fill 51% (8/20) · rebond 52% (4/8)
   - **gap-up** (101 séances) :
      · −1.0% : fill 51% (54/101) · rebond 68% (38/54)
      · −2.0% : fill 36% (35/101) · rebond 76% (25/35)
      · −3.0% : fill 26% (23/101) · rebond 89% (19/23)
      · −4.0% : fill 13% (12/101) · rebond 80% (11/12)
      · −5.0% : fill 10% (9/101) · rebond 100% (9/9)
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

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
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

- **RSI** : 66.7  _(momentum haussier)_
- **ADX** : 17.1  _(pas de tendance nette)_
- **MACD** : hist 7690.608  _(pas de croisement recent)_
- **BB** : %B 0.63 · largeur 46.8%
- **ATR** : 73714.29 (59.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV rising · CMF 0.003  _(neutre)_
- **Vol ratio** : 0.4  _(volume atone)_
- **Choppiness** : 41.0  _(transition)_
- **MA** : MA20 1043900.0 · MA50 1041020.0 · MA200 1147720.32  _(prix > MA20)_
- **Dist MA** : MA20 +5.9% · MA50 +6.1% · MA200 -3.7%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (741156 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
