==========
pyFxTrader
==========

.. image:: https://travis-ci.org/jmelett/pyFxTrader.svg
    :target: https://travis-ci.org/jmelett/pyFxTrader

.. image:: https://img.shields.io/github/license/mashape/apistatus.svg
    :target: https://github.com/jmelett/pyFxTrader/blob/master/LICENSE


Scope
=====

* The goal is to provide a backtesting and live trading tool, which can run
  multiple strategies on up to 10 currency pairs.
* Strategies can monitor up to three timeframes (e.g. H1, H2 and D1) and 
  calculate buy/sell actions based on them.


Strategy
========

Indicators
----------

Besides building your own, you can also use a wide range of indicators via `TA-Lib` or `numpy`.


Timeframes
----------

* OANDA supports most commonly used timeframes. You can find all supported values here_.
.. _here: http://developer.oanda.com/rest-live/rates/#retrieveInstrumentHistory.


TODO
====

* Add Matplot/Plot.ly support. See also following tutorial_.
.. _tutorial: http://www.randalolson.com/2014/06/28/how-to-make-beautiful-data-visualizations-in-python-with-matplotlib/.
* Implement proxy class for backtesting, which will first check if data is 
  available locally and only then fetch/save via API.
* Implement usage of ETags to reduce traffic/latency.
* Prepare Makefile.


Installation
============

::

    git clone git@github.com:jmelett/pyFxTrader.git
    cd pyFxTrader
    virtualenv env
    source env/bin/activate
    pip install -e .
    ./cmd.py -h
