# Submit A Plugin to WordPress.org Repository

A step by step guidelines to submit plugin to WordPress.org

## Check svn status

```bash
svn stat
```

### Add all files to staging

Navigate to the project directory. Run the following command to stage all the files of `trunk` folder.

```bash
svn add trunk/ --force
```

### Commit and Push to WP repository

```bash
svn ci -m "Update readme file"
```

### Tagging Version

Before running the following command, we need to add the stable version tag information to the readme.txt file. Tagging code pattern.

```bash
svn cp "<trunk_path>" "<trunk_version>" -m "tag message"
```

Here are a few examples.

### BAF

```bash
svn cp "https://plugins.svn.wordpress.org/bwl-advanced-faq-manager-lite/trunk" \
       "https://plugins.svn.wordpress.org/bwl-advanced-faq-manager-lite/tags/1.1.1" \
       -m "Tagging version 1.1.1"
```

```bash
BPM
svn cp "https://plugins.svn.wordpress.org/bwl-poll-manager-lite/trunk" "https://plugins.svn.wordpress.org/bwl-poll-manager-lite/tags/1.0.6" -m "Tagging version 1.0.6"
```

```bash
USAVC
svn cp" https://plugins.svn.wordpress.org/ultimate-searchable-accordion-lite-wpbakery-page-builder-addon/trunk"
"https://plugins.svn.wordpress.org/ultimate-searchable-accordion-lite-wpbakery-page-builder-addon/tags/1.0.7" -m "Tagging version 1.0.7"
```
