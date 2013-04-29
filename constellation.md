# The Constellation Architecture

## Elements

- Multiple products
  - Could be sold separately
- Tribal knowledge

## Unbundling
- Services
  - Can''t do Post.comments anymore because they live inseparate places

## Break down

### Little apps
- Multi tenant database
  - Trade-offs
    - Security - Security breach compromises everyone
    - Privacy - accidental data leakage from one tenant to another
    - Corruption - All eggs one basket
    - Uptime - One tenant can bring down the whole house

- Single tenant database
  - Security - If one user is compromise, other users are safe
  - Privacy - impossible to ship a bug that shows private data to a wrong user
  - corruption - no one corrupted record bring down all
  - Many users = many databases -> too many

- Many apps, many DBs
  - Deployment - can''t do a single "git push"
    - Scheduling
    - Batching

- Autonomy
  - Should I update and deploy?
  - Each app calls home and if update is necessary, updates itself
  - Buddy system - Heroku can''t autodeploy, so appA deploys appB and viceversa

- Limited concerns
  - Keep each product simple and grokkable

- Hub
  - Admin user creation
  - Client admin

- Client hub
  -
### Pull (Poll)
- Push
  - Hotness
  - Is not webby, pull is easier
  - Doesn''t scale well -> Overworked server -> expensive
- Pull
  - easier

### HTML not JSON for interapp communication
- JSON is a trend (?) just like XML was or SOAP
- Why not HTML?
  - Has primitives
    - ol -> array
    - dl -> hash
    - table
    - integer -> absent
  - Formats
    - Microdata
    - Microformats
    - Schema.org


github.com/g5


