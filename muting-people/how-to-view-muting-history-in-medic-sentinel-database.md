# 👓 How to view muting history in medic-sentinel database

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption><p>Database view</p></figcaption></figure>





* Every time the muted state of a contact (person, family, etc) is updated, an entry is added to their “muting\_history”
* “muting\_history” can be found in the info-docs saved inmedic-sentinel database
*   Each entry includes the following information:

    ○  a Boolean “muted” property, describing the new state

    ○  an ISO formatted “date” describing when the action was processed

    ○  a “report\_id” property which contains the “\_id” of the report that triggered the action

![page23image9326528](blob:https://app.gitbook.com/53b400d0-be83-4fef-a28a-214380133a7c)



report that triggered the action

![page23image9326528](blob:https://app.gitbook.com/ad7eee45-4afe-4b02-9720-953621516b9e)
