# uptime-monitor

Checks every public site from GitHub's servers every 5 minutes (outside the home network) and sends an ntfy push when a site goes down or recovers.
Sites live in `sites.txt`. Add the ntfy topic as the repository secret `NTFY_TOPIC` (Settings > Secrets and variables > Actions); without it the run
still works and shows results in the Actions log, but sends no phone notification.
Public repo on purpose: GitHub Actions minutes are unlimited for public repos (a private repo only gets 2000 min/month, and this uses about 8600).
Contains no secrets: the site list is public information and the ntfy topic is a secret, not a file.
