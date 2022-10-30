---
title: Forecasting and time variability analysis of Ozone concentrations using nitrogen oxide and meteorological variables as predictors
keywords:
- markdown
- publishing
- manubot
lang: en-US
date-meta: '2022-10-30'
author-meta:
- Jiewen Luo
- Rourou Ji
- Bernardo Burbano
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta name="dc.title" content="Forecasting and time variability analysis of Ozone concentrations using nitrogen oxide and meteorological variables as predictors" />
  <meta name="citation_title" content="Forecasting and time variability analysis of Ozone concentrations using nitrogen oxide and meteorological variables as predictors" />
  <meta property="og:title" content="Forecasting and time variability analysis of Ozone concentrations using nitrogen oxide and meteorological variables as predictors" />
  <meta property="twitter:title" content="Forecasting and time variability analysis of Ozone concentrations using nitrogen oxide and meteorological variables as predictors" />
  <meta name="dc.date" content="2022-10-30" />
  <meta name="citation_publication_date" content="2022-10-30" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Jiewen Luo" />
  <meta name="citation_author_institution" content="Department of CEE, University of Illinois at Urbana&amp;Champaign" />
  <meta name="citation_author" content="Rourou Ji" />
  <meta name="citation_author_institution" content="Department of CEE, University of Illinois at Urbana&amp;Champaign" />
  <meta name="citation_author" content="Bernardo Burbano" />
  <meta name="citation_author_institution" content="Department of CEE, University of Illinois at Urbana&amp;Champaign" />
  <link rel="canonical" href="https://uiceds.github.io/cee-492-term-project-fall-2022-hydrograds/" />
  <meta property="og:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-hydrograds/" />
  <meta property="twitter:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-hydrograds/" />
  <meta name="citation_fulltext_html_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-hydrograds/" />
  <meta name="citation_pdf_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-hydrograds/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://uiceds.github.io/cee-492-term-project-fall-2022-hydrograds/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://uiceds.github.io/cee-492-term-project-fall-2022-hydrograds/v/c8758cb6c2c9e1543c9a2b48cd98bd38e9585e6c/" />
  <meta name="manubot_html_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-hydrograds/v/c8758cb6c2c9e1543c9a2b48cd98bd38e9585e6c/" />
  <meta name="manubot_pdf_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-hydrograds/v/c8758cb6c2c9e1543c9a2b48cd98bd38e9585e6c/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...






