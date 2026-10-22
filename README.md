# What really drives an electric car's range and efficiency? (R analysis)

A statistical study of **478 electric-vehicle models (2025 specifications)** in R Markdown. It asks five questions and answers each with regression, non-parametric tests and ANOVA:

1. Which factors drive energy efficiency (Wh/km)?
2. Do "sporty" EVs (fast 0–100 km/h) sacrifice range?
3. Do EV-native brands differ from traditional carmakers?
4. How much of the range does battery capacity explain?
5. Do size, body type and number of seats affect efficiency and range?

## Main findings

- **Battery capacity is the strongest predictor of range.** A simple linear model explains about 77 % of its variance.
- **There is no petrol-style trade-off between performance and range.** Faster cars tend to have more range, about 27 km more per second saved on the 0–100 time, because they also carry larger batteries and premium drivetrains.
- **Brand origin doesn't explain the specs.** EV-native and traditional brands only differ in acceleration, and that gap disappears once the model controls for sporty cars.
- **Efficiency depends on the drivetrain more than on physical size.** Length, width and height add little.
- **Seats and body type matter** (significant ANOVA): more seats means lower efficiency, SUVs and crossovers consume more but carry bigger batteries, and compact cars are the most efficient.

The report closes with the data's limits: no price, no motor power, no weight, and test-cycle figures rather than real-world use.

## Files

- `ProyectoAnalisis.Rmd`: source (Spanish).
- `ProyectoAnalisis.html`: knitted report. Download it or view it through GitHub Pages.
- `styles.css`: report styling.

## Data

`electric_vehicles_spec_2025.csv`: 478 models and 22 columns (battery, range, efficiency, acceleration, dimensions, body type and more), compiled from [ev-database.org](https://ev-database.org). Its licence isn't clear, so the file isn't committed. To re-knit the report, place the CSV next to the `.Rmd`.

## Stack

R, RStudio, R Markdown, readr, dplyr, ggplot2; linear and multiple regression, Wilcoxon / Mann-Whitney tests, ANOVA.

## Team

Carlos Tesoriero and Juan Camilo Fajardo. Final project for *Análisis de Datos*, AI Engineering, Tecnun – Universidad de Navarra, November 2025.
