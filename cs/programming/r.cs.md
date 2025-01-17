{
  "date" : "2021-09-06", 
  "keywords" :[ "R", "soubor", "přípona", "formát souboru", "knihovny R", "Průvodce programováním", "příklad r", "kód R", "knihovny R", "Microsoft R" , "R kód", "jazyk R", "RStudio" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"R - Programming Language File",
  "description":"Další informace o formátu souboru R a rozhraních API, která mohou vytvářet a otevírat soubory R.",
  "linktitle" : "R",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-06"
}

## Co je soubor R?

Soubor s příponou .r patří do programovacího jazyka R. Tento jazyk je určen pro statistické výpočty a je oblíbený mezi komunitou statistiků. Analýza dat a vývoj statistického softwaru jsou dvě hlavní kategorie prováděné tímto jazykem v oblasti dolování dat. Další výhodou použití tohoto jazyka a softwaru je, že poskytuje možnost statických grafů, které jsou užitečné při vytváření kvalitních grafů. Některé další balíčky se používají pro dynamickou a interaktivní grafiku.

Software tohoto jazyka obsahuje General Public License, takže jeho dostupnost je zdarma. Kód R je obvykle napsán v jazycích vysoké úrovně, jako je [C](/cs/programming/c/) a také samotné R. Software zahrnuje rozhraní příkazového řádku spolu s dostupností rozhraní třetích stran, jako jsou grafická uživatelská rozhraní RStudio a Jupyter (rozhraní notebooku). Existují statistické techniky používané při implementaci knihoven R. Zahrnuje také modelování jako lineární a nelineární.


## Stručná historie ##

Tento jazyk je implementací sémantiky lexikálního rozsahu spolu s jazykem S. V roce 1976 v Bell Labs vyvinul John Chambers jazyk S. Dokonce ani tam není žádná změna ve velké části kódu S-PLUS při použití v jazyce R. V roce 1995 vytvořil Martin Maechler a jeho společníci jazyk R spolu se svobodným softwarem pod licencí General public.

Oficiální oznámení Comprehensive R Archive Network bylo učiněno 23. dubna 1997. V roce 2000 byla oficiálně vydána verze 1.0, která byla první stabilní beta verzí. Jeho první vydání se uskutečnilo v roce 1995, zatímco CRAN (comprehensive R archive network) byla vydána v pozdějších letech.

Základní tým byl vytvořen v roce 1997 pro další vývoj jazyka po prvních verzích. Mnoho aktualizací a upravených verzí bylo vydáváno v pozdějších letech a zahrnovalo nové funkce podle moderních operačních systémů a technologií. Nedávná úprava byla představena v květnu 2021.


## Technická specifikace ##

R je tlumočnický jazyk a pro přístup k tomuto jazyku je vyžadován tlumočník příkazového řádku. Výpočty jako součet se zadávají do příkazu promo a výsledky se zobrazí po interpretaci. Data a kód jsou reprezentovány S-výrazy. Další specifikací tohoto jazyka je, že může být provozován jako sada nástrojů, která poskytuje možnost výpočtu obecné matice.

Ke spouštění a úpravě R kódu se používají různé aplikace. Integrovaná vývojová prostředí jako Rattle GUI, RKWard jsou také k dispozici pro spuštění kódu programovacího jazyka R. Další software od společnosti Microsoft známý jako Microsoft R open je také dostupný s kompatibilitou s distribucí R pro složité výpočty, jako jsou výpočty s více vlákny. R je jedním z pěti vybraných programovacích jazyků po celém světě, které obsahují Apache Spark API.

Jazyk R podporuje procedurální programování spolu s funkcemi. Zejména pro některé funkce však podporuje OOP (objektově orientované programování) spolu s generickými funkcemi. Hodnoty se používají k předávání argumentů, pokud funkce a jejich vyhodnocení probíhá při jejich použití, což znamená, že se nevyhodnocují, když jsou funkce volány.

## Příklad formátu souboru R ##

### Syntaxe ###

```
> x <- 1:6 # Create a numeric vector in the current environment
> y <- x^2 # Create vector based on the values in x.
> print(y) # Print the vector’s contents.
[1]  1  4  9 16 25 36

> z <- x + y # Create a new vector that is the sum of x and y
> z # return the contents of z to the current environment.
[1]  2  6 12 20 30 42

> z_matrix <- matrix(z, nrow=3) # Create a new matrix that turns the vector z into a 3x2 matrix object
> z_matrix 
     [,1] [,2]
[1,]    2   20
[2,]    6   30
[3,]   12   42

> 2*t(z_matrix)-2 # Transpose the matrix, multiply every element by 2, subtract 2 from each element in the matrix, and return the results to the terminal.
     [,1] [,2] [,3]
[1,]    2   10   22
[2,]   38   58   82

> new_df <- data.frame(t(z_matrix), row.names=c('A','B')) # Create a new data.frame object that contains the data from a transposed z_matrix, with row names 'A' and 'B'
> names(new_df) <- c('X','Y','Z') # set the column names of new_df as X, Y, and Z.
> print(new_df)  #print the current results.
   X  Y  Z
A  2  6 12
B 20 30 42

> new_df$Z #output the Z column
[1] 12 42

> new_df$Z==new_df['Z'] && new_df[3]==new_df$Z # the data.frame column Z can be accessed using $Z, ['Z'], or [3] syntax, and the values are the same. 
[1] TRUE

> attributes(new_df) #print attributes information about the new_df object
$names
[1] "X" "Y" "Z"

$row.names
[1] "A" "B"

$class
[1] "data.frame"

> attributes(new_df)$row.names <- c('one','two') ## access and then change the row.names attribute; can also be done using rownames()
> new_df
     X  Y  Z
one  2  6 12
two 20 30 42
```

### Funkce ###

```
# Declare function “f” with parameters “x”, “y“
# that returns a linear combination of x and y.
f <- function(x, y) {
  z <- 3 * x + 4 * y
  return(z) ## the return() function is optional here
}
```

```
> f(1, 2)
[1] 11

> f(c(1,2,3), c(5,3,4))
[1] 23 18 25

> f(1:3, 4)
[1] 19 22 25
```

### Datové modelování

```
> x <- 1:6 # Create x and y values
> y <- x^2  
> model <- lm(y ~ x)  # Linear regression model y = A + B * x.
> summary(model)  # Display an in-depth summary of the model.

Call:
lm(formula = y ~ x)

Residuals:
      1       2       3       4       5       6
 3.3333 -0.6667 -2.6667 -2.6667 -0.6667  3.3333

Coefficients:
            Estimate Std. Error t value Pr(>|t|)   
(Intercept)  -9.3333     2.8441  -3.282 0.030453 * 
x             7.0000     0.7303   9.585 0.000662 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 3.055 on 4 degrees of freedom
Multiple R-squared:  0.9583, Adjusted R-squared:  0.9478
F-statistic: 91.88 on 1 and 4 DF,  p-value: 0.000662

> par(mfrow = c(2, 2))  # Create a 2 by 2 layout for figures.
> plot(model)  # Output diagnostic plots of the model.
```

## reference ##

* [R – z Wikipedie](https://en.wikipedia.org/wiki/R_(programming_language))