<small><em>
This manuscript
([permalink](https://uiceds.github.io/cee-492-term-project-fall-2022-hydrograds/v/c8758cb6c2c9e1543c9a2b48cd98bd38e9585e6c/))
was automatically generated
from [uiceds/cee-492-term-project-fall-2022-hydrograds@c8758cb](https://github.com/uiceds/cee-492-term-project-fall-2022-hydrograds/tree/c8758cb6c2c9e1543c9a2b48cd98bd38e9585e6c)
on October 30, 2022.
</em></small>

## Authors



+ **Jiewen Luo**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [Noomi-Luo](https://github.com/Noomi-Luo)<br>
  <small>
     Department of CEE, University of Illinois at Urbana&Champaign
  </small>

+ **Rourou Ji**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [JadeJi](https://github.com/JadeJi)<br>
  <small>
     Department of CEE, University of Illinois at Urbana&Champaign
  </small>

+ **Bernardo Burbano**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [BernieJBA](https://github.com/BernieJBA)<br>
  <small>
     Department of CEE, University of Illinois at Urbana&Champaign
  </small>



## CEE 492 Final Project Selection 
1. Dataset description:

The dataset used in this project is a `CSV` file about the air quality in northern Taiwan collected in 2015 [https://www.kaggle.com/datasets/nelsonchu/air-quality-in-northern-taiwan], which include air quality data and meteorological monitoring data for research and analysis, originally from Environmental Protection Administration, Executive Yuan, R.O.C. (Taiwan). There are 25 observation stations in total. Columns in this CSV file are the following:

1. Time - The first column is the observation time of 2015

2. Station - The second column is the station name, there are 25 observation stations, those stations are showing at the table @tbl:1.


|  |  | station |  |  |
|:---:|:---:|:---:|:---:|:---:|
| Banqiao | Cailiao | Datong | Dayuan | Guanyin |
| Guting | Keelung | Longtan | Pingzhen | Sanchong |
| Shilin | Songshan | Tamsui | Taoyuan | Tucheng |
| Wanhua | Wanli | Xindian | Xinzhuang | Xizhi |
| Yangming | Yonghe | Zhongli | Zhongshan | Linkou |

Table: A table contain all stations in Taiwan.
{#tbl:1}

3. Items - From the third column to the last one

4. item - `unit` - description
- SO~2~ - `ppb` - Sulfur dioxide
- CO - `ppm` - Carbon monoxide
- O~3~ - `ppb` - ozone
- PM~10~ - `μg/m^3` - Particulate matter
- PM~2.5~ - `μg/m^3` - Particulate matter
- NO~x~ - `ppb`- Nitrogen oxides
- NO - `ppb` - Nitric oxide
- NO~2~ - `ppb` - Nitrogen dioxide
- THC - `ppm` - Total Hydrocarbons
- NMHC - `ppm` - Non-Methane Hydrocarbon
- CH4 - `ppm` - Methane
- UVB - `UVI` - Ultraviolet index
- AMB_TEMP - `Celsius` - Ambient air temperature
- RAINFALL - `mm`
- RH - `%` - Relative humidity
- WIND_SPEED - `m/sec` - The average of the last ten minutes per hour
- WIND_DIREC - `degrees` - The average of the last ten minutes per hour
- WS_HR - `m/sec` - The average of an hour
- WD_HR - `degrees` - The average of an hour
- PH_RAIN - `PH` - Acid rain
- RAIN_COND - `μS/cm` - Conductivity of acid rain

## Proposal:
The purpose of this project is to predict O~3~ concentrations using measurements of concentration of other pollutants and available meteorological measurements.  Ozone might be formed when heat and sunlight cause chemical reactions between oxides of nitrogen (NO~x~) and Volatile Organic Compounds (VOC), which are also known as Hydrocarbons. Therefore it could be hypothesized that using measurements of NO~x~ as an independent variable a model could be developed to predict O~3~ concentrations. Additionally, meteorological variables such as air temperature, relative humidity(RH) and ultraviolet index (UVB - UVI) could be included as independent variables to assess their influence on temporal variability of ozone. As an additional step wind-related variables such as mean wind velocity and direction will be included to study their effect on temporal variability of ozone.

After the air quality data has been processed the strongest O~3~ predictors will be determined using PCA. PCA could be used to identify the main axes of variance within the dataset and explore underlying correlations that exist in a set of variables. Variables that are highly correlated cluster together. Using PCA 2D figures per each pair of variables are not needed, instead all the variables could be visualized simultaneously. Differences on PC1 are more important than differences on PC2. After plotting PCA plots, a heatmap could also be plotted to check the results. As additional criteria to identify the strongest predictors a LSTM network (long short-term memory network) can be used since the data used is time dependent. The network should contain several LSTM layers and fully-connected layers. The output should contain the pollution concentration and will point out the weights assigned to each correlated criterion, the values of such weights should also indicate what the strongest predictors are. Once the strongest predictors have been identified, genetic programming will be used to develop the models to predict O~3~ concentrations. 

## Exploratory Data Analysis:
![Heatmap](images/heatmap.jpg){#fig:heatmap width=7in}
![Hour](images/hour.png){#fig:hour width=7in}
![month](images/month.png){#fig:month width=7in}
![O3 & Independent variable](images/O312.jpg){#fig:O3 width=7in}
![variables](images/InformationDensity.png){#fig:var width=7in}


|                      | **count** | **mean**  | **std** | **min** | **25%** | **50%** | **75%** | **max** |
|----------------------|-----------|-----------|---------|---------|---------|---------|---------|---------|
| **AMB_TEMP**         | 8682      | 1.18E-15  | 1.00    | -2.47   | -0.89   | 0.15    | 0.68    | 2.25    |
| **NMHC**             | 8619      | -4.74E-15 | 1.00    | -1.32   | -0.62   | -0.30   | 0.29    | 16.26   |
| **NO**               | 8462      | 3.20E-15  | 1.00    | -0.75   | -0.50   | -0.32   | 0.05    | 23.55   |
| **NO2**              | 8462      | 1.56E-15  | 1.00    | -1.94   | -0.78   | -0.10   | 0.57    | 5.48    |
| **NOx**              | 8462      | 1.62E-15  | 1.00    | -1.54   | -0.69   | -0.20   | 0.42    | 14.67   |
| **O3**               | 8685      | -8.78E-16 | 1.00    | -1.35   | -0.80   | -0.07   | 0.54    | 6.06    |
| **RH**               | 8684      | -1.56E-15 | 1.00    | -4.85   | -0.75   | 0.17    | 0.76    | 2.35    |
| **UVB**              | 8684      | 3.53E-15  | 1.00    | -0.56   | -0.56   | -0.56   | 0.12    | 4.81    |
| **WD_Hour**          | 8680      | 2.64E-16  | 1.00    | -1.58   | -0.78   | -0.59   | 1.01    | 2.32    |
| **WIND_DIREC_10min** | 8682      | 6.96E-16  | 1.00    | -1.56   | -0.78   | -0.58   | 1.01    | 2.31    |
| **WIND_SPEED_10min** | 8682      | -6.21E-15 | 1.00    | -1.43   | -0.72   | -0.18   | 0.53    | 7.92    |
| **WS_HR**            | 8680      | -2.83E-15 | 1.00    | -1.67   | -0.80   | -0.12   | 0.56    | 7.86    |

Table:Descriptive statistics of features that compose in this analysis 
{#tbl:2}






## Predictive Modeling
The independent variables were segmented in pollutants and meteorological measurements. In order to visualize how the measurements change throughout the year the values were average per month. Then the resulting values were standardized using their mean. Once the values were standardized they were plotted against time.

![Standardized pollutants and ozone monthly concentration changes](images/Pollutants.png){#fig:Pollutants width=7in}

![Standardized meteorological measurements and standardized ozone monthly concentration changes](images/Meteo_Vars.png){#fig:MetereologicalVars width=7in}

As seen in the previous figure, O3 peaked in the months when concentration of the nitrogen based pollutants and non-methane hydrocarbons dropped. This is especially the case for NO concentrations (green line). This pattern of corresponding decreasing pollutant concentrations and increasing ozone could suggest that the pollutant concentrations are negatively correlated with ozone concentrations. This is also consistent with figure @fig:Pollutants (correlation plot)

In regards to the meteorological variables, UVB (ultraviolet index) and air temperature peak in the same months. Both temperature and UVB experience and increase in their values from the beginning of the year peaking in June. After June, both values experience a steady decrease. No discernable pattern can be observed in terms of the relation of the latter two variables and ozone concentrations. 

Wind direction values are telling of changes in direction with respect to yearly average direction. The increase or decrease of the values shown in figure @fig:MetereologicalVars correspond to a relative shift in direction of the wind compared to the yearly wind direction. These shifts in the direction of the wind can be used later on the forecasting of O3 concentration. Wind direction could help elucidate if O3 concentration from upwind neighboring locations could affect O3 values in the location of interest, Banquiao. 

The exploratory data analysis suggests that in order to forecast ozone concentration the model inputs i.e. independent variables will have to be averaged over the month. Furthermore, such monthly mean values will have to be standardized using the mean annual corresponding values. Once the data has been standardized it will be used to train a model.

As a first iteration, a linear model with multiple independent variables will be optimized using available standardized measurements of ozone. A first model will be produced only using standardized pollutant values, and a second model will include as additional variables wind direction and upwind station standardized ozone concentrations from corresponding upwind stations.
If the linear model mean square error, computed using predictions of ozone and observation, is below 0.5 a more involved model will be used. Two candidates for the second iteration of the predictive model will be considered. A fully connected neural network and a model produced with genetic programming packages in python for model discovery. 
In order to train the neural network pollutant measurements as well as  from 9 out of the 12 months will be used as well as the corresponding mean wind direction values of Banquiao coupled with the ozone measurements from the 6 neighboring stations shown below. In order to validate the model, 12 the remaining data will be used.

![Geographic location of 7 stations we focused on](images/geogra.png){#fig:MetereologicalVars width=7in}


This manuscript is a template (aka "rootstock") for [Manubot](https://manubot.org/ "Manubot"), a tool for writing scholarly manuscripts.
Use this template as a starting point for your manuscript.

The rest of this document is a full list of formatting elements/features supported by Manubot.
Compare the input (`.md` files in the `/content` directory) to the output you see below.

## Basic formatting

**Bold** __text__

[Semi-bold text]{.semibold}

[Centered text]{.center}

[Right-aligned text]{.right}

*Italic* _text_

Combined *italics and __bold__*

~~Strikethrough~~

1. Ordered list item
2. Ordered list item
    a. Sub-item
    b. Sub-item
        i. Sub-sub-item
3. Ordered list item
    a. Sub-item

- List item
- List item
- List item

subscript: H~2~O is a liquid

superscript: 2^10^ is 1024.

[unicode superscripts](https://www.google.com/search?q=superscript+generator)⁰¹²³⁴⁵⁶⁷⁸⁹

[unicode subscripts](https://www.google.com/search?q=superscript+generator)₀₁₂₃₄₅₆₇₈₉

A long paragraph of text.
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

Putting each sentence on its own line has numerous benefits with regard to [editing](https://asciidoctor.org/docs/asciidoc-recommended-practices/#one-sentence-per-line) and [version control](https://rhodesmill.org/brandon/2012/one-sentence-per-line/).

Line break without starting a new paragraph by putting  
two spaces at end of line.

## Document organization

Document section headings:

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

##### Heading 5

###### Heading 6

### A heading centered on its own printed page{.center .page_center}

<!-- an arbitrary comment. visible in input, but not visible in output. -->

Horizontal rule:

---

`Heading 1`'s are recommended to be reserved for the title of the manuscript.

`Heading 2`'s are recommended for broad sections such as *Abstract*, *Methods*, *Conclusion*, etc.

`Heading 3`'s and `Heading 4`'s are recommended for sub-sections.

## Links

Bare URL link: <https://manubot.org>

[Long link with lots of words and stuff and junk and bleep and blah and stuff and other stuff and more stuff yeah](https://manubot.org)

[Link with text](https://manubot.org)

[Link with hover text](https://manubot.org "Manubot Homepage")

[Link by reference][manubot homepage]

[Manubot Homepage]: https://manubot.org

## Citations

Citation by DOI [@doi:10.7554/eLife.32822].

Citation by PubMed Central ID [@pmc:PMC6103790].

Citation by PubMed ID [@pubmed:30718888].

Citation by Wikidata ID [@wikidata:Q56458321].

Citation by ISBN [@isbn:9780262517638].

Citation by URL [@{https://greenelab.github.io/meta-review/}].

Citation by alias [@deep-review].

Multiple citations can be put inside the same set of brackets [@doi:10.7554/eLife.32822; @deep-review; @isbn:9780262517638].
Manubot plugins provide easier, more convenient visualization of and navigation between citations [@doi:10.1371/journal.pcbi.1007128; @pubmed:30718888; @pmc:PMC6103790; @deep-review].

Citation tags (i.e. aliases) can be defined in their own paragraphs using Markdown's reference link syntax:

[@deep-review]: doi:10.1098/rsif.2017.0387

## Referencing figures, tables, equations

Figure @fig:square-image

Figure @fig:wide-image

Figure @fig:tall-image

Figure @fig:vector-image

Table @tbl:bowling-scores

Equation @eq:regular-equation

Equation @eq:long-equation

## Quotes and code

> Quoted text

> Quoted block of text
>
> Two roads diverged in a wood, and I—  
> I took the one less traveled by,  
> And that has made all the difference.

Code `in the middle` of normal text, aka `inline code`.

Code block with Python syntax highlighting:

```python
from manubot.cite.doi import expand_short_doi

def test_expand_short_doi():
    doi = expand_short_doi("10/c3bp")
    # a string too long to fit within page:
    assert doi == "10.25313/2524-2695-2018-3-vliyanie-enhansera-copia-i-insulyatora-gypsy-na-sintez-ernk-modifikatsii-hromatina-i-svyazyvanie-insulyatornyh-belkov-vtransfetsirovannyh-geneticheskih-konstruktsiyah"
```

Code block with no syntax highlighting:

```
Exporting HTML manuscript
Exporting DOCX manuscript
Exporting PDF manuscript
```

## Figures

![
**A square image at actual size and with a bottom caption.**
Loaded from the latest version of image on GitHub.
](https://github.com/manubot/resources/raw/15493970f8882fce22bef829619d3fb37a613ba5/test/square.png "Square image"){#fig:square-image}

![
**An image too wide to fit within page at full size.**
Loaded from a specific (hashed) version of the image on GitHub.
](https://github.com/manubot/resources/raw/15493970f8882fce22bef829619d3fb37a613ba5/test/wide.png "Wide image"){#fig:wide-image}

![
**A tall image with a specified height.**
Loaded from a specific (hashed) version of the image on GitHub.
](https://github.com/manubot/resources/raw/15493970f8882fce22bef829619d3fb37a613ba5/test/tall.png "Tall image"){#fig:tall-image height=3in}

![
**A vector `.svg` image loaded from GitHub.**
The parameter `sanitize=true` is necessary to properly load SVGs hosted via GitHub URLs.
White background specified to serve as a backdrop for transparent sections of the image.
](https://raw.githubusercontent.com/manubot/resources/main/test/vector.svg?sanitize=true "Vector image"){#fig:vector-image height=2.5in .white}

## Tables

| *Bowling Scores* | Jane          | John          | Alice         | Bob           |
|:-----------------|:-------------:|:-------------:|:-------------:|:-------------:|
| Game 1 | 150 | 187 | 210 | 105 |
| Game 2 |  98 | 202 | 197 | 102 |
| Game 3 | 123 | 180 | 238 | 134 |

Table: A table with a top caption and specified relative column widths.
{#tbl:bowling-scores}

|         | Digits 1-33                        | Digits 34-66                      | Digits 67-99                      | Ref.                                                        |
|:--------|:-----------------------------------|:----------------------------------|:----------------------------------|:------------------------------------------------------------|
| pi      | 3.14159265358979323846264338327950 | 288419716939937510582097494459230 | 781640628620899862803482534211706 | [`piday.org`](https://www.piday.org/million/)               |
| e       | 2.71828182845904523536028747135266 | 249775724709369995957496696762772 | 407663035354759457138217852516642 | [`nasa.gov`](https://apod.nasa.gov/htmltest/gifcity/e.2mil) |

Table: A table too wide to fit within page.
{#tbl:constant-digits}

|          | **Colors** <!-- $colspan="2" --> |                      |
|:--------:|:--------------------------------:|:--------------------:|
| **Size** | **Text Color**                   | **Background Color** |
| big      | blue                             | orange               |
| small    | black                            | white                |

Table: A table with merged cells using the `attributes` plugin.
{#tbl: merged-cells}

## Equations

A LaTeX equation:

$$\int_0^\infty e^{-x^2} dx=\frac{\sqrt{\pi}}{2}$$ {#eq:regular-equation}

An equation too long to fit within page:

$$x = a + b + c + d + e + f + g + h + i + j + k + l + m + n + o + p + q + r + s + t + u + v + w + x + y + z + 1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9$$ {#eq:long-equation}

## Special

<i class="fas fa-exclamation-triangle"></i> [WARNING]{.semibold} _The following features are only supported and intended for `.html` and `.pdf` exports._
_Journals are not likely to support them, and they may not display correctly when converted to other formats such as `.docx`._

[Link styled as a button](https://manubot.org "Manubot Homepage"){.button}

Adding arbitrary HTML attributes to an element using Pandoc's attribute syntax:

::: {#some_id_1 .some_class style="background: #ad1457; color: white; margin-left: 40px;" title="a paragraph of text" data-color="white" disabled="true"}
Manubot Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot.
Manubot Manubot.
Manubot.
:::

Adding arbitrary HTML attributes to an element with the Manubot `attributes` plugin (more flexible than Pandoc's method in terms of which elements you can add attributes to):

Manubot Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot Manubot.
Manubot Manubot Manubot.
Manubot Manubot.
Manubot.
<!-- $id="element_id" class="some_class" $style="color: #ad1457; margin-left: 40px;" $disabled="true" $title="a paragraph of text" $data-color="red" -->

Available background colors for text, images, code, banners, etc:  

`white`{.white}
`lightgrey`{.lightgrey}
`grey`{.grey}
`darkgrey`{.darkgrey}
`black`{.black}
`lightred`{.lightred}
`lightyellow`{.lightyellow}
`lightgreen`{.lightgreen}
`lightblue`{.lightblue}
`lightpurple`{.lightpurple}
`red`{.red}
`orange`{.orange}
`yellow`{.yellow}
`green`{.green}
`blue`{.blue}
`purple`{.purple}

Using the [Font Awesome](https://fontawesome.com/) icon set:

<!-- include the Font Awesome library, per: https://fontawesome.com/start -->
<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.7.2/css/all.css">

<i class="fas fa-check"></i> <i class="fas fa-question"></i> <i class="fas fa-star"></i> <i class="fas fa-bell"></i> <i class="fas fa-times-circle"></i> <i class="fas fa-ellipsis-h"></i>

[
<i class="fas fa-scroll fa-lg"></i> **Light Grey Banner**<br>
useful for *general information* - [manubot.org](https://manubot.org/)
]{.banner .lightgrey}

[
<i class="fas fa-info-circle fa-lg"></i> **Blue Banner**<br>
useful for *important information* - [manubot.org](https://manubot.org/)
]{.banner .lightblue}

[
<i class="fas fa-ban fa-lg"></i> **Light Red Banner**<br>
useful for *warnings* - [manubot.org](https://manubot.org/)
]{.banner .lightred}

## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
