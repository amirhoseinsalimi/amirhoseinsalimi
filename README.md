## HEY!

<a href="https://www.linkedin.com/in/amirhoseinsalimi/">
  <img align="left" alt="Amir Hosein Salimi's Linkdein" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/linkedin.svg" />
</a>
<a href="https://twitter.com/AHoseinSalimi">
  <img align="left" alt="Amir Hosein Salimi's Twitter" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/twitter.svg" />
</a>
<a href="https://t.me/amirhoseinsalimii">
  <img align="left" alt="Amir Hosein Salimi's Telegram" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/telegram.svg" />
</a>

<br />
<br />


[![Amir Hosein Salimi's GitHub Stats](https://github-readme-stats.vercel.app/api?username=amirhoseinsalimi&show_icons=true)](https://github.com/amirhoseinsalimi)

# Visit https://github.com/lowlighter/metrics/blob/master/action.yml for full reference
name: Metrics
on:
  # Schedule updates
  schedule: [{cron: "0 * * * *"}]
  push: {branches: "master"}
jobs:
  github-metrics:
    runs-on: ubuntu-latest
    steps:
      - uses: lowlighter/metrics@latest
        with:
          # You'll need to setup a personal token in your secrets.
          token: ${{ secrets.METRICS_TOKEN }}
          # GITHUB_TOKEN is a special auto-generated token used for commits
          committer_token: ${{ secrets.GITHUB_TOKEN }}

          # Options
          user: amirhoseinsalimi
          template: classic
          base: header, activity, community, repositories, metadata
          config_timezone: Asia/Tehran
