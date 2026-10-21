# 267260

**Generated** : 2026-10-21T21:53:27.038575+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : strong_trend · volatilite low · ₩499000.00  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 11/125 fenêtres (p_fill pondéré 8 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot ₩499000.00 (+8.9% vs entrée) · entrée ₩458250.00 · stop ₩421590.00 · T1 ₩478625.00 · R/R 0.56  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -148 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-21 : 499000.0 · ATR Wilder 39201.17 (7.86 %)_
- **Swing** : plage **455719.43 → 431124.18** (-8.67 % a -13.6 % sous la cloture, 0.63 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 426591.77-439785.35 (A). stop INDICATIF 384513.29 (-10.81 % sous le bas ; sous le support 404113.88-414854.93 (- 0,5 ATR)).
- **Deep** : plage **431124.18 → 366049.84** (-13.6 % a -26.64 % sous la cloture, 1.66 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 426591.77-439785.35 (A) ; 404113.88-414854.93 (A) ; 379192.67-397761.41 (A) ; 352922.99-371374.28 (A). stop INDICATIF 310129.44 (-15.28 % sous le bas ; sous le support 329730.02-343032.56 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.1 ATR sous le plus haut 20 s., RSI(2) 42.5. Limite **479399.41** (seance suivante), stop catastrophe 322594.72, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 472914.77-480358.35 (A, -3.74 %) ; 426591.77-439785.35 (A, -11.87 %) ; 404113.88-414854.93 (A, -16.86 %) ; 379192.67-397761.41 (A, -20.29 %) ; 352922.99-371374.28 (A, -25.58 %) ; 329730.02-343032.56 (B, -31.26 %)
- Resistances reelles au-dessus : 537084.55-537084.55 (C, 7.63 %) ; 673000.0-691000.0 (B, 34.87 %) ; 698000.0-715779.98 (A, 39.88 %) ; 730462.3-748326.87 (A, 46.39 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.27 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (24.5 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 24.5 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.713 % | p01 -4.833 % | pire -11.715 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0888** [0.0532 ; 0.138] _(largeur 8.5 pt, n_eff 173.1)_
   - swing : **0.3003** [0.2538 ; 0.3501] _(largeur 9.6 pt, n_eff 345.6)_
   - deep : **0.2515** [0.208 ; 0.2992] _(largeur 9.1 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.98 %** | CVaR **-9.24 %** | vol 4.54 %/j
   - _fenêtre arrêtée : rupture de regime a 300 seances en arriere (volatilite 2.89 % contre 5.02 % aujourd'hui, rapport 0.58)_
   - ⚠ le regime n'est homogene que sur 240 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.4 % vs -12.2 % si l'on extrapolait par √5 _(rapport 0.934 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0626** (β de hausse 0.8447, asymétrie 1.2581) vs KS11 — 555 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.063 | EV/share : ₩-2311.432 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 15 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 62.4 | bear 25.3 | side 12.3  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=11))
  - **swing** : indisponible (échantillon insuffisant (n=3, n_eff=3))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→81% · +1.0%→65% · +2.0%→44% · +3.0%→29% · +5.0%→10% · +8.0%→3%
- Range intraday médian 5.43% (p90 9.76%) · excursion haute méd. +1.61% / basse méd. −3.14%
- Profil de vol intra : ouverture 3.843% vs midi 1.047% vs clôture 1.133% _(ouverture ~3.7× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 88% · range 12% · trend ↑0%/↓0% ; spike-down 83% · recovery-V 27%)_
- **Régime intraday** : **chop** _(efficiency 0.117 ; mean-reverting — autocorr -0.093)_ ; drift intra méd. -0.48% ; recovery-V 24%
- **σ réalisé intraday** 3.079% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 48% / bas 59% / whipsaw 12%
- POC intraday (dernière séance, temps-au-prix) : 670212.5 (VA 668787.5–678762.5 ; dernier close 676000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 25% · rebond 73% · **stop −4.4%** sous le fill (sous le bruit) · cible +2.21% · R/R 0.5 (high win-rate)
- Gaps overnight (n=152) : méd. 0.37% · baisse 41% (gap-down >1% 22% · >2% 12%)
- Excursion ouverture 5min (n=160) : bas méd −1.48% (p90 −3.62%) · haut méd +0.73% · range méd 2.47%
- Excursion ouverture 15min (n=160) : bas méd −1.66% (p90 −3.95%) · haut méd +0.84% · range méd 2.96%
- Excursion ouverture 30min (n=160) : bas méd −1.82% (p90 −4.62%) · haut méd +0.95% · range méd 3.19%
- Excursion ouverture 60min (n=160) : bas méd −1.95% (p90 −4.76%) · haut méd +1.08% · range méd 3.55%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 678000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 66% · séance 74% (104/152) · gap 34% · délai 0.0min · rebond 52% (51/104) (MFE +1.05%)
   - −1.0% : fill 30min 57% · séance 68% (97/152) · gap 22% · délai 0.0min · rebond 57% (55/97) (MFE +1.29%)
   - −1.5% : fill 30min 51% · séance 65% (90/152) · gap 18% · délai 0.3min · rebond 62% (56/90) (MFE +1.26%)
   - −2.0% : fill 30min 44% · séance 58% (82/152) · gap 12% · délai 1.1min · rebond 68% (56/82) (MFE +1.78%)
   - −3.0% : fill 30min 32% · séance 47% (67/152) · gap 8% · délai 3.4min · rebond 70% (48/67) (MFE +1.77%)
   - −4.0% : fill 30min 20% · séance 34% (51/152) · gap 4% · délai 8.6min · rebond 74% (37/51) (MFE +1.72%)
   - −5.0% : fill 30min 12% · séance 25% (39/152) · gap 2% · délai 37.1min · rebond 73% (29/39) (MFE +2.21%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.88% (p90 −3.14%) → stop au-delà de −2.06% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.99% (p90 −3.0%) → stop au-delà de −2.07% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.08% (p90 −3.96%) → stop au-delà de −3.05% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=825 jambes) : jambe baissière méd −1.15% (p90 −3.12%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (51 séances) :
      · −1.0% : fill 100% (51/51) · rebond 53% (27/51)
      · −2.0% : fill 99% (48/51) · rebond 67% (31/48)
      · −3.0% : fill 82% (42/51) · rebond 75% (30/42)
      · −4.0% : fill 61% (33/51) · rebond 76% (24/33)
      · −5.0% : fill 47% (26/51) · rebond 77% (21/26)
   - **flat** (16 séances) :
      · −1.0% : fill 97% (15/16) · rebond 65% (9/15)
      · −2.0% : fill 66% (11/16) · rebond 55% (8/11)
      · −3.0% : fill 54% (9/16) · rebond 34% (5/9)
      · −4.0% : fill 35% (7/16) · rebond 63% (4/7)
      · −5.0% : fill 35% (7/16) · rebond 72% (5/7)
   - **gap-up** (85 séances) :
      · −1.0% : fill 39% (31/85) · rebond 59% (19/31)
      · −2.0% : fill 28% (23/85) · rebond 79% (17/23)
      · −3.0% : fill 19% (16/85) · rebond 75% (13/16)
      · −4.0% : fill 13% (11/85) · rebond 72% (9/11)
      · −5.0% : fill 6% (6/85) · rebond 55% (3/6)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 35% en base · 42% si les 15 1res min sont vertes (61 cas) · 32% si rouges (99 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **1:30** → P(séance verte=clôture>ouverture) 76% si début vert vs 13% si rouge (base 35% · écart 63 pts) ; prédictivité sature ensuite (plafond brut 176min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=63) : tient le vert **76%** · continue >prix actuel 52% ; creux résiduel méd -1.32% (q20 -3.55%) → **SL/trailing à −3.55%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.42% / q75 +2.59% → **scale +1.42% / runner +2.59%**, sortie à la clôture
  - **si ROUGE au coude** (n=97) : edge inversé — récupère vert seulement **13%** (continue à baisser 49%) → **RÉDUIRE ~85%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.23%** (au-delà de la MAE q10 -4.23%), cible rebond +0.97% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.33% .. +2.67%] · haut q95 +3.81% · bas q05 -5.1%
   - 60min (n=160) : retour [-5.12% .. +2.44%] · haut q95 +4.27% · bas q05 -5.68%
   - 2h (n=160) : retour [-5.67% .. +3.46%] · haut q95 +4.58% · bas q05 -6.42%
   - 4h (n=160) : retour [-6.35% .. +3.35%] · haut q95 +4.79% · bas q05 -7.79%
   - 6h (n=160) : retour [-6.77% .. +4.49%] · haut q95 +5.4% · bas q05 -8.54%
   - session (n=160) : retour [-6.53% .. +4.5%] · haut q95 +5.73% · bas q05 -8.69%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (2) pour des stats fiables : 1.3% des séances seulement sont des jours de hausse propre — 267260 = **volatil sans tendance propre (choppy)** (vol intra méd 3.48%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.18 · part idiosyncratique 0.82
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-5 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-5 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 21.8  _(survente)_
- **ADX** : 35.4  _(tendance etablie)_
- **MACD** : hist -12034.685  _(pas de croisement recent)_
- **BB** : %B 0.15 · largeur 55.2%
- **ATR** : 40750.0 (21.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.19  _(distribution)_
- **Vol ratio** : 0.71  _(volume normal)_
- **Choppiness** : 34.8  _(marche directionnel)_
- **MA** : MA20 618225.0 · MA50 696772.17 · MA200 896303.24  _(prix < MA20)_
- **Dist MA** : MA20 -19.3% · MA50 -28.4% · MA200 -44.3%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (475402 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
