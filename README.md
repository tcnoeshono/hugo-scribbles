# New Post

```bash
vim content/posts/<post-name>.md
# Update until done
sed -i -re '/^draft:/{s/true/false/}' !$
# Test site
hugo server -D

# Update site
hugo -D

# Publish site
cd public
git add content/posts/<post-name>.md
git commit -am "add: <post name>"
git push

cd ..
git add public
git commit -av "add: <post name>"
git push
```

