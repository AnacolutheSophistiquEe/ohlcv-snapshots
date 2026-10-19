# 000660

**Generated** : 2026-10-19T00:14:27.359309+00:00  
**Couverture** : bulletin complet  
> ⚠️ **Données suspectes** : barres source hors échelle (prix/vol) — bulletin NON FIABLE, re-télécharger les données KR.  

**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩1272000.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (8 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩1272000.00 (+0.5% vs entrée) · entrée ₩1265432.46 · stop ₩1239782.46 · T1 ₩1308182.46 · R/R 1.67  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −2.03% cohérent avec le bruit 5 s (EV-optimal ≈ −1.5%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -95 % hors [0,100] (R² max 0.58). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 20.0 < 20 (tendance pas encore confirmée) alors que Choppiness 22.4 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-16 : 1272000.0 · ATR Wilder 96232.61 (7.57 %)_
- **Swing** : plage **1162755.46 → 1091098.56** (-8.59 % a -14.22 % sous la cloture, 0.74 ATR) — touchee 50 % → 30 % du temps en 10 seances ; aucun support reel dans la plage. stop INDICATIF 993483.58 (-8.95 % sous le bas ; sous le support 1041599.89-1077586.1 (- 0,5 ATR)).
- **Deep** : plage **1091098.56 → 930224.37** (-14.22 % a -26.87 % sous la cloture, 1.67 ATR) — touchee 41 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1041599.89-1077586.1 (B) ; 883660.61-989619.88 (B). stop INDICATIF 833991.76 (-10.35 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.89 ATR sous le plus haut 20 s., RSI(2) 8.3. Limite **1223883.69** (seance suivante), stop catastrophe 838953.24, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 1041599.89-1077586.1 (B, -15.28 %) ; 883660.61-989619.88 (B, -22.2 %) ; 772277.75-807689.81 (A, -36.5 %) ; 722389.03-731369.02 (B, -42.5 %) ; 591680.52-623609.38 (B, -50.97 %) ; 499527.51-530436.33 (A, -58.3 %)
- Resistances reelles au-dessus : 1556662.48-1558000.0 (B, 22.38 %) ; 1671000.0-1717627.62 (A, 31.37 %) ; 1731624.54-1736000.0 (B, 36.13 %) ; 1791611.52-1791611.57 (C, 40.85 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=6.65 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.86 %)** : le gap seul le franchit 0.821 % des séances (10 fois sur 1218).
   - exécution **1.038 pt plus bas** dans le cas TYPIQUE (médiane), 2.53 au p90, **3.0 au pire**
   - perte réelle **9.087 %** en moyenne _(tirée par la queue)_, jusqu'à **10.86 %** — au lieu des 7.86 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0101 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 10 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -3.478 % | p01 -7.068 % | pire -10.86 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.4904** [0.4166 ; 0.5645] _(largeur 14.8 pt, n_eff 173.1)_
   - swing : **0.3509** [0.302 ; 0.4023] _(largeur 10.0 pt, n_eff 345.6)_
   - deep : **0.3015** [0.2549 ; 0.3514] _(largeur 9.6 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-9.56 %** | CVaR **-11.58 %** | vol 5.81 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.77 % contre 6.70 % aujourd'hui, rapport 0.56)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -9.72 % vs -10.83 % si l'on extrapolait par √5 _(rapport 0.898 ; < 1 = le √5 surestime)_
- **β de baisse : 1.4247** (β de hausse 1.6217, asymétrie 0.8785) vs KS11 — 556 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.052 | EV/share : ₩-1346.433 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 25 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 36.9 | bear 5.0 | side 58.1  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.513% → cible +3.378% / stop −2.027%, p_fill 81%, n_eff≈87.4) : P(cible|rempli) **19%** · **EV/risk -0.281** (×p_fill ; si rempli -0.70% du capital)
  - **swing** (entrée dip −1.138% → cible +8.477% / stop −6.799%, p_fill 77%, n_eff≈89.7) : P(cible|rempli) **38%** · **EV/risk -0.118** (×p_fill ; si rempli -1.04% du capital)
  - **deep** (entrée dip −1.758% → cible +10.818% / stop −10.263%, p_fill 77%, n_eff≈84.4) : P(cible|rempli) **48%** · **EV/risk -0.052** (×p_fill ; si rempli -0.69% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→90% · +1.0%→77% · +2.0%→54% · +3.0%→38% · +5.0%→21% · +8.0%→8%
- Range intraday médian 5.51% (p90 10.55%) · excursion haute méd. +2.19% / basse méd. −2.54%
- Profil de vol intra : ouverture 2.923% vs midi 1.197% vs clôture 1.401% _(ouverture ~2.4× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 82% · range 17% · trend ↑1%/↓0% ; spike-down 57% · recovery-V 25%)_
- **Régime intraday** : **chop** _(efficiency 0.135 ; neutre — autocorr -0.027)_ ; drift intra méd. -0.174% ; recovery-V 21%
- **σ réalisé intraday** 2.966% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 60% / bas 58% / whipsaw 28%
- POC intraday (dernière séance, temps-au-prix) : 1845912.5 (VA 1837812.5–1847937.5 ; dernier close 1843000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 24% · rebond 70% · **stop −7.14%** sous le fill (sous le bruit) · cible +2.04% · R/R 0.29 (high win-rate)
- Gaps overnight (n=152) : méd. 0.6% · baisse 45% (gap-down >1% 29% · >2% 22%)
- Excursion ouverture 5min (n=160) : bas méd −0.54% (p90 −1.8%) · haut méd +0.76% · range méd 1.36%
- Excursion ouverture 15min (n=160) : bas méd −0.84% (p90 −2.29%) · haut méd +0.95% · range méd 1.86%
- Excursion ouverture 30min (n=160) : bas méd −1.02% (p90 −3.02%) · haut méd +1.28% · range méd 2.47%
- Excursion ouverture 60min (n=160) : bas méd −1.23% (p90 −3.82%) · haut méd +1.38% · range méd 2.98%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 1841000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 53% · séance 63% (93/152) · gap 37% · délai 0.0min · rebond 60% (53/93) (MFE +1.37%)
   - −1.0% : fill 30min 45% · séance 59% (86/152) · gap 29% · délai 0.0min · rebond 61% (55/86) (MFE +1.52%)
   - −1.5% : fill 30min 36% · séance 53% (78/152) · gap 24% · délai 0.1min · rebond 69% (53/78) (MFE +1.6%)
   - −2.0% : fill 30min 30% · séance 42% (69/152) · gap 22% · délai 0.0min · rebond 61% (45/69) (MFE +1.77%)
   - −3.0% : fill 30min 26% · séance 38% (59/152) · gap 18% · délai 0.8min · rebond 69% (40/59) (MFE +1.74%)
   - −4.0% : fill 30min 21% · séance 31% (50/152) · gap 12% · délai 1.0min · rebond 64% (35/50) (MFE +2.2%)
   - −5.0% : fill 30min 13% · séance 24% (38/152) · gap 7% · délai 12.9min · rebond 70% (25/38) (MFE +2.04%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.29% (p90 −2.29%) → stop au-delà de −1.23% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.53% (p90 −2.55%) → stop au-delà de −1.74% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.7% (p90 −2.65%) → stop au-delà de −2.27% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=831 jambes) : jambe baissière méd −1.2% (p90 −3.25%) · ~10.9 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (60 séances) :
      · −1.0% : fill 97% (59/60) · rebond 57% (33/59)
      · −2.0% : fill 73% (50/60) · rebond 49% (28/50)
      · −3.0% : fill 70% (45/60) · rebond 62% (28/45)
      · −4.0% : fill 62% (41/60) · rebond 59% (27/41)
      · −5.0% : fill 46% (31/60) · rebond 62% (18/31)
   - **flat** (10 séances) :
      · −1.0% : fill 27% (6/10) · rebond 100% (6/6)
      · −2.0% : fill 14% (3/10) · rebond 100% (3/3)
      · −3.0% : fill 10% (2/10) · rebond 100% (2/2)
      · −4.0% : fill 0% (0/10) · rebond 0% (0/0)
      · −5.0% : fill 0% (0/10) · rebond 0% (0/0)
   - **gap-up** (82 séances) :
      · −1.0% : fill 33% (21/82) · rebond 66% (16/21)
      · −2.0% : fill 23% (16/82) · rebond 87% (14/16)
      · −3.0% : fill 17% (12/82) · rebond 86% (10/12)
      · −4.0% : fill 11% (9/82) · rebond 83% (8/9)
      · −5.0% : fill 10% (7/82) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 45% en base · 58% si les 15 1res min sont vertes (84 cas) · 28% si rouges (76 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:50** → P(séance verte=clôture>ouverture) 70% si début vert vs 11% si rouge (base 45% · écart 59 pts) ; prédictivité sature ensuite (plafond brut 223min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=89) : tient le vert **70%** · continue >prix actuel 54% ; creux résiduel méd -1.24% (q20 -3.31%) → **SL/trailing à −3.31%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.55% / q75 +2.89% → **scale +1.55% / runner +2.89%**, sortie à la clôture
  - **si ROUGE au coude** (n=71) : edge inversé — récupère vert seulement **11%** (continue à baisser 58%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −6.13%** (au-delà de la MAE q10 -6.13%), cible rebond +1.0% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.02% .. +2.58%] · haut q95 +3.28% · bas q05 -3.89%
   - 60min (n=160) : retour [-3.3% .. +4.21%] · haut q95 +4.7% · bas q05 -5.02%
   - 2h (n=160) : retour [-4.39% .. +4.41%] · haut q95 +5.98% · bas q05 -6.58%
   - 4h (n=160) : retour [-6.22% .. +5.15%] · haut q95 +6.66% · bas q05 -7.39%
   - 6h (n=160) : retour [-6.31% .. +5.01%] · haut q95 +7.83% · bas q05 -8.0%
   - session (n=160) : retour [-6.86% .. +5.54%] · haut q95 +8.01% · bas q05 -8.13%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — 000660 = **volatil sans tendance propre (choppy)** (vol intra méd 3.1%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.75/2 | R/R T1 : 2.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.21 · part idiosyncratique 0.79
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 13.8  _(survente)_
- **ADX** : 20.0  _(pas de tendance nette)_
- **MACD** : hist -62226.898  _(pas de croisement recent)_
- **BB** : %B -0.05 · largeur 45.1%
- **ATR** : 85500.0 (58.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.361  _(distribution)_
- **Vol ratio** : 1.36  _(volume normal)_
- **Choppiness** : 22.4  _(marche directionnel)_
- **MA** : MA20 1689100.0 · MA50 1662235.72 · MA200 1456156.11  _(prix < MA20)_
- **Dist MA** : MA20 -24.7% · MA50 -23.5% · MA200 -12.6%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (494250 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
