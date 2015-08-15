# Archives

## ZIP

### Compress

```bash
zip -r archive_name.zip directory_to_compress
```

### Extract

```bash
unzip archive_name.zip
unzip archive_name.zip -d /tmp/extract_here/
```

## tar

### Compress

```bash
tar -cvf archive_name.tar directory_to_compress
```

### Extract

```bash
tar -xvf archive_name.tar.gz
tar -xvf archive_name.tar -C /tmp/extract_here/
```

## tar gzip

### Compress

```bash
tar -zcvf archive_name.tar.gz directory_to_compress
```

### Extract

```bash
tar -zxvf archive_name.tar.gz
tar -zxvf archive_name.tar.gz -C /tmp/extract_here/
```

## tar bzip2

### Compress

```bash
tar -jcvf archive_name.tar.bz2 directory_to_compress
```

### Extract

```bash
tar -jxvf archive_name.tar.bz2
tar -jxvf archive_name.tar.bz2 -C /tmp/extract_here/
```
