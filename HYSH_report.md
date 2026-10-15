# 298040

**Generated** : 2026-10-15T00:16:37.029001+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 3/10 — **Rating** : Unknown  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite low · ₩2135000.00  

> ⛔ **STAND-DOWN** — NON ESTIMABLE — la source du rating est inéligible (source périmée (6 séance(s) de retard, drapeau lu sur first_passage_by_horizon)) ; aucun repli sur un autre moteur (R09)  
> ↳ spot ₩2135000.00 (+0.6% vs entrée) · entrée ₩2122765.15 · stop ₩1952943.94 · T1 ₩2206860.71 · R/R 0.5  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -89 % hors [0,100] (R² max 0.42). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## ⚠ Contradictions techniques

- 🟠 **Tendance en transition (ADX / Choppiness)** — ADX 18.7 < 20 (tendance pas encore confirmée) alors que Choppiness 25.4 < 38 (marché déjà directionnel) — les deux jauges ne pointent pas au même stade.
  - _Le plus probable — DÉBUT de tendance : la Choppiness réagit plus vite que l'ADX (lissé Wilder, qui retarde) ; le prix progresse déjà en ligne mais l'ADX n'a pas franchi 20 → tendance jeune qui accélère, surveiller le passage ADX > 20/25 pour confirmation._
  - _Tendance lente / peu volatile : mouvement net mais de faible amplitude par barre → ADX bas (DI spread modeste) bien que la direction soit claire (Choppiness basse)._
  - _Vraie incohérence (rare) : ADX et Choppiness calculés sur des fenêtres ou des données décalées rendraient la comparaison invalide — ici les deux sont en daily 14 périodes, donc comparables._


## Lecture chartiste

