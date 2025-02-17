# Привет, я [ggrachev] 👋

- 🔭 Сейчас работаю над ... Telegram bot that tracks Pudgy Penguins sticker packs 
- 🌱 Изучаю ...  Python
- 💬 Спросите меня о ...  cryptocurrencies
- 📫 Как со мной связаться: [почта/соцсети] https://t.me/gregory_grachev
.github/workflows/update.yml
name: Update README

on:
  schedule:
    - cron: "0 0 * * *"

jobs:
  update:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - run: echo "Last updated: $(date)" > LAST_UPDATE.md
      - uses: stefanzweifel/git-auto-commit-action@v4
