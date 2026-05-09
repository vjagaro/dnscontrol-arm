# DNSControl for 32-bit ARM

A personal access token is needed to trigger the `release.yml` workflow after a
tag is generated from the `auto-version.yml` workflow. See the [GitHub
documentation](https://docs.github.com/en/actions/how-tos/write-workflows/choose-when-workflows-run/trigger-a-workflow#triggering-a-workflow-from-a-workflow)
for more information.

## GitHub Actions Setup

1.  Open https://github.com/settings/personal-access-tokens/new.
2.  Enter or select:
    - **Token name**: Auto-version dnscontrol-arm
    - **Expiration**: No expiration
    - **Repository access**: Only select repositories
        - vjagaro/dnscontrol-arm
    - **Repository permissions**: Contents, Metadata
        - **Contents access**: Read and write
3.  Click **Generate token**.
4.  Copy the generated token.
5.  Open https://github.com/vjagaro/dnscontrol-arm/settings/secrets/actions/new.
6.  Enter:
    - **Name**: PAT
    - **Secret**: _(Paste the generated token)_
7.  Click **Add secret**.
