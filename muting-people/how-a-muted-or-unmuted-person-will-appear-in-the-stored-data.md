# 🖇 How a muted or unmuted person will appear in the stored data

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption><p>Appearance in stored data</p></figcaption></figure>



* Muting is persistent. When a person is muted, a “muted” property is stored in its CouchDB document
* The “muted” property contains a date in ISO format which represents the moment the muting action was processed by Sentinel
* When the action of muting a person is processed, allregistrations about that person are updated, changing the state of all “pending” or “scheduled” SMS schedules to “muted”
* When muting an already muted person, the “muted” property is not updated, retaining its initial value, also none of the registrations are updated
* When unmuting, the “muted” property is removed, along with updating all registrations about the person, setting present/future “muted” SMS schedules to a “scheduled” state
