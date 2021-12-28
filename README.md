![corona bandaid](header.jpg)

Periodically determine the first year allowed for NL Booster Shots.
This is a really bad hack that just runs as a cronjob and publishes
the static site.

The official site sets a CORS header so this can't do queries from
the user's web browser to find the date.

The cloudflare firewall rules prevent github servers from fetching
the the API, so it can't run as a github action.

So instead it runs in a loop on a desktop machine somewhere.


*NOTE* If you want to change anything, do not touch the `index.html`
since it is overwritten by the `publish` script each time.  Update
`template.html` instead.
