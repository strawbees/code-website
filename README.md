# Strawbees CODE Website
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fstrawbees%2Fcode-website.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fstrawbees%2Fcode-website?ref=badge_shield)


This repository is responsible for dealing with all website things regarding [Strawbees CODE](https://code.strawbees.com).

Right now it does mainly one thing: Publishes the built UI ([`code-ui`](https://github.com/strawbees/code-ui)) to the correct AWS S3 bucket.

## Publishing to S3

It uses [`s3-publisher`](https://github.com/strawbees/s3-publisher) to publish so in order for it to work you must set the environment variables accordingly. Check the documentation for more details but the main variables to set are:

```
S3_KEY=aws-credential-key-id
S3_SECRET=aws-credential-secret
```

Then you can run `npm run publish-stage` or `npm run publish-production` to publish to the correct bucket. Check `package.json` for more details.

## Continuous Integration

This repository triggers a build process on AppVeyor that just publish to AWS S3.


## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fstrawbees%2Fcode-website.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fstrawbees%2Fcode-website?ref=badge_large)