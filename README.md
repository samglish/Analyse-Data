# FORMATION, MODULE : ANALYSE DE DONNEES

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## Chargement des données

```{r}
data <- read.csv("donnees_patients.csv")
head(data)
```

## Statistiques descriptives

### Âge moyen

```{r}
mean(data$Age)
```

### Répartition par sexe

```{r}
table(data$Sexe)
barplot(table(data$Sexe), col=c("skyblue", "pink"))
```

### Maladie : Oui / Non

```{r}
table(data$Maladie)
barplot(table(data$Maladie), col=c("green", "red"))
```

### Croisement Sexe vs Maladie

```{r}
table(data$Sexe, data$Maladie)
```

## Histogramme des âges

```{r}
hist(data$Age, col="lightblue", main="Distribution des âges", xlab="Âge")
```
