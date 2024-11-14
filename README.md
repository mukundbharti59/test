name: Update GitHub Profile Page
on: [push]

jobs:
  gadpp_job:
    runs-on: ubuntu-latest
    name: Update GitHub Profile Page
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: GADPP
        uses: umutphp/github-action-dynamic-profile-page@v5
        id: gadpp
        env:
          API_TOKEN_GITHUB: ${{ secrets.API_TOKEN_GITHUB }}
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          github-username: 'YOUR_GITHUB_USERNAME'
          user-email: 'EMAIL_USED_ON_GITHUB'
