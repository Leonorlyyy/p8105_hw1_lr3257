p8105_HW1
================
2024-09-14

## P8105 HW1

### Problem 1

``` r
### Import dataset
data("penguins", package = "palmerpenguins")
```

Description:  
There are 8 variables in total in this dataset.  
- species: Qualitative with 3 levels: Adelie, Chinstrap, Gentoo; the
specific species of the penguin.  
- island: Qualitative with 3 levels: Biscoe, Dream, Torgersen; the
island the penguin lives.  
- bill_length_mm: Quantitative, length of the penguin’s bill in mm.  
- bill_depth_mm: Quantitative, depth of the penguin’s bill in mm.  
- flipper_length_mm: Quantitative, length of the penguin’s flipper in
mm.  
- body_mass_g: Quantitative, weight of the penguin in gram.  
- sex: Qualitative with 2 levels: male, female; sex of the penguin.  
- year: Quantitative ordinal variable.

Size of the dataset:  
- There are 8 columns and 344 rows in this dataset.

Mean flipper length: The mean flipper length of the penguins is
200.9152047 mm.

``` r
### Scatterplot
species = penguins %>% pull(species)
plot_df =
  tibble(
    x = penguins %>% pull(bill_length_mm),
    y = penguins %>% pull(flipper_length_mm)
  )
ggplot(plot_df, aes(x = x, y = y, color = species)) +
  geom_point()
```

    ## Warning: Removed 2 rows containing missing values or values outside the scale range
    ## (`geom_point()`).

![](HW1_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

Make a scatterplot of flipper_length_mm (y) vs bill_length_mm (x); color
points using the species variable (adding color = … inside of aes in
your ggplot code should help)

### Problem 2
