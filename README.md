# ExhentaiFlowViewer
Forked from [exhentai flow viewer](https://sleazyfork.org/en/scripts/27056-exhentai-flow-viewer)

This scripts helps you to view a gallery in a single page, from up to down.

## Fixes

### 2024/10/02

With the original extension,if an image failed to load (due to a timeout), the page would be automatically redirected to a backup URL to fetch the image. This process would reload the entire gallery, causing all images to be fetched again. Additionally, the backup URL for the failed image would not be applied in the new round of fetching, leading to repeated failures and endless reloads.

Our forked version addresses this issue by overriding the image fetching failure action. When an image fails to load, the extension automatically fetches the backup image and replaces the timed-out one without reloading the entire gallery. This ensures a seamless and uninterrupted browsing experience, allowing users to enjoy the gallery without unnecessary delays or repeated failures.