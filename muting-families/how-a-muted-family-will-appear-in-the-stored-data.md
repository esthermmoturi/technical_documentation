# 📎 How a muted family will appear in the stored data

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption><p>How muting appears in the stored data</p></figcaption></figure>



* Muting is persistent. When a family is muted, a “muted” property is stored in its CouchDB document
* The “muted” property contains a date in ISO format which represents the moment the muting action was processed by Sentinel
*   When the action of muting a family is processed:

    &#x20; ○  all family members are also muted (including

    saving the “muted” property in their CouchDB docs and adding a “muting\_history” entry in their Sentinel info doc)

    &#x20; ○  all registrations about the family or any family members are updated, changing the state of all “pending” or “scheduled” SMS schedules to “muted”
* When muting an already muted family, the “muted” property is not updated, retaining its initial value (this also applies to already muted family members and registrations about already muted family members)
