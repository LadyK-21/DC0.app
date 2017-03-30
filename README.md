# Probot: DCO

a GitHub Integration built with [probot](https://github.com/probot/probot) that enforces the [Developer Certificate of Origin](https://developercertificate.org/) (DCO) on Pull Requests. It requires all commit messages to contain the `Signed-off-by` line with an email address that matches the commit author.

## Usage

[Configure the integration](https://github.com/integration/dco) for your organization or repositories. Enable [required status checks](docs/required-statuses.md) if you want to enforce the DCO on all commits.

## How it works

The Developer Certificate of Origin (DCO) is a lightweight way for contributors to certify that they wrote or otherwise have the right to submit the code they are contributing to the project. Here is the full [text of the DCO](https://developercertificate.org/), reformatted for readability:

> By making a contribution to this project, I certify that:
>
> 1. The contribution was created in whole or in part by me and I have the right to submit it under the open source license indicated in the file; or
>
> 2. The contribution is based upon previous work that, to the best of my knowledge, is covered under an appropriate open source license and I have the right under that license to submit that work with modifications, whether created in whole or in part by me, under the same open source license (unless I am permitted to submit under a different license), as indicated in the file; or
>
> 3. The contribution was provided directly to me by some other person who certified (a), (b) or (c) and I have not modified it.
>
> 4. I understand and agree that this project and the contribution are public and that a record of the contribution (including all personal information I submit with it, including my sign-off) is maintained indefinitely and may be redistributed consistent with this project or the open source license(s) involved.

Contributors _sign-off_ that they adhere to these requirements by adding a `Signed-off-by` line to commit messages.

```
This is my commit message

Signed-off-by: Random J Developer <random@developer.example.org>
```

Git even has a `-s` command line option to append this automatically to your commit message:

```
$ git commit -s -m 'This is my commit message'
```

Once [installed](#usage), this integration will check that each commit in a Pull Request includes this sign-off, and set the status to `failed` if it doesn't.

![](screenshot)

## Further Reading

If you want to learn more about the DCO and why it might be necessary, here are some good resources:

- [Developer Certificate of Origin versus Contributor License Agreements](https://julien.ponge.org/blog/developer-certificate-of-origin-versus-contributor-license-agreements/)
- [The most powerful contributor agreement](https://lwn.net/Articles/592503/)
