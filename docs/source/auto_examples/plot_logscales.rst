.. note::
    :class: sphx-glr-download-link-note

    Click :ref:`here <sphx_glr_download_auto_examples_plot_logscales.py>` to download the full example code
.. rst-class:: sphx-glr-example-title

.. _sphx_glr_auto_examples_plot_logscales.py:


Log scales
==========

Brokenaxe compute automatically the correct layout for a 1:1 scale. However, for
logarithmic scales, the 1:1 scale has to be adapted. This is done via the
`yscale` or `xscale` arguments.




.. image:: /auto_examples/images/sphx_glr_plot_logscales_001.png
    :class: sphx-glr-single-img





.. code-block:: default



    import matplotlib.pyplot as plt
    from brokenaxes import brokenaxes
    import numpy as np

    fig = plt.figure(figsize=(5,5))
    bax = brokenaxes(xlims=((1, 500), (600, 10000)),
    	     ylims=((1, 500), (600, 10000)),
    		 hspace=.15, xscale='log', yscale='log')

    x = np.logspace(0.0, 4, 100)
    bax.loglog(x, x, label='$y=x=10^{0}$ to $10^{4}$')

    bax.legend(loc='best')
    bax.grid(axis='both', which='major', ls='-')
    bax.grid(axis='both', which='minor', ls='--', alpha=0.4)
    bax.set_xlabel('x')
    bax.set_ylabel('y')
    plt.show()


.. rst-class:: sphx-glr-timing

   **Total running time of the script:** ( 1 minutes  8.214 seconds)


.. _sphx_glr_download_auto_examples_plot_logscales.py:


.. only :: html

 .. container:: sphx-glr-footer
    :class: sphx-glr-footer-example



  .. container:: sphx-glr-download

     :download:`Download Python source code: plot_logscales.py <plot_logscales.py>`



  .. container:: sphx-glr-download

     :download:`Download Jupyter notebook: plot_logscales.ipynb <plot_logscales.ipynb>`


.. only:: html

 .. rst-class:: sphx-glr-signature

    `Gallery generated by Sphinx-Gallery <https://sphinx-gallery.readthedocs.io>`_
