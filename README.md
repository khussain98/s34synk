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
 - Install Plugin
 - Set Email
 - Set Password
 - Set Poll Interval to 60
 - Set Inverter S/N (OPTIONAL - YOU CAN AUTO-RETRIEVE OTHERWISE ON NEXT SCREEN)
 - Press OK
 - Next screen should autofetch a list where you can select your inverter.

A successful setup should indicate in logs:
- 2026-01-20 19:01:45.962 INFO (MainThread) [s34synk] S34Synk | Authenticating via signed OpenAPI (JSON Mode)
- 2026-01-20 19:01:47.933 INFO (MainThread) [s34synk] S34Synk | OpenAPI authentication SUCCESS
- 2026-01-20 19:01:47.934 INFO (MainThread) [s34synk] S34Synk | Discovering plant metadata
- 2026-01-20 19:01:48.363 INFO (MainThread) [s34synk] Plant Found: PLANT ABC (ID: XXXXX)
- 2026-01-20 19:01:48.784 INFO (MainThread) [s34synk] Inverter: SN=XXXXXX26, Power=0W

Add this to the end of your Home Assistant Configuration.yaml:
logger:
  default: warning
  logs:
    s34synk: debug