Plan privilegie A (intraday), composite 3/10, conviction 'Unknown'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-14 : 2135000.0 · ATR Wilder 147336.3 (6.9 %)_
- **Swing** : plage **1977537.72 → 1856737.04** (-7.38 % a -13.03 % sous la cloture, 0.82 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 1834000.0-1862017.62 (B). stop INDICATIF 1649942.84 (-11.14 % sous le bas ; sous le support 1723610.98-1793312.2 (- 0,5 ATR)).
- **Deep** : plage **1856737.04 → 1651811.32** (-13.03 % a -22.63 % sous la cloture, 1.39 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 1834000.0-1862017.62 (B) ; 1723610.98-1793312.2 (A). stop INDICATIF 1369146.53 (-17.11 % sous le bas ; sous le support 1442814.68-1491605.62 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 5.93 ATR sous le plus haut 20 s., RSI(2) 0.7. Limite **2061331.85** (seance suivante), stop catastrophe 1471986.66, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 2016356.01-2071121.22 (C, -2.99 %) ; 1834000.0-1862017.62 (B, -12.79 %) ; 1723610.98-1793312.2 (A, -16.0 %) ; 1442814.68-1491605.62 (C, -30.14 %) ; 1350211.69-1364151.97 (A, -36.11 %) ; 1264578.88-1309386.78 (A, -38.67 %)
- Resistances reelles au-dessus : 2189000.0-2220000.0 (B, 2.53 %) ; 2400000.0-2472400.84 (A, 12.41 %) ; 2506000.0-2550000.0 (B, 17.38 %) ; 2599000.0-2671000.0 (A, 21.73 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.28 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (7.41 %)** : le gap seul le franchit 0.164 % des séances (2 fois sur 1218).
   - exécution **2.173 pt plus bas** dans le cas TYPIQUE (médiane), 3.856 au p90, **4.276 au pire**
   - perte réelle **9.583 %** en moyenne _(tirée par la queue)_, jusqu'à **11.686 %** — au lieu des 7.41 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0036 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 2 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.494 % | p01 -4.657 % | pire -11.686 % _(sur 1218 séances)_
- **P(stop avant cible)** _(source : daily, 1219 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0829** [0.0487 ; 0.1309] _(largeur 8.2 pt, n_eff 173.1)_
   - swing : **0.4413** [0.3896 ; 0.494] _(largeur 10.4 pt, n_eff 345.6)_
   - deep : **0.4141** [0.3631 ; 0.4666] _(largeur 10.4 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-7.15 %** | CVaR **-9.56 %** | vol 5.02 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.50 % contre 5.74 % aujourd'hui, rapport 0.61)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -12.12 % vs -12.69 % si l'on extrapolait par √5 _(rapport 0.956 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0844** (β de hausse 0.997, asymétrie 1.0877) vs KS11 — 555 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.049 | EV/share : ₩-8395.445 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 24 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 7.9 | bear 7.1 | side 85.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈120.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −0.576% → cible +3.962% / stop −8.0%, p_fill 89%, n_eff≈96.4) : P(cible|rempli) **21%** · **EV/risk -0.082** (×p_fill ; si rempli -0.74% du capital)
  - **swing** (entrée dip −1.255% → cible +6.968% / stop −6.233%, p_fill 88%, n_eff≈100.5) : P(cible|rempli) **45%** · **EV/risk -0.017** (×p_fill ; si rempli -0.12% du capital)
  - **deep** (entrée dip −1.949% → cible +15.748% / stop −9.415%, p_fill 87%, n_eff≈96.1) : P(cible|rempli) **26%** · **EV/risk -0.081** (×p_fill ; si rempli -0.87% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→77% · +1.0%→62% · +2.0%→50% · +3.0%→34% · +5.0%→18% · +8.0%→5%
- Range intraday médian 5.73% (p90 9.57%) · excursion haute méd. +2.0% / basse méd. −3.17%
- Profil de vol intra : ouverture 3.913% vs midi 1.01% vs clôture 1.04% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 22% · trend ↑0%/↓0% ; spike-down 74% · recovery-V 31%)_
- **Régime intraday** : **chop** _(efficiency 0.126 ; mean-reverting — autocorr -0.063)_ ; drift intra méd. -0.579% ; recovery-V 31%
- **σ réalisé intraday** 3.027% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 46% / bas 53% / whipsaw 9%
- POC intraday (dernière séance, temps-au-prix) : 2780512.5 (VA 2771912.5–2785887.5 ; dernier close 2781000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 26% · rebond 75% · **stop −4.27%** sous le fill (sous le bruit) · cible +2.24% · R/R 0.52 (high win-rate)
- Gaps overnight (n=152) : méd. 0.43% · baisse 36% (gap-down >1% 22% · >2% 16%)
- Excursion ouverture 5min (n=160) : bas méd −1.32% (p90 −2.87%) · haut méd +0.5% · range méd 2.09%
- Excursion ouverture 15min (n=160) : bas méd −1.78% (p90 −3.74%) · haut méd +0.76% · range méd 2.7%
- Excursion ouverture 30min (n=160) : bas méd −1.93% (p90 −4.19%) · haut méd +0.81% · range méd 3.1%
- Excursion ouverture 60min (n=160) : bas méd −2.17% (p90 −4.71%) · haut méd +1.01% · range méd 3.63%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2785000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 65% · séance 71% (101/152) · gap 32% · délai 0.0min · rebond 54% (56/101) (MFE +1.15%)
   - −1.0% : fill 30min 55% · séance 65% (93/152) · gap 22% · délai 0.2min · rebond 47% (47/93) (MFE +0.9%)
   - −1.5% : fill 30min 47% · séance 56% (83/152) · gap 19% · délai 1.4min · rebond 54% (46/83) (MFE +1.09%)
   - −2.0% : fill 30min 43% · séance 53% (77/152) · gap 16% · délai 3.6min · rebond 53% (39/77) (MFE +1.08%)
   - −3.0% : fill 30min 29% · séance 41% (62/152) · gap 9% · délai 7.5min · rebond 65% (39/62) (MFE +1.57%)
   - −4.0% : fill 30min 20% · séance 34% (54/152) · gap 5% · délai 21.6min · rebond 67% (39/54) (MFE +2.23%)
   - −5.0% : fill 30min 12% · séance 26% (41/152) · gap 3% · délai 57.8min · rebond 75% (30/41) (MFE +2.24%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −2.81%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −1.03% (p90 −2.51%) → stop au-delà de −1.94% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.91% (p90 −2.46%) → stop au-delà de −1.89% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=821 jambes) : jambe baissière méd −1.34% (p90 −3.28%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (47 séances) :
      · −1.0% : fill 95% (46/47) · rebond 36% (21/46)
      · −2.0% : fill 91% (42/47) · rebond 49% (20/42)
      · −3.0% : fill 80% (39/47) · rebond 65% (24/39)
      · −4.0% : fill 70% (35/47) · rebond 69% (24/35)
      · −5.0% : fill 51% (27/47) · rebond 83% (21/27)
   - **flat** (21 séances) :
      · −1.0% : fill 87% (17/21) · rebond 55% (10/17)
      · −2.0% : fill 48% (13/21) · rebond 31% (5/13)
      · −3.0% : fill 26% (8/21) · rebond 57% (5/8)
      · −4.0% : fill 26% (8/21) · rebond 54% (6/8)
      · −5.0% : fill 20% (4/21) · rebond 40% (2/4)
   - **gap-up** (84 séances) :
      · −1.0% : fill 39% (30/84) · rebond 60% (16/30)
      · −2.0% : fill 28% (22/84) · rebond 72% (14/22)
      · −3.0% : fill 18% (15/84) · rebond 66% (10/15)
      · −4.0% : fill 13% (11/84) · rebond 66% (9/11)
      · −5.0% : fill 10% (10/84) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 40% en base · 56% si les 15 1res min sont vertes (57 cas) · 32% si rouges (103 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **46min** → P(séance verte=clôture>ouverture) 73% si début vert vs 21% si rouge (base 40% · écart 51 pts) ; prédictivité sature ensuite (plafond brut 140min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=62) : tient le vert **73%** · continue >prix actuel 40% ; creux résiduel méd -1.69% (q20 -3.42%) → **SL/trailing à −3.42%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.48% / q75 +2.94% → **scale +1.48% / runner +2.94%**, sortie à la clôture
  - **si ROUGE au coude** (n=98) : edge inversé — récupère vert seulement **21%** (continue à baisser 52%) → **RÉDUIRE ~79%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.35%** (au-delà de la MAE q10 -5.35%), cible rebond +1.26% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-3.56% .. +3.86%] · haut q95 +5.86% · bas q05 -4.99%
   - 60min (n=160) : retour [-4.72% .. +3.18%] · haut q95 +5.91% · bas q05 -5.39%
   - 2h (n=160) : retour [-5.32% .. +3.61%] · haut q95 +6.1% · bas q05 -6.27%
   - 4h (n=160) : retour [-6.37% .. +4.53%] · haut q95 +6.12% · bas q05 -7.87%
   - 6h (n=160) : retour [-7.14% .. +5.0%] · haut q95 +6.31% · bas q05 -8.46%
   - session (n=160) : retour [-6.47% .. +5.32%] · haut q95 +6.31% · bas q05 -8.59%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (7) pour des stats fiables : 4.4% des séances seulement sont des jours de hausse propre — 298040 = **volatil sans tendance propre (choppy)** (vol intra méd 3.64%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : extreme
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.14 · part idiosyncratique 0.86
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 10.0  _(survente)_
- **ADX** : 18.7  _(pas de tendance nette)_
- **MACD** : hist -78881.406  _(pas de croisement recent)_
- **BB** : %B -0.07 · largeur 37.0%
- **ATR** : 131392.86 (24.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.318  _(distribution)_
- **Vol ratio** : 1.05  _(volume normal)_
- **Choppiness** : 25.4  _(marche directionnel)_
- **MA** : MA20 2701200.0 · MA50 2768120.0 · MA200 2851426.36  _(prix < MA20)_
- **Dist MA** : MA20 -21.0% · MA50 -22.9% · MA200 -25.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (597680 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
