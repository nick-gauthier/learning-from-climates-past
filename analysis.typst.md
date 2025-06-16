---
title: "Learning More Effectively from Climate’s Past"
subtitle: "Reproducible Data Analysis"
author: Nicolas Gauthier
date: last-modified
date-format: "[Last updated:] MMMM D, YYYY"
execute:
  keep-md: true
format: 
  typst:
    toc: true
    margin:
      x: 1in
      y: 1in
editor: visual
---


::: {.cell}

:::

::: {.cell}

:::




## Introduction

This is a fully reproducible analysis written in R and Quarto. The source code for this document, including all the R code to run the preprocess the data, run the analysis, and produce the tables you see below, is available [here on GitHub](https://github.com/nick-gauthier/hcs-meta/analysis.qmd).

This analysis pulls data directly from the original Excel Spreadsheet [at this link](https://github.com/nick-gauthier/hcs-meta/Learning More Effectively Database.xlsx), so the tables will update automatically when the analysis is rerun if the spreadsheet changes.



::: {.cell}

:::


{{< pagebreak >}}






## Simple Questions

### 1. How many publications do we have from each discipline?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="whlkwvqyoo" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#whlkwvqyoo table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#whlkwvqyoo thead, #whlkwvqyoo tbody, #whlkwvqyoo tfoot, #whlkwvqyoo tr, #whlkwvqyoo td, #whlkwvqyoo th {
  border-style: none;
}

#whlkwvqyoo p {
  margin: 0;
  padding: 0;
}

#whlkwvqyoo .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#whlkwvqyoo .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#whlkwvqyoo .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#whlkwvqyoo .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#whlkwvqyoo .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#whlkwvqyoo .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#whlkwvqyoo .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#whlkwvqyoo .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#whlkwvqyoo .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#whlkwvqyoo .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#whlkwvqyoo .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#whlkwvqyoo .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#whlkwvqyoo .gt_spanner_row {
  border-bottom-style: hidden;
}

#whlkwvqyoo .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#whlkwvqyoo .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#whlkwvqyoo .gt_from_md > :first-child {
  margin-top: 0;
}

#whlkwvqyoo .gt_from_md > :last-child {
  margin-bottom: 0;
}

#whlkwvqyoo .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#whlkwvqyoo .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#whlkwvqyoo .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#whlkwvqyoo .gt_row_group_first td {
  border-top-width: 2px;
}

#whlkwvqyoo .gt_row_group_first th {
  border-top-width: 2px;
}

#whlkwvqyoo .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#whlkwvqyoo .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#whlkwvqyoo .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#whlkwvqyoo .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#whlkwvqyoo .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#whlkwvqyoo .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#whlkwvqyoo .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#whlkwvqyoo .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#whlkwvqyoo .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#whlkwvqyoo .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#whlkwvqyoo .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#whlkwvqyoo .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#whlkwvqyoo .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#whlkwvqyoo .gt_left {
  text-align: left;
}

#whlkwvqyoo .gt_center {
  text-align: center;
}

#whlkwvqyoo .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#whlkwvqyoo .gt_font_normal {
  font-weight: normal;
}

#whlkwvqyoo .gt_font_bold {
  font-weight: bold;
}

#whlkwvqyoo .gt_font_italic {
  font-style: italic;
}

#whlkwvqyoo .gt_super {
  font-size: 65%;
}

#whlkwvqyoo .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#whlkwvqyoo .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#whlkwvqyoo .gt_indent_1 {
  text-indent: 5px;
}

#whlkwvqyoo .gt_indent_2 {
  text-indent: 10px;
}

#whlkwvqyoo .gt_indent_3 {
  text-indent: 15px;
}

#whlkwvqyoo .gt_indent_4 {
  text-indent: 20px;
}

#whlkwvqyoo .gt_indent_5 {
  text-indent: 25px;
}

#whlkwvqyoo .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#whlkwvqyoo div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_0"><span data-qmd-base64="PHN0cm9uZz5OID0gMSwxOTE8L3N0cm9uZz4="><span class='gt_from_md'><strong>N = 1,191</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Discipline</td>
<td headers="stat_0" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Archaeology</td>
<td headers="stat_0" class="gt_row gt_center">149 (13%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Economics</td>
<td headers="stat_0" class="gt_row gt_center">5 (0.4%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Epidemiology</td>
<td headers="stat_0" class="gt_row gt_center">2 (0.2%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Geography</td>
<td headers="stat_0" class="gt_row gt_center">25 (2.1%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    History</td>
<td headers="stat_0" class="gt_row gt_center">206 (17%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Joint Fields</td>
<td headers="stat_0" class="gt_row gt_center">211 (18%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Literature</td>
<td headers="stat_0" class="gt_row gt_center">35 (2.9%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Other</td>
<td headers="stat_0" class="gt_row gt_center">13 (1.1%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Paleoclimatology</td>
<td headers="stat_0" class="gt_row gt_center">545 (46%)</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="2"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::


### 2. How many publications are from each region?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="uhfrrqcset" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#uhfrrqcset table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#uhfrrqcset thead, #uhfrrqcset tbody, #uhfrrqcset tfoot, #uhfrrqcset tr, #uhfrrqcset td, #uhfrrqcset th {
  border-style: none;
}

#uhfrrqcset p {
  margin: 0;
  padding: 0;
}

#uhfrrqcset .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#uhfrrqcset .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#uhfrrqcset .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#uhfrrqcset .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#uhfrrqcset .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#uhfrrqcset .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#uhfrrqcset .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#uhfrrqcset .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#uhfrrqcset .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#uhfrrqcset .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#uhfrrqcset .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#uhfrrqcset .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#uhfrrqcset .gt_spanner_row {
  border-bottom-style: hidden;
}

#uhfrrqcset .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#uhfrrqcset .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#uhfrrqcset .gt_from_md > :first-child {
  margin-top: 0;
}

#uhfrrqcset .gt_from_md > :last-child {
  margin-bottom: 0;
}

#uhfrrqcset .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#uhfrrqcset .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#uhfrrqcset .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#uhfrrqcset .gt_row_group_first td {
  border-top-width: 2px;
}

#uhfrrqcset .gt_row_group_first th {
  border-top-width: 2px;
}

#uhfrrqcset .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#uhfrrqcset .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#uhfrrqcset .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#uhfrrqcset .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#uhfrrqcset .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#uhfrrqcset .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#uhfrrqcset .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#uhfrrqcset .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#uhfrrqcset .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#uhfrrqcset .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#uhfrrqcset .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#uhfrrqcset .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#uhfrrqcset .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#uhfrrqcset .gt_left {
  text-align: left;
}

#uhfrrqcset .gt_center {
  text-align: center;
}

#uhfrrqcset .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#uhfrrqcset .gt_font_normal {
  font-weight: normal;
}

#uhfrrqcset .gt_font_bold {
  font-weight: bold;
}

#uhfrrqcset .gt_font_italic {
  font-style: italic;
}

#uhfrrqcset .gt_super {
  font-size: 65%;
}

#uhfrrqcset .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#uhfrrqcset .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#uhfrrqcset .gt_indent_1 {
  text-indent: 5px;
}

#uhfrrqcset .gt_indent_2 {
  text-indent: 10px;
}

#uhfrrqcset .gt_indent_3 {
  text-indent: 15px;
}

#uhfrrqcset .gt_indent_4 {
  text-indent: 20px;
}

#uhfrrqcset .gt_indent_5 {
  text-indent: 25px;
}

#uhfrrqcset .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#uhfrrqcset div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_0"><span data-qmd-base64="PHN0cm9uZz5OID0gMSwxOTE8L3N0cm9uZz4="><span class='gt_from_md'><strong>N = 1,191</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Geographic Region</td>
<td headers="stat_0" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Africa</td>
<td headers="stat_0" class="gt_row gt_center">45 (3.8%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Americas</td>
<td headers="stat_0" class="gt_row gt_center">174 (15%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Asia</td>
<td headers="stat_0" class="gt_row gt_center">271 (23%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Europe</td>
<td headers="stat_0" class="gt_row gt_center">347 (29%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Global</td>
<td headers="stat_0" class="gt_row gt_center">228 (19%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Middle East</td>
<td headers="stat_0" class="gt_row gt_center">61 (5.1%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Oceania</td>
<td headers="stat_0" class="gt_row gt_center">25 (2.1%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Polar</td>
<td headers="stat_0" class="gt_row gt_center">40 (3.4%)</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="2"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::


{{< pagebreak >}}






### 3. How many publications are from each period?

Note that N is larger here because each paper can cover multiple time periods.



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="fhvrotypek" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#fhvrotypek table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#fhvrotypek thead, #fhvrotypek tbody, #fhvrotypek tfoot, #fhvrotypek tr, #fhvrotypek td, #fhvrotypek th {
  border-style: none;
}

#fhvrotypek p {
  margin: 0;
  padding: 0;
}

#fhvrotypek .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#fhvrotypek .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#fhvrotypek .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#fhvrotypek .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#fhvrotypek .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#fhvrotypek .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#fhvrotypek .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#fhvrotypek .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#fhvrotypek .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#fhvrotypek .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#fhvrotypek .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#fhvrotypek .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#fhvrotypek .gt_spanner_row {
  border-bottom-style: hidden;
}

#fhvrotypek .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#fhvrotypek .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#fhvrotypek .gt_from_md > :first-child {
  margin-top: 0;
}

#fhvrotypek .gt_from_md > :last-child {
  margin-bottom: 0;
}

#fhvrotypek .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#fhvrotypek .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#fhvrotypek .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#fhvrotypek .gt_row_group_first td {
  border-top-width: 2px;
}

#fhvrotypek .gt_row_group_first th {
  border-top-width: 2px;
}

#fhvrotypek .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fhvrotypek .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#fhvrotypek .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#fhvrotypek .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#fhvrotypek .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fhvrotypek .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#fhvrotypek .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#fhvrotypek .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#fhvrotypek .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#fhvrotypek .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#fhvrotypek .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fhvrotypek .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#fhvrotypek .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fhvrotypek .gt_left {
  text-align: left;
}

#fhvrotypek .gt_center {
  text-align: center;
}

#fhvrotypek .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#fhvrotypek .gt_font_normal {
  font-weight: normal;
}

#fhvrotypek .gt_font_bold {
  font-weight: bold;
}

#fhvrotypek .gt_font_italic {
  font-style: italic;
}

#fhvrotypek .gt_super {
  font-size: 65%;
}

#fhvrotypek .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#fhvrotypek .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#fhvrotypek .gt_indent_1 {
  text-indent: 5px;
}

#fhvrotypek .gt_indent_2 {
  text-indent: 10px;
}

#fhvrotypek .gt_indent_3 {
  text-indent: 15px;
}

#fhvrotypek .gt_indent_4 {
  text-indent: 20px;
}

#fhvrotypek .gt_indent_5 {
  text-indent: 25px;
}

#fhvrotypek .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#fhvrotypek div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_0"><span data-qmd-base64="PHN0cm9uZz5OID0gMywyNjI8L3N0cm9uZz4="><span class='gt_from_md'><strong>N = 3,262</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Period</td>
<td headers="stat_0" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Pleistocene</td>
<td headers="stat_0" class="gt_row gt_center">65 (2.0%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Early-Mid Holocene</td>
<td headers="stat_0" class="gt_row gt_center">145 (4.4%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Ancient</td>
<td headers="stat_0" class="gt_row gt_center">345 (11%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Medieval</td>
<td headers="stat_0" class="gt_row gt_center">569 (17%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Early Modern</td>
<td headers="stat_0" class="gt_row gt_center">720 (22%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Modern</td>
<td headers="stat_0" class="gt_row gt_center">751 (23%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Present</td>
<td headers="stat_0" class="gt_row gt_center">667 (20%)</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="2"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 4. How many of our publications use methods that are quantitative, statistical, both, or neither?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="sjkzrtemej" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#sjkzrtemej table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#sjkzrtemej thead, #sjkzrtemej tbody, #sjkzrtemej tfoot, #sjkzrtemej tr, #sjkzrtemej td, #sjkzrtemej th {
  border-style: none;
}

#sjkzrtemej p {
  margin: 0;
  padding: 0;
}

#sjkzrtemej .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#sjkzrtemej .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#sjkzrtemej .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#sjkzrtemej .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#sjkzrtemej .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#sjkzrtemej .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#sjkzrtemej .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#sjkzrtemej .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#sjkzrtemej .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#sjkzrtemej .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#sjkzrtemej .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#sjkzrtemej .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#sjkzrtemej .gt_spanner_row {
  border-bottom-style: hidden;
}

#sjkzrtemej .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#sjkzrtemej .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#sjkzrtemej .gt_from_md > :first-child {
  margin-top: 0;
}

#sjkzrtemej .gt_from_md > :last-child {
  margin-bottom: 0;
}

#sjkzrtemej .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#sjkzrtemej .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#sjkzrtemej .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#sjkzrtemej .gt_row_group_first td {
  border-top-width: 2px;
}

#sjkzrtemej .gt_row_group_first th {
  border-top-width: 2px;
}

#sjkzrtemej .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#sjkzrtemej .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#sjkzrtemej .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#sjkzrtemej .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#sjkzrtemej .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#sjkzrtemej .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#sjkzrtemej .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#sjkzrtemej .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#sjkzrtemej .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#sjkzrtemej .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#sjkzrtemej .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#sjkzrtemej .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#sjkzrtemej .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#sjkzrtemej .gt_left {
  text-align: left;
}

#sjkzrtemej .gt_center {
  text-align: center;
}

#sjkzrtemej .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#sjkzrtemej .gt_font_normal {
  font-weight: normal;
}

#sjkzrtemej .gt_font_bold {
  font-weight: bold;
}

#sjkzrtemej .gt_font_italic {
  font-style: italic;
}

#sjkzrtemej .gt_super {
  font-size: 65%;
}

#sjkzrtemej .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#sjkzrtemej .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#sjkzrtemej .gt_indent_1 {
  text-indent: 5px;
}

#sjkzrtemej .gt_indent_2 {
  text-indent: 10px;
}

#sjkzrtemej .gt_indent_3 {
  text-indent: 15px;
}

#sjkzrtemej .gt_indent_4 {
  text-indent: 20px;
}

#sjkzrtemej .gt_indent_5 {
  text-indent: 25px;
}

#sjkzrtemej .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#sjkzrtemej div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_0"><span data-qmd-base64="PHN0cm9uZz5OID0gMSwxOTE8L3N0cm9uZz4="><span class='gt_from_md'><strong>N = 1,191</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Method</td>
<td headers="stat_0" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Both</td>
<td headers="stat_0" class="gt_row gt_center">164 (14%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Neither</td>
<td headers="stat_0" class="gt_row gt_center">126 (11%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Qualitative</td>
<td headers="stat_0" class="gt_row gt_center">219 (18%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Quantitative</td>
<td headers="stat_0" class="gt_row gt_center">682 (57%)</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="2"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 5. How many of our publications are original research, a literature review, or a response article?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="cwhocylujs" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#cwhocylujs table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#cwhocylujs thead, #cwhocylujs tbody, #cwhocylujs tfoot, #cwhocylujs tr, #cwhocylujs td, #cwhocylujs th {
  border-style: none;
}

#cwhocylujs p {
  margin: 0;
  padding: 0;
}

#cwhocylujs .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#cwhocylujs .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#cwhocylujs .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#cwhocylujs .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#cwhocylujs .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#cwhocylujs .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#cwhocylujs .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#cwhocylujs .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#cwhocylujs .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#cwhocylujs .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#cwhocylujs .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#cwhocylujs .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#cwhocylujs .gt_spanner_row {
  border-bottom-style: hidden;
}

#cwhocylujs .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#cwhocylujs .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#cwhocylujs .gt_from_md > :first-child {
  margin-top: 0;
}

#cwhocylujs .gt_from_md > :last-child {
  margin-bottom: 0;
}

#cwhocylujs .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#cwhocylujs .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#cwhocylujs .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#cwhocylujs .gt_row_group_first td {
  border-top-width: 2px;
}

#cwhocylujs .gt_row_group_first th {
  border-top-width: 2px;
}

#cwhocylujs .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#cwhocylujs .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#cwhocylujs .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#cwhocylujs .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#cwhocylujs .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#cwhocylujs .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#cwhocylujs .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#cwhocylujs .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#cwhocylujs .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#cwhocylujs .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#cwhocylujs .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#cwhocylujs .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#cwhocylujs .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#cwhocylujs .gt_left {
  text-align: left;
}

#cwhocylujs .gt_center {
  text-align: center;
}

#cwhocylujs .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#cwhocylujs .gt_font_normal {
  font-weight: normal;
}

#cwhocylujs .gt_font_bold {
  font-weight: bold;
}

#cwhocylujs .gt_font_italic {
  font-style: italic;
}

#cwhocylujs .gt_super {
  font-size: 65%;
}

#cwhocylujs .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#cwhocylujs .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#cwhocylujs .gt_indent_1 {
  text-indent: 5px;
}

#cwhocylujs .gt_indent_2 {
  text-indent: 10px;
}

#cwhocylujs .gt_indent_3 {
  text-indent: 15px;
}

#cwhocylujs .gt_indent_4 {
  text-indent: 20px;
}

#cwhocylujs .gt_indent_5 {
  text-indent: 25px;
}

#cwhocylujs .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#cwhocylujs div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_0"><span data-qmd-base64="PHN0cm9uZz5OID0gMSwxOTE8L3N0cm9uZz4="><span class='gt_from_md'><strong>N = 1,191</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">type</td>
<td headers="stat_0" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Lit. Review/Method Intervention</td>
<td headers="stat_0" class="gt_row gt_center">165 (14%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Original Research</td>
<td headers="stat_0" class="gt_row gt_center">1,024 (86%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Response Article</td>
<td headers="stat_0" class="gt_row gt_center">2 (0.2%)</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="2"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::


{{< pagebreak >}}






### 6. How many publications are books, "book/theses" (PhD theses), articles, or "chapter/articles" (book chapters)?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="koekrgpllr" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#koekrgpllr table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#koekrgpllr thead, #koekrgpllr tbody, #koekrgpllr tfoot, #koekrgpllr tr, #koekrgpllr td, #koekrgpllr th {
  border-style: none;
}

#koekrgpllr p {
  margin: 0;
  padding: 0;
}

#koekrgpllr .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#koekrgpllr .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#koekrgpllr .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#koekrgpllr .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#koekrgpllr .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#koekrgpllr .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#koekrgpllr .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#koekrgpllr .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#koekrgpllr .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#koekrgpllr .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#koekrgpllr .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#koekrgpllr .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#koekrgpllr .gt_spanner_row {
  border-bottom-style: hidden;
}

#koekrgpllr .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#koekrgpllr .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#koekrgpllr .gt_from_md > :first-child {
  margin-top: 0;
}

#koekrgpllr .gt_from_md > :last-child {
  margin-bottom: 0;
}

#koekrgpllr .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#koekrgpllr .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#koekrgpllr .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#koekrgpllr .gt_row_group_first td {
  border-top-width: 2px;
}

#koekrgpllr .gt_row_group_first th {
  border-top-width: 2px;
}

#koekrgpllr .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#koekrgpllr .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#koekrgpllr .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#koekrgpllr .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#koekrgpllr .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#koekrgpllr .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#koekrgpllr .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#koekrgpllr .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#koekrgpllr .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#koekrgpllr .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#koekrgpllr .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#koekrgpllr .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#koekrgpllr .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#koekrgpllr .gt_left {
  text-align: left;
}

#koekrgpllr .gt_center {
  text-align: center;
}

#koekrgpllr .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#koekrgpllr .gt_font_normal {
  font-weight: normal;
}

#koekrgpllr .gt_font_bold {
  font-weight: bold;
}

#koekrgpllr .gt_font_italic {
  font-style: italic;
}

#koekrgpllr .gt_super {
  font-size: 65%;
}

#koekrgpllr .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#koekrgpllr .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#koekrgpllr .gt_indent_1 {
  text-indent: 5px;
}

#koekrgpllr .gt_indent_2 {
  text-indent: 10px;
}

#koekrgpllr .gt_indent_3 {
  text-indent: 15px;
}

#koekrgpllr .gt_indent_4 {
  text-indent: 20px;
}

#koekrgpllr .gt_indent_5 {
  text-indent: 25px;
}

#koekrgpllr .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#koekrgpllr div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_0"><span data-qmd-base64="PHN0cm9uZz5OID0gMSwxOTE8L3N0cm9uZz4="><span class='gt_from_md'><strong>N = 1,191</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Publication Type</td>
<td headers="stat_0" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Article</td>
<td headers="stat_0" class="gt_row gt_center">887 (74%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Book</td>
<td headers="stat_0" class="gt_row gt_center">55 (4.6%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Book/Thesis</td>
<td headers="stat_0" class="gt_row gt_center">2 (0.2%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Chapter/Article</td>
<td headers="stat_0" class="gt_row gt_center">247 (21%)</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="2"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 7. How many of our publications use AGW to argue for their importance?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="tsuulhoizf" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#tsuulhoizf table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#tsuulhoizf thead, #tsuulhoizf tbody, #tsuulhoizf tfoot, #tsuulhoizf tr, #tsuulhoizf td, #tsuulhoizf th {
  border-style: none;
}

#tsuulhoizf p {
  margin: 0;
  padding: 0;
}

#tsuulhoizf .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#tsuulhoizf .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#tsuulhoizf .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#tsuulhoizf .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#tsuulhoizf .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#tsuulhoizf .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#tsuulhoizf .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#tsuulhoizf .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#tsuulhoizf .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#tsuulhoizf .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#tsuulhoizf .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#tsuulhoizf .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#tsuulhoizf .gt_spanner_row {
  border-bottom-style: hidden;
}

