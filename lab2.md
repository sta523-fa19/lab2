---
title: "Lab 2"
author: "Shawn Santo"
date: "09/09/2019"
output: 
  html_document:
    keep_md: yes
---



# Packages

Install package `rjson` if you do not already have it with 
`install.packages("rjson")`. Do this in your console.

Load `rjson` with


```r
library(rjson)
```

# U.S. senators

## Data

The JSON data on US senators is available at 
https://www.govtrack.us/api/v2/role?current=true&role_type=senator. We will
read this in using a function from package `rjson`.


```r
json_file <- "https://www.govtrack.us/api/v2/role?current=true&role_type=senator"
senators <- fromJSON(paste(readLines(json_file), collapse = ""))
```

## Tasks

#### Task 1

Print the structure for the first senator, Lamar Alexander, in the list.

#### Task 2

Extract the birthday for each North Carolina senator.

#### Task 3

Write a loop that prints the twitter ID for each senator in the leadership, i.e.
where `leadership_title` is not null.

# Command line

Folder `organize-me` contains files you may have if you run a simulation on
a high performance computer. Organize folder `organize-me` using the command 
line according to the following rules:

- delete all `.input2` files,
- remove the `flags` folder and all of its contents,
- place the test data text files in a folder named `test-data`,
- place the `.sh` files in a folder named `shell-scripts`,
- place the `.R` files in a folder named `R-scripts`,
- place the `.qsub` files in a folder named `hpc-run`,
- change the name of folder `organize-me` to `simulation`.







