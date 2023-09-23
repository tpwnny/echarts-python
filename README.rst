
-----------

.. code-block:: python

    from echarts import Echart, Legend, Bar, Axis

    chart = Echart('GDP', 'This is a fake chart')
    chart.use(Bar('China', [2, 3, 4, 5]))
    chart.use(Legend(['GDP']))
    chart.use(Axis('category', 'bottom', data=['Nov', 'Dec', 'Jan', 'Feb']))

The `chart.json` property will be

.. code-block:: javascript

    {
        "title": {
            "text": "GDP",
            "subtext": "This is a fake chart"
        },
        "series": [
            {
                "type": "bar",
                "data": [
                    2,
                    3,
                    4,
                    5
                ],
                "name": "China"
            }
        ],
        "legend": {
            "y": "top",
            "x": "center",
            "data": [
                "GDP"
            ],
            "orient": "horizontal"
        },
        "xAxis": [
            {
                "position": "bottom",
                "data": [
                    "Nov",
                    "Dec",
                    "Jan",
                    "Feb"
                ],
                "type": "category"
            }
        ],
        "yAxis": {}
    }

on Mac OSX, you also can execute ::

    chart.plot()

and invoke a browser to display the chart.


Contribution
------------

This package authored by Hsiaoming Yang <me@lepture.com> in 2014.

If you have any question or want to improve this repository, welcome to create
an `issue <https://github.com/yufeiminds/echarts-python/issues>`__
or `pull requests <https://github.com/yufeiminds/echarts-python/pulls>`__ .

This repo is maintained by Yufei Li <yufeiminds@gmail.com> now,
you can also send a email to me.