#tsuulhoizf .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#tsuulhoizf .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#tsuulhoizf .gt_from_md > :first-child {
  margin-top: 0;
}

#tsuulhoizf .gt_from_md > :last-child {
  margin-bottom: 0;
}

#tsuulhoizf .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#tsuulhoizf .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#tsuulhoizf .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#tsuulhoizf .gt_row_group_first td {
  border-top-width: 2px;
}

#tsuulhoizf .gt_row_group_first th {
  border-top-width: 2px;
}

#tsuulhoizf .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#tsuulhoizf .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#tsuulhoizf .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#tsuulhoizf .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#tsuulhoizf .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#tsuulhoizf .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#tsuulhoizf .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#tsuulhoizf .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#tsuulhoizf .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#tsuulhoizf .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#tsuulhoizf .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#tsuulhoizf .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#tsuulhoizf .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#tsuulhoizf .gt_left {
  text-align: left;
}

#tsuulhoizf .gt_center {
  text-align: center;
}

#tsuulhoizf .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#tsuulhoizf .gt_font_normal {
  font-weight: normal;
}

#tsuulhoizf .gt_font_bold {
  font-weight: bold;
}

#tsuulhoizf .gt_font_italic {
  font-style: italic;
}

#tsuulhoizf .gt_super {
  font-size: 65%;
}

#tsuulhoizf .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#tsuulhoizf .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#tsuulhoizf .gt_indent_1 {
  text-indent: 5px;
}

#tsuulhoizf .gt_indent_2 {
  text-indent: 10px;
}

#tsuulhoizf .gt_indent_3 {
  text-indent: 15px;
}

#tsuulhoizf .gt_indent_4 {
  text-indent: 20px;
}

#tsuulhoizf .gt_indent_5 {
  text-indent: 25px;
}

#tsuulhoizf .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#tsuulhoizf div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_0"><span data-qmd-base64="PHN0cm9uZz5OID0gMSwxOTE8L3N0cm9uZz4="><span class='gt_from_md'><strong>N = 1,191</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Uses AGW</td>
<td headers="stat_0" class="gt_row gt_center">658 (55%)</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="2"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 8. How many of our publications include lessons for the present/future?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="ryrgubcdhl" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#ryrgubcdhl table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#ryrgubcdhl thead, #ryrgubcdhl tbody, #ryrgubcdhl tfoot, #ryrgubcdhl tr, #ryrgubcdhl td, #ryrgubcdhl th {
  border-style: none;
}

#ryrgubcdhl p {
  margin: 0;
  padding: 0;
}

#ryrgubcdhl .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#ryrgubcdhl .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#ryrgubcdhl .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#ryrgubcdhl .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#ryrgubcdhl .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#ryrgubcdhl .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ryrgubcdhl .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#ryrgubcdhl .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#ryrgubcdhl .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#ryrgubcdhl .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#ryrgubcdhl .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#ryrgubcdhl .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#ryrgubcdhl .gt_spanner_row {
  border-bottom-style: hidden;
}

#ryrgubcdhl .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#ryrgubcdhl .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#ryrgubcdhl .gt_from_md > :first-child {
  margin-top: 0;
}

#ryrgubcdhl .gt_from_md > :last-child {
  margin-bottom: 0;
}

#ryrgubcdhl .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#ryrgubcdhl .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#ryrgubcdhl .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#ryrgubcdhl .gt_row_group_first td {
  border-top-width: 2px;
}

#ryrgubcdhl .gt_row_group_first th {
  border-top-width: 2px;
}

#ryrgubcdhl .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ryrgubcdhl .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#ryrgubcdhl .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#ryrgubcdhl .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ryrgubcdhl .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ryrgubcdhl .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#ryrgubcdhl .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#ryrgubcdhl .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#ryrgubcdhl .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ryrgubcdhl .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#ryrgubcdhl .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ryrgubcdhl .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#ryrgubcdhl .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ryrgubcdhl .gt_left {
  text-align: left;
}

#ryrgubcdhl .gt_center {
  text-align: center;
}

#ryrgubcdhl .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#ryrgubcdhl .gt_font_normal {
  font-weight: normal;
}

#ryrgubcdhl .gt_font_bold {
  font-weight: bold;
}

#ryrgubcdhl .gt_font_italic {
  font-style: italic;
}

#ryrgubcdhl .gt_super {
  font-size: 65%;
}

#ryrgubcdhl .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#ryrgubcdhl .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#ryrgubcdhl .gt_indent_1 {
  text-indent: 5px;
}

#ryrgubcdhl .gt_indent_2 {
  text-indent: 10px;
}

#ryrgubcdhl .gt_indent_3 {
  text-indent: 15px;
}

#ryrgubcdhl .gt_indent_4 {
  text-indent: 20px;
}

#ryrgubcdhl .gt_indent_5 {
  text-indent: 25px;
}

#ryrgubcdhl .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#ryrgubcdhl div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_0"><span data-qmd-base64="PHN0cm9uZz5OID0gMSwxOTE8L3N0cm9uZz4="><span class='gt_from_md'><strong>N = 1,191</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Includes lessons</td>
<td headers="stat_0" class="gt_row gt_center">194 (16%)</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="2"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 9. What types of lessons or recommendations are most common?

Note, some papers can have multiple recommendation types. This analysis counts those separately (like we do for periods) so our N is greater than the number of articles.



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="cmguwyvaar" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#cmguwyvaar table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#cmguwyvaar thead, #cmguwyvaar tbody, #cmguwyvaar tfoot, #cmguwyvaar tr, #cmguwyvaar td, #cmguwyvaar th {
  border-style: none;
}

#cmguwyvaar p {
  margin: 0;
  padding: 0;
}

#cmguwyvaar .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#cmguwyvaar .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#cmguwyvaar .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#cmguwyvaar .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#cmguwyvaar .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#cmguwyvaar .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#cmguwyvaar .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#cmguwyvaar .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#cmguwyvaar .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#cmguwyvaar .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#cmguwyvaar .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#cmguwyvaar .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#cmguwyvaar .gt_spanner_row {
  border-bottom-style: hidden;
}

#cmguwyvaar .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#cmguwyvaar .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#cmguwyvaar .gt_from_md > :first-child {
  margin-top: 0;
}

#cmguwyvaar .gt_from_md > :last-child {
  margin-bottom: 0;
}

#cmguwyvaar .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#cmguwyvaar .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#cmguwyvaar .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#cmguwyvaar .gt_row_group_first td {
  border-top-width: 2px;
}

#cmguwyvaar .gt_row_group_first th {
  border-top-width: 2px;
}

#cmguwyvaar .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#cmguwyvaar .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#cmguwyvaar .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#cmguwyvaar .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#cmguwyvaar .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#cmguwyvaar .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#cmguwyvaar .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#cmguwyvaar .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#cmguwyvaar .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#cmguwyvaar .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#cmguwyvaar .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#cmguwyvaar .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#cmguwyvaar .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#cmguwyvaar .gt_left {
  text-align: left;
}

#cmguwyvaar .gt_center {
  text-align: center;
}

#cmguwyvaar .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#cmguwyvaar .gt_font_normal {
  font-weight: normal;
}

#cmguwyvaar .gt_font_bold {
  font-weight: bold;
}

#cmguwyvaar .gt_font_italic {
  font-style: italic;
}

#cmguwyvaar .gt_super {
  font-size: 65%;
}

#cmguwyvaar .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#cmguwyvaar .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#cmguwyvaar .gt_indent_1 {
  text-indent: 5px;
}

#cmguwyvaar .gt_indent_2 {
  text-indent: 10px;
}

#cmguwyvaar .gt_indent_3 {
  text-indent: 15px;
}

#cmguwyvaar .gt_indent_4 {
  text-indent: 20px;
}

#cmguwyvaar .gt_indent_5 {
  text-indent: 25px;
}

#cmguwyvaar .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#cmguwyvaar div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_0"><span data-qmd-base64="PHN0cm9uZz5OID0gMSwyMjQ8L3N0cm9uZz4="><span class='gt_from_md'><strong>N = 1,224</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">rec_type</td>
<td headers="stat_0" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Broad, abstract, or vague</td>
<td headers="stat_0" class="gt_row gt_center">94 (7.7%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific but not actionable</td>
<td headers="stat_0" class="gt_row gt_center">77 (6.3%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific and actionable</td>
<td headers="stat_0" class="gt_row gt_center">56 (4.6%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    No recommendation</td>
<td headers="stat_0" class="gt_row gt_center">997 (81%)</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="2"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::


{{< pagebreak >}}






### 10. Among lessons (so leaving out "none of the above") what types of lessons or recommendations are most common?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="mvtzctxmwk" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#mvtzctxmwk table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#mvtzctxmwk thead, #mvtzctxmwk tbody, #mvtzctxmwk tfoot, #mvtzctxmwk tr, #mvtzctxmwk td, #mvtzctxmwk th {
  border-style: none;
}

#mvtzctxmwk p {
  margin: 0;
  padding: 0;
}

#mvtzctxmwk .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#mvtzctxmwk .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#mvtzctxmwk .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#mvtzctxmwk .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#mvtzctxmwk .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#mvtzctxmwk .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#mvtzctxmwk .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#mvtzctxmwk .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#mvtzctxmwk .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#mvtzctxmwk .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#mvtzctxmwk .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#mvtzctxmwk .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#mvtzctxmwk .gt_spanner_row {
  border-bottom-style: hidden;
}

#mvtzctxmwk .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#mvtzctxmwk .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#mvtzctxmwk .gt_from_md > :first-child {
  margin-top: 0;
}

#mvtzctxmwk .gt_from_md > :last-child {
  margin-bottom: 0;
}

#mvtzctxmwk .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#mvtzctxmwk .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#mvtzctxmwk .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#mvtzctxmwk .gt_row_group_first td {
  border-top-width: 2px;
}

#mvtzctxmwk .gt_row_group_first th {
  border-top-width: 2px;
}

#mvtzctxmwk .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mvtzctxmwk .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#mvtzctxmwk .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#mvtzctxmwk .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#mvtzctxmwk .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mvtzctxmwk .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#mvtzctxmwk .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#mvtzctxmwk .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#mvtzctxmwk .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#mvtzctxmwk .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#mvtzctxmwk .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mvtzctxmwk .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#mvtzctxmwk .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mvtzctxmwk .gt_left {
  text-align: left;
}

#mvtzctxmwk .gt_center {
  text-align: center;
}

#mvtzctxmwk .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#mvtzctxmwk .gt_font_normal {
  font-weight: normal;
}

#mvtzctxmwk .gt_font_bold {
  font-weight: bold;
}

#mvtzctxmwk .gt_font_italic {
  font-style: italic;
}

#mvtzctxmwk .gt_super {
  font-size: 65%;
}

#mvtzctxmwk .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#mvtzctxmwk .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#mvtzctxmwk .gt_indent_1 {
  text-indent: 5px;
}

#mvtzctxmwk .gt_indent_2 {
  text-indent: 10px;
}

#mvtzctxmwk .gt_indent_3 {
  text-indent: 15px;
}

#mvtzctxmwk .gt_indent_4 {
  text-indent: 20px;
}

#mvtzctxmwk .gt_indent_5 {
  text-indent: 25px;
}

#mvtzctxmwk .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#mvtzctxmwk div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_0"><span data-qmd-base64="PHN0cm9uZz5OID0gMjI3PC9zdHJvbmc+"><span class='gt_from_md'><strong>N = 227</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">rec_type</td>
<td headers="stat_0" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Broad, abstract, or vague</td>
<td headers="stat_0" class="gt_row gt_center">94 (41%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific but not actionable</td>
<td headers="stat_0" class="gt_row gt_center">77 (34%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific and actionable</td>
<td headers="stat_0" class="gt_row gt_center">56 (25%)</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    No recommendation</td>
<td headers="stat_0" class="gt_row gt_center">0 (0%)</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="2"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 11. How many of our publications in each discipline use methods that are quantitative, qualitative, both, or neither?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="ipbcdxsphm" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#ipbcdxsphm table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#ipbcdxsphm thead, #ipbcdxsphm tbody, #ipbcdxsphm tfoot, #ipbcdxsphm tr, #ipbcdxsphm td, #ipbcdxsphm th {
  border-style: none;
}

#ipbcdxsphm p {
  margin: 0;
  padding: 0;
}

#ipbcdxsphm .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#ipbcdxsphm .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#ipbcdxsphm .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#ipbcdxsphm .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#ipbcdxsphm .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#ipbcdxsphm .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ipbcdxsphm .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#ipbcdxsphm .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#ipbcdxsphm .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#ipbcdxsphm .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#ipbcdxsphm .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#ipbcdxsphm .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#ipbcdxsphm .gt_spanner_row {
  border-bottom-style: hidden;
}

#ipbcdxsphm .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#ipbcdxsphm .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#ipbcdxsphm .gt_from_md > :first-child {
  margin-top: 0;
}

#ipbcdxsphm .gt_from_md > :last-child {
  margin-bottom: 0;
}

#ipbcdxsphm .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#ipbcdxsphm .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#ipbcdxsphm .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#ipbcdxsphm .gt_row_group_first td {
  border-top-width: 2px;
}

#ipbcdxsphm .gt_row_group_first th {
  border-top-width: 2px;
}

#ipbcdxsphm .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ipbcdxsphm .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#ipbcdxsphm .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#ipbcdxsphm .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ipbcdxsphm .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ipbcdxsphm .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#ipbcdxsphm .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#ipbcdxsphm .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#ipbcdxsphm .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ipbcdxsphm .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#ipbcdxsphm .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ipbcdxsphm .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#ipbcdxsphm .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ipbcdxsphm .gt_left {
  text-align: left;
}

#ipbcdxsphm .gt_center {
  text-align: center;
}

#ipbcdxsphm .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#ipbcdxsphm .gt_font_normal {
  font-weight: normal;
}

#ipbcdxsphm .gt_font_bold {
  font-weight: bold;
}

#ipbcdxsphm .gt_font_italic {
  font-style: italic;
}

#ipbcdxsphm .gt_super {
  font-size: 65%;
}

#ipbcdxsphm .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#ipbcdxsphm .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#ipbcdxsphm .gt_indent_1 {
  text-indent: 5px;
}

#ipbcdxsphm .gt_indent_2 {
  text-indent: 10px;
}

#ipbcdxsphm .gt_indent_3 {
  text-indent: 15px;
}

#ipbcdxsphm .gt_indent_4 {
  text-indent: 20px;
}

#ipbcdxsphm .gt_indent_5 {
  text-indent: 25px;
}

#ipbcdxsphm .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#ipbcdxsphm div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Cb3RoPC9zdHJvbmc+PGJyIC8+Ck4gPSAxNjQ="><span class='gt_from_md'><strong>Both</strong><br />
N = 164</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5OZWl0aGVyPC9zdHJvbmc+PGJyIC8+Ck4gPSAxMjY="><span class='gt_from_md'><strong>Neither</strong><br />
N = 126</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5RdWFsaXRhdGl2ZTwvc3Ryb25nPjxiciAvPgpOID0gMjE5"><span class='gt_from_md'><strong>Qualitative</strong><br />
N = 219</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5RdWFudGl0YXRpdmU8L3N0cm9uZz48YnIgLz4KTiA9IDY4Mg=="><span class='gt_from_md'><strong>Quantitative</strong><br />
N = 682</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Discipline</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="stat_3" class="gt_row gt_center"><br /></td>
<td headers="stat_4" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Archaeology</td>
<td headers="stat_1" class="gt_row gt_center">29 (18%)</td>
<td headers="stat_2" class="gt_row gt_center">16 (13%)</td>
<td headers="stat_3" class="gt_row gt_center">25 (11%)</td>
<td headers="stat_4" class="gt_row gt_center">79 (12%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Economics</td>
<td headers="stat_1" class="gt_row gt_center">2 (1.2%)</td>
<td headers="stat_2" class="gt_row gt_center">0 (0%)</td>
<td headers="stat_3" class="gt_row gt_center">1 (0.5%)</td>
<td headers="stat_4" class="gt_row gt_center">2 (0.3%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Epidemiology</td>
<td headers="stat_1" class="gt_row gt_center">0 (0%)</td>
<td headers="stat_2" class="gt_row gt_center">1 (0.8%)</td>
<td headers="stat_3" class="gt_row gt_center">0 (0%)</td>
<td headers="stat_4" class="gt_row gt_center">1 (0.1%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Geography</td>
<td headers="stat_1" class="gt_row gt_center">3 (1.8%)</td>
<td headers="stat_2" class="gt_row gt_center">0 (0%)</td>
<td headers="stat_3" class="gt_row gt_center">11 (5.0%)</td>
<td headers="stat_4" class="gt_row gt_center">11 (1.6%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    History</td>
<td headers="stat_1" class="gt_row gt_center">30 (18%)</td>
<td headers="stat_2" class="gt_row gt_center">36 (29%)</td>
<td headers="stat_3" class="gt_row gt_center">127 (58%)</td>
<td headers="stat_4" class="gt_row gt_center">13 (1.9%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Joint Fields</td>
<td headers="stat_1" class="gt_row gt_center">91 (55%)</td>
<td headers="stat_2" class="gt_row gt_center">23 (18%)</td>
<td headers="stat_3" class="gt_row gt_center">8 (3.7%)</td>
<td headers="stat_4" class="gt_row gt_center">89 (13%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Literature</td>
<td headers="stat_1" class="gt_row gt_center">0 (0%)</td>
<td headers="stat_2" class="gt_row gt_center">4 (3.2%)</td>
<td headers="stat_3" class="gt_row gt_center">31 (14%)</td>
<td headers="stat_4" class="gt_row gt_center">0 (0%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Other</td>
<td headers="stat_1" class="gt_row gt_center">1 (0.6%)</td>
<td headers="stat_2" class="gt_row gt_center">4 (3.2%)</td>
<td headers="stat_3" class="gt_row gt_center">5 (2.3%)</td>
<td headers="stat_4" class="gt_row gt_center">3 (0.4%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Paleoclimatology</td>
<td headers="stat_1" class="gt_row gt_center">8 (4.9%)</td>
<td headers="stat_2" class="gt_row gt_center">42 (33%)</td>
<td headers="stat_3" class="gt_row gt_center">11 (5.0%)</td>
<td headers="stat_4" class="gt_row gt_center">484 (71%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 12. How many publications that are *not* in Paleoclimatology/Historical Climatology use Quantitative Analysis?



::: {.cell}

:::



354 publications from disciplines other than paleoclimatology use quantitative analysis.




{{< pagebreak >}}






### 13. What percentage of publications in every method consider each region?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="bsciaykgmt" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#bsciaykgmt table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#bsciaykgmt thead, #bsciaykgmt tbody, #bsciaykgmt tfoot, #bsciaykgmt tr, #bsciaykgmt td, #bsciaykgmt th {
  border-style: none;
}

#bsciaykgmt p {
  margin: 0;
  padding: 0;
}

#bsciaykgmt .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#bsciaykgmt .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#bsciaykgmt .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#bsciaykgmt .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#bsciaykgmt .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#bsciaykgmt .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#bsciaykgmt .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#bsciaykgmt .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#bsciaykgmt .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#bsciaykgmt .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#bsciaykgmt .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#bsciaykgmt .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#bsciaykgmt .gt_spanner_row {
  border-bottom-style: hidden;
}

#bsciaykgmt .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#bsciaykgmt .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#bsciaykgmt .gt_from_md > :first-child {
  margin-top: 0;
}

#bsciaykgmt .gt_from_md > :last-child {
  margin-bottom: 0;
}

#bsciaykgmt .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#bsciaykgmt .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#bsciaykgmt .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#bsciaykgmt .gt_row_group_first td {
  border-top-width: 2px;
}

#bsciaykgmt .gt_row_group_first th {
  border-top-width: 2px;
}

#bsciaykgmt .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#bsciaykgmt .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#bsciaykgmt .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#bsciaykgmt .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#bsciaykgmt .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#bsciaykgmt .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#bsciaykgmt .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#bsciaykgmt .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#bsciaykgmt .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#bsciaykgmt .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#bsciaykgmt .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#bsciaykgmt .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#bsciaykgmt .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#bsciaykgmt .gt_left {
  text-align: left;
}

#bsciaykgmt .gt_center {
  text-align: center;
}

#bsciaykgmt .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#bsciaykgmt .gt_font_normal {
  font-weight: normal;
}

#bsciaykgmt .gt_font_bold {
  font-weight: bold;
}

#bsciaykgmt .gt_font_italic {
  font-style: italic;
}

#bsciaykgmt .gt_super {
  font-size: 65%;
}

#bsciaykgmt .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#bsciaykgmt .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#bsciaykgmt .gt_indent_1 {
  text-indent: 5px;
}

#bsciaykgmt .gt_indent_2 {
  text-indent: 10px;
}

#bsciaykgmt .gt_indent_3 {
  text-indent: 15px;
}

#bsciaykgmt .gt_indent_4 {
  text-indent: 20px;
}

#bsciaykgmt .gt_indent_5 {
  text-indent: 25px;
}

#bsciaykgmt .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#bsciaykgmt div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Cb3RoPC9zdHJvbmc+PGJyIC8+Ck4gPSAxNjQ="><span class='gt_from_md'><strong>Both</strong><br />
N = 164</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5OZWl0aGVyPC9zdHJvbmc+PGJyIC8+Ck4gPSAxMjY="><span class='gt_from_md'><strong>Neither</strong><br />
N = 126</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5RdWFsaXRhdGl2ZTwvc3Ryb25nPjxiciAvPgpOID0gMjE5"><span class='gt_from_md'><strong>Qualitative</strong><br />
N = 219</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5RdWFudGl0YXRpdmU8L3N0cm9uZz48YnIgLz4KTiA9IDY4Mg=="><span class='gt_from_md'><strong>Quantitative</strong><br />
N = 682</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Geographic Region</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="stat_3" class="gt_row gt_center"><br /></td>
<td headers="stat_4" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Africa</td>
<td headers="stat_1" class="gt_row gt_center">9 (5.5%)</td>
<td headers="stat_2" class="gt_row gt_center">0 (0%)</td>
<td headers="stat_3" class="gt_row gt_center">9 (4.1%)</td>
<td headers="stat_4" class="gt_row gt_center">27 (4.0%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Americas</td>
<td headers="stat_1" class="gt_row gt_center">18 (11%)</td>
<td headers="stat_2" class="gt_row gt_center">8 (6.3%)</td>
<td headers="stat_3" class="gt_row gt_center">38 (17%)</td>
<td headers="stat_4" class="gt_row gt_center">110 (16%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Asia</td>
<td headers="stat_1" class="gt_row gt_center">25 (15%)</td>
<td headers="stat_2" class="gt_row gt_center">9 (7.1%)</td>
<td headers="stat_3" class="gt_row gt_center">9 (4.1%)</td>
<td headers="stat_4" class="gt_row gt_center">228 (33%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Europe</td>
<td headers="stat_1" class="gt_row gt_center">66 (40%)</td>
<td headers="stat_2" class="gt_row gt_center">26 (21%)</td>
<td headers="stat_3" class="gt_row gt_center">96 (44%)</td>
<td headers="stat_4" class="gt_row gt_center">159 (23%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Global</td>
<td headers="stat_1" class="gt_row gt_center">22 (13%)</td>
<td headers="stat_2" class="gt_row gt_center">80 (63%)</td>
<td headers="stat_3" class="gt_row gt_center">43 (20%)</td>
<td headers="stat_4" class="gt_row gt_center">83 (12%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Middle East</td>
<td headers="stat_1" class="gt_row gt_center">20 (12%)</td>
<td headers="stat_2" class="gt_row gt_center">0 (0%)</td>
<td headers="stat_3" class="gt_row gt_center">12 (5.5%)</td>
<td headers="stat_4" class="gt_row gt_center">29 (4.3%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Oceania</td>
<td headers="stat_1" class="gt_row gt_center">3 (1.8%)</td>
<td headers="stat_2" class="gt_row gt_center">1 (0.8%)</td>
<td headers="stat_3" class="gt_row gt_center">6 (2.7%)</td>
<td headers="stat_4" class="gt_row gt_center">15 (2.2%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Polar</td>
<td headers="stat_1" class="gt_row gt_center">1 (0.6%)</td>
<td headers="stat_2" class="gt_row gt_center">2 (1.6%)</td>
<td headers="stat_3" class="gt_row gt_center">6 (2.7%)</td>
<td headers="stat_4" class="gt_row gt_center">31 (4.5%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



## Compound Questions

### 1. What percentage of publications in each discipline and method use AGW to argue for their importance?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="fpzfzjxpaa" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#fpzfzjxpaa table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#fpzfzjxpaa thead, #fpzfzjxpaa tbody, #fpzfzjxpaa tfoot, #fpzfzjxpaa tr, #fpzfzjxpaa td, #fpzfzjxpaa th {
  border-style: none;
}

#fpzfzjxpaa p {
  margin: 0;
  padding: 0;
}

#fpzfzjxpaa .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#fpzfzjxpaa .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#fpzfzjxpaa .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#fpzfzjxpaa .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#fpzfzjxpaa .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#fpzfzjxpaa .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#fpzfzjxpaa .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#fpzfzjxpaa .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#fpzfzjxpaa .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#fpzfzjxpaa .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#fpzfzjxpaa .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#fpzfzjxpaa .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#fpzfzjxpaa .gt_spanner_row {
  border-bottom-style: hidden;
}

#fpzfzjxpaa .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#fpzfzjxpaa .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#fpzfzjxpaa .gt_from_md > :first-child {
  margin-top: 0;
}

#fpzfzjxpaa .gt_from_md > :last-child {
  margin-bottom: 0;
}

#fpzfzjxpaa .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#fpzfzjxpaa .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#fpzfzjxpaa .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#fpzfzjxpaa .gt_row_group_first td {
  border-top-width: 2px;
}

#fpzfzjxpaa .gt_row_group_first th {
  border-top-width: 2px;
}

#fpzfzjxpaa .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fpzfzjxpaa .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#fpzfzjxpaa .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#fpzfzjxpaa .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#fpzfzjxpaa .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fpzfzjxpaa .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#fpzfzjxpaa .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#fpzfzjxpaa .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#fpzfzjxpaa .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#fpzfzjxpaa .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#fpzfzjxpaa .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fpzfzjxpaa .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#fpzfzjxpaa .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fpzfzjxpaa .gt_left {
  text-align: left;
}

#fpzfzjxpaa .gt_center {
  text-align: center;
}

#fpzfzjxpaa .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#fpzfzjxpaa .gt_font_normal {
  font-weight: normal;
}

#fpzfzjxpaa .gt_font_bold {
  font-weight: bold;
}

#fpzfzjxpaa .gt_font_italic {
  font-style: italic;
}

#fpzfzjxpaa .gt_super {
  font-size: 65%;
}

#fpzfzjxpaa .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#fpzfzjxpaa .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#fpzfzjxpaa .gt_indent_1 {
  text-indent: 5px;
}

#fpzfzjxpaa .gt_indent_2 {
  text-indent: 10px;
}

#fpzfzjxpaa .gt_indent_3 {
  text-indent: 15px;
}

#fpzfzjxpaa .gt_indent_4 {
  text-indent: 20px;
}

#fpzfzjxpaa .gt_indent_5 {
  text-indent: 25px;
}

#fpzfzjxpaa .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#fpzfzjxpaa div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Obzwvc3Ryb25nPjxiciAvPgpOID0gNTMz"><span class='gt_from_md'><strong>No</strong><br />
N = 533</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5ZZXM8L3N0cm9uZz48YnIgLz4KTiA9IDY1OA=="><span class='gt_from_md'><strong>Yes</strong><br />
N = 658</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Discipline</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Archaeology</td>
<td headers="stat_1" class="gt_row gt_center">74 (14%)</td>
<td headers="stat_2" class="gt_row gt_center">75 (11%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Economics</td>
<td headers="stat_1" class="gt_row gt_center">2 (0.4%)</td>
<td headers="stat_2" class="gt_row gt_center">3 (0.5%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Epidemiology</td>
<td headers="stat_1" class="gt_row gt_center">0 (0%)</td>
<td headers="stat_2" class="gt_row gt_center">2 (0.3%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Geography</td>
<td headers="stat_1" class="gt_row gt_center">8 (1.5%)</td>
<td headers="stat_2" class="gt_row gt_center">17 (2.6%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    History</td>
<td headers="stat_1" class="gt_row gt_center">130 (24%)</td>
<td headers="stat_2" class="gt_row gt_center">76 (12%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Joint Fields</td>
<td headers="stat_1" class="gt_row gt_center">121 (23%)</td>
<td headers="stat_2" class="gt_row gt_center">90 (14%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Literature</td>
<td headers="stat_1" class="gt_row gt_center">15 (2.8%)</td>
<td headers="stat_2" class="gt_row gt_center">20 (3.0%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Other</td>
<td headers="stat_1" class="gt_row gt_center">3 (0.6%)</td>
<td headers="stat_2" class="gt_row gt_center">10 (1.5%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Paleoclimatology</td>
<td headers="stat_1" class="gt_row gt_center">180 (34%)</td>
<td headers="stat_2" class="gt_row gt_center">365 (55%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Method</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Both</td>
<td headers="stat_1" class="gt_row gt_center">95 (18%)</td>
<td headers="stat_2" class="gt_row gt_center">69 (10%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Neither</td>
<td headers="stat_1" class="gt_row gt_center">54 (10%)</td>
<td headers="stat_2" class="gt_row gt_center">72 (11%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Qualitative</td>
<td headers="stat_1" class="gt_row gt_center">122 (23%)</td>
<td headers="stat_2" class="gt_row gt_center">97 (15%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Quantitative</td>
<td headers="stat_1" class="gt_row gt_center">262 (49%)</td>
<td headers="stat_2" class="gt_row gt_center">420 (64%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk7IFBlYXJzb27igJlzIENoaS1zcXVhcmVkIHRlc3Q="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates); Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::


{{< pagebreak >}}






### 2a. What percentage of publications in Paleoclimatology/Historical Climatology use modern global warming to argue for their significance? What percentage of publications in all *other* disciplines do the same?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="qnbvocqdzl" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#qnbvocqdzl table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#qnbvocqdzl thead, #qnbvocqdzl tbody, #qnbvocqdzl tfoot, #qnbvocqdzl tr, #qnbvocqdzl td, #qnbvocqdzl th {
  border-style: none;
}

#qnbvocqdzl p {
  margin: 0;
  padding: 0;
}

#qnbvocqdzl .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#qnbvocqdzl .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#qnbvocqdzl .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#qnbvocqdzl .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#qnbvocqdzl .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#qnbvocqdzl .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#qnbvocqdzl .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#qnbvocqdzl .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#qnbvocqdzl .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#qnbvocqdzl .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#qnbvocqdzl .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#qnbvocqdzl .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#qnbvocqdzl .gt_spanner_row {
  border-bottom-style: hidden;
}

#qnbvocqdzl .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#qnbvocqdzl .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#qnbvocqdzl .gt_from_md > :first-child {
  margin-top: 0;
}

#qnbvocqdzl .gt_from_md > :last-child {
  margin-bottom: 0;
}

#qnbvocqdzl .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#qnbvocqdzl .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#qnbvocqdzl .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#qnbvocqdzl .gt_row_group_first td {
  border-top-width: 2px;
}

#qnbvocqdzl .gt_row_group_first th {
  border-top-width: 2px;
}

#qnbvocqdzl .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#qnbvocqdzl .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#qnbvocqdzl .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#qnbvocqdzl .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#qnbvocqdzl .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#qnbvocqdzl .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#qnbvocqdzl .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#qnbvocqdzl .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#qnbvocqdzl .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#qnbvocqdzl .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#qnbvocqdzl .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#qnbvocqdzl .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#qnbvocqdzl .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#qnbvocqdzl .gt_left {
  text-align: left;
}

#qnbvocqdzl .gt_center {
  text-align: center;
}

#qnbvocqdzl .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#qnbvocqdzl .gt_font_normal {
  font-weight: normal;
}

#qnbvocqdzl .gt_font_bold {
  font-weight: bold;
}

#qnbvocqdzl .gt_font_italic {
  font-style: italic;
}

#qnbvocqdzl .gt_super {
  font-size: 65%;
}

#qnbvocqdzl .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#qnbvocqdzl .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#qnbvocqdzl .gt_indent_1 {
  text-indent: 5px;
}

#qnbvocqdzl .gt_indent_2 {
  text-indent: 10px;
}

#qnbvocqdzl .gt_indent_3 {
  text-indent: 15px;
}

#qnbvocqdzl .gt_indent_4 {
  text-indent: 20px;
}

#qnbvocqdzl .gt_indent_5 {
  text-indent: 25px;
}

#qnbvocqdzl .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#qnbvocqdzl div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5BbGwgb3RoZXIgZGlzY2lwbGluZXM8L3N0cm9uZz48YnIgLz4KTiA9IDY0Ng=="><span class='gt_from_md'><strong>All other disciplines</strong><br />
N = 646</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5QYWxlb2NsaW1hdG9sb2d5PC9zdHJvbmc+PGJyIC8+Ck4gPSA1NDU="><span class='gt_from_md'><strong>Paleoclimatology</strong><br />
N = 545</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Uses AGW</td>
<td headers="stat_1" class="gt_row gt_center">293 (45%)</td>
<td headers="stat_2" class="gt_row gt_center">365 (67%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 2b. What percentage of publications using quantitative analysis use modern global warming to argue for their significance? And what percentage of publications using the other methods do the same?

Note that here we again combine Quantitative and Both categories.



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="bqydfygayi" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#bqydfygayi table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#bqydfygayi thead, #bqydfygayi tbody, #bqydfygayi tfoot, #bqydfygayi tr, #bqydfygayi td, #bqydfygayi th {
  border-style: none;
}

#bqydfygayi p {
  margin: 0;
  padding: 0;
}

#bqydfygayi .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#bqydfygayi .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#bqydfygayi .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#bqydfygayi .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#bqydfygayi .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#bqydfygayi .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#bqydfygayi .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#bqydfygayi .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#bqydfygayi .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#bqydfygayi .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#bqydfygayi .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#bqydfygayi .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#bqydfygayi .gt_spanner_row {
  border-bottom-style: hidden;
}

#bqydfygayi .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#bqydfygayi .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#bqydfygayi .gt_from_md > :first-child {
  margin-top: 0;
}

#bqydfygayi .gt_from_md > :last-child {
  margin-bottom: 0;
}

#bqydfygayi .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#bqydfygayi .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#bqydfygayi .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#bqydfygayi .gt_row_group_first td {
  border-top-width: 2px;
}

#bqydfygayi .gt_row_group_first th {
  border-top-width: 2px;
}

#bqydfygayi .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#bqydfygayi .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#bqydfygayi .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#bqydfygayi .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#bqydfygayi .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#bqydfygayi .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#bqydfygayi .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#bqydfygayi .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#bqydfygayi .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#bqydfygayi .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#bqydfygayi .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#bqydfygayi .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#bqydfygayi .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#bqydfygayi .gt_left {
  text-align: left;
}

#bqydfygayi .gt_center {
  text-align: center;
}

#bqydfygayi .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#bqydfygayi .gt_font_normal {
  font-weight: normal;
}

#bqydfygayi .gt_font_bold {
  font-weight: bold;
}

#bqydfygayi .gt_font_italic {
  font-style: italic;
}

#bqydfygayi .gt_super {
  font-size: 65%;
}

#bqydfygayi .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#bqydfygayi .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#bqydfygayi .gt_indent_1 {
  text-indent: 5px;
}

#bqydfygayi .gt_indent_2 {
  text-indent: 10px;
}

#bqydfygayi .gt_indent_3 {
  text-indent: 15px;
}

#bqydfygayi .gt_indent_4 {
  text-indent: 20px;
}

#bqydfygayi .gt_indent_5 {
  text-indent: 25px;
}

#bqydfygayi .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#bqydfygayi div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5PdGhlciBNZXRob2RzPC9zdHJvbmc+PGJyIC8+Ck4gPSAzNDU="><span class='gt_from_md'><strong>Other Methods</strong><br />
N = 345</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5RdWFudGl0YXRpdmU8L3N0cm9uZz48YnIgLz4KTiA9IDg0Ng=="><span class='gt_from_md'><strong>Quantitative</strong><br />
N = 846</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Uses AGW</td>
<td headers="stat_1" class="gt_row gt_center">169 (49%)</td>
<td headers="stat_2" class="gt_row gt_center">489 (58%)</td>
<td headers="p.value" class="gt_row gt_center">0.006</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 3a. What percentage of publications from each region use AGW to argue for their importance?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="dvmjsdybqn" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#dvmjsdybqn table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#dvmjsdybqn thead, #dvmjsdybqn tbody, #dvmjsdybqn tfoot, #dvmjsdybqn tr, #dvmjsdybqn td, #dvmjsdybqn th {
  border-style: none;
}

#dvmjsdybqn p {
  margin: 0;
  padding: 0;
}

#dvmjsdybqn .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#dvmjsdybqn .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#dvmjsdybqn .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#dvmjsdybqn .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#dvmjsdybqn .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#dvmjsdybqn .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#dvmjsdybqn .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#dvmjsdybqn .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#dvmjsdybqn .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#dvmjsdybqn .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#dvmjsdybqn .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#dvmjsdybqn .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#dvmjsdybqn .gt_spanner_row {
  border-bottom-style: hidden;
}

#dvmjsdybqn .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#dvmjsdybqn .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#dvmjsdybqn .gt_from_md > :first-child {
  margin-top: 0;
}

#dvmjsdybqn .gt_from_md > :last-child {
  margin-bottom: 0;
}

#dvmjsdybqn .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#dvmjsdybqn .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#dvmjsdybqn .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#dvmjsdybqn .gt_row_group_first td {
  border-top-width: 2px;
}

#dvmjsdybqn .gt_row_group_first th {
  border-top-width: 2px;
}

#dvmjsdybqn .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#dvmjsdybqn .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#dvmjsdybqn .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#dvmjsdybqn .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#dvmjsdybqn .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#dvmjsdybqn .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#dvmjsdybqn .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#dvmjsdybqn .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#dvmjsdybqn .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#dvmjsdybqn .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#dvmjsdybqn .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#dvmjsdybqn .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#dvmjsdybqn .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#dvmjsdybqn .gt_left {
  text-align: left;
}

#dvmjsdybqn .gt_center {
  text-align: center;
}

#dvmjsdybqn .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#dvmjsdybqn .gt_font_normal {
  font-weight: normal;
}

#dvmjsdybqn .gt_font_bold {
  font-weight: bold;
}

#dvmjsdybqn .gt_font_italic {
  font-style: italic;
}

#dvmjsdybqn .gt_super {
  font-size: 65%;
}

#dvmjsdybqn .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#dvmjsdybqn .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#dvmjsdybqn .gt_indent_1 {
  text-indent: 5px;
}

#dvmjsdybqn .gt_indent_2 {
  text-indent: 10px;
}

#dvmjsdybqn .gt_indent_3 {
  text-indent: 15px;
}

#dvmjsdybqn .gt_indent_4 {
  text-indent: 20px;
}

#dvmjsdybqn .gt_indent_5 {
  text-indent: 25px;
}

#dvmjsdybqn .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#dvmjsdybqn div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Obzwvc3Ryb25nPjxiciAvPgpOID0gNTMz"><span class='gt_from_md'><strong>No</strong><br />
N = 533</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5ZZXM8L3N0cm9uZz48YnIgLz4KTiA9IDY1OA=="><span class='gt_from_md'><strong>Yes</strong><br />
N = 658</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Geographic Region</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Africa</td>
<td headers="stat_1" class="gt_row gt_center">22 (4.1%)</td>
<td headers="stat_2" class="gt_row gt_center">23 (3.5%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Americas</td>
<td headers="stat_1" class="gt_row gt_center">73 (14%)</td>
<td headers="stat_2" class="gt_row gt_center">101 (15%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Asia</td>
<td headers="stat_1" class="gt_row gt_center">89 (17%)</td>
<td headers="stat_2" class="gt_row gt_center">182 (28%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Europe</td>
<td headers="stat_1" class="gt_row gt_center">211 (40%)</td>
<td headers="stat_2" class="gt_row gt_center">136 (21%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Global</td>
<td headers="stat_1" class="gt_row gt_center">85 (16%)</td>
<td headers="stat_2" class="gt_row gt_center">143 (22%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Middle East</td>
<td headers="stat_1" class="gt_row gt_center">38 (7.1%)</td>
<td headers="stat_2" class="gt_row gt_center">23 (3.5%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Oceania</td>
<td headers="stat_1" class="gt_row gt_center">9 (1.7%)</td>
<td headers="stat_2" class="gt_row gt_center">16 (2.4%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Polar</td>
<td headers="stat_1" class="gt_row gt_center">6 (1.1%)</td>
<td headers="stat_2" class="gt_row gt_center">34 (5.2%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::


{{< pagebreak >}}






### 3b. What percentage of publications from each period use AGW to argue for their importance?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="ikmenbyfic" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#ikmenbyfic table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#ikmenbyfic thead, #ikmenbyfic tbody, #ikmenbyfic tfoot, #ikmenbyfic tr, #ikmenbyfic td, #ikmenbyfic th {
  border-style: none;
}

#ikmenbyfic p {
  margin: 0;
  padding: 0;
}

#ikmenbyfic .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#ikmenbyfic .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#ikmenbyfic .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#ikmenbyfic .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#ikmenbyfic .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#ikmenbyfic .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ikmenbyfic .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#ikmenbyfic .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#ikmenbyfic .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#ikmenbyfic .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#ikmenbyfic .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#ikmenbyfic .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#ikmenbyfic .gt_spanner_row {
  border-bottom-style: hidden;
}

#ikmenbyfic .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#ikmenbyfic .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#ikmenbyfic .gt_from_md > :first-child {
  margin-top: 0;
}

#ikmenbyfic .gt_from_md > :last-child {
  margin-bottom: 0;
}

#ikmenbyfic .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#ikmenbyfic .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#ikmenbyfic .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#ikmenbyfic .gt_row_group_first td {
  border-top-width: 2px;
}

#ikmenbyfic .gt_row_group_first th {
  border-top-width: 2px;
}

#ikmenbyfic .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ikmenbyfic .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#ikmenbyfic .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#ikmenbyfic .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ikmenbyfic .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ikmenbyfic .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#ikmenbyfic .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#ikmenbyfic .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#ikmenbyfic .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ikmenbyfic .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#ikmenbyfic .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ikmenbyfic .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#ikmenbyfic .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ikmenbyfic .gt_left {
  text-align: left;
}

#ikmenbyfic .gt_center {
  text-align: center;
}

#ikmenbyfic .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#ikmenbyfic .gt_font_normal {
  font-weight: normal;
}

#ikmenbyfic .gt_font_bold {
  font-weight: bold;
}

#ikmenbyfic .gt_font_italic {
  font-style: italic;
}

#ikmenbyfic .gt_super {
  font-size: 65%;
}

#ikmenbyfic .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#ikmenbyfic .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#ikmenbyfic .gt_indent_1 {
  text-indent: 5px;
}

#ikmenbyfic .gt_indent_2 {
  text-indent: 10px;
}

#ikmenbyfic .gt_indent_3 {
  text-indent: 15px;
}

