# R2 Asset Sync

The HTML zones should stay in GitHub and deploy through Cloudflare Pages.

Use R2 for heavier or edited static assets if needed:

- cropped team logos
- cached sailor headshots
- custom news/weather images
- video files that are not handled by ScreenCloud's YouTube app

Suggested local folder:

```text
assets/
```

With `rclone`, the workflow can be:

```sh
rclone sync assets/ cloudflare-r2:BUCKET_NAME/assets/
```

The zone HTML should then reference the public R2/custom-domain URL, not local file paths.

Important:

- Do not use `file://` URLs in hosted HTML.
- Do not use `127.0.0.1` URLs in hosted HTML.
- Keep private credentials out of this repo.
