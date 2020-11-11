# weekly-schedule-manager

A web app to manage weekly work schedules for a group of users managed by a team of managers.
All users must be registered via email, and at least one of whom is defined as a manager.

How does it work?

Setup:
After registration, a user can create schedules. Each user owns the schedules they create.
A schedule owner must define the following parameters:
  * Start of Week (SOW): A number between [0 - 1] ([Sunday - Monday])
  * A work week: for each work day, zero or more shifts may be defined
  * A shift is defined by its start and end times
  * The times the shift request form is published and closed each week

This app supports/contains the following features:
  
  *  Two types of roles; Manager and User
  
    * Users can:
      * Submit their shift requests to be reviewed a manager(s)
      * Submit swap requests after the shift request form is closed

      Version 2 and above:
      * Send emails to other users
      * Chat with other users
      * Upload a profile picture
      * Edit their display name

    * Managers can, in addition to the User capabilities listed above (A manager's request is auto-approved):
      * Add / Remove users
      * Grant / Revoke Manager status
      * Define work shifts
      * Limit the number of users per shift
      * Define when the shift request form is published each week
      * Define the duration of time until the published form closes
      * Add a user to a shift
      * Remove a user from a shift
      * Accept / Refuse shift swaps
      * Approve / Deny day offs
      * Cancel a shift
        * Version 2 and above:
          * When a shift is canceled, the manager that performed the operation will be prompted to choose a replacement shift
            * Available options:
              * Default: Remove all users (All users will be given a day off)
              * Move all users to another shift
              * Randomly divide users according to a given ratio between the remaining available shifts
              * Randomly select a number of users to add to another shift
      
      Version 2 and above:
        * Broadcast a message to all users
  
  * Daily email reminders to submit their shift requests
    * Version 2 and above:
      * Text message support
      * A user can opt out of reminders (Email and/or Text)
      * A user can pick the time of the reminder
  
