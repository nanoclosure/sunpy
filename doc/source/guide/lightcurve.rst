===========
Lightcurves
===========

Time series data are a fundamental part of many data analysis projects as much in 
heliophysics as other areas. SunPy therefore provides a lightcurve object to deal 
with this data type. Thankfully most of the heavy lifting in this area has already been
done for us. The lightcurve object makes use of the `pandas <http://pandas.pydata.org/`_
python module. Pandas is a high-quality and optimized module which is in use in a wide 
variety of academic and commercial fields, including Finance, Neuroscience, Economics, 
Statistics, Advertising, and Web Analytics. The lightcurve object is essentially a wrapper
around a pandas dataframe object which holds some of the meta-data from the original 
data source. In this tutorial we provide a quick introduction to 
the lightcurve object and pandas. We highly recommend any user of the lightcurve object 
take a look at the great `pandas documentation <http://pandas.pydata.org/pandas-docs/stable/`_.
for more information.

============
Data Support
============

The lightcurve object currently supports the following data sources

- SDO/EVE
- GOES XRS
- PROBA3/LYRA

1. Creating a Lightcurve
------------------------
