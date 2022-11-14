# 🖇 How an unmuted family is stored in the data

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption><p>Stored data view</p></figcaption></figure>



* An unmuted family does not have a “muted” property present in its CouchDB document
*   When the action of unmuting a family is processed:

    ○  all family members are also unmuted (including removing the “muted” property in the CouchDB docs and adding a “muting\_history” entry in their Sentinel info doc)

    ○  all registrations about the family or any family members are updated, changing the state of all present or future “muted” SMS schedules to “scheduled”

    ○  schedules that are past their due date retain the “muted” state

