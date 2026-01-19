name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *" # Her gün gece yarısı çalışır
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: kullaniciadiniz
          gif_out_path: dist/github-contribution-grid-snake.gif
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/gh-action-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
