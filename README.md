# sir-model
A simple SIR model tested on COVID data from S-ward in Mumbai.
This code has been used for the Homi Bhabha Balvaidnyanik Competition in 2021 for the project round.

Python packages used in the project are:
```text
numpy
pandas
scipy
plotly
```

## Details about the model
The model used in this study follows the very first fundamental model described by Kermack and McKendrick in 1927. 
It is assumed that birth and death rates are negligible in comparison to rate of infection and are thus not considered in this model.
The equations describing the dynamics of the epidemic are :
```math
\frac{dS}{dt} = \frac{-\beta IS}{N}
```
```math
\frac{dI}{dt} = \frac{\beta IS}{N} - \gamma I
```
```math
\frac{dR}{dt} = \gamma I
```
where $S$ = Susceptible Population, $I$ = Infected Population, $R$ = Removed Population (Immune + Deceased) and $N = S+I+R$.

$\beta$ and $\gamma$ represent the rate of infection and rate of removal respectively.

The goal of the project was to estimate the value of $R_0$ (Basic Reproductive Number) for my locality and simulate the growth of COVID using numerical integration methods.
$R_0$ represents the expected number of cases directly generated by one case in a population where all individuals are susceptible to infection.

The estimated value for $R_0$ comes out to be 3.027.