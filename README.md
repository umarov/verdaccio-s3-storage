# verdaccio-s3-storage

📦 AWS S3 storage plugin for verdaccio 

## Usage

```
npm install verdaccio-s3-storage
```

This will pull AWS credentials from your environment.

In your verdaccio config, configure

```yaml
# necessary (see https://github.com/verdaccio/verdaccio/issues/673)
storage: ./storage

store:
  s3-storage:
    bucket: your-s3-bucket
    keyPrefix: some-prefix # optional, has the effect of nesting all files in a subdirectory
    region: us-west-2 # optional, will use aws s3's default behavior if not specified
    endpoint: https://{service}.{region}.amazonaws.com # optional, will use aws s3's default behavior if not specified
    s3ForcePathStyle: false # optional, will use path style URLs for S3 objects
```
