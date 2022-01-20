  

INVALIDATE TEST ENV

AWS_PROFILE=cloudcycle-test aws cloudfront create-invalidation --distribution-id E2GROWL66I4IR8 --paths "/*"

or

aws cloudfront create-invalidation --distribution-id E2GROWL66I4IR8 --paths "/*" --profile cloudcycle-test

  

INVLAIDATE DEV Event

AWS_PROFILE=cloudcycle-dev aws cloudfront create-invalidation --distribution-id E2WZH0AEEJOOQT --paths "/*"

or

aws cloudfront create-invalidation --distribution-id E2WZH0AEEJOOQT --paths "/*" --profile cloudcycle-dev