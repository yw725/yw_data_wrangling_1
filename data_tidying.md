data\_tidying
================
yuning wang
9/24/2019

``` r
knitr::opts_chunk$set(echo = TRUE)

library(tidyverse)
```

## Wide to Long

``` r
pulse_data = haven::read_sas("./data/public_pulse_data.sas7bdat") %>%
  janitor::clean_names() %>%
  pivot_longer(
    bdi_score_bl:bdi_score_12m,
    names_to = "visit",
    names_prefix = "bdi_score_",
    values_to = "bdi"
    ) %>%
  mutate(
    visit = recode(visit, "bl" = "00m")
  )
```
