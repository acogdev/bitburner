hackAnalyzeThreads() Netscript Function
=======================================

.. js:function:: hackAnalyzeThreads(hostname/ip, hackAmount)

    :param string hostname/ip: IP or hostname of server to analyze
    :param number hackAmount: Amount of money you want to hack from the server
    :returns: The number of threads needed to hack() the server for *hackAmount* money
    :RAM cost: 1 GB

    This function returns the number of script threads you need when running
    the `hack()` command to steal the specified amount of money from the target server.

    If `hackAmount` is less than zero or greater than the amount of money available
    on the server, then this function returns -1.

    For example, let's say the `foodnstuff` server has $10m and you run::

        hackAnalyzeThreads("foodnstuff", 1e6);

    If this function returns 50, this means that if your next `hack()` call
    is run on a script with 50 threads, it will steal $1m from the `foodnstuff` server.

    **Warning**: The value returned by this function isn't necessarily a whole number.
