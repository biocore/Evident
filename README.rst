E-vident: elucidating sampling effort for microbial analysis studies
====================================================================

|Build Status| |Coverage Status|

A critical consideration in any clinical study is power analysis, yet it has
been difficult to perform such analyses for microbiome studies because the effect
sizes of different disorders are unknown. Fortunately, several larger cohort studies,
including but not limited to the Human Microbiome Project, now allow us to identify
effect sizes for differences among ages and populations, and differences associated
with obesity, IBD, and other disorders.

The original Evident demo was a web-based software tool that can be found `here <https://github.com/biocore/Evident-initial-demo>`__.

Evident is comprised of the following steps:

1. clean your metadata file to only contain categorical metadata columns that are
   not derived from other columns, for example: barcode with sample name or any
   numeric column should be binned
2. find your alpha and beta diversity calculation files, in classic qiime 1
   format, based on which one you want to estimate the effect size
3. run `evident effect-size` using your clean metadata file and your alpha and
   beta files; note that you need to define which none values the effect size
   should ignore (via `--na_values`) e.g. 'NA', ' ', 'None', 'Not Applicable'
4. run the effect size summaries `evident summarize`

.. |Build Status| image:: https://travis-ci.org/biocore/evident.svg
   :target: https://travis-ci.org/biocore/evident
.. |Coverage Status| image:: https://coveralls.io/repos/biocore/evident/badge.svg
   :target: https://coveralls.io/r/biocore/evident
