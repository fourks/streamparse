API
===


Tuples
------

.. autoclass:: streamparse.Tuple

You should never have to instantiate an instance of a
:class:`streamparse.Tuple` yourself as streamparse handles this for you
prior to, for example, a :class:`streamparse.Bolt`'s ``process()`` method
being called.

None of the emit methods for bolts or spouts require that you pass a
:class:`streamparse.Tuple` instance.


Components
----------

Both :class:`streamparse.Bolt` and :class:`streamparse.Spout` inherit from a
common base-class, :class:`streamparse.storm.component.Component`.  It extends
pystorm's code for handling `Multi-Lang IPC between Storm and Python <https://storm.apache.org/documentation/Multilang-protocol.html>`__
and adds suport for our Python Topology DSL.

Spouts
^^^^^^

Spouts are data sources for topologies, they can read from any data source and
emit tuples into streams.

.. autoclass:: streamparse.Spout
    :inherited-members:
    :show-inheritance:

Bolts
^^^^^

.. autoclass:: streamparse.Bolt
    :inherited-members:
    :show-inheritance:


.. autoclass:: streamparse.BatchingBolt
    :inherited-members:
    :show-inheritance:


Logging
-------

.. autoclass:: streamparse.StormHandler
    :inherited-members:
