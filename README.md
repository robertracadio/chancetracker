# Chance Tracker

Speedometer dials showing how likely each friend is to say yes to a plan, from 0 to 100%.

Log each invite (who, what kind of plan, yes / no / flaked). Each friend's chance is their
recency-weighted yes rate, blended with the group average as if they'd had 5 typical invites.
Picking a kind of plan runs the same blend on just those invites, starting from the friend's
overall chance. Invites lose half their weight every 90 days; a flake counts as a heavier no.

`index.html` is the whole app. It's hosted as a claude.ai artifact, which keeps the shared
log in the artifact's database. Opened anywhere else it runs in preview mode with nothing saved.
Use **Export CSV** on the hosted page to back up the data.