#ikmenbyfic .gt_indent_4 {
  text-indent: 20px;
}

#ikmenbyfic .gt_indent_5 {
  text-indent: 25px;
}

#ikmenbyfic .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#ikmenbyfic div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Obzwvc3Ryb25nPjxiciAvPgpOID0gMSwyMzU="><span class='gt_from_md'><strong>No</strong><br />
N = 1,235</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5ZZXM8L3N0cm9uZz48YnIgLz4KTiA9IDIsMDI3"><span class='gt_from_md'><strong>Yes</strong><br />
N = 2,027</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">period</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Pleistocene</td>
<td headers="stat_1" class="gt_row gt_center">27 (2.2%)</td>
<td headers="stat_2" class="gt_row gt_center">38 (1.9%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Early-Mid Holocene</td>
<td headers="stat_1" class="gt_row gt_center">71 (5.7%)</td>
<td headers="stat_2" class="gt_row gt_center">74 (3.7%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Ancient</td>
<td headers="stat_1" class="gt_row gt_center">164 (13%)</td>
<td headers="stat_2" class="gt_row gt_center">181 (8.9%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Medieval</td>
<td headers="stat_1" class="gt_row gt_center">247 (20%)</td>
<td headers="stat_2" class="gt_row gt_center">322 (16%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Early Modern</td>
<td headers="stat_1" class="gt_row gt_center">276 (22%)</td>
<td headers="stat_2" class="gt_row gt_center">444 (22%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Modern</td>
<td headers="stat_1" class="gt_row gt_center">252 (20%)</td>
<td headers="stat_2" class="gt_row gt_center">499 (25%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Present</td>
<td headers="stat_1" class="gt_row gt_center">198 (16%)</td>
<td headers="stat_2" class="gt_row gt_center">469 (23%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 4. What percentage of publications that cover each region use global warming to argue for their significance?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="csugkcwflk" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#csugkcwflk table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#csugkcwflk thead, #csugkcwflk tbody, #csugkcwflk tfoot, #csugkcwflk tr, #csugkcwflk td, #csugkcwflk th {
  border-style: none;
}

#csugkcwflk p {
  margin: 0;
  padding: 0;
}

#csugkcwflk .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#csugkcwflk .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#csugkcwflk .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#csugkcwflk .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#csugkcwflk .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#csugkcwflk .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#csugkcwflk .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#csugkcwflk .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#csugkcwflk .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#csugkcwflk .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#csugkcwflk .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#csugkcwflk .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#csugkcwflk .gt_spanner_row {
  border-bottom-style: hidden;
}

#csugkcwflk .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#csugkcwflk .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#csugkcwflk .gt_from_md > :first-child {
  margin-top: 0;
}

#csugkcwflk .gt_from_md > :last-child {
  margin-bottom: 0;
}

#csugkcwflk .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#csugkcwflk .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#csugkcwflk .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#csugkcwflk .gt_row_group_first td {
  border-top-width: 2px;
}

#csugkcwflk .gt_row_group_first th {
  border-top-width: 2px;
}

#csugkcwflk .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#csugkcwflk .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#csugkcwflk .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#csugkcwflk .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#csugkcwflk .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#csugkcwflk .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#csugkcwflk .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#csugkcwflk .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#csugkcwflk .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#csugkcwflk .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#csugkcwflk .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#csugkcwflk .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#csugkcwflk .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#csugkcwflk .gt_left {
  text-align: left;
}

#csugkcwflk .gt_center {
  text-align: center;
}

#csugkcwflk .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#csugkcwflk .gt_font_normal {
  font-weight: normal;
}

#csugkcwflk .gt_font_bold {
  font-weight: bold;
}

#csugkcwflk .gt_font_italic {
  font-style: italic;
}

#csugkcwflk .gt_super {
  font-size: 65%;
}

#csugkcwflk .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#csugkcwflk .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#csugkcwflk .gt_indent_1 {
  text-indent: 5px;
}

#csugkcwflk .gt_indent_2 {
  text-indent: 10px;
}

#csugkcwflk .gt_indent_3 {
  text-indent: 15px;
}

#csugkcwflk .gt_indent_4 {
  text-indent: 20px;
}

#csugkcwflk .gt_indent_5 {
  text-indent: 25px;
}

#csugkcwflk .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#csugkcwflk div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5BZnJpY2E8L3N0cm9uZz48YnIgLz4KTiA9IDQ1"><span class='gt_from_md'><strong>Africa</strong><br />
N = 45</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5BbWVyaWNhczwvc3Ryb25nPjxiciAvPgpOID0gMTc0"><span class='gt_from_md'><strong>Americas</strong><br />
N = 174</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5Bc2lhPC9zdHJvbmc+PGJyIC8+Ck4gPSAyNzE="><span class='gt_from_md'><strong>Asia</strong><br />
N = 271</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5FdXJvcGU8L3N0cm9uZz48YnIgLz4KTiA9IDM0Nw=="><span class='gt_from_md'><strong>Europe</strong><br />
N = 347</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_5"><span data-qmd-base64="PHN0cm9uZz5HbG9iYWw8L3N0cm9uZz48YnIgLz4KTiA9IDIyOA=="><span class='gt_from_md'><strong>Global</strong><br />
N = 228</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_6"><span data-qmd-base64="PHN0cm9uZz5NaWRkbGUgRWFzdDwvc3Ryb25nPjxiciAvPgpOID0gNjE="><span class='gt_from_md'><strong>Middle East</strong><br />
N = 61</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_7"><span data-qmd-base64="PHN0cm9uZz5PY2VhbmlhPC9zdHJvbmc+PGJyIC8+Ck4gPSAyNQ=="><span class='gt_from_md'><strong>Oceania</strong><br />
N = 25</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_8"><span data-qmd-base64="PHN0cm9uZz5Qb2xhcjwvc3Ryb25nPjxiciAvPgpOID0gNDA="><span class='gt_from_md'><strong>Polar</strong><br />
N = 40</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Uses AGW</td>
<td headers="stat_1" class="gt_row gt_center">23 (51%)</td>
<td headers="stat_2" class="gt_row gt_center">101 (58%)</td>
<td headers="stat_3" class="gt_row gt_center">182 (67%)</td>
<td headers="stat_4" class="gt_row gt_center">136 (39%)</td>
<td headers="stat_5" class="gt_row gt_center">143 (63%)</td>
<td headers="stat_6" class="gt_row gt_center">23 (38%)</td>
<td headers="stat_7" class="gt_row gt_center">16 (64%)</td>
<td headers="stat_8" class="gt_row gt_center">34 (85%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="10"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="10"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::


{{< pagebreak >}}






### 5. What percentage of publications that include lessons come from each discipline? What percentage comes from each method?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="fhekgcpsid" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#fhekgcpsid table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#fhekgcpsid thead, #fhekgcpsid tbody, #fhekgcpsid tfoot, #fhekgcpsid tr, #fhekgcpsid td, #fhekgcpsid th {
  border-style: none;
}

#fhekgcpsid p {
  margin: 0;
  padding: 0;
}

#fhekgcpsid .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#fhekgcpsid .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#fhekgcpsid .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#fhekgcpsid .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#fhekgcpsid .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#fhekgcpsid .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#fhekgcpsid .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#fhekgcpsid .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#fhekgcpsid .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#fhekgcpsid .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#fhekgcpsid .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#fhekgcpsid .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#fhekgcpsid .gt_spanner_row {
  border-bottom-style: hidden;
}

#fhekgcpsid .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#fhekgcpsid .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#fhekgcpsid .gt_from_md > :first-child {
  margin-top: 0;
}

#fhekgcpsid .gt_from_md > :last-child {
  margin-bottom: 0;
}

#fhekgcpsid .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#fhekgcpsid .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#fhekgcpsid .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#fhekgcpsid .gt_row_group_first td {
  border-top-width: 2px;
}

#fhekgcpsid .gt_row_group_first th {
  border-top-width: 2px;
}

#fhekgcpsid .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fhekgcpsid .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#fhekgcpsid .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#fhekgcpsid .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#fhekgcpsid .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fhekgcpsid .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#fhekgcpsid .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#fhekgcpsid .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#fhekgcpsid .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#fhekgcpsid .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#fhekgcpsid .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fhekgcpsid .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#fhekgcpsid .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#fhekgcpsid .gt_left {
  text-align: left;
}

#fhekgcpsid .gt_center {
  text-align: center;
}

#fhekgcpsid .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#fhekgcpsid .gt_font_normal {
  font-weight: normal;
}

#fhekgcpsid .gt_font_bold {
  font-weight: bold;
}

#fhekgcpsid .gt_font_italic {
  font-style: italic;
}

#fhekgcpsid .gt_super {
  font-size: 65%;
}

#fhekgcpsid .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#fhekgcpsid .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#fhekgcpsid .gt_indent_1 {
  text-indent: 5px;
}

#fhekgcpsid .gt_indent_2 {
  text-indent: 10px;
}

#fhekgcpsid .gt_indent_3 {
  text-indent: 15px;
}

#fhekgcpsid .gt_indent_4 {
  text-indent: 20px;
}

#fhekgcpsid .gt_indent_5 {
  text-indent: 25px;
}

#fhekgcpsid .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#fhekgcpsid div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Obzwvc3Ryb25nPjxiciAvPgpOID0gOTk3"><span class='gt_from_md'><strong>No</strong><br />
N = 997</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5ZZXM8L3N0cm9uZz48YnIgLz4KTiA9IDE5NA=="><span class='gt_from_md'><strong>Yes</strong><br />
N = 194</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Discipline</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Archaeology</td>
<td headers="stat_1" class="gt_row gt_center">110 (11%)</td>
<td headers="stat_2" class="gt_row gt_center">39 (20%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Economics</td>
<td headers="stat_1" class="gt_row gt_center">3 (0.3%)</td>
<td headers="stat_2" class="gt_row gt_center">2 (1.0%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Epidemiology</td>
<td headers="stat_1" class="gt_row gt_center">1 (0.1%)</td>
<td headers="stat_2" class="gt_row gt_center">1 (0.5%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Geography</td>
<td headers="stat_1" class="gt_row gt_center">19 (1.9%)</td>
<td headers="stat_2" class="gt_row gt_center">6 (3.1%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    History</td>
<td headers="stat_1" class="gt_row gt_center">160 (16%)</td>
<td headers="stat_2" class="gt_row gt_center">46 (24%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Joint Fields</td>
<td headers="stat_1" class="gt_row gt_center">175 (18%)</td>
<td headers="stat_2" class="gt_row gt_center">36 (19%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Literature</td>
<td headers="stat_1" class="gt_row gt_center">24 (2.4%)</td>
<td headers="stat_2" class="gt_row gt_center">11 (5.7%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Other</td>
<td headers="stat_1" class="gt_row gt_center">5 (0.5%)</td>
<td headers="stat_2" class="gt_row gt_center">8 (4.1%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Paleoclimatology</td>
<td headers="stat_1" class="gt_row gt_center">500 (50%)</td>
<td headers="stat_2" class="gt_row gt_center">45 (23%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Method</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Both</td>
<td headers="stat_1" class="gt_row gt_center">130 (13%)</td>
<td headers="stat_2" class="gt_row gt_center">34 (18%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Neither</td>
<td headers="stat_1" class="gt_row gt_center">101 (10%)</td>
<td headers="stat_2" class="gt_row gt_center">25 (13%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Qualitative</td>
<td headers="stat_1" class="gt_row gt_center">156 (16%)</td>
<td headers="stat_2" class="gt_row gt_center">63 (32%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Quantitative</td>
<td headers="stat_1" class="gt_row gt_center">610 (61%)</td>
<td headers="stat_2" class="gt_row gt_center">72 (37%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk7IFBlYXJzb27igJlzIENoaS1zcXVhcmVkIHRlc3Q="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates); Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 6a. What percentage of publications in each discipline include lessons for the present/future?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="ahhedjqegz" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#ahhedjqegz table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#ahhedjqegz thead, #ahhedjqegz tbody, #ahhedjqegz tfoot, #ahhedjqegz tr, #ahhedjqegz td, #ahhedjqegz th {
  border-style: none;
}

#ahhedjqegz p {
  margin: 0;
  padding: 0;
}

#ahhedjqegz .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#ahhedjqegz .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#ahhedjqegz .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#ahhedjqegz .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#ahhedjqegz .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#ahhedjqegz .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ahhedjqegz .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#ahhedjqegz .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#ahhedjqegz .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#ahhedjqegz .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#ahhedjqegz .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#ahhedjqegz .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#ahhedjqegz .gt_spanner_row {
  border-bottom-style: hidden;
}

#ahhedjqegz .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#ahhedjqegz .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#ahhedjqegz .gt_from_md > :first-child {
  margin-top: 0;
}

#ahhedjqegz .gt_from_md > :last-child {
  margin-bottom: 0;
}

#ahhedjqegz .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#ahhedjqegz .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#ahhedjqegz .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#ahhedjqegz .gt_row_group_first td {
  border-top-width: 2px;
}

#ahhedjqegz .gt_row_group_first th {
  border-top-width: 2px;
}

#ahhedjqegz .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ahhedjqegz .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#ahhedjqegz .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#ahhedjqegz .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ahhedjqegz .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ahhedjqegz .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#ahhedjqegz .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#ahhedjqegz .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#ahhedjqegz .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ahhedjqegz .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#ahhedjqegz .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ahhedjqegz .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#ahhedjqegz .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ahhedjqegz .gt_left {
  text-align: left;
}

#ahhedjqegz .gt_center {
  text-align: center;
}

#ahhedjqegz .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#ahhedjqegz .gt_font_normal {
  font-weight: normal;
}

#ahhedjqegz .gt_font_bold {
  font-weight: bold;
}

#ahhedjqegz .gt_font_italic {
  font-style: italic;
}

#ahhedjqegz .gt_super {
  font-size: 65%;
}

#ahhedjqegz .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#ahhedjqegz .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#ahhedjqegz .gt_indent_1 {
  text-indent: 5px;
}

#ahhedjqegz .gt_indent_2 {
  text-indent: 10px;
}

#ahhedjqegz .gt_indent_3 {
  text-indent: 15px;
}

#ahhedjqegz .gt_indent_4 {
  text-indent: 20px;
}

#ahhedjqegz .gt_indent_5 {
  text-indent: 25px;
}

#ahhedjqegz .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#ahhedjqegz div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5BcmNoYWVvbG9neTwvc3Ryb25nPjxiciAvPgpOID0gMTQ5"><span class='gt_from_md'><strong>Archaeology</strong><br />
N = 149</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5FY29ub21pY3M8L3N0cm9uZz48YnIgLz4KTiA9IDU="><span class='gt_from_md'><strong>Economics</strong><br />
N = 5</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5FcGlkZW1pb2xvZ3k8L3N0cm9uZz48YnIgLz4KTiA9IDI="><span class='gt_from_md'><strong>Epidemiology</strong><br />
N = 2</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5HZW9ncmFwaHk8L3N0cm9uZz48YnIgLz4KTiA9IDI1"><span class='gt_from_md'><strong>Geography</strong><br />
N = 25</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_5"><span data-qmd-base64="PHN0cm9uZz5IaXN0b3J5PC9zdHJvbmc+PGJyIC8+Ck4gPSAyMDY="><span class='gt_from_md'><strong>History</strong><br />
N = 206</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_6"><span data-qmd-base64="PHN0cm9uZz5Kb2ludCBGaWVsZHM8L3N0cm9uZz48YnIgLz4KTiA9IDIxMQ=="><span class='gt_from_md'><strong>Joint Fields</strong><br />
N = 211</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_7"><span data-qmd-base64="PHN0cm9uZz5MaXRlcmF0dXJlPC9zdHJvbmc+PGJyIC8+Ck4gPSAzNQ=="><span class='gt_from_md'><strong>Literature</strong><br />
N = 35</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_8"><span data-qmd-base64="PHN0cm9uZz5PdGhlcjwvc3Ryb25nPjxiciAvPgpOID0gMTM="><span class='gt_from_md'><strong>Other</strong><br />
N = 13</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_9"><span data-qmd-base64="PHN0cm9uZz5QYWxlb2NsaW1hdG9sb2d5PC9zdHJvbmc+PGJyIC8+Ck4gPSA1NDU="><span class='gt_from_md'><strong>Paleoclimatology</strong><br />
N = 545</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">39 (26%)</td>
<td headers="stat_2" class="gt_row gt_center">2 (40%)</td>
<td headers="stat_3" class="gt_row gt_center">1 (50%)</td>
<td headers="stat_4" class="gt_row gt_center">6 (24%)</td>
<td headers="stat_5" class="gt_row gt_center">46 (22%)</td>
<td headers="stat_6" class="gt_row gt_center">36 (17%)</td>
<td headers="stat_7" class="gt_row gt_center">11 (31%)</td>
<td headers="stat_8" class="gt_row gt_center">8 (62%)</td>
<td headers="stat_9" class="gt_row gt_center">45 (8.3%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="11"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="11"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 6b. What percentage of publications in each method include lessons for the present/future?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="kywqulqhje" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#kywqulqhje table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#kywqulqhje thead, #kywqulqhje tbody, #kywqulqhje tfoot, #kywqulqhje tr, #kywqulqhje td, #kywqulqhje th {
  border-style: none;
}

#kywqulqhje p {
  margin: 0;
  padding: 0;
}

#kywqulqhje .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#kywqulqhje .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#kywqulqhje .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#kywqulqhje .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#kywqulqhje .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#kywqulqhje .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#kywqulqhje .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#kywqulqhje .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#kywqulqhje .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#kywqulqhje .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#kywqulqhje .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#kywqulqhje .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#kywqulqhje .gt_spanner_row {
  border-bottom-style: hidden;
}

#kywqulqhje .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#kywqulqhje .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#kywqulqhje .gt_from_md > :first-child {
  margin-top: 0;
}

#kywqulqhje .gt_from_md > :last-child {
  margin-bottom: 0;
}

#kywqulqhje .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#kywqulqhje .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#kywqulqhje .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#kywqulqhje .gt_row_group_first td {
  border-top-width: 2px;
}

#kywqulqhje .gt_row_group_first th {
  border-top-width: 2px;
}

#kywqulqhje .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#kywqulqhje .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#kywqulqhje .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#kywqulqhje .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#kywqulqhje .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#kywqulqhje .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#kywqulqhje .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#kywqulqhje .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#kywqulqhje .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#kywqulqhje .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#kywqulqhje .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#kywqulqhje .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#kywqulqhje .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#kywqulqhje .gt_left {
  text-align: left;
}

#kywqulqhje .gt_center {
  text-align: center;
}

#kywqulqhje .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#kywqulqhje .gt_font_normal {
  font-weight: normal;
}

#kywqulqhje .gt_font_bold {
  font-weight: bold;
}

#kywqulqhje .gt_font_italic {
  font-style: italic;
}

#kywqulqhje .gt_super {
  font-size: 65%;
}

#kywqulqhje .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#kywqulqhje .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#kywqulqhje .gt_indent_1 {
  text-indent: 5px;
}

#kywqulqhje .gt_indent_2 {
  text-indent: 10px;
}

#kywqulqhje .gt_indent_3 {
  text-indent: 15px;
}

#kywqulqhje .gt_indent_4 {
  text-indent: 20px;
}

#kywqulqhje .gt_indent_5 {
  text-indent: 25px;
}

#kywqulqhje .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#kywqulqhje div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Cb3RoPC9zdHJvbmc+PGJyIC8+Ck4gPSAxNjQ="><span class='gt_from_md'><strong>Both</strong><br />
N = 164</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5OZWl0aGVyPC9zdHJvbmc+PGJyIC8+Ck4gPSAxMjY="><span class='gt_from_md'><strong>Neither</strong><br />
N = 126</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5RdWFsaXRhdGl2ZTwvc3Ryb25nPjxiciAvPgpOID0gMjE5"><span class='gt_from_md'><strong>Qualitative</strong><br />
N = 219</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5RdWFudGl0YXRpdmU8L3N0cm9uZz48YnIgLz4KTiA9IDY4Mg=="><span class='gt_from_md'><strong>Quantitative</strong><br />
N = 682</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">34 (21%)</td>
<td headers="stat_2" class="gt_row gt_center">25 (20%)</td>
<td headers="stat_3" class="gt_row gt_center">63 (29%)</td>
<td headers="stat_4" class="gt_row gt_center">72 (11%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 7. What percentage of publications that include lessons focus on each region and period?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="zcvbujzekg" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#zcvbujzekg table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#zcvbujzekg thead, #zcvbujzekg tbody, #zcvbujzekg tfoot, #zcvbujzekg tr, #zcvbujzekg td, #zcvbujzekg th {
  border-style: none;
}

#zcvbujzekg p {
  margin: 0;
  padding: 0;
}

#zcvbujzekg .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#zcvbujzekg .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#zcvbujzekg .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#zcvbujzekg .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#zcvbujzekg .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#zcvbujzekg .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#zcvbujzekg .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#zcvbujzekg .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#zcvbujzekg .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#zcvbujzekg .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#zcvbujzekg .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#zcvbujzekg .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#zcvbujzekg .gt_spanner_row {
  border-bottom-style: hidden;
}

#zcvbujzekg .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#zcvbujzekg .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#zcvbujzekg .gt_from_md > :first-child {
  margin-top: 0;
}

#zcvbujzekg .gt_from_md > :last-child {
  margin-bottom: 0;
}

#zcvbujzekg .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#zcvbujzekg .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#zcvbujzekg .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#zcvbujzekg .gt_row_group_first td {
  border-top-width: 2px;
}

#zcvbujzekg .gt_row_group_first th {
  border-top-width: 2px;
}

