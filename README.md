# FundSleuth — AI Portfolio Intelligence & Mutual Fund X-Ray

[![Java 17](https://img.shields.io/badge/Java-17-orange.svg)](https://www.oracle.com/java/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2.4-brightgreen.svg)](https://spring.io/projects/spring-boot)
[![Build](https://github.com/surana-rishabh/FundSleuth/actions/workflows/maven.yml/badge.svg)](https://github.com/surana-rishabh/FundSleuth/actions/workflows/maven.yml)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

FundSleuth is a wealth-management analytics platform for examining mutual-fund portfolios, revealing stock-level overlap, identifying concentration and portfolio-health risks, and estimating the long-term cost of distributor commissions.

## What it does

- **Portfolio overlap analysis:** Maps schemes and underlying stocks to surface hidden diversification risk.
- **Portfolio health scoring:** Produces a 0–100 score using overlap, expense ratios, and risky-stock exposure.
- **Sector concentration alerts:** Flags portfolios where a sector exceeds the configured concentration threshold.
- **Stock health inspection:** Groups holdings into profitable, stagnant/high-valuation, and loss-making/high-risk categories.
- **Cost-drag estimation:** Compares the projected impact of regular-plan commissions over five- and ten-year periods.
- **Actionable recommendations:** Generates prioritized restructuring steps.
- **Portfolio input support:** Includes CAS PDF and portfolio screenshot workflows.
- **Interactive reporting:** Provides charts, network visualizations, voice summaries, and PDF export in the browser UI.

## Technology

- **Backend:** Java 17, Spring Boot 3.2.4, Apache PDFBox, and JGraphT
- **Frontend:** HTML5, Bootstrap 5.3, custom CSS, Chart.js, Vis.js Network, Font Awesome, and Plus Jakarta Sans
- **Build:** Apache Maven
- **Delivery:** Spring Boot serves the packaged UI from `src/main/resources/static`

## Requirements

- JDK 17 or newer
- Apache Maven 3.8 or newer

## Run locally

```bash
git clone https://github.com/surana-rishabh/FundSleuth.git
cd FundSleuth

# Compile the application
mvn clean compile

# Run the application
mvn spring-boot:run
```

Open [http://localhost:8080](http://localhost:8080) after the application starts.

## Verify changes

Run the test suite before opening a pull request:

```bash
mvn test
```

Every push and pull request also runs the Maven build through GitHub Actions.

## Repository layout

```text
src/main/java/                 Spring Boot application code
src/main/resources/static/     Packaged HTML, CSS, and JavaScript UI
src/test/java/                 Automated tests
pom.xml                        Maven build and dependency configuration
```

## License

This project is licensed under the MIT License.
