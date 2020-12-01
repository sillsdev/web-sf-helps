# web-sf-helps

This repo is to help see differences from SF Help HTML pages (S3 bucket site) in English that need to be uploaded to *Crowdin*.

Setup AWS CLI including credentials. See https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html#cli-quick-configuration

Run
```bash
cd src/en/
aws s3 sync s3://help.scriptureforge.org/en . --exact-timestamps
```

Look at the git differences to see which HTML files need to be updated in *Crowdin*. After updating commit the differences.

See https://github.com/sillsdev/web-xforge/blob/master/src/Help/UpdateHelp/Program.cs for how to deal with other languages.
