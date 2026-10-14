# 326030

**Generated** : 2026-10-14T21:58:35.382128+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩70300.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)  
> ↳ spot ₩70300.00 (+3.2% vs entrée) · entrée ₩68142.86 · stop ₩62691.43 · T1 ₩69221.43 · R/R 0.2  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-14 : 70300.0 · ATR Wilder 2628.57 (3.74 %)_
- **Swing** : plage **66806.46 → 65048.63** (-4.97 % a -7.47 % sous la cloture, 0.67 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 62420.06 (-4.04 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **65048.63 → 59903.08** (-7.47 % a -14.79 % sous la cloture, 1.96 ATR) — touchee 49 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 57274.51 (-4.39 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (COMBO) : 3.88 ATR sous le plus haut 20 s., RSI(2) 2.9. Limite **68985.72** (seance suivante), stop catastrophe 58471.44, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Resistances reelles au-dessus : 72600.0-73800.0 (A, 3.27 %) ; 74000.0-74900.0 (A, 5.26 %) ; 75500.0-76300.0 (A, 7.4 %) ; 77100.0-78000.0 (A, 9.67 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.07 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (9.21 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 9.21 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.578 % | p01 -3.013 % | pire -5.539 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0053** [0.0005 ; 0.0258] _(largeur 2.5 pt, n_eff 173.1)_
   - swing : **0.5378** [0.4851 ; 0.5899] _(largeur 10.5 pt, n_eff 345.6)_
   - deep : **0.554** [0.5013 ; 0.6058] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 28.7 observations effectives », dont la borne haute a 95 % vaut environ 10.5 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (34.8 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.34 %** | CVaR **-6.25 %** | vol 2.95 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.73 % contre 2.97 % aujourd'hui, rapport 0.58)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.24 % vs -8.65 % si l'on extrapolait par √5 _(rapport 0.953 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5892** (β de hausse 0.4322, asymétrie 1.3634) vs KS11 — 555 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.032 | EV/share : ₩-171.704 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 47 % | T2 23 % | T3 10 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 84.7 | side 10.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈60.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.065% → cible +1.583% / stop −8.0%, p_fill 23%, n_eff≈28.7) : P(cible|rempli) **43%** · **EV/risk +0.009** (×p_fill ; si rempli +0.33% du capital)
  - **swing** : indisponible (échantillon insuffisant (n=13, n_eff=13))
  - **deep** : indisponible (échantillon insuffisant (n=7, n_eff=7))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→74% · +1.0%→60% · +2.0%→40% · +3.0%→25% · +5.0%→8% · +8.0%→4%
- Range intraday médian 3.9% (p90 6.9%) · excursion haute méd. +1.42% / basse méd. −2.03%
- Profil de vol intra : ouverture 2.58% vs midi 0.802% vs clôture 0.823% _(ouverture ~3.2× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 86% · range 13% · trend ↑1%/↓1% ; spike-down 58% · recovery-V 20%)_
- **Régime intraday** : **chop** _(efficiency 0.122 ; mean-reverting — autocorr -0.142)_ ; drift intra méd. -0.24% ; recovery-V 17%
- **σ réalisé intraday** 2.355% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 47% / bas 61% / whipsaw 16%
- POC intraday (dernière séance, temps-au-prix) : 75291.25 (VA 75206.25–75588.75 ; dernier close 75700.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 18% · rebond 70% · **stop −3.57%** sous le fill (sous le bruit) · cible +1.28% · R/R 0.36 (high win-rate)
- Gaps overnight (n=152) : méd. 0.0% · baisse 43% (gap-down >1% 19% · >2% 5%)
- Excursion ouverture 5min (n=160) : bas méd −0.67% (p90 −2.2%) · haut méd +0.47% · range méd 1.48%
- Excursion ouverture 15min (n=160) : bas méd −1.02% (p90 −2.69%) · haut méd +0.54% · range méd 1.86%
- Excursion ouverture 30min (n=160) : bas méd −1.1% (p90 −2.77%) · haut méd +0.6% · range méd 2.29%
- Excursion ouverture 60min (n=160) : bas méd −1.16% (p90 −2.94%) · haut méd +0.84% · range méd 2.75%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 75800.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 68% · séance 80% (116/152) · gap 30% · délai 0.0min · rebond 41% (46/116) (MFE +0.76%)
   - −1.0% : fill 30min 51% · séance 70% (104/152) · gap 19% · délai 0.9min · rebond 51% (49/104) (MFE +1.06%)
   - −1.5% : fill 30min 40% · séance 59% (84/152) · gap 10% · délai 4.2min · rebond 61% (48/84) (MFE +1.25%)
   - −2.0% : fill 30min 30% · séance 46% (66/152) · gap 5% · délai 8.6min · rebond 55% (36/66) (MFE +1.18%)
   - −3.0% : fill 30min 15% · séance 28% (44/152) · gap 4% · délai 24.9min · rebond 54% (23/44) (MFE +1.28%)
   - −4.0% : fill 30min 9% · séance 18% (31/152) · gap 3% · délai 50.1min · rebond 70% (20/31) (MFE +1.28%)
   - −5.0% : fill 30min 4% · séance 9% (17/152) · gap 1% · délai 74.1min · rebond 83% (11/17) (MFE +1.45%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.42% (p90 −2.5%) → stop au-delà de −1.43% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −1.78%) → stop au-delà de −1.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.38% (p90 −1.43%) → stop au-delà de −1.11% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=572 jambes) : jambe baissière méd −1.02% (p90 −2.37%) · ~8.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 91% (51/54) · rebond 60% (28/51)
      · −2.0% : fill 68% (38/54) · rebond 66% (22/38)
      · −3.0% : fill 49% (28/54) · rebond 56% (16/28)
      · −4.0% : fill 34% (21/54) · rebond 63% (13/21)
      · −5.0% : fill 18% (11/54) · rebond 84% (7/11)
   - **flat** (36 séances) :
      · −1.0% : fill 76% (27/36) · rebond 39% (9/27)
      · −2.0% : fill 53% (17/36) · rebond 42% (9/17)
      · −3.0% : fill 31% (11/36) · rebond 38% (3/11)
      · −4.0% : fill 22% (9/36) · rebond 81% (6/9)
      · −5.0% : fill 12% (6/36) · rebond 80% (4/6)
   - **gap-up** (62 séances) :
      · −1.0% : fill 46% (26/62) · rebond 47% (12/26)
      · −2.0% : fill 21% (11/62) · rebond 39% (5/11)
      · −3.0% : fill 7% (5/62) · rebond 87% (4/5)
      · −4.0% : fill 1% (1/62) · rebond 100% (1/1)
      · −5.0% : fill 0% (0/62) · rebond 0% (0/0)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 38% en base · 69% si les 15 1res min sont vertes (59 cas) · 20% si rouges (101 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→234min, n=160) : COUDE à **34min** → P(séance verte=clôture>ouverture) 77% si début vert vs 15% si rouge (base 38% · écart 62 pts) ; prédictivité sature ensuite (plafond brut 192min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=60) : tient le vert **77%** · continue >prix actuel 63% ; creux résiduel méd -1.23% (q20 -2.67%) → **SL/trailing à −2.67%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.87% / q75 +2.61% → **scale +1.87% / runner +2.61%**, sortie à la clôture
  - **si ROUGE au coude** (n=100) : edge inversé — récupère vert seulement **15%** (continue à baisser 55%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −2.93%** (au-delà de la MAE q10 -2.93%), cible rebond +0.9% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-2.57% .. +2.3%] · haut q95 +3.4% · bas q05 -3.44%
   - 60min (n=160) : retour [-2.82% .. +3.49%] · haut q95 +4.29% · bas q05 -3.73%
   - 2h (n=160) : retour [-3.18% .. +3.45%] · haut q95 +4.47% · bas q05 -3.93%
   - 4h (n=160) : retour [-3.3% .. +3.96%] · haut q95 +5.79% · bas q05 -4.53%
   - 6h (n=160) : retour [-3.89% .. +4.19%] · haut q95 +6.07% · bas q05 -4.99%
   - session (n=160) : retour [-3.93% .. +4.09%] · haut q95 +6.07% · bas q05 -4.99%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (0) pour des stats fiables : 0% des séances seulement sont des jours de hausse propre — 326030 = **plat / peu volatil** (vol intra méd 2.6%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.13 · part idiosyncratique 0.87
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US Core CPI (ex food & energy) (J-0 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 23.9  _(survente)_
- **ADX** : 24.0  _(pas de tendance nette)_
- **MACD** : hist -450.422  _(pas de croisement recent)_
- **BB** : %B 0.0 · largeur 14.7%
- **ATR** : 2157.14 (3.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.236  _(distribution)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 40.0  _(transition)_
- **MA** : MA20 75870.0 · MA50 81510.0 · MA200 96533.0  _(prix < MA20)_
- **Dist MA** : MA20 -7.3% · MA50 -13.8% · MA200 -27.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (593597 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
