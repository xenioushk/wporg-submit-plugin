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

### BWL Advanced FAQ Lite

```bash
svn cp "https://plugins.svn.wordpress.org/bwl-advanced-faq-manager-lite/trunk" \
       "https://plugins.svn.wordpress.org/bwl-advanced-faq-manager-lite/tags/1.1.1" \
       -m "Tagging version 1.1.1"
```

### BWL Poll Manager Lite

```bash
svn cp "https://plugins.svn.wordpress.org/bwl-poll-manager-lite/trunk" \
       "https://plugins.svn.wordpress.org/bwl-poll-manager-lite/tags/1.0.8" \
       -m "Tagging version 1.0.8"
```

### Ultimate Searchable Accordion Lite

```bash
svn cp "https://plugins.svn.wordpress.org/ultimate-searchable-accordion-lite-wpbakery-page-builder-addon/trunk" \
       "https://plugins.svn.wordpress.org/ultimate-searchable-accordion-lite-wpbakery-page-builder-addon/tags/1.0.8" \
       -m "Tagging version 1.0.8"
```
