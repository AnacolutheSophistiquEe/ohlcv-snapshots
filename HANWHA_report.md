# 012450

**Generated** : 2026-10-01T21:58:28.637131+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 7/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩1034000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)  
> ↳ spot ₩1034000.00 (+2.4% vs entrée) · entrée ₩1009875.55 · stop ₩929085.51 · T1 ₩1033982.69 · R/R 0.3  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 7/10, conviction 'Unknown'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩1006810.64–₩1012940.46 (mid ₩1009875.55)
- Spot actuel : ₩1034000.00 (+2.4% au-dessus de la zone — repli à attendre)
- Stop : ₩929085.51 (plancher anti-bruit 5 s — stop EV-optimal −8% (first-passage 5 s réel) ; -8.00 % depuis l'entree)
- Targets : T1 ₩1033982.69 · R/R 0.3 | T2 ₩1058089.84 · R/R 0.6 | T3 ₩1082196.98 · R/R 0.9
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩929085.51


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.8 %)** : le gap seul le franchit 0.164 % des séances (2 fois sur 1219).
   - exécution **3.388 pt plus bas** dans le cas TYPIQUE (médiane), 3.413 au p90, **3.419 au pire**
   - perte réelle **13.188 %** en moyenne _(tirée par la queue)_, jusqu'à **13.219 %** — au lieu des 9.8 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0056 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.81 % | p01 -3.826 % | pire -13.219 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0581** [0.0303 ; 0.1005] _(largeur 7.0 pt, n_eff 173.1)_
   - swing : **0.4659** [0.4138 ; 0.5186] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.5084** [0.4558 ; 0.5609] _(largeur 10.5 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : swing (28.7 pt), deep (29.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 720 séances)** : VaR **-5.93 %** | CVaR **-7.65 %** | vol 3.96 %/j
   - _fenêtre arrêtée : rupture de regime a 780 seances en arriere (volatilite 2.35 % contre 3.93 % aujourd'hui, rapport 0.60)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.29 % vs -12.04 % si l'on extrapolait par √5 _(rapport 0.855 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5104** (β de hausse 0.2908, asymétrie 1.7549) vs KS11 — 554 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.252× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.088 | EV/share : ₩-7139.920 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 39 % | T2 14 % | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 11.1 | bear 5.0 | side 83.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.337% → cible +2.387% / stop −8.0%, p_fill 53%, n_eff≈59.9) : P(cible|rempli) **34%** · **EV/risk -0.034** (×p_fill ; si rempli -0.51% du capital)
  - **swing** (entrée dip −5.137% → cible +5.495% / stop −4.915%, p_fill 36%, n_eff≈43.0) : P(cible|rempli) **37%** · **EV/risk -0.080** (×p_fill ; si rempli -1.09% du capital)
  - **deep** (entrée dip −7.936% → cible +8.008% / stop −7.597%, p_fill 36%, n_eff≈41.2) : P(cible|rempli) **43%** · **EV/risk -0.024** (×p_fill ; si rempli -0.51% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→65% · +2.0%→44% · +3.0%→30% · +5.0%→14% · +8.0%→3%
- Range intraday médian 5.58% (p90 8.69%) · excursion haute méd. +1.85% / basse méd. −2.69%
- Profil de vol intra : ouverture 3.977% vs midi 1.046% vs clôture 1.119% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 18% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 28%)_
- **Régime intraday** : **chop** _(efficiency 0.154 ; mean-reverting — autocorr -0.066)_ ; drift intra méd. -0.736% ; recovery-V 22%
- **σ réalisé intraday** 3.248% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 52% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 1010900.0 (VA 1009100.0–1022300.0 ; dernier close 1007000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 18% · rebond 78% · **stop −4.72%** sous le fill (sous le bruit) · cible +1.64% · R/R 0.35 (high win-rate)
- Gaps overnight (n=152) : méd. 0.51% · baisse 26% (gap-down >1% 11% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −1.26% (p90 −3.61%) · haut méd +0.82% · range méd 2.45%
- Excursion ouverture 15min (n=160) : bas méd −1.57% (p90 −4.21%) · haut méd +1.08% · range méd 3.25%
- Excursion ouverture 30min (n=160) : bas méd −1.97% (p90 −4.62%) · haut méd +1.09% · range méd 3.65%
- Excursion ouverture 60min (n=160) : bas méd −2.06% (p90 −5.0%) · haut méd +1.28% · range méd 4.19%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1007000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 77% (116/152) · gap 18% · délai 0.2min · rebond 58% (61/116) (MFE +1.2%)
   - −1.0% : fill 30min 55% · séance 68% (103/152) · gap 11% · délai 1.4min · rebond 54% (51/103) (MFE +1.11%)
   - −1.5% : fill 30min 42% · séance 53% (86/152) · gap 9% · délai 1.5min · rebond 47% (39/86) (MFE +0.97%)
   - −2.0% : fill 30min 34% · séance 47% (79/152) · gap 5% · délai 4.5min · rebond 59% (43/79) (MFE +1.14%)
   - −3.0% : fill 30min 25% · séance 39% (63/152) · gap 1% · délai 17.3min · rebond 63% (38/63) (MFE +1.33%)
   - −4.0% : fill 30min 14% · séance 28% (49/152) · gap 1% · délai 23.1min · rebond 73% (35/49) (MFE +1.61%)
   - −5.0% : fill 30min 10% · séance 18% (35/152) · gap 1% · délai 8.8min · rebond 78% (29/35) (MFE +1.64%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.73% (p90 −2.21%) → stop au-delà de −1.91% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.83% (p90 −2.63%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.82% (p90 −2.66%) → stop au-delà de −1.97% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=765 jambes) : jambe baissière méd −1.19% (p90 −3.22%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (38 séances) :
      · −1.0% : fill 100% (38/38) · rebond 40% (13/38)
      · −2.0% : fill 87% (34/38) · rebond 56% (16/34)
      · −3.0% : fill 85% (32/38) · rebond 66% (19/32)
      · −4.0% : fill 70% (27/38) · rebond 66% (17/27)
      · −5.0% : fill 50% (22/38) · rebond 84% (19/22)
   - **flat** (29 séances) :
      · −1.0% : fill 83% (25/29) · rebond 78% (17/25)
      · −2.0% : fill 54% (19/29) · rebond 52% (10/19)
      · −3.0% : fill 42% (12/29) · rebond 48% (6/12)
      · −4.0% : fill 24% (9/29) · rebond 84% (7/9)
      · −5.0% : fill 15% (5/29) · rebond 32% (2/5)
   - **gap-up** (85 séances) :
      · −1.0% : fill 50% (40/85) · rebond 47% (21/40)
      · −2.0% : fill 29% (26/85) · rebond 67% (17/26)
      · −3.0% : fill 20% (19/85) · rebond 69% (13/19)
      · −4.0% : fill 14% (13/85) · rebond 79% (11/13)
      · −5.0% : fill 8% (8/85) · rebond 100% (8/8)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 77% si les 15 1res min sont vertes (55 cas) · 17% si rouges (105 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **49min** → P(séance verte=clôture>ouverture) 86% si début vert vs 14% si rouge (base 38% · écart 72 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=54) : tient le vert **86%** · continue >prix actuel 50% ; creux résiduel méd -1.41% (q20 -2.9%) → **SL/trailing à −2.9%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +2.14% / q75 +3.61% → **scale +2.14% / runner +3.61%**, sortie à la clôture
  - **si ROUGE au coude** (n=106) : edge inversé — récupère vert seulement **14%** (continue à baisser 61%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.95%** (au-delà de la MAE q10 -4.95%), cible rebond +1.22% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.75% .. +3.5%] · haut q95 +4.39% · bas q05 -5.98%
   - 60min (n=160) : retour [-4.93% .. +3.57%] · haut q95 +5.57% · bas q05 -6.09%
   - 2h (n=160) : retour [-5.69% .. +3.58%] · haut q95 +6.69% · bas q05 -8.12%
   - 4h (n=160) : retour [-6.78% .. +5.29%] · haut q95 +7.05% · bas q05 -8.37%
   - 6h (n=160) : retour [-6.64% .. +5.04%] · haut q95 +7.08% · bas q05 -8.4%
   - session (n=160) : retour [-6.48% .. +4.94%] · haut q95 +7.08% · bas q05 -8.4%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.48%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : neutre
- Proximité zone : 0.5/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.13 · part idiosyncratique 0.87
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-02 — US Employment Situation (NFP / unemployment / earnings) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 48.2  _(neutre)_
- **ADX** : 9.1  _(pas de tendance nette)_
- **MACD** : hist -6698.661  _(pas de croisement recent)_
- **BB** : %B 0.35 · largeur 11.8%
- **ATR** : 48214.29 (18.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.17  _(distribution)_
- **Vol ratio** : 0.68  _(volume normal)_
- **Choppiness** : 56.5  _(transition)_
- **MA** : MA20 1052500.0 · MA50 1046220.0 · MA200 1167711.82  _(prix < MA20)_
- **Dist MA** : MA20 -1.8% · MA50 -1.2% · MA200 -11.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (548808 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
