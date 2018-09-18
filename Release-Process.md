This page describes how we use branches and tags with every new release.

Considering all commits added to `master` branch are submitted via pull requests and properly reviewed, the `master` branch is expected to always be working.  
`master` can also be referred to as the _current_ version. The _latest_ stable version is the latest version listed in the [Releases](https://github.com/SuperblocksHQ/superblocks-lab/releases) section in _GitHub_ (also accessed via `git tag` command).

## Versioning rules
```
<MAJOR>.<MINOR>.<PATCH>
X.Y.Z
```

* Patch (Z): only contains solved issues labelled as bugs
* Minor (Y): contains solved issues labelled as features
* Major (X): marks a big changeset when incompatible modifications or additions occur


## Simplified method (currently in use)

1. Bump version in `master` branch according to versioning rules.
```
./bump_version.sh "X.Y.Z"
```

2. Tag the `master` branch according to versioning rules.
```
git tag -a X.Y.Z -m "Version X.Y.Z"
git push origin X.Y.Z
```

3. Build from the latest tag

4. Deploy the latest build

5. New bugs and features are resolved on the next release


## Release branches (for later reference)

1. During `the final countdown`, a release branch is created: `release/1.10`.
2. Superblocks Lab is built from the `release/1.10` branch and released into https://lab-beta.superblocks.com
2. Superblocks Lab is functionally and smoke tested with a build from that branch.
3. Any critical issues should have fixed delivered to both `master` and `release/1.10` and properly verified with step 2.
4. When there are no more additional critical issues, a release tag `1.10.0` is created.
5. Superblocks Lab is built from the `1.10.0` tag and shipped to customers.
6. Any further recovery builds should be from commits on the `release/1.10` branch and patch versions should be used: `1.10.1`, `1.10.2`, etc.
