================
pattern_analysis
================


.. image:: https://img.shields.io/pypi/v/pattern_analysis.svg
        :target: https://pypi.python.org/pypi/pattern_analysis

.. image:: https://img.shields.io/travis/ScienceComputing/pattern_analysis.svg
        :target: https://travis-ci.com/ScienceComputing/pattern_analysis

.. image:: https://readthedocs.org/projects/pattern-analysis/badge/?version=latest
        :target: https://pattern-analysis.readthedocs.io/en/latest/?version=latest
        :alt: Documentation Status



A package for analyzing patterns in biological data.


* Free software: MIT license
* Python Package Index: https://pypi.org/project/pattern-analysis/
* Documentation: https://pattern-analysis.readthedocs.io.


Features
--------

* Count patterns of nucleotide interest in a genome sequence
* Generate the complement for a genome sequence

Usage
--------
.. code-block:: python

    pip install pattern-analysis

    from pattern_analysis import pattern_analysis

    # Estimate the number of patterns equal to "TGATCA" in the ori sequence
    ori = "ATCAATGATCAACGTAAGCTTCTAAGCATGATCAAGGTGCTCACACAGTTTATCCACAACCTGAGTGGATGACATCAAGATAGGTCGTTGTATCTCCTTCCTCTCGTACTCTCATGACCACGGAAAGATGATCAAGAGAGGATGATTTCTTGGCCATATCGCAATGAATACTTGTGACTTGTGCTTCCAATTGACATCTTCAGCGCCATATTGCGCTGGCCAAGGTGACGGAGCGGGATTACGAAAGCATGATCATGGCTGTTGTTCTGTTTATCTTGTTTTGACTGAGACTTGTTAGGATAGACGGTTTTTCATCACTGACTAGCCAAAGCCTTACTCTGCCTGACATCGACCGTAAATTGATAATGAATTTACATGCTTCCGCGACGATTTACCTCTTGATCATCGATCCGATTGAAGATCTTCAATTGTTAATTCTCTTGCCTCGACTCATAGCCATGATGAGCTCTTGATCATGTTTCCTTAACCCTCTATTTTTTACGGAAGAATGATCAAGCTGCTGCTCTTGATCATCGTTTC"

    pat = "TGATCA"
    res = pattern_analysis.pattern_count(ori, pat)

    print("A total of {} {} are found.".format(res, pat)) # Return "A total of 8 TGATCA are found."


Credits
-------

This package was created with Cookiecutter_ and the `audreyr/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`audreyr/cookiecutter-pypackage`: https://github.com/audreyr/cookiecutter-pypackage