#zcvbujzekg .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#zcvbujzekg .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#zcvbujzekg .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#zcvbujzekg .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#zcvbujzekg .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#zcvbujzekg .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#zcvbujzekg .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#zcvbujzekg .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#zcvbujzekg .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#zcvbujzekg .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#zcvbujzekg .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#zcvbujzekg .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#zcvbujzekg .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#zcvbujzekg .gt_left {
  text-align: left;
}

#zcvbujzekg .gt_center {
  text-align: center;
}

#zcvbujzekg .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#zcvbujzekg .gt_font_normal {
  font-weight: normal;
}

#zcvbujzekg .gt_font_bold {
  font-weight: bold;
}

#zcvbujzekg .gt_font_italic {
  font-style: italic;
}

#zcvbujzekg .gt_super {
  font-size: 65%;
}

#zcvbujzekg .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#zcvbujzekg .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#zcvbujzekg .gt_indent_1 {
  text-indent: 5px;
}

#zcvbujzekg .gt_indent_2 {
  text-indent: 10px;
}

#zcvbujzekg .gt_indent_3 {
  text-indent: 15px;
}

#zcvbujzekg .gt_indent_4 {
  text-indent: 20px;
}

#zcvbujzekg .gt_indent_5 {
  text-indent: 25px;
}

#zcvbujzekg .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#zcvbujzekg div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Obzwvc3Ryb25nPjxiciAvPgpOID0gOTk3"><span class='gt_from_md'><strong>No</strong><br />
N = 997</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5ZZXM8L3N0cm9uZz48YnIgLz4KTiA9IDE5NA=="><span class='gt_from_md'><strong>Yes</strong><br />
N = 194</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Geographic Region</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Africa</td>
<td headers="stat_1" class="gt_row gt_center">35 (3.5%)</td>
<td headers="stat_2" class="gt_row gt_center">10 (5.2%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Americas</td>
<td headers="stat_1" class="gt_row gt_center">140 (14%)</td>
<td headers="stat_2" class="gt_row gt_center">34 (18%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Asia</td>
<td headers="stat_1" class="gt_row gt_center">247 (25%)</td>
<td headers="stat_2" class="gt_row gt_center">24 (12%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Europe</td>
<td headers="stat_1" class="gt_row gt_center">304 (30%)</td>
<td headers="stat_2" class="gt_row gt_center">43 (22%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Global</td>
<td headers="stat_1" class="gt_row gt_center">171 (17%)</td>
<td headers="stat_2" class="gt_row gt_center">57 (29%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Middle East</td>
<td headers="stat_1" class="gt_row gt_center">49 (4.9%)</td>
<td headers="stat_2" class="gt_row gt_center">12 (6.2%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Oceania</td>
<td headers="stat_1" class="gt_row gt_center">18 (1.8%)</td>
<td headers="stat_2" class="gt_row gt_center">7 (3.6%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Polar</td>
<td headers="stat_1" class="gt_row gt_center">33 (3.3%)</td>
<td headers="stat_2" class="gt_row gt_center">7 (3.6%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::

::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="erltakliwm" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#erltakliwm table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#erltakliwm thead, #erltakliwm tbody, #erltakliwm tfoot, #erltakliwm tr, #erltakliwm td, #erltakliwm th {
  border-style: none;
}

#erltakliwm p {
  margin: 0;
  padding: 0;
}

#erltakliwm .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#erltakliwm .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#erltakliwm .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#erltakliwm .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#erltakliwm .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#erltakliwm .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#erltakliwm .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#erltakliwm .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#erltakliwm .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#erltakliwm .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#erltakliwm .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#erltakliwm .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#erltakliwm .gt_spanner_row {
  border-bottom-style: hidden;
}

#erltakliwm .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#erltakliwm .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#erltakliwm .gt_from_md > :first-child {
  margin-top: 0;
}

#erltakliwm .gt_from_md > :last-child {
  margin-bottom: 0;
}

#erltakliwm .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#erltakliwm .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#erltakliwm .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#erltakliwm .gt_row_group_first td {
  border-top-width: 2px;
}

#erltakliwm .gt_row_group_first th {
  border-top-width: 2px;
}

#erltakliwm .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#erltakliwm .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#erltakliwm .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#erltakliwm .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#erltakliwm .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#erltakliwm .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#erltakliwm .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#erltakliwm .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#erltakliwm .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#erltakliwm .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#erltakliwm .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#erltakliwm .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#erltakliwm .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#erltakliwm .gt_left {
  text-align: left;
}

#erltakliwm .gt_center {
  text-align: center;
}

#erltakliwm .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#erltakliwm .gt_font_normal {
  font-weight: normal;
}

#erltakliwm .gt_font_bold {
  font-weight: bold;
}

#erltakliwm .gt_font_italic {
  font-style: italic;
}

#erltakliwm .gt_super {
  font-size: 65%;
}

#erltakliwm .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#erltakliwm .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#erltakliwm .gt_indent_1 {
  text-indent: 5px;
}

#erltakliwm .gt_indent_2 {
  text-indent: 10px;
}

#erltakliwm .gt_indent_3 {
  text-indent: 15px;
}

#erltakliwm .gt_indent_4 {
  text-indent: 20px;
}

#erltakliwm .gt_indent_5 {
  text-indent: 25px;
}

#erltakliwm .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#erltakliwm div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Obzwvc3Ryb25nPjxiciAvPgpOID0gMiw3MDE="><span class='gt_from_md'><strong>No</strong><br />
N = 2,701</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5ZZXM8L3N0cm9uZz48YnIgLz4KTiA9IDU2MQ=="><span class='gt_from_md'><strong>Yes</strong><br />
N = 561</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">period</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center">0.068</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Pleistocene</td>
<td headers="stat_1" class="gt_row gt_center">46 (1.7%)</td>
<td headers="stat_2" class="gt_row gt_center">19 (3.4%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Early-Mid Holocene</td>
<td headers="stat_1" class="gt_row gt_center">115 (4.3%)</td>
<td headers="stat_2" class="gt_row gt_center">30 (5.3%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Ancient</td>
<td headers="stat_1" class="gt_row gt_center">292 (11%)</td>
<td headers="stat_2" class="gt_row gt_center">53 (9.4%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Medieval</td>
<td headers="stat_1" class="gt_row gt_center">484 (18%)</td>
<td headers="stat_2" class="gt_row gt_center">85 (15%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Early Modern</td>
<td headers="stat_1" class="gt_row gt_center">601 (22%)</td>
<td headers="stat_2" class="gt_row gt_center">119 (21%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Modern</td>
<td headers="stat_1" class="gt_row gt_center">619 (23%)</td>
<td headers="stat_2" class="gt_row gt_center">132 (24%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Present</td>
<td headers="stat_1" class="gt_row gt_center">544 (20%)</td>
<td headers="stat_2" class="gt_row gt_center">123 (22%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 8a. What percentage of publications from each region include lessons for the present/future?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="hzckhjebku" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#hzckhjebku table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#hzckhjebku thead, #hzckhjebku tbody, #hzckhjebku tfoot, #hzckhjebku tr, #hzckhjebku td, #hzckhjebku th {
  border-style: none;
}

#hzckhjebku p {
  margin: 0;
  padding: 0;
}

#hzckhjebku .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#hzckhjebku .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#hzckhjebku .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#hzckhjebku .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#hzckhjebku .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#hzckhjebku .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#hzckhjebku .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#hzckhjebku .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#hzckhjebku .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#hzckhjebku .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#hzckhjebku .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#hzckhjebku .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#hzckhjebku .gt_spanner_row {
  border-bottom-style: hidden;
}

#hzckhjebku .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#hzckhjebku .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#hzckhjebku .gt_from_md > :first-child {
  margin-top: 0;
}

#hzckhjebku .gt_from_md > :last-child {
  margin-bottom: 0;
}

#hzckhjebku .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#hzckhjebku .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#hzckhjebku .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#hzckhjebku .gt_row_group_first td {
  border-top-width: 2px;
}

#hzckhjebku .gt_row_group_first th {
  border-top-width: 2px;
}

#hzckhjebku .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#hzckhjebku .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#hzckhjebku .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#hzckhjebku .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#hzckhjebku .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#hzckhjebku .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#hzckhjebku .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#hzckhjebku .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#hzckhjebku .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#hzckhjebku .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#hzckhjebku .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#hzckhjebku .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#hzckhjebku .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#hzckhjebku .gt_left {
  text-align: left;
}

#hzckhjebku .gt_center {
  text-align: center;
}

#hzckhjebku .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#hzckhjebku .gt_font_normal {
  font-weight: normal;
}

#hzckhjebku .gt_font_bold {
  font-weight: bold;
}

#hzckhjebku .gt_font_italic {
  font-style: italic;
}

#hzckhjebku .gt_super {
  font-size: 65%;
}

#hzckhjebku .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#hzckhjebku .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#hzckhjebku .gt_indent_1 {
  text-indent: 5px;
}

#hzckhjebku .gt_indent_2 {
  text-indent: 10px;
}

#hzckhjebku .gt_indent_3 {
  text-indent: 15px;
}

#hzckhjebku .gt_indent_4 {
  text-indent: 20px;
}

#hzckhjebku .gt_indent_5 {
  text-indent: 25px;
}

#hzckhjebku .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#hzckhjebku div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5BZnJpY2E8L3N0cm9uZz48YnIgLz4KTiA9IDQ1"><span class='gt_from_md'><strong>Africa</strong><br />
N = 45</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5BbWVyaWNhczwvc3Ryb25nPjxiciAvPgpOID0gMTc0"><span class='gt_from_md'><strong>Americas</strong><br />
N = 174</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5Bc2lhPC9zdHJvbmc+PGJyIC8+Ck4gPSAyNzE="><span class='gt_from_md'><strong>Asia</strong><br />
N = 271</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5FdXJvcGU8L3N0cm9uZz48YnIgLz4KTiA9IDM0Nw=="><span class='gt_from_md'><strong>Europe</strong><br />
N = 347</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_5"><span data-qmd-base64="PHN0cm9uZz5HbG9iYWw8L3N0cm9uZz48YnIgLz4KTiA9IDIyOA=="><span class='gt_from_md'><strong>Global</strong><br />
N = 228</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_6"><span data-qmd-base64="PHN0cm9uZz5NaWRkbGUgRWFzdDwvc3Ryb25nPjxiciAvPgpOID0gNjE="><span class='gt_from_md'><strong>Middle East</strong><br />
N = 61</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_7"><span data-qmd-base64="PHN0cm9uZz5PY2VhbmlhPC9zdHJvbmc+PGJyIC8+Ck4gPSAyNQ=="><span class='gt_from_md'><strong>Oceania</strong><br />
N = 25</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_8"><span data-qmd-base64="PHN0cm9uZz5Qb2xhcjwvc3Ryb25nPjxiciAvPgpOID0gNDA="><span class='gt_from_md'><strong>Polar</strong><br />
N = 40</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">10 (22%)</td>
<td headers="stat_2" class="gt_row gt_center">34 (20%)</td>
<td headers="stat_3" class="gt_row gt_center">24 (8.9%)</td>
<td headers="stat_4" class="gt_row gt_center">43 (12%)</td>
<td headers="stat_5" class="gt_row gt_center">57 (25%)</td>
<td headers="stat_6" class="gt_row gt_center">12 (20%)</td>
<td headers="stat_7" class="gt_row gt_center">7 (28%)</td>
<td headers="stat_8" class="gt_row gt_center">7 (18%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="10"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="10"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 8b. What percentage of publications from each period include lessons for the present/future?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="etwxgjirhc" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#etwxgjirhc table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#etwxgjirhc thead, #etwxgjirhc tbody, #etwxgjirhc tfoot, #etwxgjirhc tr, #etwxgjirhc td, #etwxgjirhc th {
  border-style: none;
}

#etwxgjirhc p {
  margin: 0;
  padding: 0;
}

#etwxgjirhc .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#etwxgjirhc .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#etwxgjirhc .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#etwxgjirhc .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#etwxgjirhc .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#etwxgjirhc .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#etwxgjirhc .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#etwxgjirhc .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#etwxgjirhc .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#etwxgjirhc .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#etwxgjirhc .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#etwxgjirhc .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#etwxgjirhc .gt_spanner_row {
  border-bottom-style: hidden;
}

#etwxgjirhc .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#etwxgjirhc .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#etwxgjirhc .gt_from_md > :first-child {
  margin-top: 0;
}

#etwxgjirhc .gt_from_md > :last-child {
  margin-bottom: 0;
}

#etwxgjirhc .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#etwxgjirhc .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#etwxgjirhc .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#etwxgjirhc .gt_row_group_first td {
  border-top-width: 2px;
}

#etwxgjirhc .gt_row_group_first th {
  border-top-width: 2px;
}

#etwxgjirhc .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#etwxgjirhc .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#etwxgjirhc .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#etwxgjirhc .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#etwxgjirhc .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#etwxgjirhc .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#etwxgjirhc .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#etwxgjirhc .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#etwxgjirhc .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#etwxgjirhc .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#etwxgjirhc .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#etwxgjirhc .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#etwxgjirhc .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#etwxgjirhc .gt_left {
  text-align: left;
}

#etwxgjirhc .gt_center {
  text-align: center;
}

#etwxgjirhc .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#etwxgjirhc .gt_font_normal {
  font-weight: normal;
}

#etwxgjirhc .gt_font_bold {
  font-weight: bold;
}

#etwxgjirhc .gt_font_italic {
  font-style: italic;
}

#etwxgjirhc .gt_super {
  font-size: 65%;
}

#etwxgjirhc .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#etwxgjirhc .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#etwxgjirhc .gt_indent_1 {
  text-indent: 5px;
}

#etwxgjirhc .gt_indent_2 {
  text-indent: 10px;
}

#etwxgjirhc .gt_indent_3 {
  text-indent: 15px;
}

#etwxgjirhc .gt_indent_4 {
  text-indent: 20px;
}

#etwxgjirhc .gt_indent_5 {
  text-indent: 25px;
}

#etwxgjirhc .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#etwxgjirhc div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5QbGVpc3RvY2VuZTwvc3Ryb25nPjxiciAvPgpOID0gNjU="><span class='gt_from_md'><strong>Pleistocene</strong><br />
N = 65</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5FYXJseS1NaWQgSG9sb2NlbmU8L3N0cm9uZz48YnIgLz4KTiA9IDE0NQ=="><span class='gt_from_md'><strong>Early-Mid Holocene</strong><br />
N = 145</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5BbmNpZW50PC9zdHJvbmc+PGJyIC8+Ck4gPSAzNDU="><span class='gt_from_md'><strong>Ancient</strong><br />
N = 345</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5NZWRpZXZhbDwvc3Ryb25nPjxiciAvPgpOID0gNTY5"><span class='gt_from_md'><strong>Medieval</strong><br />
N = 569</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_5"><span data-qmd-base64="PHN0cm9uZz5FYXJseSBNb2Rlcm48L3N0cm9uZz48YnIgLz4KTiA9IDcyMA=="><span class='gt_from_md'><strong>Early Modern</strong><br />
N = 720</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_6"><span data-qmd-base64="PHN0cm9uZz5Nb2Rlcm48L3N0cm9uZz48YnIgLz4KTiA9IDc1MQ=="><span class='gt_from_md'><strong>Modern</strong><br />
N = 751</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_7"><span data-qmd-base64="PHN0cm9uZz5QcmVzZW50PC9zdHJvbmc+PGJyIC8+Ck4gPSA2Njc="><span class='gt_from_md'><strong>Present</strong><br />
N = 667</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">19 (29%)</td>
<td headers="stat_2" class="gt_row gt_center">30 (21%)</td>
<td headers="stat_3" class="gt_row gt_center">53 (15%)</td>
<td headers="stat_4" class="gt_row gt_center">85 (15%)</td>
<td headers="stat_5" class="gt_row gt_center">119 (17%)</td>
<td headers="stat_6" class="gt_row gt_center">132 (18%)</td>
<td headers="stat_7" class="gt_row gt_center">123 (18%)</td>
<td headers="p.value" class="gt_row gt_center">0.068</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="9"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="9"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 9a. What percentage of publications in each discipline include distinct types of recommendation?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="avtobjgeyi" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#avtobjgeyi table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#avtobjgeyi thead, #avtobjgeyi tbody, #avtobjgeyi tfoot, #avtobjgeyi tr, #avtobjgeyi td, #avtobjgeyi th {
  border-style: none;
}

#avtobjgeyi p {
  margin: 0;
  padding: 0;
}

#avtobjgeyi .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#avtobjgeyi .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#avtobjgeyi .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#avtobjgeyi .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#avtobjgeyi .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#avtobjgeyi .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#avtobjgeyi .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#avtobjgeyi .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#avtobjgeyi .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#avtobjgeyi .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#avtobjgeyi .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#avtobjgeyi .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#avtobjgeyi .gt_spanner_row {
  border-bottom-style: hidden;
}

#avtobjgeyi .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#avtobjgeyi .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#avtobjgeyi .gt_from_md > :first-child {
  margin-top: 0;
}

#avtobjgeyi .gt_from_md > :last-child {
  margin-bottom: 0;
}

#avtobjgeyi .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#avtobjgeyi .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#avtobjgeyi .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#avtobjgeyi .gt_row_group_first td {
  border-top-width: 2px;
}

#avtobjgeyi .gt_row_group_first th {
  border-top-width: 2px;
}

#avtobjgeyi .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#avtobjgeyi .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#avtobjgeyi .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#avtobjgeyi .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#avtobjgeyi .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#avtobjgeyi .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#avtobjgeyi .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#avtobjgeyi .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#avtobjgeyi .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#avtobjgeyi .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#avtobjgeyi .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#avtobjgeyi .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#avtobjgeyi .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#avtobjgeyi .gt_left {
  text-align: left;
}

#avtobjgeyi .gt_center {
  text-align: center;
}

#avtobjgeyi .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#avtobjgeyi .gt_font_normal {
  font-weight: normal;
}

#avtobjgeyi .gt_font_bold {
  font-weight: bold;
}

#avtobjgeyi .gt_font_italic {
  font-style: italic;
}

#avtobjgeyi .gt_super {
  font-size: 65%;
}

#avtobjgeyi .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#avtobjgeyi .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#avtobjgeyi .gt_indent_1 {
  text-indent: 5px;
}

#avtobjgeyi .gt_indent_2 {
  text-indent: 10px;
}

#avtobjgeyi .gt_indent_3 {
  text-indent: 15px;
}

#avtobjgeyi .gt_indent_4 {
  text-indent: 20px;
}

#avtobjgeyi .gt_indent_5 {
  text-indent: 25px;
}

#avtobjgeyi .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#avtobjgeyi div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5BcmNoYWVvbG9neTwvc3Ryb25nPjxiciAvPgpOID0gMTU4"><span class='gt_from_md'><strong>Archaeology</strong><br />
N = 158</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5FY29ub21pY3M8L3N0cm9uZz48YnIgLz4KTiA9IDU="><span class='gt_from_md'><strong>Economics</strong><br />
N = 5</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5FcGlkZW1pb2xvZ3k8L3N0cm9uZz48YnIgLz4KTiA9IDI="><span class='gt_from_md'><strong>Epidemiology</strong><br />
N = 2</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5HZW9ncmFwaHk8L3N0cm9uZz48YnIgLz4KTiA9IDI3"><span class='gt_from_md'><strong>Geography</strong><br />
N = 27</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_5"><span data-qmd-base64="PHN0cm9uZz5IaXN0b3J5PC9zdHJvbmc+PGJyIC8+Ck4gPSAyMTM="><span class='gt_from_md'><strong>History</strong><br />
N = 213</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_6"><span data-qmd-base64="PHN0cm9uZz5Kb2ludCBGaWVsZHM8L3N0cm9uZz48YnIgLz4KTiA9IDIxNw=="><span class='gt_from_md'><strong>Joint Fields</strong><br />
N = 217</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_7"><span data-qmd-base64="PHN0cm9uZz5MaXRlcmF0dXJlPC9zdHJvbmc+PGJyIC8+Ck4gPSAzNQ=="><span class='gt_from_md'><strong>Literature</strong><br />
N = 35</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_8"><span data-qmd-base64="PHN0cm9uZz5PdGhlcjwvc3Ryb25nPjxiciAvPgpOID0gMTY="><span class='gt_from_md'><strong>Other</strong><br />
N = 16</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_9"><span data-qmd-base64="PHN0cm9uZz5QYWxlb2NsaW1hdG9sb2d5PC9zdHJvbmc+PGJyIC8+Ck4gPSA1NTE="><span class='gt_from_md'><strong>Paleoclimatology</strong><br />
N = 551</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">rec_type</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="stat_3" class="gt_row gt_center"><br /></td>
<td headers="stat_4" class="gt_row gt_center"><br /></td>
<td headers="stat_5" class="gt_row gt_center"><br /></td>
<td headers="stat_6" class="gt_row gt_center"><br /></td>
<td headers="stat_7" class="gt_row gt_center"><br /></td>
<td headers="stat_8" class="gt_row gt_center"><br /></td>
<td headers="stat_9" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Broad, abstract, or vague</td>
<td headers="stat_1" class="gt_row gt_center">15 (9.5%)</td>
<td headers="stat_2" class="gt_row gt_center">1 (20%)</td>
<td headers="stat_3" class="gt_row gt_center">0 (0%)</td>
<td headers="stat_4" class="gt_row gt_center">5 (19%)</td>
<td headers="stat_5" class="gt_row gt_center">27 (13%)</td>
<td headers="stat_6" class="gt_row gt_center">21 (9.7%)</td>
<td headers="stat_7" class="gt_row gt_center">8 (23%)</td>
<td headers="stat_8" class="gt_row gt_center">4 (25%)</td>
<td headers="stat_9" class="gt_row gt_center">13 (2.4%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific but not actionable</td>
<td headers="stat_1" class="gt_row gt_center">20 (13%)</td>
<td headers="stat_2" class="gt_row gt_center">0 (0%)</td>
<td headers="stat_3" class="gt_row gt_center">1 (50%)</td>
<td headers="stat_4" class="gt_row gt_center">2 (7.4%)</td>
<td headers="stat_5" class="gt_row gt_center">19 (8.9%)</td>
<td headers="stat_6" class="gt_row gt_center">12 (5.5%)</td>
<td headers="stat_7" class="gt_row gt_center">1 (2.9%)</td>
<td headers="stat_8" class="gt_row gt_center">3 (19%)</td>
<td headers="stat_9" class="gt_row gt_center">19 (3.4%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific and actionable</td>
<td headers="stat_1" class="gt_row gt_center">13 (8.2%)</td>
<td headers="stat_2" class="gt_row gt_center">1 (20%)</td>
<td headers="stat_3" class="gt_row gt_center">0 (0%)</td>
<td headers="stat_4" class="gt_row gt_center">1 (3.7%)</td>
<td headers="stat_5" class="gt_row gt_center">7 (3.3%)</td>
<td headers="stat_6" class="gt_row gt_center">9 (4.1%)</td>
<td headers="stat_7" class="gt_row gt_center">2 (5.7%)</td>
<td headers="stat_8" class="gt_row gt_center">4 (25%)</td>
<td headers="stat_9" class="gt_row gt_center">19 (3.4%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    No recommendation</td>
<td headers="stat_1" class="gt_row gt_center">110 (70%)</td>
<td headers="stat_2" class="gt_row gt_center">3 (60%)</td>
<td headers="stat_3" class="gt_row gt_center">1 (50%)</td>
<td headers="stat_4" class="gt_row gt_center">19 (70%)</td>
<td headers="stat_5" class="gt_row gt_center">160 (75%)</td>
<td headers="stat_6" class="gt_row gt_center">175 (81%)</td>
<td headers="stat_7" class="gt_row gt_center">24 (69%)</td>
<td headers="stat_8" class="gt_row gt_center">5 (31%)</td>
<td headers="stat_9" class="gt_row gt_center">500 (91%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="11"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="11"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::


{{< pagebreak >}}






### 9b. What percentage of publications in each method include distinct types of recommendation?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="skusqhyyzi" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#skusqhyyzi table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#skusqhyyzi thead, #skusqhyyzi tbody, #skusqhyyzi tfoot, #skusqhyyzi tr, #skusqhyyzi td, #skusqhyyzi th {
  border-style: none;
}

#skusqhyyzi p {
  margin: 0;
  padding: 0;
}

#skusqhyyzi .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#skusqhyyzi .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#skusqhyyzi .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#skusqhyyzi .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#skusqhyyzi .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#skusqhyyzi .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#skusqhyyzi .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#skusqhyyzi .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#skusqhyyzi .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#skusqhyyzi .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#skusqhyyzi .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#skusqhyyzi .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#skusqhyyzi .gt_spanner_row {
  border-bottom-style: hidden;
}

#skusqhyyzi .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#skusqhyyzi .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#skusqhyyzi .gt_from_md > :first-child {
  margin-top: 0;
}

