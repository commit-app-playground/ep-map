# EP Map

#### A simple visualization of all EPs and SPs locations on the map.




Initial notes, scope and architecture proposal:

# Scope
- A map for the EP locations with their profile picture from LinkedIn profile
- Access/Security with a list of emails
- DB will be updated with manual execution of scripts

# Use cases
- Login with a textbox to capture the email, 
  (V2: a token will be send to the email if the email is present on the allowed access list)
- Map with all the EP listed - no filters

# Routes
  - login - Routes to request and validate a login token to setup a session cookie
  - list - list of EP with location details and profile picture

# Architecture
- React with App Playground
- Backend GO(Node typescript) REST routes with App Playground
- Postgres DB with spatial extension

# Utils
- Script to parse and insert the gsheet CSV into the database
- Script to generate the database location from a province, contry pair and update the database
- Script to get information from the EP LinkedIn profile
