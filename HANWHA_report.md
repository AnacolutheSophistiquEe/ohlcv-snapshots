# 012450

**Generated** : 2026-10-27T21:59:18.914252+00:00  
**Couverture** : bulletin complet  
**Santé technique** : 4/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩768000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)  
> ↳ spot ₩768000.00 (+7.9% vs entrée) · entrée ₩711678.57 · stop ₩654744.29 · T1 ₩739839.29 · R/R 0.49  
> ↳ ¼-Kelly 0.0 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : down | **H1** : down  
- **Flag multi-TF** : mixed (score 1)


## Lecture chartiste

Plan privilegie A (intraday), composite 4/10, conviction 'Pass'.


## Plans d'achat — Swing / Deep (methode v4)

_Cloture 2026-10-27 : 768000.0 · ATR Wilder 54790.69 (7.13 %)_
- **Swing** : plage **700592.51 → 664062.69** (-8.78 % a -13.53 % sous la cloture, 0.67 ATR) — touchee 50 % → 30 % du temps en 10 seances ; supports reels dans la plage : 695359.79-714206.92 (C). stop INDICATIF 603487.43 (-9.12 % sous le bas ; sous le support 630882.78-639810.36 (- 0,5 ATR)).
- **Deep** : plage **664062.69 → 569290.34** (-13.53 % a -25.87 % sous la cloture, 1.73 ATR) — touchee 43 % → 15 % du temps en 20 seances ; supports reels dans la plage : 630882.78-639810.36 (B) ; 587236.78-603108.04 (A). stop INDICATIF 514499.65 (-9.62 % sous le bas ; 1 ATR sous le bas de la plage (aucun support proche)).
- 🟢 **ACHAT PAS CHER actif** (DD20) : 6.26 ATR sous le plus haut 20 s., RSI(2) 28.3. Limite **740604.66** (seance suivante), stop catastrophe 521441.91, sortie : vente a l'ouverture qui suit la 1re cloture au-dessus de la MM5, au plus tard 21 seances.
- Supports reels sous le cours (pour le Warden) : 695359.79-714206.92 (C, -7.0 %) ; 630882.78-639810.36 (B, -16.69 %) ; 587236.78-603108.04 (A, -21.47 %) ; 387638.51-438939.65 (A, -42.85 %) ; 359721.44-380768.98 (A, -50.42 %) ; 323204.22-346911.95 (B, -54.83 %)
- Resistances reelles au-dessus : 802490.8-806458.62 (A, 4.49 %) ; 831257.47-857048.28 (A, 8.24 %) ; 862000.0-885814.95 (A, 12.24 %) ; 891766.7-918549.41 (A, 16.12 %)
- _Swing et Deep sont des PLAGES d'achat contigues (decote croissante) : il n'y a pas de point optimal, la profondeur fait l'avantage (rejeu 2001-2026), pas l'emplacement exact d'un niveau ; le stop est INDICATIF, le Warden decide ; le signal ACHAT PAS CHER est le seul avantage prouve contre un achat au hasard._


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🟠 **Régime de gap : intermediaire** — p_breach(-3 %)=1.48 % — entre les deux regimes ; ni queue pure ni franchissement ordinaire
- **Au stop du plan (22.0 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1219).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 22.0 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
- Chocs d'ouverture : p05 -1.855 % | p01 -3.826 % | pire -13.219 % _(sur 1219 séances)_
- **P(stop avant cible)** _(source : daily, 1220 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0593** [0.0312 ; 0.102] _(largeur 7.1 pt, n_eff 173.1)_
   - swing : **0.3224** [0.2748 ; 0.373] _(largeur 9.8 pt, n_eff 345.6)_
   - deep : **0.2527** [0.2091 ; 0.3004] _(largeur 9.1 pt, n_eff 345.6)_
- **VaR/CVaR à 1 j (fenêtre adaptative, 660 séances)** : VaR **-6.05 %** | CVaR **-8.04 %** | vol 4.09 %/j
   - _fenêtre arrêtée : rupture de regime a 720 seances en arriere (volatilite 2.54 % contre 4.15 % aujourd'hui, rapport 0.61)_
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -10.67 % vs -12.04 % si l'on extrapolait par √5 _(rapport 0.887 ; < 1 = le √5 surestime)_
- **β de baisse : 0.5366** (β de hausse 0.2954, asymétrie 1.8165) vs KS11 — 555 séances de repli, historique complet
   - ⚠ le β de baisse récent vaut 0.265× celui de l'historique complet : la sensibilité du titre au marché a changé.


## Edge, scénarios & sizing

- EV/risk : -0.066 | EV/share : ₩-3775.286 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 20 % | T2 — | T3 —
- Kelly (position) : f* 0.0 | ¼-Kelly 0.0 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=125 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 70.0 | bear 25.0 | side 5.0  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel — (= 0 part(s) × prix) · cible 0.0


## Microstructure intraday (5 s réel · 125 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈None séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** : indisponible (échantillon insuffisant (n=11, n_eff=10))
  - **swing** : indisponible (échantillon insuffisant (n=1, n_eff=1))
  - **deep** : indisponible (échantillon insuffisant (n=1, n_eff=1))
- Courbe de touche réelle (high atteint, en séance) : +0.5%→78% · +1.0%→63% · +2.0%→41% · +3.0%→27% · +5.0%→14% · +8.0%→3%
- Range intraday médian 5.62% (p90 9.0%) · excursion haute méd. +1.7% / basse méd. −2.92%
- Profil de vol intra : ouverture 4.06% vs midi 1.055% vs clôture 1.136% _(ouverture ~3.8× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 78% · range 15% · trend ↑0%/↓6% ; spike-down 77% · recovery-V 32%)_
- **Régime intraday** : **chop** _(efficiency 0.157 ; mean-reverting — autocorr -0.031)_ ; drift intra méd. -1.035% ; recovery-V 34%
- **σ réalisé intraday** 3.383% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 42% / bas 57% / whipsaw 8%
- POC intraday (dernière séance, temps-au-prix) : 784437.5 (VA 779537.5–791787.5 ; dernier close 787000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−4.0%** sous le close veille · fill 36% · rebond 74% · **stop −4.08%** sous le fill (sous le bruit) · cible +1.93% · R/R 0.47 (high win-rate)
- Gaps overnight (n=152) : méd. 0.2% · baisse 33% (gap-down >1% 14% · >2% 7%)
- Excursion ouverture 5min (n=160) : bas méd −1.42% (p90 −3.11%) · haut méd +0.79% · range méd 2.58%
- Excursion ouverture 15min (n=160) : bas méd −1.95% (p90 −4.62%) · haut méd +1.02% · range méd 3.23%
- Excursion ouverture 30min (n=160) : bas méd −2.16% (p90 −4.73%) · haut méd +1.03% · range méd 3.64%
- Excursion ouverture 60min (n=160) : bas méd −2.22% (p90 −4.94%) · haut méd +1.09% · range méd 4.22%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 792000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 71% · séance 79% (116/152) · gap 25% · délai 0.0min · rebond 56% (62/116) (MFE +1.2%)
   - −1.0% : fill 30min 61% · séance 71% (105/152) · gap 14% · délai 0.1min · rebond 57% (55/105) (MFE +1.13%)
   - −1.5% : fill 30min 51% · séance 59% (88/152) · gap 10% · délai 0.5min · rebond 53% (43/88) (MFE +1.16%)
   - −2.0% : fill 30min 41% · séance 53% (81/152) · gap 7% · délai 1.8min · rebond 60% (46/81) (MFE +1.25%)
   - −3.0% : fill 30min 32% · séance 46% (68/152) · gap 1% · délai 10.2min · rebond 68% (43/68) (MFE +1.42%)
   - −4.0% : fill 30min 18% · séance 36% (54/152) · gap 1% · délai 31.9min · rebond 74% (39/54) (MFE +1.93%)
   - −5.0% : fill 30min 11% · séance 23% (37/152) · gap 1% · délai 31.9min · rebond 64% (28/37) (MFE +1.56%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.82% (p90 −2.52%) → stop au-delà de −2.01% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.85% (p90 −2.59%) → stop au-delà de −1.97% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.82% (p90 −2.63%) → stop au-delà de −1.77% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=779 jambes) : jambe baissière méd −1.23% (p90 −3.2%) · ~9.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (42 séances) :
      · −1.0% : fill 100% (42/42) · rebond 52% (18/42)
      · −2.0% : fill 93% (38/42) · rebond 55% (19/38)
      · −3.0% : fill 86% (36/42) · rebond 69% (22/36)
      · −4.0% : fill 73% (31/42) · rebond 67% (20/31)
      · −5.0% : fill 56% (25/42) · rebond 62% (19/25)
   - **flat** (29 séances) :
      · −1.0% : fill 86% (25/29) · rebond 74% (17/25)
      · −2.0% : fill 61% (19/29) · rebond 65% (11/19)
      · −3.0% : fill 52% (14/29) · rebond 65% (8/14)
      · −4.0% : fill 38% (11/29) · rebond 91% (9/11)
      · −5.0% : fill 12% (5/29) · rebond 32% (2/5)
   - **gap-up** (81 séances) :
      · −1.0% : fill 47% (38/81) · rebond 51% (20/38)
      · −2.0% : fill 25% (24/81) · rebond 67% (16/24)
      · −3.0% : fill 18% (18/81) · rebond 70% (13/18)
      · −4.0% : fill 12% (12/81) · rebond 78% (10/12)
      · −5.0% : fill 7% (7/81) · rebond 100% (7/7)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 41% en base · 76% si les 15 1res min sont vertes (55 cas) · 24% si rouges (105 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **40min** → P(séance verte=clôture>ouverture) 86% si début vert vs 22% si rouge (base 41% · écart 64 pts) ; prédictivité sature ensuite (plafond brut 184min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=53) : tient le vert **86%** · continue >prix actuel 42% ; creux résiduel méd -1.29% (q20 -3.18%) → **SL/trailing à −3.18%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.65% / q75 +3.71% → **scale +1.65% / runner +3.71%**, sortie à la clôture
  - **si ROUGE au coude** (n=107) : edge inversé — récupère vert seulement **22%** (continue à baisser 57%) → **RÉDUIRE ~78%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −4.89%** (au-delà de la MAE q10 -4.89%), cible rebond +1.3% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-5.0% .. +3.65%] · haut q95 +4.67% · bas q05 -6.13%
   - 60min (n=160) : retour [-5.02% .. +3.72%] · haut q95 +5.84% · bas q05 -6.24%
   - 2h (n=160) : retour [-6.64% .. +3.9%] · haut q95 +6.91% · bas q05 -8.36%
   - 4h (n=160) : retour [-7.24% .. +5.54%] · haut q95 +7.14% · bas q05 -8.39%
   - 6h (n=160) : retour [-6.85% .. +5.19%] · haut q95 +7.44% · bas q05 -8.73%
   - session (n=160) : retour [-6.58% .. +5.09%] · haut q95 +7.44% · bas q05 -8.73%


## 🚀 RIDER DE JOUR DE TENDANCE — non disponible

_Trop peu de séances trend-up (1) pour des stats fiables : 0.6% des séances seulement sont des jours de hausse propre — 012450 = **volatil sans tendance propre (choppy)** (vol intra méd 3.52%). La stratégie « rider » réduit / s'abstient (la pêche aux gaps reste l'angle adapté)._


## Timing d'entrée (observe-only)

- **Verdict timing** : survente — dip présent, entrée sur faiblesse (favorable au dip-buy)
- Proximité zone : 0.25/2 | R/R T1 : 1.0 | extension : stretched_down
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : R² 0.19 · part idiosyncratique 0.81
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-10-28 — US FOMC Rate Decision (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 22.8  _(survente)_
- **ADX** : 17.9  _(pas de tendance nette)_
- **MACD** : hist -10214.589  _(pas de croisement recent)_
- **BB** : %B 0.18 · largeur 45.5%
- **ATR** : 56321.43 (28.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF -0.127  _(distribution)_
- **Vol ratio** : 0.77  _(volume normal)_
- **Choppiness** : 39.0  _(transition)_
- **MA** : MA20 897450.0 · MA50 1014980.0 · MA200 1165310.0  _(prix < MA20)_
- **Dist MA** : MA20 -14.4% · MA50 -24.3% · MA200 -34.1%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (478874 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
