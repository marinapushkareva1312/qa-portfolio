# Test Cases: Login Form — demoblaze.com

**Tester:** Marina Pushkareva  
**Date:** 2026-05-31  
**Application:** STORE (demoblaze.com)  
**Feature:** Log in modal window  
**Environment:** Browser (Firefox/Chrome), Desktop

-----

## Scope

Testing the Log in modal window that appears after clicking the **Log in** button in the navigation bar.

**Elements under test:**

- Username field
- Password field
- Log in button
- Close button (×)
- Close button (text)

-----

## Test Cases

|TC ID|Title                                  |Preconditions      |Steps                                                                                                               |Expected Result                                                                   |Status|
|-----|---------------------------------------|-------------------|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|------|
|TC-01|Successful login with valid credentials|User is registered |1. Click Log in in nav bar<br>2. Enter valid username<br>3. Enter valid password<br>4. Click Log in                 |User is logged in, modal closes, username appears in nav bar                      |-     |
|TC-02|Login with incorrect password          |User is registered |1. Open Log in modal<br>2. Enter valid username<br>3. Enter wrong password<br>4. Click Log in                       |Error message is displayed, user stays on login modal                             |-     |
|TC-03|Login with non-existent username       |—                  |1. Open Log in modal<br>2. Enter username that does not exist<br>3. Enter any password<br>4. Click Log in           |Error message is displayed                                                        |-     |
|TC-04|Login with empty Username field        |—                  |1. Open Log in modal<br>2. Leave Username empty<br>3. Enter any password<br>4. Click Log in                         |Error message or validation warning is displayed                                  |-     |
|TC-05|Login with empty Password field        |—                  |1. Open Log in modal<br>2. Enter valid username<br>3. Leave Password empty<br>4. Click Log in                       |Error message or validation warning is displayed                                  |-     |
|TC-06|Login with both fields empty           |—                  |1. Open Log in modal<br>2. Leave both fields empty<br>3. Click Log in                                               |Error message or validation warning is displayed                                  |-     |
|TC-07|Close modal with × button              |Modal is open      |1. Open Log in modal<br>2. Click × in top right corner                                                              |Modal closes, user stays on the page                                              |-     |
|TC-08|Close modal with Close button          |Modal is open      |1. Open Log in modal<br>2. Click Close button                                                                       |Modal closes, user stays on the page                                              |-     |
|TC-09|Login with spaces in Username          |—                  |1. Open Log in modal<br>2. Enter username with leading/trailing spaces<br>3. Enter valid password<br>4. Click Log in|App handles spaces correctly (trims or shows error)                               |-     |
|TC-10|Username field — max length input      |—                  |1. Open Log in modal<br>2. Paste very long string (200+ characters) into Username<br>3. Click Log in                |App handles long input without crashing                                           |-     |
|TC-11|Password field input is masked         |—                  |1. Open Log in modal<br>2. Type any characters into Password field                                                  |Password characters are hidden (shown as ••••)                                    |-     |
|TC-12|Modal opens correctly                  |User is on any page|1. Click Log in in the nav bar                                                                                      |Log in modal appears with Username field, Password field, Close and Log in buttons|-     |

-----

## Notes

- TC-01 requires a pre-registered test account
- Status column: Pass / Fail / Blocked — to be filled during test execution
- Priority: TC-01, TC-02, TC-04, TC-05, TC-06 are high priority (core functionality)