# 298040

**Generated** : 2026-09-10T00:26:53.121251+00:00  
**Santé technique** : 6/10 — **Rating** : Pass  
_(score = santé technique durable ; le rating = tradabilité/EV. Timing d'entrée distinct ci-dessous — audit §A3.)_  
**Subtitle** : indeterminate · volatilite normal · ₩2931000.00  

> ❄️ **EVENT-FROZEN** — horizon gelé jusqu'au 2026-09-11 — US CPI (headline) (J-1 sess · macro taux)  
> ↳ spot ₩2931000.00 (+3.5% vs entrée) · entrée ₩2832150.05 · stop ₩2605578.05 · T1 ₩2897832.81 · R/R 0.29  
> ↳ P(T1 av. stop) 40 % _(réel 5 s)_ · EV/risk 0.009 _(réel 5 s)_ (GBM -0.133) · ¼-Kelly 0.024 · _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_  
> ↳ stop −8.0% cohérent avec le bruit 5 s (EV-optimal ≈ −8.0%)  

## Régime & alignement multi-TF

- **Daily** : range (trend-range)  
- **H4** : range | **H1** : range  
- **Flag multi-TF** : mixed (score 3)


## Lecture chartiste

Plan privilegie A (intraday), composite 6/10, conviction 'Pass'.


## Niveaux clés & plan principal

**Plan A — intraday** (order_type LMT)
- Entry (zone de repli) : ₩2819013.50–₩2845286.60 (mid ₩2832150.05)
- Spot actuel : ₩2931000.00 (+3.5% au-dessus de la zone — repli à attendre)
- Stop : ₩2605578.05 (stop swing_plan-based (-13.21%))
- Targets : T1 ₩2897832.81 · R/R 0.29 | T2 ₩2963515.57 · R/R 0.58 | T3 ₩3029198.33 · R/R 0.87
- Activation : entree LMT en attente de touche de zone
- Invalidation : close sous ₩2605578.05


## Risque mesuré — ce qui borne (et ce qui ne borne pas) la perte

- 🔴 **Régime de gap : gap_prone** — p_breach(-3 %)=3.21 % >= 3 % — franchissements FREQUENTS ; la reponse est une TAILLE plus faible, pas un stop plus large
- **Au stop du plan (13.21 %)** : le gap seul le franchit 0.0 % des séances (0 fois sur 1217).
   - exécution **— pt plus bas** dans le cas TYPIQUE (médiane), — au p90, **— au pire**
   - perte réelle **— %** en moyenne _(tirée par la queue)_, jusqu'à **— %** — au lieu des 13.21 % annoncés par la distance
   - coût AMORTI sur toutes les séances : 0.0 % _(ce que le gap coûte en moyenne, pas ce qu'il coûte le jour où il frappe)_
   - ⚠ seulement 0 franchissement(s) observé(s) : montants indicatifs, pas des espérances fiables. La médiane résiste mieux que la moyenne à un si petit nombre.
  - ⚠ **Sur un titre gap-prone, la réponse est une TAILLE plus faible, PAS un stop plus large** : élargir échange de la fréquence contre de la sévérité (T1). Ne jamais proposer d'élargir un stop en invoquant le gap.
- Chocs d'ouverture : p05 -2.467 % | p01 -4.658 % | pire -11.686 % _(sur 1217 séances)_
- **P(stop avant cible)** _(source : daily, 1218 séances — à préférer au 5 s sur swing et deep, où celui-ci ne dispose que d'une trentaine d'observations effectives)_ :
   - intraday : **0.0725** [0.0408 ; 0.1183] _(largeur 7.8 pt, n_eff 173.1)_
   - swing : **0.3698** [0.3202 ; 0.4216] _(largeur 10.1 pt, n_eff 345.6)_
   - deep : **0.3148** [0.2675 ; 0.3652] _(largeur 9.8 pt, n_eff 345.6)_
- ⚠ 5 s / deep : probabilite(s) EXACTEMENT nulle(s) : p_no_touch. Ce n'est PAS « jamais » — c'est « aucune occurrence sur 18.8 observations effectives », dont la borne haute a 95 % vaut environ 16.0 %.
- ⚠ **5 s — échantillon insuffisant sur : intraday (36.9 pt), swing (46.3 pt), deep (41.0 pt).** Ces chiffres peuvent être CITÉS, jamais servir à dimensionner ni à arbitrer entre deux plans.
- **VaR/CVaR à 1 j (fenêtre adaptative, 250 séances)** : VaR **-6.93 %** | CVaR **-9.26 %** | vol 4.99 %/j
   - _fenêtre arrêtée : rupture de regime a 240 seances en arriere (volatilite 3.60 % contre 5.98 % aujourd'hui, rapport 0.60)_
   - ⚠ le regime n'est homogene que sur 180 seances, sous le plancher de 250 necessaire a un 5e percentile. La fenetre a ete ETENDUE au plancher : elle inclut donc un regime anterieur different. A lire comme une borne, pas comme une mesure du regime courant.
   - _C'est CETTE fenêtre qu'il faut utiliser pour dimensionner : ni l'année civile (arbitraire) ni l'historique complet (qui mélange des régimes sans rapport)._
- 5 jours **mesuré** : VaR -11.96 % vs -12.61 % si l'on extrapolait par √5 _(rapport 0.949 ; < 1 = le √5 surestime)_
- **β de baisse : 1.0771** (β de hausse 0.9987, asymétrie 1.0785) vs KS11 — 552 séances de repli, historique complet


## Edge, scénarios & sizing

- EV/risk : -0.133 | EV/share : ₩-30061.758 | p_fill : —
- P(cible avant stop) _(first-passage MC, la proba OCO)_ : T1 44 % | T2 21 % | T3 20 %
- Kelly (position) : f* 0.095 | ¼-Kelly 0.024 _(fraction du capital ; ¼-Kelly recommandé ; Kelly ≤ 0 ⇒ mise optimale nulle ⇒ Pass, même si l'EV blended scale-out reste marginalement positive)_
- Calibration des probas : _first-passage 5 s RÉEL intra-séance (vrai ordre intrabar, n=80 séances) · non recalibrée track-record (n=0)_
- Régime probabiliste (posterior HMM, intraday) : bull 83.7 | bear 6.8 | side 9.5  _(probas d'ÉTAT de régime, bornées [5,85]% ; ≠ Monte-Carlo de l'EV ci-dessus)_
- Sizing : notional réel 0.0 (= 0 part(s) × prix) · cible 400.0


## Microstructure intraday (5 s réel · 80 séances)

- **First-passage & EV RÉELS par horizon** _(vérité terrain 5 s, **pondérés par récence** demi-vie ≈15.0 séances → régime des ~2-3 dernières semaines dominant ; entrée au DIP ; n_eff = échantillon effectif ; à comparer à l'EV GBM — le GBM tend à sur-estimer)_ :
  - **intraday** (entrée dip −3.37% → cible +2.319% / stop −8.0%, p_fill 51%, n_eff≈25.5) : P(cible|rempli) **40%** · **EV/risk +0.009** (×p_fill ; si rempli +0.14% du capital)
  - **swing** (entrée dip −7.42% → cible +5.186% / stop −6.254%, p_fill 23%, n_eff≈15.0) : P(cible|rempli) **28%** · **EV/risk -0.061** (×p_fill ; si rempli -1.69% du capital)
  - **deep** (entrée dip −11.464% → cible +7.334% / stop −9.81%, p_fill 25%, n_eff≈18.8) : P(cible|rempli) **36%** · **EV/risk -0.089** (×p_fill ; si rempli -3.50% du capital)
- Courbe de touche réelle (high atteint, en séance) : +0.5%→76% · +1.0%→61% · +2.0%→50% · +3.0%→36% · +5.0%→20% · +8.0%→5%
- Range intraday médian 6.81% (p90 10.49%) · excursion haute méd. +2.05% / basse méd. −3.94%
- Profil de vol intra : ouverture 4.524% vs midi 1.157% vs clôture 1.225% _(ouverture ~3.9× plus volatile → privilégier/éviter selon le setup)_
- **Asset Behavior Profiler** (160 séances, frais pipeline) : **choppy-dominant (trend-following risqué)** _(jours choppy 77% · range 22% · trend ↑0%/↓0% ; spike-down 82% · recovery-V 29%)_
- **Régime intraday** : **chop** _(efficiency 0.115 ; neutre — autocorr -0.021)_ ; drift intra méd. -1.117% ; recovery-V 32%
- **σ réalisé intraday** 4.102% (sans gap overnight) — le MC l'utilise pour l'horizon intraday (le σ daily, plus élevé, surestimait les touches)
- Opening range (30min) : cassure haut 40% / bas 58% / whipsaw 14%
- POC intraday (dernière séance, temps-au-prix) : 2704250.0 (VA 2689250.0–2731750.0 ; dernier close 2733000.0)


## 🎣 PRE-OUVERTURE FISHING — playbook début de séance (5 s)

_À appliquer au réveil ~30 min avant l'open US : où poser des limit/trailing buy AVANT l'ouverture (réf. = close de la veille), avec proba de remplissage et de rebond. Vérité terrain 5 s, pondérée récence._
- **▶ Plan recommandé** : achat **−5.0%** sous le close veille · fill 33% · rebond 75% · **stop −4.61%** sous le fill (sous le bruit) · cible +2.09% · R/R 0.45 (high win-rate)
- Gaps overnight (n=159) : méd. 0.91% · baisse 33% (gap-down >1% 25% · >2% 19%)
- Excursion ouverture 5min (n=160) : bas méd −1.61% (p90 −3.25%) · haut méd +0.66% · range méd 2.47%
- Excursion ouverture 15min (n=160) : bas méd −2.07% (p90 −4.21%) · haut méd +0.79% · range méd 3.14%
- Excursion ouverture 30min (n=160) : bas méd −2.44% (p90 −4.36%) · haut méd +0.81% · range méd 3.89%
- Excursion ouverture 60min (n=160) : bas méd −2.6% (p90 −5.28%) · haut méd +1.03% · range méd 4.42%
- **Niveaux d'achat fishing** (limit buy à −L% sous le close veille 2732000.0 ; rebond = P(prix +1.0% après fill, déclenche un réveil de gestion)) :
   - −0.5% : fill 30min 64% · séance 71% (108/159) · gap 30% · délai 0.1min · rebond 55% (64/108) (MFE +1.15%)
   - −1.0% : fill 30min 58% · séance 65% (100/159) · gap 25% · délai 0.3min · rebond 55% (58/100) (MFE +1.33%)
   - −1.5% : fill 30min 48% · séance 57% (89/159) · gap 23% · délai 1.2min · rebond 51% (52/89) (MFE +1.02%)
   - −2.0% : fill 30min 45% · séance 55% (80/159) · gap 19% · délai 2.8min · rebond 54% (43/80) (MFE +1.13%)
   - −3.0% : fill 30min 32% · séance 47% (68/159) · gap 12% · délai 6.3min · rebond 67% (44/68) (MFE +1.6%)
   - −4.0% : fill 30min 24% · séance 39% (58/159) · gap 7% · délai 14.3min · rebond 71% (43/58) (MFE +2.27%)
   - −5.0% : fill 30min 18% · séance 33% (45/159) · gap 5% · délai 24.2min · rebond 75% (33/45) (MFE +2.09%)
- **Stop « survie au bruit »** (creux NORMAL d'une trajectoire pourtant gagnante → ne jamais couper au-dessus) :
   - capter +1.0% : creux à tolérer méd −0.86% (p90 −3.39%) → stop au-delà de −2.41% (survit 80% du bruit)
   - capter +2.0% : creux à tolérer méd −0.97% (p90 −2.67%) → stop au-delà de −2.26% (survit 80% du bruit)
   - capter +3.0% : creux à tolérer méd −0.94% (p90 −2.63%) → stop au-delà de −2.2% (survit 80% du bruit)
- Zig-zag intra-séance (seuil 0.5% · n=854 jambes) : jambe baissière méd −1.38% (p90 −3.37%) · ~12.0 jambes/séance
- **Fishing selon l'ouverture** (tu vois le gap au pré-open ; comptes bruts entre parenthèses) :
   - **gap-down** (52 séances) :
      · −1.0% : fill 100% (52/52) · rebond 46% (29/52)
      · −2.0% : fill 91% (43/52) · rebond 43% (21/43)
      · −3.0% : fill 91% (42/52) · rebond 63% (26/42)
      · −4.0% : fill 89% (39/52) · rebond 73% (28/39)
      · −5.0% : fill 75% (32/52) · rebond 84% (25/32)
   - **flat** (18 séances) :
      · −1.0% : fill 80% (14/18) · rebond 57% (9/14)
      · −2.0% : fill 77% (13/18) · rebond 41% (6/13)
      · −3.0% : fill 43% (8/18) · rebond 59% (5/8)
      · −4.0% : fill 34% (7/18) · rebond 44% (5/7)
      · −5.0% : fill 25% (3/18) · rebond 24% (1/3)
   - **gap-up** (89 séances) :
      · −1.0% : fill 43% (34/89) · rebond 66% (20/34)
      · −2.0% : fill 29% (24/89) · rebond 78% (16/24)
      · −3.0% : fill 23% (18/89) · rebond 78% (13/18)
      · −4.0% : fill 12% (12/89) · rebond 79% (10/12)
      · −5.0% : fill 11% (10/89) · rebond 67% (7/10)
- **P(clôture VERTE) selon le drive 15min** (n=160) : 36% en base · 52% si les 15 1res min sont vertes (61 cas) · 29% si rouges (99 cas) — même proba, 3 conditions (l'écart = pouvoir prédictif)
- **Fenêtre du début la PLUS prédictive** (balayage 5min→228min, n=160) : COUDE à **46min** → P(séance verte=clôture>ouverture) 72% si début vert vs 18% si rouge (base 36% · écart 55 pts) ; prédictivité sature ensuite (plafond brut 150min ~trivial proche clôture)
- **GESTION si rempli & vert au coude** (cond. vert au coude, n=64) : tient le vert **72%** · continue >prix actuel 44% ; creux résiduel méd -1.9% (q20 -3.74%) → **SL/trailing à −3.74%** sous le prix (survit 80% du bruit) ; potentiel restant MFE méd +1.7% / q75 +3.78% → **scale +1.7% / runner +3.78%**, sortie à la clôture
  - **si ROUGE au coude** (n=96) : edge inversé — récupère vert seulement **18%** (continue à baisser 58%) → **RÉDUIRE ~82%** de la position, garder un petit runner (≈ taille des odds de récup.) à **stop large −5.68%** (au-delà de la MAE q10 -5.68%), cible rebond +1.51% ; ne PAS se contenter de serrer le SL (balayé sur le bruit)
- Bandes d'excursion forward depuis l'open (QUANTILES, pas des probas : 90% des séances entre q05 et q95) :
   - 30min (n=160) : retour [-4.18% .. +4.34%] · haut q95 +6.12% · bas q05 -5.24%
   - 60min (n=160) : retour [-5.24% .. +3.84%] · haut q95 +6.26% · bas q05 -5.95%
   - 2h (n=160) : retour [-6.01% .. +3.88%] · haut q95 +6.45% · bas q05 -6.83%
   - 4h (n=160) : retour [-6.89% .. +4.98%] · haut q95 +6.46% · bas q05 -9.06%
   - 6h (n=160) : retour [-7.53% .. +5.18%] · haut q95 +6.64% · bas q05 -9.14%
   - session (n=160) : retour [-6.97% .. +5.41%] · haut q95 +6.64% · bas q05 -9.3%


## 🚀 RIDER DE JOUR DE TENDANCE — playbook climb / autoloop (5 s, conditionné trend-up)

_Symétrique du fishing : quand l'actif imprime un JOUR DE HAUSSE PROPRE, on CHEVAUCHE la tendance (climb = monte TP+SL de concert ; autoloop = ré-entrée sur les replis qui rebondissent) au lieu de scalper le retour à la moyenne. Stats sur séances trend-up uniquement, pondérées récence. Observe-only._
- **Éligibilité** : 5.0% des séances sont trend-up (mild 0% / strong 5.0%) · base = 8 séances trend-up (n_eff 5.4)
- **ARMER** : fenêtre la + prédictive = **120 min** → P(reste trend-up à la clôture) **55%**. Lecture précoce 30 min : signature présente → 17% vs absente 0% (base 5%)
- **RIDER — replis (autoloop)** : profondeur médiane 0.98% (p75 1.53% / p90 2.47%) · ~4.0 replis/séance, durée méd 54.79 min. P(nouveau plus-haut après repli) :
   - −0.5% → **81%** (reprise méd 26.87 min, n=28)
   - −1.0% → **83%** (reprise méd 56.82 min, n=12)
   - −1.5% → **67%** (reprise méd 61.26 min, n=6)
   - −2.0% → **67%** (reprise méd None min, n=3)
- **RIDER — climb (trail + cibles)** : trail **−2.47%** (p90, défaut prudent ; serré/agressif −1.53%) ; extension open→close méd +5.76% (q75 +7.39% / q95 +8.29%), MFE méd +6.29% / q90 +9.17%
   - Échelle scale-out : +6.29% (33%) / +8.55% (33%) / +9.17% (34%)
- **DÉSARMER** : repli > **−2.47%** depuis le plus-haut = décay → P(retournement) **25%** (préavis méd 180.0 min, n=1) → CLIMB_STOP/AUTOLOOP_STOP. Blow-off > +9.17% : P(retournement après) 0% (mèche méd 0.97%)
- **CONTEXTE** : la dernière heure tient les gains 57% du temps (retour médian dernière heure +0.24%)


## Timing d'entrée (observe-only)

- **Verdict timing** : loin du support — entrée non optimale (chasing)
- Proximité zone : 0.0/2 | R/R T1 : 1.0 | extension : normal
_Le timing n'entre PAS dans le score de santé : un actif sain peut afficher un timing d'entrée défavorable (et inversement)._


## Positioning & factor

**Factor** : attribution factorielle indisponible
**Short/Insider** : SI —% | insider — | verdict neutral
**Options** : indisponible


## Event risk & invalidation

**Gate event par horizon** _(gel = ne pas ouvrir un plan qui couvrirait l'event)_ :
- **intraday** : ❄️ GELÉ jusqu'au 2026-09-11 — US CPI (headline) (J-1 sess · macro taux)
- **swing** : ❄️ GELÉ jusqu'au 2026-09-11 — US CPI (headline) (J-1 sess · macro taux)
- **deep** : ❄️ GELÉ jusqu'au 2026-09-11 — US CPI (headline) (J-1 sess · macro taux)


## Indicateurs (résumé)

- **RSI** : 52.4  _(neutre)_
- **ADX** : 8.2  _(pas de tendance nette)_
- **MACD** : hist 1591.732  _(bullish_recent)_
- **BB** : %B 0.59 · largeur 17.0%
- **ATR** : 169714.29 (48.0e pct 1a)  _(volatilite normale)_
- **OBV/CMF** : OBV falling · CMF 0.042  _(neutre)_
- **Vol ratio** : 0.75  _(volume normal)_
- **Choppiness** : 48.2  _(transition)_
- **MA** : MA20 2887000.0 · MA50 2822040.0 · MA200 2771165.48  _(prix > MA20)_
- **Dist MA** : MA20 +1.5% · MA50 +3.9% · MA200 +5.8%


---

_Bulletin compact généré depuis `<TICKER>_report_data.json` (487884 bytes source)._  
_Sans overlay Claude — fallback narratif pipeline baseline (à reviser pour enrichissement)._
