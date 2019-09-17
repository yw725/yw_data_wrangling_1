Data Import
================
Yuning Wang
9/17/2019

## Load in a dataset

``` r
## reads in a dataset
#absolute path & relative path, use relative path!
litters_data = read_csv(file = "./data/FAS_litters.csv")
head(litters_data)
```

    ## # A tibble: 6 x 8
    ##   Group `Litter Number` `GD0 weight` `GD18 weight` `GD of Birth`
    ##   <chr> <chr>                  <dbl>         <dbl>         <dbl>
    ## 1 Con7  #85                     19.7          34.7            20
    ## 2 Con7  #1/2/95/2               27            42              19
    ## 3 Con7  #5/5/3/83/3-3           26            41.4            19
    ## 4 Con7  #5/4/2/95/2             28.5          44.1            19
    ## 5 Con7  #4/2/95/3-3             NA            NA              20
    ## 6 Con7  #2/2/95/3-2             NA            NA              20
    ## # … with 3 more variables: `Pups born alive` <dbl>, `Pups dead @
    ## #   birth` <dbl>, `Pups survive` <dbl>
