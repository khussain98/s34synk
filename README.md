Got bored, wanted to add Sunsynk integration to my HA with no real options useful options out there without doing modbus crap, so I decided to use the Official Sunsynk API. No Extra Peripherals, No Wiring, No faffing around, just str8 api yo

V1 Release:
- Current Read Only API
- Latest OAuth Handling as per SS API
- Fixed SSL Cert Handling (due to SS intermediate ssl missing.. lazy)
- Retrieves Plant Overview Details
- Retrieves Inverter S/N and Other Settings

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
<img width="742" height="195" alt="image" src="https://github.com/user-attachments/assets/199d9c16-eedc-4224-b3c6-0c985f948d65" />


Add this to the end of your Home Assistant Configuration.yaml:
logger:
  default: warning
  logs:
    s34synk: debug


