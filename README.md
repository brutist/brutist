### Hi there 👋

Just me and nothing else


<!--START_SECTION:waka-->
name: Waka Readme

on:
  workflow_dispatch:
  schedule:
    # Runs at 12am UTC
    - cron: "0 0 * * *"

jobs:
  update-readme:
    name: WakaReadme DevMetrics
    runs-on: ubuntu-latest
    steps:
      - uses: athul/waka-readme@master
        with:
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          SHOW_TITLE: true
          BLOCKS: ->
          TIME_RANGE: all_time
          SHOW_TIME: true
          SHOW_MASKED_TIME: true
          LANG_COUNT: 10
<!--END_SECTION:waka-->
