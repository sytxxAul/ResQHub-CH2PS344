# ResQHub
(This readme.md is not finished)
## Developers:
1. Raihansyah Arifin (<span style="color:red;">CC</span>|C010BSY3731) - Ex. Machine Learning Cohort, Cloud Computing Cohort
   - ResQHub API Developer
   - GCP Infrastructure Manager
   - Machine Learning advisor
   
2. Mahrunisa Indah Puteri Alia (<span style="color:red;">CC</span>|C486BSX3022) - Cloud Computing Cohort
   - ResQHub API Developer
   - GCP Infrastructure Manager
   
3. Jason Albert Natanael (<span style="color:red;">ML</span>|M010BSY0255) - Machine Learning Cohort
   - Machine Learning Developer
   
4. Marlo Emiliano Muktiono (<span style="color:red;">ML</span>|M010BSY0107) - Machine Learning Cohort
   - Machine Learning Developer
   
5. Alip Maskhuri (<span style="color:red;">ML</span>|M486BSY1368) – Machine Learning Cohort 
   - Machine Learning Developer
   
6. Aula Firdaus Azmi (<span style="color:red;">MD</span>|A486BSY2915) - Mobile Development Cohort
   - Android Mobile Developer
   
7. Indrawan Jefray Delo (<span style="color:red;">MD</span>|A710BSY2587) - Mobile Development Cohort
   - Android Mobile Developer

## What
ResQHub is a human safety application that enables users to invoke SOS calls and requests in a dangerous situation. Featured with diverse functions such as auto-messaging to pre-approved contacts, automatic calls to nearby police stations and/or hospitals, audio transcription, logs, and many more, this application is expected to grant users safety everywhere anytime.

## Features
1. Invoking automatic SOS Calls
   When SOS mode is triggered (<span style="color: red;">Note: Mobile Developer, please propose solution</span>), users will be dialed to the best nearest police station and/or medical station. Pertaining to the invocation, user can disable the automatic SOS calls and instead receive the list of all information of nearby police stations and medical stations such as phone number, rating, rating count, arrival estimation, distance approximation, open-hours, etc.
2. Sending automatic SOS messages to pre-approved contacts
   When SOS mode is triggered, pre-approved contacts will be notified with an SOS message that user has planned to send, followed by the real-time user's location
3. Real-time Location Tracking
   Keep pre-approved contacts notified about user's location.
4. Audio transcription
   Enable user to transcribe their audio to text. This feature can be used to send messages in urgent situation, as an evidence, etc. All audio is stored in the database for 30 days.
5. Face identification
   In the registration page, we feature our application with face identification to match user's face against their face in the national ID card. This feature would prevent unaccountable users. 

## Usage
<span style="color:red;">STILL UNDER DEVELOPMENT</span>
1. (NOT PUBLIC) Request all nearby SOS stations within a certain radius
	```bash
	curl -X POST -d '{
		"lat": "<YOUR-LATITUDE>",
		"long": "<YOUR-LONGITUDE>",
		"station": "<POLICE-or-HOSPITAL>",
		"scope": "<RADIUS>",
		"username": "<USERNAME>",
		"app-key": "<SECRET KEY>"
	}' \
	-H 'Content-Type: application/json' \
	https://resqhub-api1a-[unique]-et.a.run.app/safe-dedicated-user
	```

2. (PUBLIC) Request all nearby SOS stations (2 km radius only, less informative)
	```bash
	curl -X POST -d '{
		"lat": "<YOUR-LATITUDE>",
		"long": "<YOUR-LONGITUDE>",
		"station": "<POLICE-or-HOSPITAL>"
	}' \
	-H 'Content-Type: application/json' \
	https://resqhub-api1a-[unique]-et.a.run.app/safe-dedicated-user
	```

3. (NOT PUBLIC) Verification code generator
   ```bash
	curl -X POST -d '{
		"email": "<USER-INPUT-EMAIL>",
		"app-key": "<SECRET KEY>"
	}' \
	-H 'Content-Type: application/json' \
	https://resqhub-api1b-frontend-[unique]-et.a.run.app/send-verification
	```

4. (NOT PUBLIC) Verification process
   ```bash
	curl -X POST -d '{
		"email": "<USER-INPUT-EMAIL>",
		"code": "<USER-INPUT-CODE>",
		"app-key": "<SECRET KEY>"
	}' \
	-H 'Content-Type: application/json' \
	https://resqhub-api1b-[unique]-et.a.run.app/validify
	```

5. (PUBLIC) Face verification process
    ```bash
	curl -X POST -F face1=@<FACE1-IMG-URL> -F face2=@<FACE2-IMG-URL> \
	https://resqhub-api3-[unique]-et.a.run.app/verify
	```

6. (PUBLIC) Audio transcription
    ```bash
	curl -X POST -F wavFile=@<AUDIO-FILE-WAV>\
	https://resqhub-api2-[unique]-et.a.run.app/transcribe
	```
