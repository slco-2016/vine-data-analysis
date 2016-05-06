# VINE Data Layouts

### Case Record:
| CA        | Case record |
| --------- |-------------|
| locn_code		|	Court’s 4-character location code |
| court_type		|	court type (D = district, J = justice) |
| party_num		|	court assigned internal party number |
| case_num		|	court assigned 9-digit case number |
| first_name		|	defendant first name |
| last_name		|	defendant last name |
| disp_date		|	case disposition date |
| disp_code		|	case disposition code |
| bail_amt		|	bail amount set on the case |
| blank field		|	-- may eventually send the defendants SSN |
| birth_date		|	defendant’s birth date |
| race_code		|	race code of the defendant |
| gender		|		gender of the defendant |
| disposition | descry	description of the case disposition code |
| booking_num	|	booking number of the defendant. |


### Court Event Record:
| CE        | indicates Court Event Record |
| --------- |-------------|
| locn_code		| court’s 4-character location code |
| court_type		| court type (D = district, J = justice) |
| party_num		| court assigned internal party number |
| case_num		| court assigned 9-digit case number |
| first_name		| defendant first name |
| last_name		| defendant last name |
| appear_date		| scheduled appearance date |
| time			| scheduled appearance time |
| hearing_code		code for the type of hearing |
| room			| courtroom |
| int_case_num	|	courts internal case number |
| create_datetime	| datetime the event was scheduled |
| cancel_datetime	| datetime the event was cancelled (if not null) |
| cancel_reason		| reason for cancellation |


### Charge Record:
| CH			| indicates Charge Record |
| --------- |-------------|
| locn_code	|	court’s 4-character location code |
| court_type |		court type (D = district, J = justice) |
| party_num	|	court assigned internal party number |
| case_num	|	court assigned 9-digit case number |
| viol_code	|	statute code for the violation |
| severity	|	severity of the violation (F1, MA, etc.) |
| seq			| charge sequence on the case |
| amt_due	|	total fine amount due on the case |
| jdmt_code	|	disposition of the charge |
| case_type	|	case type |
| offense descr	|	description of the charge |
| viol_datetime	|	datetime of violation  (only the date should be considered good) |
| arrest_date	|	arrest date |
| jdmt_date	|	date of disposition of the charge |
| judgment descr |	description of the disposition of the charge |


### Calendar Delete Record:
| DE			| indicates a Calendar Delete record (in case clerks delete, rather than just cancel an event)  |
| --------- |-------------|
| locn_code |		court’s 4-character location code |
| court_type |		court type (D = district, J = justice) |
| case_num |		court assigned 9-digit case number |
| appear_date |		appearance date of the event to be deleted |
| hearing_code |		hearing code of the event to be deleted. |

### Judge Record:
| JU		|	indicates a judge record.  (These are NOT sent to Appriss!!!) |
| --------- |-------------|
| locn_code | 		court’s 4-character location code |
| court_type | 		court type (D) |
| party_num | 		court assigned internal party number |
| case_num | 		court assigned 9-digit case number |
| appear_date | 		scheduled appearance date |
| time | 			scheduled appearance time |
| hearing_code | 		code for the type of hearing |
| create_datetime | 	datetime the event was scheduled |
| judge_id | 		court assigned internal judge id |
| first_name | 		judge first name |
| last_name | 		judge last name |

