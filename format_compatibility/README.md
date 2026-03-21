# Format Compatibility

Skills for media format and codec compatibility across platforms.

## Skills

| Skill | Command | Description |
|-------|---------|-------------|
| Audio Format Fixer | `audio-format-fixer` | Audio codecs across Mac/iOS/Windows/Android/web, format conversion |
| Font Format Fixer | `font-format-fixer` | WOFF2/WOFF/TTF/OTF/EOT, @font-face setup, browser compatibility |
| Image Format Fixer | `image-format-fixer` | Image formats across platforms, WebP/AVIF/PNG/JPEG conversion |
| Video Format Fixer | `video-format-fixer` | Video codecs across platforms, transcoding guidance |

## When to Use

- Media files not displaying/playing on certain platforms
- Choosing the right format for cross-platform compatibility
- Font rendering issues across browsers
- Image optimization (WebP, AVIF decisions)

## Usage Examples

```
Skill({ skill: 'image-format-fixer', args: 'Should we use WebP or AVIF for the product images?' })
Skill({ skill: 'font-format-fixer', args: 'Custom font not rendering on Safari' })
```
