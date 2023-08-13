Hi contributor! For security reasons, we don't automatically deploy preview builds from
pull requests unless it is manually deployed by a @recaptime-dev/squad member.

(If you have push access here and pushing from your own branch within the repo, you should have deploys running behind the scenes.)

### Need some help?

<details>
  <summary>Are you a squad member with write access to the repo?</summary>

  If you push your patches to your personal branch outside this repo, try pushing here as a seprate branch:

  ```shell
  # assuming upstream points to gh:recaptime-dev/website-next
  git push upstream HEAD:patchops/gh-pr-<number>
  ```

  Otherwise, open in an fresh Codespaces or Gitpod workspace, manually build the site with patches and deploy:

  ```shell
  # authenticate yourself with DOPPLER_TOKEN secret at https://gitpod.io/user/variables
  # assuming we provisioned you an machine token or has access to admin account
  bundle exec jekyll build -d public
  CURRENT_BRANCH=$(git symbolic-ref --short HEAD) # or just patchops/gh-pr-<number>
  doppler run -- wrangle pages deploy public --project-name recaptime-dev --branch=$CURRENT_BRANCH
  ```
</details>
<details>
  <summary>Have push access but still not automatically deployed?</summary>

  If that's the case, an code reviewer or assignee for this merge request should have a look. They might try manually deploy it for you. Apologies if that's the case.
</details>

---

_This reply was automated as [part of this workflow](https://github.com/recaptime-dev/website-next/blob/master/.github/workflows/triage-ops.yml#L18) and its source text can be found [here](https://github.com/recaptime-dev/website-next/blob/master/.github/automated-replies/manual-review-required.md). You are welcome to improve this._
