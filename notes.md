# Controlling access

### Users

Default admin is `you@example.com` and unless `GRIST_FORCE_LOGIN=true` everyone is admin. User gets created once the auth is done by IdP.

Special Users 1-4 are always created: "anon@getgrist.com", "thumbnail@getgrist.com", "everyone@getgrist.com", "support@getgrist.com", "you@example.com"

#### Questions
- Can we prevent Grist from creating a user automatically?

#### Threads
- https://github.com/gristlabs/grist-core/issues/733

### Orgs (aka "Team Page")

Assuming `GRIST_ORG_IN_PATH=true` ?

If `GRIST_SINGLE_ORG` is not set, the default org is at url `/o/docs`. Each new user gets a default org (aka personal site) created so that the actual org domain is `/docs-{userId}`, but the domain is aliased to `/o/docs`. https://support.getgrist.com/teams/#understanding-personal-sites

If you go to an org url that you don't have access to you get an access denied page.

#### Questions
- Can we prevent Grist from giving any user account access to an org?

#### Ideas
- Even if every user gets an org, they won't have access to data necessarily... But, it's still a security vulnerability to even have an account that can have API access in case there's a bug somewhere
- DataLENS could create user and give access to team orgs (with or without personal default org)