Create Visual Studio Project
===================================================
In order to store custom data on a contact, a contact facet is needed.
Contact facets are implemented in code. A Visual Studio project is 
needed before you can implement the custom contact facet.

1. In Visual Studio, create the following project:

+---------------------------+-------------------------------------------------+
| Project type              | Class Library (.NET Framework)                  |
+---------------------------+-------------------------------------------------+
| .NET version              | .NET Framework 4.6.2                            |
+---------------------------+-------------------------------------------------+
| Project name              | ``Examples.Connect.Dynamics``                   |
+---------------------------+-------------------------------------------------+

2. Add references to the following NuGet packages:

    * ``Sitecore.DataExchange.Tools.DynamicsConnect.NoReferences``
    * ``Sitecore.XConnect.NoReferences``

.. |link-for-nuget-feed| raw:: html

   <a href="https://sitecore.myget.org/gallery/sc-packages" target="_blank">https://sitecore.myget.org/gallery/sc-packages</a>

.. note::

    Sitecore's public NuGet feed is available at |link-for-nuget-feed|.