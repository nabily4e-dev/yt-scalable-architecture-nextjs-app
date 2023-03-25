<!-- Enable commitlint -->

npx husky add .husky/commit-msg 'npx --no -- commitlint --edit ${1}'

<!-- If it didn't work, try: -->

npx husky add .husky/commit-msg 'npx --no -- commitlint --edit "$1"'

<!-- or -->

npx husky add .husky/commit-msg \"npx --no -- commitlint --edit '$1'\"

<!-- or -->

npx husky add .husky/commit-msg "npx --no -- commitlint --edit $1"

<!-- test last commit with commitlint -->

npx commitlint --from HEAD~1 --to HEAD --verbose