#skusqhyyzi .gt_from_md > :last-child {
  margin-bottom: 0;
}

#skusqhyyzi .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#skusqhyyzi .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#skusqhyyzi .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#skusqhyyzi .gt_row_group_first td {
  border-top-width: 2px;
}

#skusqhyyzi .gt_row_group_first th {
  border-top-width: 2px;
}

#skusqhyyzi .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#skusqhyyzi .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#skusqhyyzi .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#skusqhyyzi .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#skusqhyyzi .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#skusqhyyzi .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#skusqhyyzi .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#skusqhyyzi .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#skusqhyyzi .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#skusqhyyzi .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#skusqhyyzi .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#skusqhyyzi .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#skusqhyyzi .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#skusqhyyzi .gt_left {
  text-align: left;
}

#skusqhyyzi .gt_center {
  text-align: center;
}

#skusqhyyzi .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#skusqhyyzi .gt_font_normal {
  font-weight: normal;
}

#skusqhyyzi .gt_font_bold {
  font-weight: bold;
}

#skusqhyyzi .gt_font_italic {
  font-style: italic;
}

#skusqhyyzi .gt_super {
  font-size: 65%;
}

#skusqhyyzi .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#skusqhyyzi .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#skusqhyyzi .gt_indent_1 {
  text-indent: 5px;
}

#skusqhyyzi .gt_indent_2 {
  text-indent: 10px;
}

#skusqhyyzi .gt_indent_3 {
  text-indent: 15px;
}

#skusqhyyzi .gt_indent_4 {
  text-indent: 20px;
}

#skusqhyyzi .gt_indent_5 {
  text-indent: 25px;
}

#skusqhyyzi .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#skusqhyyzi div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Cb3RoPC9zdHJvbmc+PGJyIC8+Ck4gPSAxNzU="><span class='gt_from_md'><strong>Both</strong><br />
N = 175</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5OZWl0aGVyPC9zdHJvbmc+PGJyIC8+Ck4gPSAxMzE="><span class='gt_from_md'><strong>Neither</strong><br />
N = 131</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5RdWFsaXRhdGl2ZTwvc3Ryb25nPjxiciAvPgpOID0gMjMz"><span class='gt_from_md'><strong>Qualitative</strong><br />
N = 233</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5RdWFudGl0YXRpdmU8L3N0cm9uZz48YnIgLz4KTiA9IDY4NQ=="><span class='gt_from_md'><strong>Quantitative</strong><br />
N = 685</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">rec_type</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="stat_3" class="gt_row gt_center"><br /></td>
<td headers="stat_4" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Broad, abstract, or vague</td>
<td headers="stat_1" class="gt_row gt_center">23 (13%)</td>
<td headers="stat_2" class="gt_row gt_center">11 (8.4%)</td>
<td headers="stat_3" class="gt_row gt_center">39 (17%)</td>
<td headers="stat_4" class="gt_row gt_center">21 (3.1%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific but not actionable</td>
<td headers="stat_1" class="gt_row gt_center">12 (6.9%)</td>
<td headers="stat_2" class="gt_row gt_center">11 (8.4%)</td>
<td headers="stat_3" class="gt_row gt_center">25 (11%)</td>
<td headers="stat_4" class="gt_row gt_center">29 (4.2%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific and actionable</td>
<td headers="stat_1" class="gt_row gt_center">10 (5.7%)</td>
<td headers="stat_2" class="gt_row gt_center">8 (6.1%)</td>
<td headers="stat_3" class="gt_row gt_center">13 (5.6%)</td>
<td headers="stat_4" class="gt_row gt_center">25 (3.6%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    No recommendation</td>
<td headers="stat_1" class="gt_row gt_center">130 (74%)</td>
<td headers="stat_2" class="gt_row gt_center">101 (77%)</td>
<td headers="stat_3" class="gt_row gt_center">156 (67%)</td>
<td headers="stat_4" class="gt_row gt_center">610 (89%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 10a. What percentage of publications from each region include distinct types of recommendation?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="sgssqnruri" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#sgssqnruri table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#sgssqnruri thead, #sgssqnruri tbody, #sgssqnruri tfoot, #sgssqnruri tr, #sgssqnruri td, #sgssqnruri th {
  border-style: none;
}

#sgssqnruri p {
  margin: 0;
  padding: 0;
}

#sgssqnruri .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#sgssqnruri .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#sgssqnruri .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#sgssqnruri .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#sgssqnruri .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#sgssqnruri .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#sgssqnruri .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#sgssqnruri .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#sgssqnruri .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#sgssqnruri .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#sgssqnruri .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#sgssqnruri .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#sgssqnruri .gt_spanner_row {
  border-bottom-style: hidden;
}

#sgssqnruri .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#sgssqnruri .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#sgssqnruri .gt_from_md > :first-child {
  margin-top: 0;
}

#sgssqnruri .gt_from_md > :last-child {
  margin-bottom: 0;
}

#sgssqnruri .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#sgssqnruri .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#sgssqnruri .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#sgssqnruri .gt_row_group_first td {
  border-top-width: 2px;
}

#sgssqnruri .gt_row_group_first th {
  border-top-width: 2px;
}

#sgssqnruri .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#sgssqnruri .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#sgssqnruri .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#sgssqnruri .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#sgssqnruri .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#sgssqnruri .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#sgssqnruri .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#sgssqnruri .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#sgssqnruri .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#sgssqnruri .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#sgssqnruri .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#sgssqnruri .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#sgssqnruri .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#sgssqnruri .gt_left {
  text-align: left;
}

#sgssqnruri .gt_center {
  text-align: center;
}

#sgssqnruri .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#sgssqnruri .gt_font_normal {
  font-weight: normal;
}

#sgssqnruri .gt_font_bold {
  font-weight: bold;
}

#sgssqnruri .gt_font_italic {
  font-style: italic;
}

#sgssqnruri .gt_super {
  font-size: 65%;
}

#sgssqnruri .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#sgssqnruri .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#sgssqnruri .gt_indent_1 {
  text-indent: 5px;
}

#sgssqnruri .gt_indent_2 {
  text-indent: 10px;
}

#sgssqnruri .gt_indent_3 {
  text-indent: 15px;
}

#sgssqnruri .gt_indent_4 {
  text-indent: 20px;
}

#sgssqnruri .gt_indent_5 {
  text-indent: 25px;
}

#sgssqnruri .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#sgssqnruri div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5BZnJpY2E8L3N0cm9uZz48YnIgLz4KTiA9IDQ1"><span class='gt_from_md'><strong>Africa</strong><br />
N = 45</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5BbWVyaWNhczwvc3Ryb25nPjxiciAvPgpOID0gMTc4"><span class='gt_from_md'><strong>Americas</strong><br />
N = 178</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5Bc2lhPC9zdHJvbmc+PGJyIC8+Ck4gPSAyNzM="><span class='gt_from_md'><strong>Asia</strong><br />
N = 273</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5FdXJvcGU8L3N0cm9uZz48YnIgLz4KTiA9IDM1MQ=="><span class='gt_from_md'><strong>Europe</strong><br />
N = 351</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_5"><span data-qmd-base64="PHN0cm9uZz5HbG9iYWw8L3N0cm9uZz48YnIgLz4KTiA9IDI0Mw=="><span class='gt_from_md'><strong>Global</strong><br />
N = 243</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_6"><span data-qmd-base64="PHN0cm9uZz5NaWRkbGUgRWFzdDwvc3Ryb25nPjxiciAvPgpOID0gNjU="><span class='gt_from_md'><strong>Middle East</strong><br />
N = 65</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_7"><span data-qmd-base64="PHN0cm9uZz5PY2VhbmlhPC9zdHJvbmc+PGJyIC8+Ck4gPSAyOA=="><span class='gt_from_md'><strong>Oceania</strong><br />
N = 28</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_8"><span data-qmd-base64="PHN0cm9uZz5Qb2xhcjwvc3Ryb25nPjxiciAvPgpOID0gNDE="><span class='gt_from_md'><strong>Polar</strong><br />
N = 41</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">rec_type</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="stat_3" class="gt_row gt_center"><br /></td>
<td headers="stat_4" class="gt_row gt_center"><br /></td>
<td headers="stat_5" class="gt_row gt_center"><br /></td>
<td headers="stat_6" class="gt_row gt_center"><br /></td>
<td headers="stat_7" class="gt_row gt_center"><br /></td>
<td headers="stat_8" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Broad, abstract, or vague</td>
<td headers="stat_1" class="gt_row gt_center">2 (4.4%)</td>
<td headers="stat_2" class="gt_row gt_center">17 (9.6%)</td>
<td headers="stat_3" class="gt_row gt_center">7 (2.6%)</td>
<td headers="stat_4" class="gt_row gt_center">27 (7.7%)</td>
<td headers="stat_5" class="gt_row gt_center">28 (12%)</td>
<td headers="stat_6" class="gt_row gt_center">5 (7.7%)</td>
<td headers="stat_7" class="gt_row gt_center">4 (14%)</td>
<td headers="stat_8" class="gt_row gt_center">4 (9.8%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific but not actionable</td>
<td headers="stat_1" class="gt_row gt_center">3 (6.7%)</td>
<td headers="stat_2" class="gt_row gt_center">6 (3.4%)</td>
<td headers="stat_3" class="gt_row gt_center">9 (3.3%)</td>
<td headers="stat_4" class="gt_row gt_center">14 (4.0%)</td>
<td headers="stat_5" class="gt_row gt_center">28 (12%)</td>
<td headers="stat_6" class="gt_row gt_center">10 (15%)</td>
<td headers="stat_7" class="gt_row gt_center">3 (11%)</td>
<td headers="stat_8" class="gt_row gt_center">4 (9.8%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific and actionable</td>
<td headers="stat_1" class="gt_row gt_center">5 (11%)</td>
<td headers="stat_2" class="gt_row gt_center">15 (8.4%)</td>
<td headers="stat_3" class="gt_row gt_center">10 (3.7%)</td>
<td headers="stat_4" class="gt_row gt_center">6 (1.7%)</td>
<td headers="stat_5" class="gt_row gt_center">16 (6.6%)</td>
<td headers="stat_6" class="gt_row gt_center">1 (1.5%)</td>
<td headers="stat_7" class="gt_row gt_center">3 (11%)</td>
<td headers="stat_8" class="gt_row gt_center">0 (0%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    No recommendation</td>
<td headers="stat_1" class="gt_row gt_center">35 (78%)</td>
<td headers="stat_2" class="gt_row gt_center">140 (79%)</td>
<td headers="stat_3" class="gt_row gt_center">247 (90%)</td>
<td headers="stat_4" class="gt_row gt_center">304 (87%)</td>
<td headers="stat_5" class="gt_row gt_center">171 (70%)</td>
<td headers="stat_6" class="gt_row gt_center">49 (75%)</td>
<td headers="stat_7" class="gt_row gt_center">18 (64%)</td>
<td headers="stat_8" class="gt_row gt_center">33 (80%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="10"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="10"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::


{{< pagebreak >}}






### 10b. What percentage of publications from each period include distinct types of recommendation?

Note, because each paper can have multiple periods *and* recommendation types, there are different ways to do this. Here we just look at all combinations, which is not necessarily the best way to do this!



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="gwhfetsehy" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#gwhfetsehy table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#gwhfetsehy thead, #gwhfetsehy tbody, #gwhfetsehy tfoot, #gwhfetsehy tr, #gwhfetsehy td, #gwhfetsehy th {
  border-style: none;
}

#gwhfetsehy p {
  margin: 0;
  padding: 0;
}

#gwhfetsehy .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#gwhfetsehy .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#gwhfetsehy .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#gwhfetsehy .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#gwhfetsehy .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#gwhfetsehy .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#gwhfetsehy .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#gwhfetsehy .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#gwhfetsehy .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#gwhfetsehy .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#gwhfetsehy .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#gwhfetsehy .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#gwhfetsehy .gt_spanner_row {
  border-bottom-style: hidden;
}

#gwhfetsehy .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#gwhfetsehy .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#gwhfetsehy .gt_from_md > :first-child {
  margin-top: 0;
}

#gwhfetsehy .gt_from_md > :last-child {
  margin-bottom: 0;
}

#gwhfetsehy .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#gwhfetsehy .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#gwhfetsehy .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#gwhfetsehy .gt_row_group_first td {
  border-top-width: 2px;
}

#gwhfetsehy .gt_row_group_first th {
  border-top-width: 2px;
}

#gwhfetsehy .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#gwhfetsehy .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#gwhfetsehy .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#gwhfetsehy .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#gwhfetsehy .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#gwhfetsehy .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#gwhfetsehy .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#gwhfetsehy .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#gwhfetsehy .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#gwhfetsehy .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#gwhfetsehy .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#gwhfetsehy .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#gwhfetsehy .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#gwhfetsehy .gt_left {
  text-align: left;
}

#gwhfetsehy .gt_center {
  text-align: center;
}

#gwhfetsehy .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#gwhfetsehy .gt_font_normal {
  font-weight: normal;
}

#gwhfetsehy .gt_font_bold {
  font-weight: bold;
}

#gwhfetsehy .gt_font_italic {
  font-style: italic;
}

#gwhfetsehy .gt_super {
  font-size: 65%;
}

#gwhfetsehy .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#gwhfetsehy .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#gwhfetsehy .gt_indent_1 {
  text-indent: 5px;
}

#gwhfetsehy .gt_indent_2 {
  text-indent: 10px;
}

#gwhfetsehy .gt_indent_3 {
  text-indent: 15px;
}

#gwhfetsehy .gt_indent_4 {
  text-indent: 20px;
}

#gwhfetsehy .gt_indent_5 {
  text-indent: 25px;
}

#gwhfetsehy .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#gwhfetsehy div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5QbGVpc3RvY2VuZTwvc3Ryb25nPjxiciAvPgpOID0gNzc="><span class='gt_from_md'><strong>Pleistocene</strong><br />
N = 77</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5FYXJseS1NaWQgSG9sb2NlbmU8L3N0cm9uZz48YnIgLz4KTiA9IDE1OA=="><span class='gt_from_md'><strong>Early-Mid Holocene</strong><br />
N = 158</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5BbmNpZW50PC9zdHJvbmc+PGJyIC8+Ck4gPSAzNjA="><span class='gt_from_md'><strong>Ancient</strong><br />
N = 360</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5NZWRpZXZhbDwvc3Ryb25nPjxiciAvPgpOID0gNTg3"><span class='gt_from_md'><strong>Medieval</strong><br />
N = 587</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_5"><span data-qmd-base64="PHN0cm9uZz5FYXJseSBNb2Rlcm48L3N0cm9uZz48YnIgLz4KTiA9IDc0Mw=="><span class='gt_from_md'><strong>Early Modern</strong><br />
N = 743</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_6"><span data-qmd-base64="PHN0cm9uZz5Nb2Rlcm48L3N0cm9uZz48YnIgLz4KTiA9IDc3NQ=="><span class='gt_from_md'><strong>Modern</strong><br />
N = 775</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_7"><span data-qmd-base64="PHN0cm9uZz5QcmVzZW50PC9zdHJvbmc+PGJyIC8+Ck4gPSA2ODg="><span class='gt_from_md'><strong>Present</strong><br />
N = 688</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">rec_type</td>
<td headers="stat_1" class="gt_row gt_center"><br /></td>
<td headers="stat_2" class="gt_row gt_center"><br /></td>
<td headers="stat_3" class="gt_row gt_center"><br /></td>
<td headers="stat_4" class="gt_row gt_center"><br /></td>
<td headers="stat_5" class="gt_row gt_center"><br /></td>
<td headers="stat_6" class="gt_row gt_center"><br /></td>
<td headers="stat_7" class="gt_row gt_center"><br /></td>
<td headers="p.value" class="gt_row gt_center">0.020</td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Broad, abstract, or vague</td>
<td headers="stat_1" class="gt_row gt_center">11 (14%)</td>
<td headers="stat_2" class="gt_row gt_center">12 (7.6%)</td>
<td headers="stat_3" class="gt_row gt_center">23 (6.4%)</td>
<td headers="stat_4" class="gt_row gt_center">42 (7.2%)</td>
<td headers="stat_5" class="gt_row gt_center">54 (7.3%)</td>
<td headers="stat_6" class="gt_row gt_center">59 (7.6%)</td>
<td headers="stat_7" class="gt_row gt_center">47 (6.8%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific but not actionable</td>
<td headers="stat_1" class="gt_row gt_center">12 (16%)</td>
<td headers="stat_2" class="gt_row gt_center">20 (13%)</td>
<td headers="stat_3" class="gt_row gt_center">29 (8.1%)</td>
<td headers="stat_4" class="gt_row gt_center">34 (5.8%)</td>
<td headers="stat_5" class="gt_row gt_center">50 (6.7%)</td>
<td headers="stat_6" class="gt_row gt_center">55 (7.1%)</td>
<td headers="stat_7" class="gt_row gt_center">53 (7.7%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    Specific and actionable</td>
<td headers="stat_1" class="gt_row gt_center">8 (10%)</td>
<td headers="stat_2" class="gt_row gt_center">11 (7.0%)</td>
<td headers="stat_3" class="gt_row gt_center">16 (4.4%)</td>
<td headers="stat_4" class="gt_row gt_center">27 (4.6%)</td>
<td headers="stat_5" class="gt_row gt_center">38 (5.1%)</td>
<td headers="stat_6" class="gt_row gt_center">42 (5.4%)</td>
<td headers="stat_7" class="gt_row gt_center">44 (6.4%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
    <tr><td headers="label" class="gt_row gt_left">    No recommendation</td>
<td headers="stat_1" class="gt_row gt_center">46 (60%)</td>
<td headers="stat_2" class="gt_row gt_center">115 (73%)</td>
<td headers="stat_3" class="gt_row gt_center">292 (81%)</td>
<td headers="stat_4" class="gt_row gt_center">484 (82%)</td>
<td headers="stat_5" class="gt_row gt_center">601 (81%)</td>
<td headers="stat_6" class="gt_row gt_center">619 (80%)</td>
<td headers="stat_7" class="gt_row gt_center">544 (79%)</td>
<td headers="p.value" class="gt_row gt_center"><br /></td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="9"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="9"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 11. What percentage of publications that use AGW to argue for their importance include lessons for the present/future?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="pcluefhdgg" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#pcluefhdgg table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#pcluefhdgg thead, #pcluefhdgg tbody, #pcluefhdgg tfoot, #pcluefhdgg tr, #pcluefhdgg td, #pcluefhdgg th {
  border-style: none;
}

#pcluefhdgg p {
  margin: 0;
  padding: 0;
}

#pcluefhdgg .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#pcluefhdgg .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#pcluefhdgg .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#pcluefhdgg .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#pcluefhdgg .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#pcluefhdgg .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#pcluefhdgg .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#pcluefhdgg .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#pcluefhdgg .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#pcluefhdgg .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#pcluefhdgg .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#pcluefhdgg .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#pcluefhdgg .gt_spanner_row {
  border-bottom-style: hidden;
}

