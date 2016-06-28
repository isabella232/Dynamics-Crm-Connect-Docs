Start a Pipeline Batch Manually
=================================

Data synchronization is controlled using items called *pipeline batches*.
A pipeline batches can be started in a number of ways. The easiest way is to
start the pipeline batches manually.

.. tip::
  Be aware of the data in your CRM. If you run the synchronization
  process against a CRM with a large number of contacts, the
  synchronization process may take a long time to complete.

  If you are only interested in testing to confirm the synchronization
  process is working, consider setting a limit on the number of
  contacts that will be handled.

1.	In Content Editor, navigate to your *tenant*.
2.	Navigate to **Pipeline Batches > CRM Contacts to xDB Sync Pipeline Batch**.
3.	Click the button **Run Pipeline Batch**.

    .. image:: _static/run-pipeline-batch.png

4.	A message will appear to indicate the pipeline batches started.

    .. image:: _static/pipeline-batch-started.png
