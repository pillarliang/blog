# [Use GitHub Action and  issues to blog on GitHub](https://github.com/pillarliang/blog/issues/1)

### Aim

Commit or modify `issues`, and `README.md` will classify `issues` according to the `labels` tag currently assigned to issues.

### Operation

1. Create a new repository.

2. [[settings](https://github.com/settings/tokens)](https://github.com/settings/tokens) --> Personal access tokens (classic) --> **Generate new token**
   - `Select scopes`: check all
   - copy the generated token
   <img width="1523" alt="image-20230120212257951" src="https://user-images.githubusercontent.com/28833267/213859333-c9ff2f96-1eaf-481f-b378-74449abbadbb.png">

3. In the settings of the new repo, **create a new secrets environment variable**, which is the Github access authorization token. The value is the personal access token generated in the previous step.

4. set `workflow permissions` to `Read and write permissions`
  <img width="1082" alt="image-20230121161725141" src="https://user-images.githubusercontent.com/28833267/213859372-d98ab74d-5236-412b-8bb5-4c1277f8afb5.png">

5. copy 3 files from this project to your own project.
     - [.github/workflows/generate_readme.yml]
     (https://github.com/pillarliang/blog/blob/main/.github/workflows/generate_readme.yml)
      Modify the relevant configuration to your own information. In Figure 2, `BLOG` corresponds to the environment variables set in Step 3 above
      <img width="288" alt="image-20230121161929753" src="https://user-images.githubusercontent.com/28833267/213859456-eafe3e28-d072-4c70-9cb6-3717ca0f90cc.png">
      <img width="836" alt="image-20230121162017339" src="https://user-images.githubusercontent.com/28833267/213859465-ef48142a-73ab-46e6-b57a-ad066558cdb4.png">
      - [main.py](https://github.com/pillarliang/blog/blob/main/main.py)
      - [requirements.txt](https://github.com/pillarliang/blog/blob/main/requirements.txt)

6. After the configuration is complete, create an issue for verification.If it fails, check the error message yourself under the Actions tab.

