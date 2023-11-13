# vpos-logger
vpos-logger

# How to test
1. import scripts logger.vsp and logger_pasteInYourCode.vsp
2. add Script links to the entry points 1-5 from logger_pasteInYourCode.vsp
3. add Script links to buttons and run tests
   * for offline tests check the log files created in Script Directory
   * for online tests check papertrail.com with credentials supplied by me or change URL_PAPERTRAIL to a Papertrail log destiantion url from your account (go to https://papertrailapp.com/account/destinations, Create log destination, check TCP "Plain text" and click Create

# How to use logger in you own script
1. import logger.vsp and set Autostart to 1
2. copy/paste in your script.vsp the following code from logger_pasteInYourCode.vsp:
   * section 1. GLOBAL DEFAULTS should be added to your script.vsp and when needed in script.ini section [LOGS]
   * section 2. LOGGER DEFINITION, should be added to script.vsp
   * section 3. INITIALIZATION PROCEDURE, shoud be added in your function (eg. readINI() ) that reads the script.ini settings, this will initializaze the logger object with the desired LOG_LEVEL.
3. after the initilization procedure you can call log.info("some log") log.warn("some log") log.debug("some log") log.trace("some log") anywhere in your code.
