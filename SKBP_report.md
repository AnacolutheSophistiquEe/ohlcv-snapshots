# 326030

**Generated** : 2026-10-09T00:22:49.503509+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩72700.00  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 42/125 fenêtres (p_fill pondéré 32 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot ₩72700.00 (+2.8% vs entrée) · entrée ₩70714.29 · stop ₩65057.14 · T1 ₩71707.14 · R/R 0.18  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -77 % hors [0,100] (R² max 0.32). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-08 : 72700.0 · ATR Wilder 2593.58 (3.57 %)_
- **Swing** : plage **69262.11 → 67537.21** (-4.73 % a -7.1 % sous la cloture, 0.67 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 64943.63 (-3.84 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- **Deep** : plage **67537.21 → 62460.44** (-7.1 % a -14.08 % sous la cloture, 1.96 ATR) — touchee 49 % → 15 % du temps en 20 seances ; aucun support reel dans la plage. stop INDICATIF 59866.86 (-4.15 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.21 ATR sous le plus haut 20 s., RSI(2) 8.4. Limite **71403.21** (seance suivante), stop catastrophe 61028.89, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Resistances reelles au-dessus : 74000.0-74900.0 (A, 1.79 %) ; 75500.0-76300.0 (A, 3.85 %) ; 77100.0-78000.0 (A, 6.05 %) ; 79000.0-79700.0 (A, 8.67 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.07 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (8.19 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 8.19 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.578 % | p01 -3.013 % | pire -5.539 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0055** [0.0006 ; 0.0262] _(largeur 2.6 pt, n_eff 173.1)_
   - swing : **0.5759** [0.5233 ; 0.6272] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.5608** [0.5082 ; 0.6124] _(largeur 10.4 pt, n_eff 345.6)_
- ⚠ 5 s / intraday : probabilite(s) EXACTEMENT nulle(s) : p_stop_first. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 37.3 observations effectives », dont la borne haute a 95 % vaut environ 8.1 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (31.1 pt), swing (44.7 pt), deep (40.3 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 540 séances)** : VaR **-4.34 %** | CVaR **-6.25 %** | vol 2.95 %/j
   - _fenêtre arrêtée : rupture de regime a 600 seances en arriere (volatilite 1.77 % contre 3.02 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -8.18 % vs -8.65 % si l'on extrapolait par √5 _(rapport 0.946 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5966** (β de hausse 0.4326, asymétrie 1.3791) vs KS11 — 553 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.033 | EV/share : ₩-186.431 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 51 % | T2 27 % | T3 13 %
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 5.0 | bear 10.9 | side 84.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.728% → cible +1.404% / stop −8.0%, p_fill 32%, n_eff≈37.3) : P(cible|rempli) **53%** · **EV/risk +0.013** (×p_fill ; si rempli +0.32% du capital)
  - **swing** (entrée dip −5.458% → cible +3.23% / stop −2.889%, p_fill 14%, n_eff≈16.6) : P(cible|rempli) **46%** · **EV/risk +0.002** (×p_fill ; si rempli +0.03% du capital)
  - **deep** (entrée dip −8.193% → cible +4.704% / stop −4.463%, p_fill 14%, n_eff≈15.8) : P(cible|rempli) **75%** · **EV/risk +0.075** (×p_fill ; si rempli +2.42% du capital)
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
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.2 · part idiosyncratique 0.8
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-14 — US CPI (headline) (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 31.2  _(momentum baissier)_
- **ADX** : 19.9  _(pas de tendance nette)_
- **MACD** : hist -172.594  _(pas de croisement recent)_
- **BB** : %B 0.07 · largeur 15.2%
- **ATR** : 1985.71 (1.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.193  _(distribution)_
- **Vol ratio** : 1.4  _(volume normal)_
- **Choppiness** : 48.6  _(transition)_
- **MA** : MA20 77790.0 · MA50 82010.0 · MA200 97491.0  _(prix < MA20)_
- **Dist MA** : MA20 -6.5% · MA50 -11.4% · MA200 -25.4%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (564523 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