#pcluefhdgg .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#pcluefhdgg .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#pcluefhdgg .gt_from_md > :first-child {
  margin-top: 0;
}

#pcluefhdgg .gt_from_md > :last-child {
  margin-bottom: 0;
}

#pcluefhdgg .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#pcluefhdgg .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#pcluefhdgg .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#pcluefhdgg .gt_row_group_first td {
  border-top-width: 2px;
}

#pcluefhdgg .gt_row_group_first th {
  border-top-width: 2px;
}

#pcluefhdgg .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#pcluefhdgg .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#pcluefhdgg .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#pcluefhdgg .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#pcluefhdgg .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#pcluefhdgg .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#pcluefhdgg .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#pcluefhdgg .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#pcluefhdgg .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#pcluefhdgg .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#pcluefhdgg .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#pcluefhdgg .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#pcluefhdgg .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#pcluefhdgg .gt_left {
  text-align: left;
}

#pcluefhdgg .gt_center {
  text-align: center;
}

#pcluefhdgg .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#pcluefhdgg .gt_font_normal {
  font-weight: normal;
}

#pcluefhdgg .gt_font_bold {
  font-weight: bold;
}

#pcluefhdgg .gt_font_italic {
  font-style: italic;
}

#pcluefhdgg .gt_super {
  font-size: 65%;
}

#pcluefhdgg .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#pcluefhdgg .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#pcluefhdgg .gt_indent_1 {
  text-indent: 5px;
}

#pcluefhdgg .gt_indent_2 {
  text-indent: 10px;
}

#pcluefhdgg .gt_indent_3 {
  text-indent: 15px;
}

#pcluefhdgg .gt_indent_4 {
  text-indent: 20px;
}

#pcluefhdgg .gt_indent_5 {
  text-indent: 25px;
}

#pcluefhdgg .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#pcluefhdgg div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Obzwvc3Ryb25nPjxiciAvPgpOID0gNTMz"><span class='gt_from_md'><strong>No</strong><br />
N = 533</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5ZZXM8L3N0cm9uZz48YnIgLz4KTiA9IDY1OA=="><span class='gt_from_md'><strong>Yes</strong><br />
N = 658</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">31 (5.8%)</td>
<td headers="stat_2" class="gt_row gt_center">163 (25%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



What percentage of paleosciences/history/literature, etc. articles that use AGW to argue for their importance include lessons for the present/future?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="vfxwdpzafm" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#vfxwdpzafm table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#vfxwdpzafm thead, #vfxwdpzafm tbody, #vfxwdpzafm tfoot, #vfxwdpzafm tr, #vfxwdpzafm td, #vfxwdpzafm th {
  border-style: none;
}

#vfxwdpzafm p {
  margin: 0;
  padding: 0;
}

#vfxwdpzafm .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#vfxwdpzafm .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#vfxwdpzafm .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#vfxwdpzafm .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#vfxwdpzafm .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#vfxwdpzafm .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#vfxwdpzafm .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#vfxwdpzafm .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#vfxwdpzafm .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#vfxwdpzafm .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#vfxwdpzafm .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#vfxwdpzafm .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#vfxwdpzafm .gt_spanner_row {
  border-bottom-style: hidden;
}

#vfxwdpzafm .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#vfxwdpzafm .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#vfxwdpzafm .gt_from_md > :first-child {
  margin-top: 0;
}

#vfxwdpzafm .gt_from_md > :last-child {
  margin-bottom: 0;
}

#vfxwdpzafm .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#vfxwdpzafm .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#vfxwdpzafm .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#vfxwdpzafm .gt_row_group_first td {
  border-top-width: 2px;
}

#vfxwdpzafm .gt_row_group_first th {
  border-top-width: 2px;
}

#vfxwdpzafm .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#vfxwdpzafm .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#vfxwdpzafm .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#vfxwdpzafm .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#vfxwdpzafm .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#vfxwdpzafm .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#vfxwdpzafm .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#vfxwdpzafm .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#vfxwdpzafm .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#vfxwdpzafm .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#vfxwdpzafm .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#vfxwdpzafm .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#vfxwdpzafm .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#vfxwdpzafm .gt_left {
  text-align: left;
}

#vfxwdpzafm .gt_center {
  text-align: center;
}

#vfxwdpzafm .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#vfxwdpzafm .gt_font_normal {
  font-weight: normal;
}

#vfxwdpzafm .gt_font_bold {
  font-weight: bold;
}

#vfxwdpzafm .gt_font_italic {
  font-style: italic;
}

#vfxwdpzafm .gt_super {
  font-size: 65%;
}

#vfxwdpzafm .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#vfxwdpzafm .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#vfxwdpzafm .gt_indent_1 {
  text-indent: 5px;
}

#vfxwdpzafm .gt_indent_2 {
  text-indent: 10px;
}

#vfxwdpzafm .gt_indent_3 {
  text-indent: 15px;
}

#vfxwdpzafm .gt_indent_4 {
  text-indent: 20px;
}

#vfxwdpzafm .gt_indent_5 {
  text-indent: 25px;
}

#vfxwdpzafm .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#vfxwdpzafm div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5BcmNoYWVvbG9neTwvc3Ryb25nPjxiciAvPgpOID0gNzU="><span class='gt_from_md'><strong>Archaeology</strong><br />
N = 75</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5FY29ub21pY3M8L3N0cm9uZz48YnIgLz4KTiA9IDM="><span class='gt_from_md'><strong>Economics</strong><br />
N = 3</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5FcGlkZW1pb2xvZ3k8L3N0cm9uZz48YnIgLz4KTiA9IDI="><span class='gt_from_md'><strong>Epidemiology</strong><br />
N = 2</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5HZW9ncmFwaHk8L3N0cm9uZz48YnIgLz4KTiA9IDE3"><span class='gt_from_md'><strong>Geography</strong><br />
N = 17</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_5"><span data-qmd-base64="PHN0cm9uZz5IaXN0b3J5PC9zdHJvbmc+PGJyIC8+Ck4gPSA3Ng=="><span class='gt_from_md'><strong>History</strong><br />
N = 76</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_6"><span data-qmd-base64="PHN0cm9uZz5Kb2ludCBGaWVsZHM8L3N0cm9uZz48YnIgLz4KTiA9IDkw"><span class='gt_from_md'><strong>Joint Fields</strong><br />
N = 90</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_7"><span data-qmd-base64="PHN0cm9uZz5MaXRlcmF0dXJlPC9zdHJvbmc+PGJyIC8+Ck4gPSAyMA=="><span class='gt_from_md'><strong>Literature</strong><br />
N = 20</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_8"><span data-qmd-base64="PHN0cm9uZz5PdGhlcjwvc3Ryb25nPjxiciAvPgpOID0gMTA="><span class='gt_from_md'><strong>Other</strong><br />
N = 10</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_9"><span data-qmd-base64="PHN0cm9uZz5QYWxlb2NsaW1hdG9sb2d5PC9zdHJvbmc+PGJyIC8+Ck4gPSAzNjU="><span class='gt_from_md'><strong>Paleoclimatology</strong><br />
N = 365</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">36 (48%)</td>
<td headers="stat_2" class="gt_row gt_center">1 (33%)</td>
<td headers="stat_3" class="gt_row gt_center">1 (50%)</td>
<td headers="stat_4" class="gt_row gt_center">5 (29%)</td>
<td headers="stat_5" class="gt_row gt_center">36 (47%)</td>
<td headers="stat_6" class="gt_row gt_center">28 (31%)</td>
<td headers="stat_7" class="gt_row gt_center">9 (45%)</td>
<td headers="stat_8" class="gt_row gt_center">7 (70%)</td>
<td headers="stat_9" class="gt_row gt_center">40 (11%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="11"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="11"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::


{{< pagebreak >}}






Same as above, but now broken down by region:



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="mpoelianfe" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#mpoelianfe table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#mpoelianfe thead, #mpoelianfe tbody, #mpoelianfe tfoot, #mpoelianfe tr, #mpoelianfe td, #mpoelianfe th {
  border-style: none;
}

#mpoelianfe p {
  margin: 0;
  padding: 0;
}

#mpoelianfe .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#mpoelianfe .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#mpoelianfe .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#mpoelianfe .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#mpoelianfe .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#mpoelianfe .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#mpoelianfe .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#mpoelianfe .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#mpoelianfe .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#mpoelianfe .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#mpoelianfe .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#mpoelianfe .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#mpoelianfe .gt_spanner_row {
  border-bottom-style: hidden;
}

#mpoelianfe .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#mpoelianfe .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#mpoelianfe .gt_from_md > :first-child {
  margin-top: 0;
}

#mpoelianfe .gt_from_md > :last-child {
  margin-bottom: 0;
}

#mpoelianfe .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#mpoelianfe .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#mpoelianfe .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#mpoelianfe .gt_row_group_first td {
  border-top-width: 2px;
}

#mpoelianfe .gt_row_group_first th {
  border-top-width: 2px;
}

#mpoelianfe .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mpoelianfe .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#mpoelianfe .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#mpoelianfe .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#mpoelianfe .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mpoelianfe .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#mpoelianfe .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#mpoelianfe .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#mpoelianfe .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#mpoelianfe .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#mpoelianfe .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mpoelianfe .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#mpoelianfe .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mpoelianfe .gt_left {
  text-align: left;
}

#mpoelianfe .gt_center {
  text-align: center;
}

#mpoelianfe .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#mpoelianfe .gt_font_normal {
  font-weight: normal;
}

#mpoelianfe .gt_font_bold {
  font-weight: bold;
}

#mpoelianfe .gt_font_italic {
  font-style: italic;
}

#mpoelianfe .gt_super {
  font-size: 65%;
}

#mpoelianfe .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#mpoelianfe .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#mpoelianfe .gt_indent_1 {
  text-indent: 5px;
}

#mpoelianfe .gt_indent_2 {
  text-indent: 10px;
}

#mpoelianfe .gt_indent_3 {
  text-indent: 15px;
}

#mpoelianfe .gt_indent_4 {
  text-indent: 20px;
}

#mpoelianfe .gt_indent_5 {
  text-indent: 25px;
}

#mpoelianfe .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#mpoelianfe div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5BZnJpY2E8L3N0cm9uZz48YnIgLz4KTiA9IDIz"><span class='gt_from_md'><strong>Africa</strong><br />
N = 23</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5BbWVyaWNhczwvc3Ryb25nPjxiciAvPgpOID0gMTAx"><span class='gt_from_md'><strong>Americas</strong><br />
N = 101</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5Bc2lhPC9zdHJvbmc+PGJyIC8+Ck4gPSAxODI="><span class='gt_from_md'><strong>Asia</strong><br />
N = 182</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5FdXJvcGU8L3N0cm9uZz48YnIgLz4KTiA9IDEzNg=="><span class='gt_from_md'><strong>Europe</strong><br />
N = 136</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_5"><span data-qmd-base64="PHN0cm9uZz5HbG9iYWw8L3N0cm9uZz48YnIgLz4KTiA9IDE0Mw=="><span class='gt_from_md'><strong>Global</strong><br />
N = 143</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_6"><span data-qmd-base64="PHN0cm9uZz5NaWRkbGUgRWFzdDwvc3Ryb25nPjxiciAvPgpOID0gMjM="><span class='gt_from_md'><strong>Middle East</strong><br />
N = 23</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_7"><span data-qmd-base64="PHN0cm9uZz5PY2VhbmlhPC9zdHJvbmc+PGJyIC8+Ck4gPSAxNg=="><span class='gt_from_md'><strong>Oceania</strong><br />
N = 16</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_8"><span data-qmd-base64="PHN0cm9uZz5Qb2xhcjwvc3Ryb25nPjxiciAvPgpOID0gMzQ="><span class='gt_from_md'><strong>Polar</strong><br />
N = 34</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">9 (39%)</td>
<td headers="stat_2" class="gt_row gt_center">30 (30%)</td>
<td headers="stat_3" class="gt_row gt_center">21 (12%)</td>
<td headers="stat_4" class="gt_row gt_center">31 (23%)</td>
<td headers="stat_5" class="gt_row gt_center">47 (33%)</td>
<td headers="stat_6" class="gt_row gt_center">11 (48%)</td>
<td headers="stat_7" class="gt_row gt_center">7 (44%)</td>
<td headers="stat_8" class="gt_row gt_center">7 (21%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="10"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="10"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



Broken down by period:



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="elqehdtrlo" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#elqehdtrlo table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#elqehdtrlo thead, #elqehdtrlo tbody, #elqehdtrlo tfoot, #elqehdtrlo tr, #elqehdtrlo td, #elqehdtrlo th {
  border-style: none;
}

#elqehdtrlo p {
  margin: 0;
  padding: 0;
}

#elqehdtrlo .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#elqehdtrlo .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#elqehdtrlo .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#elqehdtrlo .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#elqehdtrlo .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#elqehdtrlo .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#elqehdtrlo .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#elqehdtrlo .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#elqehdtrlo .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#elqehdtrlo .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#elqehdtrlo .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#elqehdtrlo .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#elqehdtrlo .gt_spanner_row {
  border-bottom-style: hidden;
}

#elqehdtrlo .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#elqehdtrlo .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#elqehdtrlo .gt_from_md > :first-child {
  margin-top: 0;
}

#elqehdtrlo .gt_from_md > :last-child {
  margin-bottom: 0;
}

#elqehdtrlo .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#elqehdtrlo .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#elqehdtrlo .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#elqehdtrlo .gt_row_group_first td {
  border-top-width: 2px;
}

#elqehdtrlo .gt_row_group_first th {
  border-top-width: 2px;
}

#elqehdtrlo .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#elqehdtrlo .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#elqehdtrlo .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#elqehdtrlo .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#elqehdtrlo .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#elqehdtrlo .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#elqehdtrlo .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#elqehdtrlo .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#elqehdtrlo .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#elqehdtrlo .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#elqehdtrlo .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#elqehdtrlo .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#elqehdtrlo .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#elqehdtrlo .gt_left {
  text-align: left;
}

#elqehdtrlo .gt_center {
  text-align: center;
}

#elqehdtrlo .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#elqehdtrlo .gt_font_normal {
  font-weight: normal;
}

#elqehdtrlo .gt_font_bold {
  font-weight: bold;
}

#elqehdtrlo .gt_font_italic {
  font-style: italic;
}

#elqehdtrlo .gt_super {
  font-size: 65%;
}

#elqehdtrlo .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#elqehdtrlo .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#elqehdtrlo .gt_indent_1 {
  text-indent: 5px;
}

#elqehdtrlo .gt_indent_2 {
  text-indent: 10px;
}

#elqehdtrlo .gt_indent_3 {
  text-indent: 15px;
}

#elqehdtrlo .gt_indent_4 {
  text-indent: 20px;
}

#elqehdtrlo .gt_indent_5 {
  text-indent: 25px;
}

#elqehdtrlo .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#elqehdtrlo div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5QbGVpc3RvY2VuZTwvc3Ryb25nPjxiciAvPgpOID0gMzg="><span class='gt_from_md'><strong>Pleistocene</strong><br />
N = 38</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5FYXJseS1NaWQgSG9sb2NlbmU8L3N0cm9uZz48YnIgLz4KTiA9IDc0"><span class='gt_from_md'><strong>Early-Mid Holocene</strong><br />
N = 74</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5BbmNpZW50PC9zdHJvbmc+PGJyIC8+Ck4gPSAxODE="><span class='gt_from_md'><strong>Ancient</strong><br />
N = 181</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5NZWRpZXZhbDwvc3Ryb25nPjxiciAvPgpOID0gMzIy"><span class='gt_from_md'><strong>Medieval</strong><br />
N = 322</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_5"><span data-qmd-base64="PHN0cm9uZz5FYXJseSBNb2Rlcm48L3N0cm9uZz48YnIgLz4KTiA9IDQ0NA=="><span class='gt_from_md'><strong>Early Modern</strong><br />
N = 444</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_6"><span data-qmd-base64="PHN0cm9uZz5Nb2Rlcm48L3N0cm9uZz48YnIgLz4KTiA9IDQ5OQ=="><span class='gt_from_md'><strong>Modern</strong><br />
N = 499</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_7"><span data-qmd-base64="PHN0cm9uZz5QcmVzZW50PC9zdHJvbmc+PGJyIC8+Ck4gPSA0Njk="><span class='gt_from_md'><strong>Present</strong><br />
N = 469</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">17 (45%)</td>
<td headers="stat_2" class="gt_row gt_center">26 (35%)</td>
<td headers="stat_3" class="gt_row gt_center">44 (24%)</td>
<td headers="stat_4" class="gt_row gt_center">74 (23%)</td>
<td headers="stat_5" class="gt_row gt_center">100 (23%)</td>
<td headers="stat_6" class="gt_row gt_center">113 (23%)</td>
<td headers="stat_7" class="gt_row gt_center">105 (22%)</td>
<td headers="p.value" class="gt_row gt_center">0.014</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="9"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="9"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



Broken down by method:



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="lxvdpuyqna" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#lxvdpuyqna table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#lxvdpuyqna thead, #lxvdpuyqna tbody, #lxvdpuyqna tfoot, #lxvdpuyqna tr, #lxvdpuyqna td, #lxvdpuyqna th {
  border-style: none;
}

#lxvdpuyqna p {
  margin: 0;
  padding: 0;
}

#lxvdpuyqna .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#lxvdpuyqna .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#lxvdpuyqna .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#lxvdpuyqna .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#lxvdpuyqna .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#lxvdpuyqna .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#lxvdpuyqna .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#lxvdpuyqna .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#lxvdpuyqna .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#lxvdpuyqna .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#lxvdpuyqna .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#lxvdpuyqna .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#lxvdpuyqna .gt_spanner_row {
  border-bottom-style: hidden;
}

#lxvdpuyqna .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#lxvdpuyqna .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#lxvdpuyqna .gt_from_md > :first-child {
  margin-top: 0;
}

#lxvdpuyqna .gt_from_md > :last-child {
  margin-bottom: 0;
}

#lxvdpuyqna .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#lxvdpuyqna .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#lxvdpuyqna .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#lxvdpuyqna .gt_row_group_first td {
  border-top-width: 2px;
}

#lxvdpuyqna .gt_row_group_first th {
  border-top-width: 2px;
}

#lxvdpuyqna .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#lxvdpuyqna .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#lxvdpuyqna .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#lxvdpuyqna .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#lxvdpuyqna .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#lxvdpuyqna .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#lxvdpuyqna .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#lxvdpuyqna .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#lxvdpuyqna .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#lxvdpuyqna .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#lxvdpuyqna .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#lxvdpuyqna .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#lxvdpuyqna .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#lxvdpuyqna .gt_left {
  text-align: left;
}

#lxvdpuyqna .gt_center {
  text-align: center;
}

#lxvdpuyqna .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#lxvdpuyqna .gt_font_normal {
  font-weight: normal;
}

#lxvdpuyqna .gt_font_bold {
  font-weight: bold;
}

#lxvdpuyqna .gt_font_italic {
  font-style: italic;
}

#lxvdpuyqna .gt_super {
  font-size: 65%;
}

#lxvdpuyqna .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#lxvdpuyqna .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#lxvdpuyqna .gt_indent_1 {
  text-indent: 5px;
}

#lxvdpuyqna .gt_indent_2 {
  text-indent: 10px;
}

#lxvdpuyqna .gt_indent_3 {
  text-indent: 15px;
}

#lxvdpuyqna .gt_indent_4 {
  text-indent: 20px;
}

#lxvdpuyqna .gt_indent_5 {
  text-indent: 25px;
}

#lxvdpuyqna .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#lxvdpuyqna div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5Cb3RoPC9zdHJvbmc+PGJyIC8+Ck4gPSA2OQ=="><span class='gt_from_md'><strong>Both</strong><br />
N = 69</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5OZWl0aGVyPC9zdHJvbmc+PGJyIC8+Ck4gPSA3Mg=="><span class='gt_from_md'><strong>Neither</strong><br />
N = 72</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5RdWFsaXRhdGl2ZTwvc3Ryb25nPjxiciAvPgpOID0gOTc="><span class='gt_from_md'><strong>Qualitative</strong><br />
N = 97</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5RdWFudGl0YXRpdmU8L3N0cm9uZz48YnIgLz4KTiA9IDQyMA=="><span class='gt_from_md'><strong>Quantitative</strong><br />
N = 420</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">27 (39%)</td>
<td headers="stat_2" class="gt_row gt_center">23 (32%)</td>
<td headers="stat_3" class="gt_row gt_center">48 (49%)</td>
<td headers="stat_4" class="gt_row gt_center">65 (15%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



Broken down by publication type:



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="mkpjevaksy" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#mkpjevaksy table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#mkpjevaksy thead, #mkpjevaksy tbody, #mkpjevaksy tfoot, #mkpjevaksy tr, #mkpjevaksy td, #mkpjevaksy th {
  border-style: none;
}

#mkpjevaksy p {
  margin: 0;
  padding: 0;
}

#mkpjevaksy .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#mkpjevaksy .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#mkpjevaksy .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#mkpjevaksy .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#mkpjevaksy .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#mkpjevaksy .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#mkpjevaksy .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#mkpjevaksy .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#mkpjevaksy .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#mkpjevaksy .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#mkpjevaksy .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#mkpjevaksy .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#mkpjevaksy .gt_spanner_row {
  border-bottom-style: hidden;
}

#mkpjevaksy .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#mkpjevaksy .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#mkpjevaksy .gt_from_md > :first-child {
  margin-top: 0;
}

