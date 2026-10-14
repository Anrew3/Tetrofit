# Firmware

Each folder holds the firmware releases for one product. The TETROFIT website reads `manifest.json` in each folder to show the latest update and its change log.

| Folder | Product |
| --- | --- |
| `hl-headlight/` | Highland Headlight Retrofit Kit |
| `hl-steering/` | Highland Steering Wheel Retrofit Kit |
| `pcb/` | TETROFIT PCB |

## Adding a release

Edit the product's `manifest.json` and add the new release at the top of `releases` (newest first):

```json
{
  "releases": [
    {
      "version": "1.2.3",
      "date": "2026-10-20",
      "notes": [
        "Fixed matrix headlight startup",
        "Improved steering wheel button response"
      ]
    }
  ]
}
```

Commit the change to `main`. The website updates automatically, with no rebuild needed.
