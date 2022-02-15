As part of my coursework for Guvi Data Science course, I was tasked with completing a mock take-home interview assignment from a ficticious company, Relax. I was provided the following narrative outlining the task:

The data is available as two attached CSV files:

takehome_user_engagement.csv

takehome_users.csv

The data has the following two tables:

1 - A user table ("takehome_users") with data on 12,000 users who signed up for the product in the last two years. This table includes:

name: the user's name
object_id: the user's id
email: email address
creation_source: how their account was created. This takes on one of 5 values:
PERSONAL_PROJECTS: invited to join another user's personal workspace
GUEST_INVITE: invited to an organization as a guest (limited permissions)
ORG_INVITE: invited to an organization (as a full member)
SIGNUP: signed up via the website
SIGNUP_GOOGLE_AUTH: signed up using Google Authentication (using a Google email account for their login id)
creation_time: when they created their account
last_session_creation_time: unix timestamp of last login
opted_in_to_mailing_list: whether they have opted into receiving marketing emails
enabled_for_marketing_drip: whether they are on the regular marketing email drip
org_id: the organization (group of users) they belong to
invited_by_user_id: which user invited them to join (if applicable).
2 - A usage summary table ( "takehome_user_engagement" ) that has a row for each day that a user logged into the product.

Defining an "adopted user" as a user who has logged into the product on three separate days in at least one seven-day period, identify which factors predict future user adoption.

Answer

Based on my analysis, I concluded that the factors that most likely lead to a particular user adopting the product are when the user is invited to join another user's workspace or is invited to an organization as a guest. My analysis also demonstrates that being a member of certain organizations, and in particular 'org_id_0,' makes it more likely for a user to adopt the product. The tuned classifier also found three of the email domains to be of increased importance (and if the user signed up using google authentication), as well as being invited to become a full member of an organization.

Based on the above, I would make the following recommendations to Relax regarding their attempts to improve future user adoption:

-Run promotions seeking to incentivize users to invite prospective users to join their personal workspaces on the product;
-Run promotions seeking to incentivize organizations to grow by sending guest and/or full invites to prospective users to join the product;
-Promote certain organizations identified by the model above (in particular org_id_0) to all users; and
-Target its regular email marketing drip to existing and prospective users with yahoo.com, hotmail.com, and gmail.com email addresses.
