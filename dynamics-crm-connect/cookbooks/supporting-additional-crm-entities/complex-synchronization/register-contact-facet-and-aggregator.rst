.. _register-contact-facet-and-aggregator:

Register Contact Facet & Aggregator
======================================

You must change the configuration in Sitecore to use the new contact 
facet model and contact aggregator. This configuration will also 
ensure the new value on the contact facet is indexed properly.

1.	Add the following file:

    +--------------+---------------------------------------+
    | Path         | **App_Config\Include\DynamicsCrm**    |
    +--------------+---------------------------------------+
    | File name    | **xExamples.DynamicsCrm.config**      |
    +--------------+---------------------------------------+

    .. note:: 
        Config file are processed in alphabetical order. The file name 
        starts with "x" in order to ensure it is processed after the 
        file **Sitecore.Analytics.DynamicsCrm.config**.

    .. note:: 
        The configuration included in these instructions is for the Lucene
        search engine. If you are using Solr you must change the node 
        **/configuration/sitecore/contentSearch/configuration**.

2.	Add the following configuration to the file. This will replace the default contact facet model with the new, extended model, and the default contact aggregator with the new, extended aggregator:

.. code-block:: xml

  <configuration xmlns:patch="http://www.sitecore.net/xmlconfig/">
    <sitecore>
      <model>
        <elements>
          <element interface="Sitecore.Analytics.DynamicsCrm.Models.ICrmContactData, Sitecore.Analytics.DynamicsCrm" implementation="Sitecore.Analytics.DynamicsCrm.Models.CrmContactData, Sitecore.Analytics.DynamicsCrm">
            <patch:attribute name="interface">Examples.DynamicsCrm.Models.ICrmContactDataEx, Examples.DynamicsCrm</patch:attribute>
            <patch:attribute name="implementation">Examples.DynamicsCrm.Models.CrmContactDataEx, Examples.DynamicsCrm</patch:attribute>
          </element>
        </elements>
        <entities>
          <contact>
            <facets>
              <facet name="DynamicsCrm" contract="Sitecore.Analytics.DynamicsCrm.Models.ICrmContactData, Sitecore.Analytics.DynamicsCrm">
                <patch:attribute name="contract">Examples.DynamicsCrm.Models.ICrmContactDataEx, Examples.DynamicsCrm</patch:attribute>
              </facet>
            </facets>
          </contact>
        </entities>
      </model>
      <pipelines>
        <group groupName="analytics.aggregation">
          <pipelines>
            <contacts>
              <processor type="Sitecore.Analytics.DynamicsCrm.Aggregators.ContactChangeContactAggregatorEx, Sitecore.Analytics.DynamicsCrm">
                <patch:attribute name="type">Examples.DynamicsCrm.Aggregators.ContactChangeContactAggregatorEx2, Examples.DynamicsCrm</patch:attribute>
              </processor>
            </contacts>
          </pipelines>
        </group>
      </pipelines>
      <contentSearch>
        <configuration type="Sitecore.ContentSearch.ContentSearchConfiguration, Sitecore.ContentSearch">
          <indexes hint="list:AddIndex">
            <index id="sitecore_analytics_index" type="Sitecore.ContentSearch.LuceneProvider.LuceneIndex, Sitecore.ContentSearch.LuceneProvider">
              <param desc="name">$(id)</param>
              <param desc="folder">$(id)</param>
              <param desc="propertyStore" ref="contentSearch/indexConfigurations/databasePropertyStore" param1="$(id)" />
              <configuration ref="contentSearch/indexConfigurations/defaultLuceneIndexConfiguration">
                <fieldMap ref="contentSearch/indexConfigurations/defaultLuceneIndexConfiguration/fieldMap">
                  <fieldNames hint="raw:AddFieldByFieldName">
                    <field fieldName="crm.account" storageType="YES" indexType="TOKENIZED" vectorType="NO" boost="1f" type="System.Guid" settingType="Sitecore.ContentSearch.LuceneProvider.LuceneSearchFieldConfiguration, Sitecore.ContentSearch.LuceneProvider">
                      <analyzer type="Sitecore.ContentSearch.LuceneProvider.Analyzers.LowerCaseKeywordAnalyzer, Sitecore.ContentSearch.LuceneProvider"/>
                    </field>
                  </fieldNames>
                </fieldMap>
              </configuration>
            </index>
          </indexes>
        </configuration>
      </contentSearch>
    </sitecore>
  </configuration>
