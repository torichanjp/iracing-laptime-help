iRacing iRacingラップテーブルツールヘルプ
=====================================

（現時点の）ビルド、更新手順
-------------------------

```shell
$ yarn build
aws s3 cp dist/ s3://stork-racing-public/ --recursive --profile stork-racing
```

URL
------------------------
[http://stork-racing-public.s3-website-ap-northeast-1.amazonaws.com/](http://stork-racing-public.s3-website-ap-northeast-1.amazonaws.com/)
