<a href = "https://github.com/madushadhanushka/simple-sqlite/graphs/contributors">
  <img src = "https://contrib.rocks/image?repo=madushadhanushka/simple-sqlite"/>
</a>


![star-history](https://api.lucabubi.me/chart?username=USERNAME&repository=REPOSITORY&color=COLOR)

[![Spotify](https://novatorem.bgstatic.vercel.app/api/spotify)](https://open.spotify.com/artist/6hyCmqlpgEhkMKKr65sFgI)

<img src="https://widgetbite.com/stats/{random-guid}" alt="watching_count" />

<img src="http://estruyf-github.azurewebsites.net/api/VisitorHit?user=madushadhanushka&repo=madushadhanushka&countColorcountColor&countColor=%237B1E7B"/>


name: Contribution snake

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update snake grid
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: madushadhanushka
          svg_out_path: dist/github-contribution-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
