# cli-muj

Cli application for MUj

- gets attendance of all subjects
- marks within the CLI
- upcoming events (updated by clubs) ?
- Class timetable
- during setup set it up like github and be on your way
	ex: 
	- cli-muj setup user.email "student@muj.in"
	- cli-muj setup user.password "password123

## Attendance
```sh
cli-muj attendance
```
- Pulls attendance from MUJ portal (via scraping or available API).
- Output in a simple table format.

```sh
Subject         | Present | Total | Percentage
------------------------------------------------
Maths           | 21      | 24    | 87.5%
Physics         | 19      | 25    | 76%
...
```
## Marks
```sh 
cli-muj marks
```
- Scrapes or pulls recent internal marks from the portal.
- Optional: Notify if marks changed since last sync.

## Timetable
```sh
cli-muj timetable
```
- Shows today's or weekly class schedule.
- Add a ``` --today``` or ```--week flag```

# Security

- Uses C
- Encrypt config: Use AES-256 for password storage (or store in system keyring).
- Add ```cli-muj logout``` to remove saved credentials.
- Plan for a future OAuth/Token-based system for portal access (if MUJ allows).

