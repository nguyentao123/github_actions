**name: name_pipeline**

on:     
    push: 
        branches: [main]


jobs:
  say-hello:
    runs-on: ubuntu-latest
    steps:
      - run: echo "TODAY=$(date +%y -%m -%d)" >> $GITHUB_ENV
      - run: echo Hello world, Today is $TODAY