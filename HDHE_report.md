# 267260

**Generated** : 2026-11-17T01:16:26.185009+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · ₩382500.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (17 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩382500.00 (+2.5% vs entrée) · entrée ₩373059.13 · stop ₩343214.40 · T1 ₩389978.58 · R/R 0.57  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : range  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-17 : 382500.0 · ATR Wilder 34311.81 (8.97 %)_
- **Swing** : plage **342680.24 → 320636.57** (-10.41 % a -16.17 % sous la cloture, 0.64 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 341779.91-358820.23 (A) ; 319305.85-332408.11 (B). stop INDICATIF 283709.81 (-11.52 % sous le bas ; sous le support 300865.72-315682.85 (- 0,5 ATR)).
- **Deep** : plage **320636.57 → 258696.81** (-16.17 % a -32.37 % sous la cloture, 1.81 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 319305.85-332408.11 (B) ; 300865.72-315682.85 (B) ; 275146.6-289198.42 (A) ; 257676.95-287118.7 (A). stop INDICATIF 221595.61 (-14.34 % sous le bas ; sous le support 238751.51-255250.6 (- 0,5 ATR)).
- ACHAT PAS CHER : inactif (3.56 ATR sous le plus haut 20 s., RSI(2) 12.4 ; seuils 4,7 ATR, ou RSI(2) < 10 et 3 ATR).
- Supports reels sous le cours (pour le Warden) : 341779.91-358820.23 (A, -6.19 %) ; 319305.85-332408.11 (B, -13.1 %) ; 300865.72-315682.85 (B, -17.47 %) ; 275146.6-289198.42 (A, -24.39 %) ; 257676.95-287118.7 (A, -24.94 %) ; 238751.51-255250.6 (A, -33.27 %)
- Resistances reelles au-dessus : 396308.91-413340.01 (A, 3.61 %) ; 425034.01-438179.32 (A, 11.12 %) ; 445972.11-457822.07 (A, 16.59 %) ; 471187.84-478604.23 (A, 23.19 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.76 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (14.28 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 14.28 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.872 % | p01 -4.901 % | pire -13.45 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0713** [0.0399 ; 0.1168] _(largeur 7.7 pt, n_eff 173.1)_
   - swing : **0.3368** [0.2885 ; 0.3878] _(largeur 9.9 pt, n_eff 345.6)_
   - deep : **0.3545** [0.3054 ; 0.406] _(largeur 10.1 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : swing (25.8 pt), deep (25.6 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-6.95 %** | CVaR **-9.15 %** | vol 4.43 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 2.91 % contre 5.03 % aujourd'hui, rapport 0.58)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.57 % vs -12.28 % si l'on extrapolait par √5 _(rapport 0.942 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0782** (β de hausse 0.8529, asymétrie 1.2641) vs KS11 — 555 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.09 | EV/share : ₩-2699.448 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 16 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 64.1 | bear 10.5 | side 25.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.467% → cible +4.535% / stop −8.0%, p_fill 65%, n_eff≈73.9) : P(cible|rempli) **14%** · **EV/risk -0.046** (×p_fill ; si rempli -0.57% du capital)
  - **swing** (entrée dip −5.434% → cible +10.459% / stop −9.355%, p_fill 46%, n_eff≈54.9) : P(cible|rempli) **20%** · **EV/risk -0.168** (×p_fill ; si rempli -3.43% du capital)
  - **deep** (entrée dip −8.389% → cible +15.269% / stop −14.486%, p_fill 48%, n_eff≈56.1) : P(cible|rempli) **24%** · **EV/risk -0.137** (×p_fill ; si rempli -4.11% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→62% · +2.0%→40% · +3.0%→29% · +5.0%→12% · +8.0%→3%
- Range intraday médian 5.9% (p90 9.8%) · excursion haute méd. +1.42% / basse méd. −3.45%
- Profil de vol intra : ouverture 3.996% vs midi 1.075% vs clôture 1.184% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 84% · range 14% · trend ↑0%/↓2% ; spike-down 84% · recovery-V 21%)_
- **Régime intraday** : **chop** _(efficiency 0.14 ; mean-reverting — autocorr -0.048)_ ; drift intra méd. -1.179% ; recovery-V 13%
- **σ réalisé intraday** 3.272% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 41% / bas 66% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 456837.5 (VA 449237.5–460637.5 ; dernier close 467000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 29% · rebond 77% · **stop −4.27%** sous le fill (sous le bruit) · cible +2.01% · R/R 0.47 (high win-rate)
- Gaps overnight (n=152) : méd. 0.5% · baisse 41% (gap-down >1% 22% · >2% 15%)
- Excursion ouverture 5min (n=160) : bas méd −1.55% (p90 −3.5%) · haut méd +0.71% · range méd 2.6%
- Excursion ouverture 15min (n=160) : bas méd −1.71% (p90 −4.15%) · haut méd +0.79% · range méd 3.15%
- Excursion ouverture 30min (n=160) : bas méd −1.95% (p90 −5.01%) · haut méd +0.84% · range méd 3.49%
- Excursion ouverture 60min (n=160) : bas méd −2.16% (p90 −5.22%) · haut méd +0.97% · range méd 3.66%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 468283.7188 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 63% · séance 73% (105/152) · gap 31% · délai 0.0min · rebond 56% (60/105) (MFE +1.16%)
   - −1.0% : fill 30min 55% · séance 70% (97/152) · gap 22% · délai 0.3min · rebond 52% (53/97) (MFE +1.12%)
   - −1.5% : fill 30min 47% · séance 65% (90/152) · gap 18% · délai 0.7min · rebond 53% (56/90) (MFE +1.18%)
   - −2.0% : fill 30min 42% · séance 61% (84/152) · gap 15% · délai 1.7min · rebond 59% (55/84) (MFE +1.23%)
   - −3.0% : fill 30min 34% · séance 51% (72/152) · gap 11% · délai 3.2min · rebond 61% (51/72) (MFE +1.8%)
   - −4.0% : fill 30min 22% · séance 38% (51/152) · gap 4% · délai 11.1min · rebond 61% (33/51) (MFE +1.26%)
   - −5.0% : fill 30min 18% · séance 29% (41/152) · gap 3% · délai 9.4min · rebond 77% (31/41) (MFE +2.01%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −3.05%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −3.0%) → stop au-delà de −2.02% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.01% (p90 −3.82%) → stop au-delà de −3.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=829 jambes) : jambe baissière méd −1.21% (p90 −3.22%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 100% (47/47) · rebond 47% (23/47)
      · −2.0% : fill 94% (43/47) · rebond 54% (25/43)
      · −3.0% : fill 78% (38/47) · rebond 56% (25/38)
      · −4.0% : fill 64% (30/47) · rebond 66% (22/30)
      · −5.0% : fill 54% (25/47) · rebond 84% (20/25)
   - **flat** (13 séances) :
      · −1.0% : fill 95% (11/13) · rebond 52% (6/11)
      · −2.0% : fill 95% (11/13) · rebond 53% (8/11)
      · −3.0% : fill 95% (11/13) · rebond 95% (10/11)
      · −4.0% : fill 52% (6/13) · rebond 57% (4/6)
      · −5.0% : fill 33% (5/13) · rebond 100% (5/5)
   - **gap-up** (92 séances) :
      · −1.0% : fill 44% (39/92) · rebond 59% (24/39)
      · −2.0% : fill 32% (30/92) · rebond 72% (22/30)
      · −3.0% : fill 24% (23/92) · rebond 50% (16/23)
      · −4.0% : fill 18% (15/92) · rebond 49% (7/15)
      · −5.0% : fill 11% (11/92) · rebond 40% (6/11)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 31% en base · 45% si les 15 1res min sont vertes (58 cas) · 24% si rouges (102 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:41** → P(séance verte=clôture>ouverture) 78% si début vert vs 8% si rouge (base 31% · écart 70 pts) ; prédictivité sature ensuite (plafond brut 224min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=60) : tient le vert **78%** · continue >prix actuel 52% ; creux résiduel méd -1.33% (q20 -3.16%) → **SL/trailing à −3.16%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.49% / q75 +2.58% → **scale +1.49% / runner +2.58%**, sortie à la clôture
  - **si ROUGE au coude** (n=100) : edge inversé — récupère vert seulement **8%** (continue à baisser 54%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −3.94%** (au-delà de la MAE q10 -3.94%), cible rebond +0.91% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.73% .. +2.63%] · haut q95 +3.79% · bas q05 -5.23%
   - 60min (n=160) : retour [-5.49% .. +2.52%] · haut q95 +4.36% · bas q05 -5.74%
   - 2h (n=160) : retour [-5.74% .. +3.72%] · haut q95 +5.15% · bas q05 -7.59%
   - 4h (n=160) : retour [-6.82% .. +4.48%] · haut q95 +5.52% · bas q05 -8.13%
   - 6h (n=160) : retour [-8.34% .. +4.77%] · haut q95 +6.72% · bas q05 -8.94%
   - session (n=160) : retour [-6.85% .. +4.99%] · haut q95 +6.96% · bas q05 -8.98%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.51%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 2.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.15 · part idiosyncratique 0.85
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 34.6  _(momentum baissier)_
- **ADX** : 44.6  _(tendance tres forte)_
- **MACD** : hist 6992.916  _(pas de croisement recent)_
- **BB** : %B 0.21 · largeur 35.5%
- **ATR** : 33838.9 (13.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV rising · CMF 0.112  _(accumulation)_
- **Vol ratio** : 0.22  _(volume atone)_
- **Choppiness** : 54.3  _(transition)_
- **MA** : MA20 426430.49 · MA50 566690.4 · MA200 853283.22  _(prix < MA20)_
- **Dist MA** : MA20 -10.3% · MA50 -32.5% · MA200 -55.2%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (404174 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
