# 000660

**Generated** : 2026-11-25T21:52:02.045158+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 2/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1035000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)  
> ↳ spot ₩1035000.00 (+2.6% vs entrée) · entrée ₩1008482.12 · stop ₩977401.67 · T1 ₩1070643.02 · R/R 2.0  
> ↳ _probas brutes, non calibrées · n=0_  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -25 % hors [0,100] (R² max 0.95). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : down  
- **Flag multi-TF** : mixed (score 2)


## Lecture chartiste

Plan privilegie A (intraday), composite 2/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-11-25 : 1035000.0 · ATR Wilder 101296.22 (9.79 %)_
- **Swing** : plage **917701.02 → 833587.02** (-11.33 % a -19.46 % sous la cloture, 0.83 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 883660.61-989619.88 (B). stop INDICATIF 735598.56 (-11.76 % sous le bas ; sous le support 786246.67-807689.81 (- 0,5 ATR)).
- **Deep** : plage **833587.02 → 640659.35** (-19.46 % a -38.1 % sous la cloture, 1.9 ATR) — touchee 40 % → 15 % du temps en 20 seances ; supports reels dans la plage : 786246.67-807689.81 (A) ; 722389.09-772277.75 (A). stop INDICATIF 541032.41 (-15.55 % sous le bas ; sous le support 591680.52-622165.99 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.45 ATR sous le plus haut 20 s., RSI(2) 22.4. Limite **984351.89** (seance suivante), stop catastrophe 579167.01, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 883660.61-989619.88 (B, -4.38 %) ; 786246.67-807689.81 (A, -21.96 %) ; 722389.09-772277.75 (A, -25.38 %) ; 591680.52-622165.99 (C, -39.89 %) ; 499527.51-530436.39 (A, -48.75 %) ; 332021.29-382871.36 (B, -63.01 %)
- Resistances reelles au-dessus : 1098578.0-1098578.0 (C, 6.14 %) ; 1245729.86-1245729.86 (C, 20.36 %) ; 1317000.0-1329000.0 (B, 27.25 %) ; 1556662.48-1587000.0 (A, 50.4 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=7.30 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (15.04 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 15.04 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.723 % | p01 -7.63 % | pire -13.845 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.3937** [0.3232 ; 0.4678] _(largeur 14.5 pt, n_eff 173.1)_
   - swing : **0.2682** [0.2236 ; 0.3167] _(largeur 9.3 pt, n_eff 345.6)_
   - deep : **0.2692** [0.2245 ; 0.3177] _(largeur 9.3 pt, n_eff 345.6)_
- ⚠ **5 s — échantillon insuffisant sur : intraday (25.6 pt), swing (28.5 pt), deep (28.7 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-9.69 %** | CVaR **-11.72 %** | vol 5.9 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 4.19 % contre 6.71 % aujourd'hui, rapport 0.62)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.98 % vs -11.45 % si l'on extrapolait par √5 _(rapport 0.872 ; < 1 = le √5 surestime)_
- **β de baisse : 1.428** (β de hausse 1.6104, asymétrie 0.8868) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- Calibration des probas : _probas brutes, non calibrées · n=0_
- Régime probabiliste (posterior HMM, intraday) : bull 72.3 | bear 16.8 | side 10.9  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −2.567% → cible +6.164% / stop −3.082%, p_fill 49%, n_eff≈55.6) : P(cible|rempli) **7%** · **EV/risk -0.116** (×p_fill ; si rempli -0.72% du capital)
  - **swing** (entrée dip −5.633% → cible +18.902% / stop −9.968%, p_fill 39%, n_eff≈44.8) : P(cible|rempli) **7%** · **EV/risk -0.153** (×p_fill ; si rempli -3.93% du capital)
  - **deep** (entrée dip −8.71% → cible +22.906% / stop −15.456%, p_fill 39%, n_eff≈44.0) : P(cible|rempli) **8%** · **EV/risk -0.133** (×p_fill ; si rempli -5.22% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→78% · +2.0%→55% · +3.0%→38% · +5.0%→23% · +8.0%→8%
- Range intraday médian 6.05% (p90 10.45%) · excursion haute méd. +2.31% / basse méd. −2.61%
- Profil de vol intra : ouverture 3.003% vs midi 1.225% vs clôture 1.446% _(ouverture ~2.5× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 83% · range 16% · trend ↑0%/↓0% ; spike-down 62% · recovery-V 22%)_
- **Régime intraday** : **chop** _(efficiency 0.139 ; neutre — autocorr -0.023)_ ; drift intra méd. -0.404% ; recovery-V 17%
- **σ réalisé intraday** 3.303% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 57% / bas 65% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 1222800.0 (VA 1186400.0–1253600.0 ; dernier close 1281000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 28% · rebond 60% · **stop −7.48%** sous le fill (sous le bruit) · cible +1.69% · R/R 0.23 (high win-rate)
- Gaps overnight (n=152) : méd. -0.07% · baisse 51% (gap-down >1% 36% · >2% 26%)
- Excursion ouverture 5min (n=160) : bas méd −0.48% (p90 −1.95%) · haut méd +0.82% · range méd 1.36%
- Excursion ouverture 15min (n=160) : bas méd −0.82% (p90 −2.42%) · haut méd +1.01% · range méd 2.04%
- Excursion ouverture 30min (n=160) : bas méd −0.97% (p90 −3.27%) · haut méd +1.34% · range méd 2.54%
- Excursion ouverture 60min (n=160) : bas méd −1.28% (p90 −3.8%) · haut méd +1.49% · range méd 3.25%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1277000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 58% · séance 69% (97/152) · gap 44% · délai 0.0min · rebond 48% (51/97) (MFE +0.92%)
   - −1.0% : fill 30min 51% · séance 66% (93/152) · gap 36% · délai 0.0min · rebond 59% (58/93) (MFE +1.3%)
   - −1.5% : fill 30min 42% · séance 60% (85/152) · gap 31% · délai 0.0min · rebond 64% (55/85) (MFE +1.63%)
   - −2.0% : fill 30min 38% · séance 50% (75/152) · gap 26% · délai 0.0min · rebond 56% (46/75) (MFE +1.52%)
   - −3.0% : fill 30min 31% · séance 43% (64/152) · gap 20% · délai 1.9min · rebond 61% (41/64) (MFE +1.3%)
   - −4.0% : fill 30min 26% · séance 37% (55/152) · gap 15% · délai 3.0min · rebond 61% (37/55) (MFE +1.84%)
   - −5.0% : fill 30min 17% · séance 28% (42/152) · gap 7% · délai 6.8min · rebond 60% (26/42) (MFE +1.69%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.27% (p90 −2.29%) → stop au-delà de −1.17% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.35% (p90 −2.6%) → stop au-delà de −2.24% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.57% (p90 −2.56%) → stop au-delà de −2.3% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=848 jambes) : jambe baissière méd −1.25% (p90 −3.37%) · ~11.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (65 séances) :
      · −1.0% : fill 98% (64/65) · rebond 55% (35/64)
      · −2.0% : fill 81% (55/65) · rebond 50% (29/55)
      · −3.0% : fill 76% (50/65) · rebond 55% (29/50)
      · −4.0% : fill 70% (46/65) · rebond 58% (29/46)
      · −5.0% : fill 51% (35/65) · rebond 54% (19/35)
   - **flat** (10 séances) :
      · −1.0% : fill 42% (6/10) · rebond 100% (6/6)
      · −2.0% : fill 11% (3/10) · rebond 100% (3/3)
      · −3.0% : fill 8% (2/10) · rebond 100% (2/2)
      · −4.0% : fill 0% (0/10) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/10) · rebond 0% (0/0)
   - **gap-up** (77 séances) :
      · −1.0% : fill 38% (23/77) · rebond 63% (17/23)
      · −2.0% : fill 25% (17/77) · rebond 74% (14/17)
      · −3.0% : fill 16% (12/77) · rebond 86% (10/12)
      · −4.0% : fill 10% (9/77) · rebond 83% (8/9)
      · −5.0% : fill 9% (7/77) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 56% si les 15 1res min sont vertes (87 cas) · 21% si rouges (73 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 65% si début vert vs 9% si rouge (base 40% · écart 56 pts) ; prédictivité sature ensuite (plafond brut 223min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=88) : tient le vert **65%** · continue >prix actuel 49% ; creux résiduel méd -1.45% (q20 -3.7%) → **SL/trailing à −3.7%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.46% / q75 +2.94% → **scale +1.46% / runner +2.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=72) : edge inversé — récupère vert seulement **9%** (continue à baisser 68%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.01%** (au-delà de la MAE q10 -5.01%), cible rebond +1.01% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.0% .. +2.65%] · haut q95 +3.82% · bas q05 -4.01%
   - 60min (n=160) : retour [-3.6% .. +3.81%] · haut q95 +4.68% · bas q05 -5.02%
   - 2h (n=160) : retour [-4.69% .. +4.46%] · haut q95 +5.68% · bas q05 -6.5%
   - 4h (n=160) : retour [-5.25% .. +4.7%] · haut q95 +6.4% · bas q05 -7.14%
   - 6h (n=160) : retour [-6.42% .. +5.56%] · haut q95 +7.17% · bas q05 -7.45%
   - session (n=160) : retour [-6.55% .. +6.05%] · haut q95 +7.17% · bas q05 -7.49%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (6) pour des stats fiables : 3.7% des séances seulement sont des jours de hausse propre — 000660 = **volatil sans tendance propre (choppy)** (vol intra méd 3.34%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 0.5 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.19 · part idiosyncratique 0.81
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-11-25 — US Core PCE Price Index — octobre 2026 (J-0 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-11-30 — MSCI — suppression de Strategy (MSTR) signalée au 30 novembre (J-4 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 36.3  _(momentum baissier)_
- **ADX** : 24.3  _(pas de tendance nette)_
- **MACD** : hist -1948.241  _(pas de croisement recent)_
- **BB** : %B 0.15 · largeur 45.8%
- **ATR** : 97357.14 (56.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.219  _(distribution)_
- **Vol ratio** : 0.74  _(volume normal)_
- **Choppiness** : 58.6  _(transition)_
- **MA** : MA20 1231850.0 · MA50 1446500.0 · MA200 1532431.65  _(prix < MA20)_
- **Dist MA** : MA20 -16.0% · MA50 -28.4% · MA200 -32.5%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (390072 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
