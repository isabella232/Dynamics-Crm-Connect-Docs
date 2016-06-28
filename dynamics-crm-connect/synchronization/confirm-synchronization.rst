Confirm Data was Synchronized
===============================

After the *pipeline batch* finishes, there are several ways you can confirm the
data was synchronized.

Option 1
    The pipeline batch item has a section **Summary**. In this section
    there is a field **Last run completed**. If this field is ticked,
    the pipeline batch finished without any critical errors.

    While this is not a fool-proof method - it is possible that a non-critical
    error occurred that prevented the data from being synchronized - it is a
    good first option to use.

Options 2
    Check the Contacts collection in MongoDB. You will find the active contacts
    from the CRM in the collection.

    .. image:: _static/contacts-collection.png

Option 3
    Open *Experience Profile*. You will find the active contacts from the CRM
    in Experience Profile.

    .. image:: _static/experience-profile.png
