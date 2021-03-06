# influencer
influencer is a cli for AWS ECS to update container image in existing task definition and update service according these changes.

## Usage
### influencer deploy
```
$ influencer deploy --help
NAME:
   influencer deploy - Update task definition by image in args and update service with the task definition

USAGE:
   influencer deploy [command options] [arguments...]

OPTIONS:
   --cluster value  cluster
   --service value  service
   --image value    image repo:tag, more than 1
   --dry-run        dry-run. output diff in pretty

Examples:
  $ influencer --awsconf default --awsregion ap-northeast-1 deploy --cluster samplecluster --service sampleservice --image sample:v1.0.0 --dry-run
  $ influencer --awsconf default --awsregion ap-northeast-1 deploy --cluster samplecluster --service sampleservice --image sample:v1.0.0
```

### sync-deploy
```
$ influencer sync-deploy --help             
NAME:
   influencer sync-deploy - Run tasks and update service synchronously

USAGE:
   influencer sync-deploy [command options] [arguments...]

OPTIONS:
   --path value  path to yaml deploy config file
   --dry-run     dry-run. output diff in pretty

Examples:
  $ influencer --awsconf default sync-deploy --path ./example/syncdeploy.yaml --dry-run
  $ influencer --awsconf default sync-deploy --path ./example/syncdeploy.yaml
```
## TODO
