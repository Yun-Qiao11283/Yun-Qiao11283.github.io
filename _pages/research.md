---
permalink: /research/
title: "Research"
author_profile: true
description: "Financial TDA: exploratory analysis of financial asset relationships using clustering, return diagnostics, and persistent homology."
---

<p class="profile-eyebrow">TOPOLOGICAL DATA ANALYSIS · QUANTITATIVE FINANCE</p>

## Financial TDA

**September 2025 – Present** · The Ohio State University<br>
Supervised by **Ph.D. Candidate Krnic Luci**

[View project on GitHub](https://github.com/Yun-Qiao11283/TDA){: .btn .btn--primary}

This Python project explores changing relationships between financial assets through **hierarchical clustering, return normality tests, PCA visualization, and persistent homology**. The pipeline downloads prices and exports charts and CSV files for exploratory research.

### Analysis workflow

1. **Download and prepare data.** By default, retrieve the first 80 symbols from the current S&P 500 constituent list on Wikipedia and add GLD, TLT, VIXY, and BTC-USD. Download adjusted closing prices with yfinance, keep weekdays, forward-fill missing prices, and compute percentage log returns. Retain assets with at least 95% return coverage and remove incomplete observations; returns are not backward-filled.
2. **Select representative assets.** Apply Ward hierarchical clustering to correlation distances and select the asset with the smallest mean within-cluster distance from each cluster, targeting at most 20 representatives by default.
3. **Explore distributions and structure.** Calculate skewness, kurtosis, Shapiro-Wilk and Jarque-Bera tests, and visualize distributions, Q-Q plots, PCA projections, and correlations. PCA is used only for visualization.
4. **Compute persistent homology.** Build Vietoris-Rips filtrations over rolling windows of 60 retained observations by default. Compute separate **H₀ and H₁ persistence landscape L₁ amplitudes**, export their time series, and generate a persistence diagram for the target date.

The correlation distance is **dᵢⱼ = √[2(1 − ρᵢⱼ)]**, where ρᵢⱼ is the Pearson correlation between asset returns within a window. H₀ describes connected components and H₁ describes loops. The network visualization uses a distance threshold, which does not limit the persistent homology filtration.

### Outputs

The pipeline exports selected-asset returns, normality statistics, and topology time series as CSV files, together with distribution plots, correlation and distance matrices, an asset network, H₀/H₁ amplitude plots, and a target-window persistence diagram. A three-dimensional PCA plot is generated when at least three assets are available.

### Scope & limitations

**This is an exploratory, retrospective analysis. It does not include strategy backtesting or an evaluation of market crisis prediction performance.** Landscape amplitudes summarize topology; they do not directly measure financial risk.

- The default pool uses current constituents, which introduces survivorship bias when applied to historical periods. Representatives are selected using the full analysis period.
- Trading calendars are not fully aligned. Forward-filled holiday prices and removed observations can affect correlations, and rolling windows count retained rows rather than consecutive exchange trading days.
- Landscape amplitudes use giotto-tda's default discretization and landscape layers, fitted separately for each window. They are not exact integrals on a shared fixed grid.

Potential extensions include historical constituent data, exchange calendar alignment, a shared landscape sampling grid, price caching, and out-of-sample event detection and backtesting.

### Code & documentation

See the [GitHub README](https://github.com/Yun-Qiao11283/TDA#readme) for Python 3.10 setup instructions, command-line options, output details, and the full reproducibility notes. The repository also includes a [project poster](https://github.com/Yun-Qiao11283/TDA/blob/HEAD/poster/TDA.pdf).

For questions about this work, please [contact me](mailto:qiao.247@osu.edu).