#mkpjevaksy .gt_from_md > :last-child {
  margin-bottom: 0;
}

#mkpjevaksy .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#mkpjevaksy .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#mkpjevaksy .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#mkpjevaksy .gt_row_group_first td {
  border-top-width: 2px;
}

#mkpjevaksy .gt_row_group_first th {
  border-top-width: 2px;
}

#mkpjevaksy .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mkpjevaksy .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#mkpjevaksy .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#mkpjevaksy .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#mkpjevaksy .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mkpjevaksy .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#mkpjevaksy .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#mkpjevaksy .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#mkpjevaksy .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#mkpjevaksy .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#mkpjevaksy .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mkpjevaksy .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#mkpjevaksy .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#mkpjevaksy .gt_left {
  text-align: left;
}

#mkpjevaksy .gt_center {
  text-align: center;
}

#mkpjevaksy .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#mkpjevaksy .gt_font_normal {
  font-weight: normal;
}

#mkpjevaksy .gt_font_bold {
  font-weight: bold;
}

#mkpjevaksy .gt_font_italic {
  font-style: italic;
}

#mkpjevaksy .gt_super {
  font-size: 65%;
}

#mkpjevaksy .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#mkpjevaksy .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#mkpjevaksy .gt_indent_1 {
  text-indent: 5px;
}

#mkpjevaksy .gt_indent_2 {
  text-indent: 10px;
}

#mkpjevaksy .gt_indent_3 {
  text-indent: 15px;
}

#mkpjevaksy .gt_indent_4 {
  text-indent: 20px;
}

#mkpjevaksy .gt_indent_5 {
  text-indent: 25px;
}

#mkpjevaksy .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#mkpjevaksy div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5MaXQuIFJldmlldy9NZXRob2QgSW50ZXJ2ZW50aW9uPC9zdHJvbmc+PGJyIC8+Ck4gPSA5Nw=="><span class='gt_from_md'><strong>Lit. Review/Method Intervention</strong><br />
N = 97</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5PcmlnaW5hbCBSZXNlYXJjaDwvc3Ryb25nPjxiciAvPgpOID0gNTYx"><span class='gt_from_md'><strong>Original Research</strong><br />
N = 561</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">36 (37%)</td>
<td headers="stat_2" class="gt_row gt_center">127 (23%)</td>
<td headers="p.value" class="gt_row gt_center">0.002</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="4"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="UGVhcnNvbuKAmXMgQ2hpLXNxdWFyZWQgdGVzdA=="><span class='gt_from_md'>Pearson’s Chi-squared test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



Broken down by publication format:



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="ivdeifnkdo" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#ivdeifnkdo table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#ivdeifnkdo thead, #ivdeifnkdo tbody, #ivdeifnkdo tfoot, #ivdeifnkdo tr, #ivdeifnkdo td, #ivdeifnkdo th {
  border-style: none;
}

#ivdeifnkdo p {
  margin: 0;
  padding: 0;
}

#ivdeifnkdo .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#ivdeifnkdo .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#ivdeifnkdo .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#ivdeifnkdo .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#ivdeifnkdo .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#ivdeifnkdo .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ivdeifnkdo .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#ivdeifnkdo .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#ivdeifnkdo .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#ivdeifnkdo .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#ivdeifnkdo .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#ivdeifnkdo .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#ivdeifnkdo .gt_spanner_row {
  border-bottom-style: hidden;
}

#ivdeifnkdo .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#ivdeifnkdo .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#ivdeifnkdo .gt_from_md > :first-child {
  margin-top: 0;
}

#ivdeifnkdo .gt_from_md > :last-child {
  margin-bottom: 0;
}

#ivdeifnkdo .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#ivdeifnkdo .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#ivdeifnkdo .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#ivdeifnkdo .gt_row_group_first td {
  border-top-width: 2px;
}

#ivdeifnkdo .gt_row_group_first th {
  border-top-width: 2px;
}

#ivdeifnkdo .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ivdeifnkdo .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#ivdeifnkdo .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#ivdeifnkdo .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ivdeifnkdo .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ivdeifnkdo .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#ivdeifnkdo .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#ivdeifnkdo .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#ivdeifnkdo .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#ivdeifnkdo .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#ivdeifnkdo .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ivdeifnkdo .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#ivdeifnkdo .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#ivdeifnkdo .gt_left {
  text-align: left;
}

#ivdeifnkdo .gt_center {
  text-align: center;
}

#ivdeifnkdo .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#ivdeifnkdo .gt_font_normal {
  font-weight: normal;
}

#ivdeifnkdo .gt_font_bold {
  font-weight: bold;
}

#ivdeifnkdo .gt_font_italic {
  font-style: italic;
}

#ivdeifnkdo .gt_super {
  font-size: 65%;
}

#ivdeifnkdo .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#ivdeifnkdo .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#ivdeifnkdo .gt_indent_1 {
  text-indent: 5px;
}

#ivdeifnkdo .gt_indent_2 {
  text-indent: 10px;
}

#ivdeifnkdo .gt_indent_3 {
  text-indent: 15px;
}

#ivdeifnkdo .gt_indent_4 {
  text-indent: 20px;
}

#ivdeifnkdo .gt_indent_5 {
  text-indent: 25px;
}

#ivdeifnkdo .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#ivdeifnkdo div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5BcnRpY2xlPC9zdHJvbmc+PGJyIC8+Ck4gPSA1MzM="><span class='gt_from_md'><strong>Article</strong><br />
N = 533</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5Cb29rPC9zdHJvbmc+PGJyIC8+Ck4gPSAzOQ=="><span class='gt_from_md'><strong>Book</strong><br />
N = 39</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5Cb29rL1RoZXNpczwvc3Ryb25nPjxiciAvPgpOID0gMg=="><span class='gt_from_md'><strong>Book/Thesis</strong><br />
N = 2</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5DaGFwdGVyL0FydGljbGU8L3N0cm9uZz48YnIgLz4KTiA9IDg0"><span class='gt_from_md'><strong>Chapter/Article</strong><br />
N = 84</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">114 (21%)</td>
<td headers="stat_2" class="gt_row gt_center">20 (51%)</td>
<td headers="stat_3" class="gt_row gt_center">2 (100%)</td>
<td headers="stat_4" class="gt_row gt_center">27 (32%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBleGFjdCB0ZXN0"><span class='gt_from_md'>Fisher’s exact test</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::



### 12. Are there journals which are particularly correlated with including lessons for the present/future?

Of the journals with 10 or more entries in our database, the following journals have the highest proportion of papers with recommendations for the present or future. However, only Climate and American Literature has a significantly higher proportion of recommendations than the average for all papers, after correcting for multiple comparisons.



::: {.cell}
::: {.cell-output .cell-output-stdout}

```
# A tibble: 29 × 7
   journal                  n_papers n_recs prop_recs    pval  p_adj significant
   <chr>                       <int>  <int>     <dbl>   <dbl>  <dbl> <lgl>      
 1 Climate and American Li…       19      9     0.474 0.00155 0.0449 TRUE       
 2 Proceedings of the Nati…       39     12     0.308 0.0265  0.192  FALSE      
 3 Global and Planetary Ch…       20      6     0.3   0.122   0.393  FALSE      
 4 Nature                         10      3     0.3   0.214   0.402  FALSE      
 5 Nature Communications          10      3     0.3   0.214   0.402  FALSE      
 6 Environmental Research …       11      3     0.273 0.403   0.556  FALSE      
 7 Geophysical Research Le…       24      6     0.25  0.265   0.404  FALSE      
 8 Climate Changes in the …       14      3     0.214 0.488   0.643  FALSE      
 9 Climate Change and Huma…       10      2     0.2   0.671   0.695  FALSE      
10 Climatic Change                25      5     0.2   0.588   0.682  FALSE      
# ℹ 19 more rows
```


:::
:::



### 13. What percentage of each publication type provides lessons versus AGW justifications?



::: {.cell}
::: {.cell-output-display}


```{=html}
<div id="frjksehghe" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#frjksehghe table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#frjksehghe thead, #frjksehghe tbody, #frjksehghe tfoot, #frjksehghe tr, #frjksehghe td, #frjksehghe th {
  border-style: none;
}

#frjksehghe p {
  margin: 0;
  padding: 0;
}

#frjksehghe .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#frjksehghe .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#frjksehghe .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#frjksehghe .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#frjksehghe .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#frjksehghe .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#frjksehghe .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#frjksehghe .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#frjksehghe .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#frjksehghe .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#frjksehghe .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#frjksehghe .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#frjksehghe .gt_spanner_row {
  border-bottom-style: hidden;
}

#frjksehghe .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#frjksehghe .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#frjksehghe .gt_from_md > :first-child {
  margin-top: 0;
}

#frjksehghe .gt_from_md > :last-child {
  margin-bottom: 0;
}

#frjksehghe .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#frjksehghe .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#frjksehghe .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#frjksehghe .gt_row_group_first td {
  border-top-width: 2px;
}

#frjksehghe .gt_row_group_first th {
  border-top-width: 2px;
}

#frjksehghe .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#frjksehghe .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#frjksehghe .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#frjksehghe .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#frjksehghe .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#frjksehghe .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#frjksehghe .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#frjksehghe .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#frjksehghe .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#frjksehghe .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#frjksehghe .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#frjksehghe .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#frjksehghe .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#frjksehghe .gt_left {
  text-align: left;
}

#frjksehghe .gt_center {
  text-align: center;
}

#frjksehghe .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#frjksehghe .gt_font_normal {
  font-weight: normal;
}

#frjksehghe .gt_font_bold {
  font-weight: bold;
}

#frjksehghe .gt_font_italic {
  font-style: italic;
}

#frjksehghe .gt_super {
  font-size: 65%;
}

#frjksehghe .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#frjksehghe .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#frjksehghe .gt_indent_1 {
  text-indent: 5px;
}

#frjksehghe .gt_indent_2 {
  text-indent: 10px;
}

#frjksehghe .gt_indent_3 {
  text-indent: 15px;
}

#frjksehghe .gt_indent_4 {
  text-indent: 20px;
}

#frjksehghe .gt_indent_5 {
  text-indent: 25px;
}

#frjksehghe .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#frjksehghe div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5BcnRpY2xlPC9zdHJvbmc+PGJyIC8+Ck4gPSA4ODc="><span class='gt_from_md'><strong>Article</strong><br />
N = 887</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5Cb29rPC9zdHJvbmc+PGJyIC8+Ck4gPSA1NQ=="><span class='gt_from_md'><strong>Book</strong><br />
N = 55</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5Cb29rL1RoZXNpczwvc3Ryb25nPjxiciAvPgpOID0gMg=="><span class='gt_from_md'><strong>Book/Thesis</strong><br />
N = 2</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_4"><span data-qmd-base64="PHN0cm9uZz5DaGFwdGVyL0FydGljbGU8L3N0cm9uZz48YnIgLz4KTiA9IDI0Nw=="><span class='gt_from_md'><strong>Chapter/Article</strong><br />
N = 247</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">130 (15%)</td>
<td headers="stat_2" class="gt_row gt_center">26 (47%)</td>
<td headers="stat_3" class="gt_row gt_center">2 (100%)</td>
<td headers="stat_4" class="gt_row gt_center">36 (15%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Uses AGW</td>
<td headers="stat_1" class="gt_row gt_center">533 (60%)</td>
<td headers="stat_2" class="gt_row gt_center">39 (71%)</td>
<td headers="stat_3" class="gt_row gt_center">2 (100%)</td>
<td headers="stat_4" class="gt_row gt_center">84 (34%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="6"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::

::: {.cell-output-display}


```{=html}
<div id="symxsxlrqm" style="padding-left:0px;padding-right:0px;padding-top:10px;padding-bottom:10px;overflow-x:auto;overflow-y:auto;width:auto;height:auto;">
<style>#symxsxlrqm table {
  font-family: system-ui, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol', 'Noto Color Emoji';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#symxsxlrqm thead, #symxsxlrqm tbody, #symxsxlrqm tfoot, #symxsxlrqm tr, #symxsxlrqm td, #symxsxlrqm th {
  border-style: none;
}

#symxsxlrqm p {
  margin: 0;
  padding: 0;
}

#symxsxlrqm .gt_table {
  display: table;
  border-collapse: collapse;
  line-height: normal;
  margin-left: auto;
  margin-right: auto;
  color: #333333;
  font-size: 11px;
  font-weight: normal;
  font-style: normal;
  background-color: #FFFFFF;
  width: auto;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #A8A8A8;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #A8A8A8;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
}

#symxsxlrqm .gt_caption {
  padding-top: 4px;
  padding-bottom: 4px;
}

#symxsxlrqm .gt_title {
  color: #333333;
  font-size: 125%;
  font-weight: initial;
  padding-top: 4px;
  padding-bottom: 4px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-color: #FFFFFF;
  border-bottom-width: 0;
}

#symxsxlrqm .gt_subtitle {
  color: #333333;
  font-size: 85%;
  font-weight: initial;
  padding-top: 3px;
  padding-bottom: 5px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-color: #FFFFFF;
  border-top-width: 0;
}

#symxsxlrqm .gt_heading {
  background-color: #FFFFFF;
  text-align: center;
  border-bottom-color: #FFFFFF;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#symxsxlrqm .gt_bottom_border {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#symxsxlrqm .gt_col_headings {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
}

#symxsxlrqm .gt_col_heading {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 6px;
  padding-left: 5px;
  padding-right: 5px;
  overflow-x: hidden;
}

#symxsxlrqm .gt_column_spanner_outer {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: normal;
  text-transform: inherit;
  padding-top: 0;
  padding-bottom: 0;
  padding-left: 4px;
  padding-right: 4px;
}

#symxsxlrqm .gt_column_spanner_outer:first-child {
  padding-left: 0;
}

#symxsxlrqm .gt_column_spanner_outer:last-child {
  padding-right: 0;
}

#symxsxlrqm .gt_column_spanner {
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: bottom;
  padding-top: 5px;
  padding-bottom: 5px;
  overflow-x: hidden;
  display: inline-block;
  width: 100%;
}

#symxsxlrqm .gt_spanner_row {
  border-bottom-style: hidden;
}

#symxsxlrqm .gt_group_heading {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  text-align: left;
}

#symxsxlrqm .gt_empty_group_heading {
  padding: 0.5px;
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  vertical-align: middle;
}

#symxsxlrqm .gt_from_md > :first-child {
  margin-top: 0;
}

#symxsxlrqm .gt_from_md > :last-child {
  margin-bottom: 0;
}

#symxsxlrqm .gt_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  margin: 10px;
  border-top-style: solid;
  border-top-width: 1px;
  border-top-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 1px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 1px;
  border-right-color: #D3D3D3;
  vertical-align: middle;
  overflow-x: hidden;
}

#symxsxlrqm .gt_stub {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
}

#symxsxlrqm .gt_stub_row_group {
  color: #333333;
  background-color: #FFFFFF;
  font-size: 100%;
  font-weight: initial;
  text-transform: inherit;
  border-right-style: solid;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
  padding-left: 5px;
  padding-right: 5px;
  vertical-align: top;
}

#symxsxlrqm .gt_row_group_first td {
  border-top-width: 2px;
}

#symxsxlrqm .gt_row_group_first th {
  border-top-width: 2px;
}

#symxsxlrqm .gt_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#symxsxlrqm .gt_first_summary_row {
  border-top-style: solid;
  border-top-color: #D3D3D3;
}

#symxsxlrqm .gt_first_summary_row.thick {
  border-top-width: 2px;
}

#symxsxlrqm .gt_last_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#symxsxlrqm .gt_grand_summary_row {
  color: #333333;
  background-color: #FFFFFF;
  text-transform: inherit;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#symxsxlrqm .gt_first_grand_summary_row {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-top-style: double;
  border-top-width: 6px;
  border-top-color: #D3D3D3;
}

#symxsxlrqm .gt_last_grand_summary_row_top {
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
  border-bottom-style: double;
  border-bottom-width: 6px;
  border-bottom-color: #D3D3D3;
}

#symxsxlrqm .gt_striped {
  background-color: rgba(128, 128, 128, 0.05);
}

#symxsxlrqm .gt_table_body {
  border-top-style: solid;
  border-top-width: 2px;
  border-top-color: #D3D3D3;
  border-bottom-style: solid;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
}

#symxsxlrqm .gt_footnotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#symxsxlrqm .gt_footnote {
  margin: 0px;
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#symxsxlrqm .gt_sourcenotes {
  color: #333333;
  background-color: #FFFFFF;
  border-bottom-style: none;
  border-bottom-width: 2px;
  border-bottom-color: #D3D3D3;
  border-left-style: none;
  border-left-width: 2px;
  border-left-color: #D3D3D3;
  border-right-style: none;
  border-right-width: 2px;
  border-right-color: #D3D3D3;
}

#symxsxlrqm .gt_sourcenote {
  font-size: 90%;
  padding-top: 1px;
  padding-bottom: 1px;
  padding-left: 5px;
  padding-right: 5px;
}

#symxsxlrqm .gt_left {
  text-align: left;
}

#symxsxlrqm .gt_center {
  text-align: center;
}

#symxsxlrqm .gt_right {
  text-align: right;
  font-variant-numeric: tabular-nums;
}

#symxsxlrqm .gt_font_normal {
  font-weight: normal;
}

#symxsxlrqm .gt_font_bold {
  font-weight: bold;
}

#symxsxlrqm .gt_font_italic {
  font-style: italic;
}

#symxsxlrqm .gt_super {
  font-size: 65%;
}

#symxsxlrqm .gt_footnote_marks {
  font-size: 75%;
  vertical-align: 0.4em;
  position: initial;
}

#symxsxlrqm .gt_asterisk {
  font-size: 100%;
  vertical-align: 0;
}

#symxsxlrqm .gt_indent_1 {
  text-indent: 5px;
}

#symxsxlrqm .gt_indent_2 {
  text-indent: 10px;
}

#symxsxlrqm .gt_indent_3 {
  text-indent: 15px;
}

#symxsxlrqm .gt_indent_4 {
  text-indent: 20px;
}

#symxsxlrqm .gt_indent_5 {
  text-indent: 25px;
}

#symxsxlrqm .katex-display {
  display: inline-flex !important;
  margin-bottom: 0.75em !important;
}

#symxsxlrqm div.Reactable > div.rt-table > div.rt-thead > div.rt-tr.rt-tr-group-header > div.rt-th-group:after {
  height: 0px !important;
}
</style>
<table class="gt_table" data-quarto-disable-processing="false" data-quarto-bootstrap="false">
  <thead>
    <tr class="gt_col_headings">
      <th class="gt_col_heading gt_columns_bottom_border gt_left" rowspan="1" colspan="1" scope="col" id="label"><span data-qmd-base64="PHN0cm9uZz5WYXJpYWJsZTwvc3Ryb25nPg=="><span class='gt_from_md'><strong>Variable</strong></span></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_1"><span data-qmd-base64="PHN0cm9uZz5BcnRpY2xlIChjb21iaW5lZCk8L3N0cm9uZz48YnIgLz4KTiA9IDEsMTM0"><span class='gt_from_md'><strong>Article (combined)</strong><br />
N = 1,134</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_2"><span data-qmd-base64="PHN0cm9uZz5Cb29rPC9zdHJvbmc+PGJyIC8+Ck4gPSA1NQ=="><span class='gt_from_md'><strong>Book</strong><br />
N = 55</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="stat_3"><span data-qmd-base64="PHN0cm9uZz5Cb29rL1RoZXNpczwvc3Ryb25nPjxiciAvPgpOID0gMg=="><span class='gt_from_md'><strong>Book/Thesis</strong><br />
N = 2</span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span></th>
      <th class="gt_col_heading gt_columns_bottom_border gt_center" rowspan="1" colspan="1" scope="col" id="p.value"><span data-qmd-base64="PHN0cm9uZz5wLXZhbHVlPC9zdHJvbmc+"><span class='gt_from_md'><strong>p-value</strong></span></span><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span></th>
    </tr>
  </thead>
  <tbody class="gt_table_body">
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Includes lessons</td>
<td headers="stat_1" class="gt_row gt_center">166 (15%)</td>
<td headers="stat_2" class="gt_row gt_center">26 (47%)</td>
<td headers="stat_3" class="gt_row gt_center">2 (100%)</td>
<td headers="p.value" class="gt_row gt_center"><0.001</td></tr>
    <tr><td headers="label" class="gt_row gt_left" style="font-weight: bold;">Uses AGW</td>
<td headers="stat_1" class="gt_row gt_center">617 (54%)</td>
<td headers="stat_2" class="gt_row gt_center">39 (71%)</td>
<td headers="stat_3" class="gt_row gt_center">2 (100%)</td>
<td headers="p.value" class="gt_row gt_center">0.015</td></tr>
  </tbody>
  
  <tfoot class="gt_footnotes">
    <tr>
      <td class="gt_footnote" colspan="5"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>1</sup></span> <span data-qmd-base64="biAoJSk="><span class='gt_from_md'>n (%)</span></span></td>
    </tr>
    <tr>
      <td class="gt_footnote" colspan="5"><span class="gt_footnote_marks" style="white-space:nowrap;font-style:italic;font-weight:normal;line-height:0;"><sup>2</sup></span> <span data-qmd-base64="RmlzaGVy4oCZcyBFeGFjdCBUZXN0IGZvciBDb3VudCBEYXRhIHdpdGggc2ltdWxhdGVkIHAtdmFsdWUKKGJhc2VkIG9uIDIwMDAgcmVwbGljYXRlcyk="><span class='gt_from_md'>Fisher’s Exact Test for Count Data with simulated p-value
(based on 2000 replicates)</span></span></td>
    </tr>
  </tfoot>
</table>
</div>
```


:::
:::
