# 267260

**Generated** : 2026-10-30T21:58:08.202939+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 1/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : trending · volatilite low · ₩424500.00  

> ⛔ **STAND-DOWN** — ENTRÉE RAREMENT ATTEINTE : l'entrée du plan est touchée dans 11/125 fenêtres (p_fill pondéré 8 %) — plan quasi jamais exécutable tel que construit ; EV conditionnelle non estimable  
> ↳ spot ₩424500.00 (+9.4% vs entrée) · entrée ₩388035.71 · stop ₩356992.86 · T1 ₩406267.86 · R/R 0.59  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

> ⚠ **QA flags (1, dont 0 high)** — champs SUSPECTS (la section data fraîche prime) :
>   - **[MEDIUM]** §04 Pitchfork — Position dans le canal -540 % hors [0,100] (R² max 0.84). Canal dégénéré (bornes possiblement sous le prix) — à ne pas interpréter.


## Régime & alignement multi-TF

- **Daily** : down (trend-down)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : triple_bearish (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 1/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-30 : 424500.0 · ATR Wilder 34839.94 (8.21 %)_
- **Swing** : plage **385873.35 → 363500.11** (-9.1 % a -14.37 % sous la cloture, 0.64 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 362314.52-379681.32 (A). stop INDICATIF 325612.56 (-10.42 % sous le bas ; sous le support 343032.52-360135.32 (- 0,5 ATR)).
- **Deep** : plage **363500.11 → 302601.67** (-14.37 % a -28.72 % sous la cloture, 1.75 ATR) — touchee 42 % → 15 % du temps en 20 seances ; supports reels dans la plage : 362314.52-379681.32 (A) ; 343032.52-360135.32 (B) ; 320476.2-333626.4 (B) ; 301968.41-316839.84 (B). stop INDICATIF 258735.04 (-14.5 % sous le bas ; sous le support 276155.01-290258.34 (- 0,5 ATR)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 7.94 ATR sous le plus haut 20 s., RSI(2) 11.0. Limite **407080.03** (seance suivante), stop catastrophe 267720.28, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 387011.08-404113.84 (B, -4.8 %) ; 362314.52-379681.32 (A, -10.56 %) ; 343032.52-360135.32 (B, -15.16 %) ; 320476.2-333626.4 (B, -21.41 %) ; 301968.41-316839.84 (B, -25.36 %) ; 276155.01-290258.34 (A, -31.62 %)
- Resistances reelles au-dessus : 472914.77-480358.35 (A, 11.41 %) ; 501200.32-516087.46 (A, 18.07 %) ; 537084.55-537084.55 (C, 26.52 %) ; 673000.0-673000.0 (C, 58.54 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=4.43 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (25.77 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 25.77 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.772 % | p01 -4.833 % | pire -11.715 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.084** [0.0495 ; 0.1323] _(largeur 8.3 pt, n_eff 173.1)_
   - swing : **0.27** [0.2253 ; 0.3186] _(largeur 9.3 pt, n_eff 345.6)_
   - deep : **0.2467** [0.2035 ; 0.2941] _(largeur 9.1 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 300 séances)** : VaR **-6.7 %** | CVaR **-8.92 %** | vol 4.32 %/j
   - _fenêtre arrêtée : rupture de regime a 360 seances en arriere (volatilite 2.89 % contre 4.89 % aujourd'hui, rapport 0.59)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.46 % vs -12.18 % si l'on extrapolait par √5 _(rapport 0.941 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0618** (β de hausse 0.8301, asymétrie 1.2792) vs KS11 — 554 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.076 | EV/share : ₩-2362.955 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 14 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 52.5 | bear 9.4 | side 38.2  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=9))
  - **swing** : indisponible (échantillon insuffisant (n=2, n_eff=2))
  - **deep** : indisponible (échantillon insuffisant (n=3, n_eff=3))
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
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 34% · rebond 74% · **stop −4.54%** sous le fill (sous le bruit) · cible +1.66% · R/R 0.37 (high win-rate)
- Gaps overnight (n=152) : méd. 0.13% · baisse 47% (gap-down >1% 26% · >2% 17%)
- Excursion ouverture 5min (n=160) : bas méd −1.55% (p90 −3.5%) · haut méd +0.71% · range méd 2.6%
- Excursion ouverture 15min (n=160) : bas méd −1.71% (p90 −4.15%) · haut méd +0.79% · range méd 3.15%
- Excursion ouverture 30min (n=160) : bas méd −1.95% (p90 −5.01%) · haut méd +0.84% · range méd 3.49%
- Excursion ouverture 60min (n=160) : bas méd −2.16% (p90 −5.22%) · haut méd +0.97% · range méd 3.66%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 470000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 69% · séance 76% (108/152) · gap 39% · délai 0.0min · rebond 50% (52/108) (MFE +0.98%)
   - −1.0% : fill 30min 61% · séance 72% (101/152) · gap 26% · délai 0.0min · rebond 53% (55/101) (MFE +1.18%)
   - −1.5% : fill 30min 54% · séance 70% (96/152) · gap 21% · délai 0.3min · rebond 57% (58/96) (MFE +1.16%)
   - −2.0% : fill 30min 47% · séance 64% (89/152) · gap 17% · délai 1.1min · rebond 55% (56/89) (MFE +1.23%)
   - −3.0% : fill 30min 36% · séance 55% (75/152) · gap 12% · délai 3.3min · rebond 67% (53/75) (MFE +1.62%)
   - −4.0% : fill 30min 27% · séance 42% (58/152) · gap 6% · délai 7.2min · rebond 59% (39/58) (MFE +1.45%)
   - −5.0% : fill 30min 18% · séance 34% (45/152) · gap 3% · délai 10.2min · rebond 74% (33/45) (MFE +1.66%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.91% (p90 −3.05%) → stop au-delà de −2.08% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.95% (p90 −3.0%) → stop au-delà de −2.02% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −1.01% (p90 −3.82%) → stop au-delà de −3.03% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=829 jambes) : jambe baissière méd −1.21% (p90 −3.22%) · ~10.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (54 séances) :
      · −1.0% : fill 100% (54/54) · rebond 46% (26/54)
      · −2.0% : fill 100% (53/54) · rebond 51% (31/53)
      · −3.0% : fill 88% (47/54) · rebond 69% (33/47)
      · −4.0% : fill 68% (37/54) · rebond 60% (25/37)
      · −5.0% : fill 58% (30/54) · rebond 79% (24/30)
   - **flat** (17 séances) :
      · −1.0% : fill 98% (16/17) · rebond 70% (10/16)
      · −2.0% : fill 71% (12/17) · rebond 43% (8/12)
      · −3.0% : fill 61% (10/17) · rebond 50% (6/10)
      · −4.0% : fill 45% (8/17) · rebond 76% (5/8)
      · −5.0% : fill 45% (8/17) · rebond 82% (6/8)
   - **gap-up** (81 séances) :
      · −1.0% : fill 41% (31/81) · rebond 57% (19/31)
      · −2.0% : fill 31% (24/81) · rebond 72% (17/24)
      · −3.0% : fill 24% (18/81) · rebond 68% (14/18)
      · −4.0% : fill 19% (13/81) · rebond 46% (9/13)
      · −5.0% : fill 9% (7/81) · rebond 33% (3/7)
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

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.2 · part idiosyncratique 0.8
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : 🟢 LIVE
- **swing** : 🟢 LIVE
- **deep** : 🟢 LIVE


## Indicateurs (résumé)

- **RSI** : 22.6  _(survente)_
- **ADX** : 46.5  _(tendance tres forte)_
- **MACD** : hist -4187.801  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 62.6%
- **ATR** : 36464.29 (14.0e pct 1a)  _(volatilite basse)_
- **OBV/CMF** : OBV falling · CMF -0.046  _(neutre)_
- **Vol ratio** : 1.22  _(volume normal)_
- **Choppiness** : 46.7  _(transition)_
- **MA** : MA20 532600.0 · MA50 652620.0 · MA200 884500.92  _(prix < MA20)_
- **Dist MA** : MA20 -20.3% · MA50 -35.0% · MA200 -52.0%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (498447 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
