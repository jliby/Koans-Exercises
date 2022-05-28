# Branch Filters

**Description:**

We have a `api-job` job in our Workflow. We have decided we only ever want to run our `api-job` job when we pass a certain parameter via an API call.

**Goals:**

- Create a personal api token
- Build a curl command
- Without modifying the `config.yml`, run `api-job`
- Share link to green Workflow.

**Help:**
<details>
  <summary>Spoiler warning</summary>

  * https://circleci.com/docs/2.0/managing-api-tokens/
  * https://circleci.com/docs/api/v2/#operation/triggerPipeline
  * https://support.circleci.com/hc/en-us/articles/360052405651-Utilizing-Basic-authorization-in-CircleCI-API-calls

  <details>
    <summary>Bonus Spoiler!</summary>

    ```shell
curl --request POST \
  --url https://circleci.com/api/v2/project/gh/jliby/Koans-Exercises/pipeline \
  --header 'authorization: Basic [MjE0Y2YyMzllOTlhMjZjNDQ1YzA4YzQ4MTE3MmQ5MTdlYjMzNWFlYg==]' \
  --header 'content-type: application/json' \
  --data '{"branch":"Exercise-15","parameters":{"run_by_api":true}}'
    ```

  </details>
</details>
