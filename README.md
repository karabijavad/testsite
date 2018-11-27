```bash
for x in b c d e f g h i j k l m n o p q r s t u v w x y z;
    do cp a.jpg $x.jpg;
done;
```

for BUCKET_NAME:

1. turn on static site hosting
2. disable default encryption
3. copy the site files over to the bucket
```bash
aws s3 cp --recursive s3://BUCKET_NAME/ .
```
4. hit the page in browser to confirm everythings good
5. turn on default encryption (AES-256)
6. begin copying the files again
```bash
aws s3 cp --recursive s3://BUCKET_NAME/ .
```
7. while the files are uploading, reload the page again and again until
confirming that images work
