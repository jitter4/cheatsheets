# brazil
## create
brazil ws create --root ~/workplace/workspace_name --versionset versionset_name --eventId event_id

brazil ws create --name SpektrJobManagerService --versionset SpektrJobManagerService/development

## use   
brazil ws use --versionset new_versionset_name --eventId event_id

## version-set
brazil vs removeUnusedPackages --vs <VersionSet/Name>

## delete
brazil ws delete

brazil ws delete --root ~/workplace/<workspace_name>

## dry-run
brazil workspace --dryrun
brazil workspace --dryrun -p <package1> -p <package2>
brazil workspace --dryrun -p <package1> -p <package2> -vs <version_set>/<dev>
brazil help workspace dryrun

## ws - workspace
## versionset
brazil ws use --versionset \<version_set\>\<\\>
brazil ws use --versionset BT101SvarshnLambda/development

### package - cloning
brazil ws use --package BT101SvarshnLambda

### sync - pull
brazil ws sync
brazil ws --sync --metadata
### |^| use for updating dependecy cache from in local and cloud desktop

### prefrences
brazil prefs

#### ruby
https://w.amazon.com/index.php/BrazilCLI_2.0/Runtimes/Ruby

## brazil-build
brazil-build
### rujn-tests
brazil-build releasei
### brazil-build apollo-pkg

## brazil-recursive-cmd
brazil-recursive-cmd brazil-build

## dependency graph
brazil-path [{DependencyName}]run.configfarm.brazil-config

# code-review
cr

# odin-get
odin-get -n -t PrivateKey <material-set> | openssl pkcs8 -nocrypt -inform DER -outform PEM

# odin-get
/apollo/env/envImprovement/bin/odin-get com.amazon.spektr.secrets.rds.resourcemanager





## 



### latest packgae
brazil ws use -p <package>


#### commit steps
brazil ws --sync --metadata
brazil-build
git diff --staged
git commit -m "<commit_message>"
git pull --rebase <origin_name> <brnach_name>
git rebase -i <brnach_name> to squash
brazil workspace --dryrun
git push
