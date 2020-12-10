# Ticket

| Name | Type | Description | Default |
| :--- | :--- | :--- | :--- |
| **ticket\_id** | int |  |  |
| status | int | Beschreibt den Staus eines Tickets, z.B. `0` für neu eingereicht, `1` für in bearbeitung, `2` für erledigt | 0 |
| **kategorie** | Kategorie |  |  |
| **beschreibung** | String |  |  |
| **raum** | int |  |  |
| **gebaeude** | char |  |  |
| **autor** | User | Die user id von der Person, die das Ticket eingereicht hatte |  |
| berbeiter | User | Die ID des Bearbeiters |  |
| datum\_eingereicht | timestamp | Das Datum von der Einreichung eines Tickets |  |
| datum\_fertigstellung | timestamp | Das Datum von wann ein Ticket erledigt wurde |  |
| datum\_berabeitung | timestamp | Das Datum von der letzten Bearbeitung |  |
| prioritaet | int | Die Prioriät eines Ticket, auf einer Skala von 0 bis 10 | 0 |

