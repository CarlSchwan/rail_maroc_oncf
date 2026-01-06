# GTFS Feed Submission Details

## Feed URL
```
https://github.com/newsbubbles/rail_maroc_oncf/raw/main/oncf_gtfs.zip
```

---

## Mobility Database
**URL:** https://database.mobilitydata.org/add-a-feed

| Field | Value |
|-------|-------|
| Feed URL | `https://github.com/newsbubbles/rail_maroc_oncf/raw/main/oncf_gtfs.zip` |
| Country | Morocco |
| Region | National |
| Provider Name | ONCF (Office National des Chemins de Fer) |
| Provider Website | `https://www.oncf-voyages.ma` |
| Feed Type | GTFS Schedule |
| License | ODbL |

**Description:**
> Community-created GTFS for Morocco's national rail network. Covers Al Boraq (high-speed), Al Atlas (intercity), and TNR (regional) services. 33 stations, 9 routes, 60 trips. Track geometry sourced from OpenStreetMap.

---

## Transitland
**Method:** GitHub PR to https://github.com/transitland/transitland-atlas

### Steps

1. **Fork** the `transitland/transitland-atlas` repo

2. **Edit** `feeds/github.com.dmfr.json` — add this entry to the `feeds` array:

```json
{
  "id": "f-oncf~morocco~rail",
  "spec": "gtfs",
  "urls": {
    "static_current": "https://github.com/newsbubbles/rail_maroc_oncf/raw/main/oncf_gtfs.zip"
  },
  "license": {
    "spdx_identifier": "ODbL-1.0",
    "url": "https://opendatacommons.org/licenses/odbl/1-0/"
  },
  "tags": {
    "source": "unofficial"
  },
  "operators": [
    {
      "onestop_id": "o-oncf~morocco",
      "name": "ONCF (Office National des Chemins de Fer)",
      "short_name": "ONCF",
      "website": "https://www.oncf-voyages.ma",
      "associated_feeds": [
        {
          "gtfs_agency_id": "ONCF"
        }
      ]
    }
  ]
}
```

3. **Commit & Push** to your fork:
```bash
git checkout -b add-oncf-morocco-rail
git add feeds/github.com.dmfr.json
git commit -m "Add ONCF Morocco Rail GTFS feed"
git push origin add-oncf-morocco-rail
```

4. **Open PR** with title: `Add ONCF Morocco Rail GTFS feed`

**PR Description:**
```
Adds community-created GTFS feed for Morocco's national rail network (ONCF).

- **Operator:** ONCF (Office National des Chemins de Fer)
- **Coverage:** Al Boraq (HSR), Al Atlas (intercity), TNR (regional)
- **Stations:** 33
- **Routes:** 9
- **License:** ODbL
- **Source:** https://github.com/newsbubbles/rail_maroc_oncf

ONCF does not publish official GTFS data. This feed was created from schedule data and OpenStreetMap track geometry.
```

---

## OpenMobilityData (TransitFeeds)
**URL:** https://transitfeeds.com/submit

| Field | Value |
|-------|-------|
| Feed URL | `https://github.com/newsbubbles/rail_maroc_oncf/raw/main/oncf_gtfs.zip` |
| Agency | ONCF |
| Location | Morocco |

---

## Google Transit Partners
**URL:** https://support.google.com/transitpartners/answer/1111481

For direct submission to Google Maps. Requires Transit Partners account.

---

## Feed Statistics
- **Stations:** 33
- **Routes:** 9
- **Trips:** 60
- **Shape Points:** 19,356
- **File Size:** ~277 KB (zipped)
