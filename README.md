# s34synk
Got bored, wanted to add Sunsynk integration to my HA with no real options useful options out there without doing modbus crap, so I decided to use the Official Sunsynk API. No Extra Peripherals, No Wiring, No faffing around, just str8 api yo

V1 Release:
- Current Read Only API
- Latest OAuth Handling as per SS API
- Fixed SSL Cert Handling (due to SS intermediate ssl missing.. oh boy)
- Retrieves Invertor List for Selection after Configuration
- Dumps all Invertor Values to log files (DEBUG)

V2 Planned Release:
- Waiting for the bloody POST api back from support.
- Post some mothafuckin values back and BOSH JOB DONE!


Configuration:
-Install Plugin
-Set Email
-Set Password
-Set Poll Interval to 60
-Press OK
-Next screen should autofetch a list where you can select your inverter.
-First Log Run will output all read only settings, which is used later on for writing back to the API.

Add this to the end of your Home Assistant Configuration.yaml:
logger:
  default: warning
  logs:
    s34synk: debug
