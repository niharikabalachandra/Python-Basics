
## Site Search
### Search Volume
* Metric comes from GA directly
* `SUM(ga_event WHERE url CONTAINS('q=') OR url CONTAINS('searchterm='))`

### Search Success Percentage
* `SUM(ga_event WHERE event_label=‘success’) / (SUM(GA events WHERE event_label=‘success’) + SUM(ga_event WHERE event_label=‘failure’))`
* Under which conditions are `event_label=‘success’` and `event_label=‘failure'`?
    * `...`
    * `...`
    * `...`

## Site Doctor Search
### Doctor Search Volume
* `SUM(ga_event WHERE event_category=‘Doctor Search’)`
* Under which conditions is `event_category='Doctor Search'`?
    * `WHEN url CONTAINS(find-a-doctor/?searchterm)`
    * `WHEN url CONTAINS(/doctors-and-departments/physicians/find-a-doctor/)`
    * `WHEN url path EQUALS(/doctors-and-departments/physicians/find-a-doctor/)`
	* `WHEN CHCO Search Page Index EQUALS(1)`
	* `WHEN Site Section CONTAINS(doctor)`
	* `WHEN Page URL CONTAINS(find-a-doctor/?searchterm)`
	* `WHEN CHCO Search Page Index GREATER THAN OR EQUALS(1)`
	

### Doctor Search Success Percentage
* `SUM(ga_event WHERE event_label='Search Success' AND event_category='Doctor Search') / SUM(ga_event WHERE event_category=‘Doctor Search’)`
* Under which conditions is `event_label='Search Success'`?
    * `...`
    * `...`
    * `...`

## Site Condition Search
### Condition Search Volume
* `SUM(ga_event WHERE event_category=‘Condition or Symptom Search’)`
* Under which conditions is `event_category='Condition or Symptom Search'`?
    * `...`
    * `...`
    * `...`

### Condition Search Success Percentage
* `SUM(ga_event WHERE event_label='Search Success' AND event_category='Condition or Symptom Search') / SUM(ga_event WHERE event_category=‘Condition or Symptom Search’)`
* Under which conditions is `event_label='Search Success'`?
    * See above under _Doctor Search Success Percentage_
