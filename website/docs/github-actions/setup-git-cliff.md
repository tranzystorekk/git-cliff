# setup-git-cliff

There is also another GitHub Action which is [setup-git-cliff](https://github.com/kenji-miyake/setup-git-cliff).

While `git-cliff-action` uses the Docker image generated by [docker.yml](https://github.com/orhun/git-cliff/blob/main/.github/workflows/docker.yml), `setup-git-cliff` installs the binary executable in the [release artifacts](https://github.com/orhun/git-cliff/releases/latest):

```yml
- name: Check out repository
  uses: actions/checkout@v3

- name: Set up git-cliff
  uses: kenji-miyake/setup-git-cliff@v1

- name: Run git-cliff
  run: |
    git cliff
```

See a practical example [here](https://github.com/autowarefoundation/autoware-github-actions/blob/v1/generate-changelog/action.yaml).
