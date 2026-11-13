# Chance Tracker

Speedometer dials showing how likely each friend is to say yes to a plan, from 0 to 100%.

Log each invite (who, what kind of plan, yes / no / flaked). Each friend's chance is their
recency-weighted yes rate, blended with the group average as if they'd had 5 typical invites.
Picking a kind of plan runs the same blend on just those invites, starting from the friend's
overall chance. Invites lose half their weight every 90 days; a flake counts as a heavier no.

`index.html` is the whole app. It's hosted as a claude.ai artifact, which keeps the shared
log in the artifact's database. Opened anywhere else it runs in preview mode with nothing saved.
Use **Export CSV** on the hosted page to back up the data.

## Deal Dial

`deal-dial.html` is the mood-tracker version. Each friend joins with their own claude.ai account
and rates their own chance of taking a deal (drag the dial, 0–100%), again whenever their mood
changes. Access rules let each person write only their own entries (`crew/<their id>`); only
the page owner can remove other people's entries, remove deals or clear everything. Deals are
named offers ("Cabin in March, $180 each"); each deal shows the crew's average of everyone's
latest rating. Each friend gets a dial with their latest rating, its change from the previous
one, and a line of past ratings. Like the tracker, it's hosted as a claude.ai artifact with
a shared database, and Export CSV backs up the data.
