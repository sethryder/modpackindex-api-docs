FORMAT: 1A
HOST: https://www.modpackindex.com/api/v1

# Modpack Index API

The API provides a way for you to get data from Modpack Index in a structured way.

### Rate Limiting

We currently rate limit the API at 3,600 requests per hour.

Need a higher limit? Get in touch on Discord and we will see what we can figure out.

### Bug Reports

If you run into any issues please let us know. You can reach us on Discord at https://www.modpackindex.com/discord.

### Using it?

If you are using the API please let us know! We would love to see how it is being used in the wild.

## Authors [/authors{?limit}{?page}]

### Get Authors [GET]

Returns a list of authors.

+ Parameters
    + limit: `3` (number, optional) - &#35; of results to return (Max: 100).
        + Default: `25`
    + page: `1` (number, optional) - Set page for results.
        + Default: `25`

+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "curse_user_id": 11806322,
              "twitch_id": 39682137,
              "name": "Shivaxi",
              "slug": "shivaxi",
              "url": "https://www.curseforge.com/members/11806322-shivaxi?username=shivaxi",
              "updated_at": "2020-05-16T05:25:45.000000Z"
            },
            {
              "id": 2,
              "curse_user_id": 25021665,
              "twitch_id": 110915960,
              "name": "Friedrich_LP",
              "slug": "friedrich-lp",
              "url": "https://www.curseforge.com/members/25021665-friedrich_lp?username=friedrich_lp",
              "updated_at": "2020-05-16T05:25:45.000000Z"
            },
            {
              "id": 3,
              "curse_user_id": 7807103,
              "twitch_id": 156102433,
              "name": "Alvtron",
              "slug": "alvtron",
              "url": "https://www.curseforge.com/members/7807103-alvtron?username=alvtron",
              "updated_at": "2020-05-16T05:25:45.000000Z"
            }
          ],
          "links": {
            "first": "https://www.modpackindex.com/api/v1/authors?page=1",
            "last": "https://www.modpackindex.com/api/v1/authors?page=7551",
            "prev": null,
            "next": "https://www.modpackindex.com/api/v1/authors?page=2"
          },
          "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 7551,
            "path": "https://www.modpackindex.com/api/v1/authors",
            "per_page": "3",
            "to": 3,
            "total": 22652
          }
        }

### Get Author [GET /author/{author_id}]

Returns an Author including any attached mods or modpacks.

+ Parameters
    + author_id (number) - Set author id.

+ Response 200 (application/json)

        {
          "data": {
            "id": 1,
            "curse_user_id": 11806322,
            "twitch_id": 39682137,
            "name": "Shivaxi",
            "slug": "shivaxi",
            "url": "https://www.curseforge.com/members/11806322-shivaxi?username=shivaxi",
            "modpacks": [
              {
                "id": 4123,
                "name": "RLCraft",
                "slug": "rlcraft",
                "summary": "A modpack specially designed to bring an incredibly hardcore and semi-realism challenge revolving around survival, RPG elements, and adventure-like exploration.",
                "download_count": 4299114,
                "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/136/944/256/256/636511227443004307.png",
                "primary_language": "enUS",
                "popularity_rank": 363,
                "latest_release_date": "2020-04-20 08:11:34",
                "last_modified": "2020-05-18 01:21:05",
                "last_updated": "2020-05-18T02:05:02.000000Z"
              }
            ],
            "mods": [
              {
                "id": 7030,
                "name": "Potion Rings",
                "slug": "potion-rings",
                "summary": "Adds simple bauble rings with potion effects.  REDUX version for RLCraft.",
                "download_count": 530071,
                "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/228/980/256/256/637053056865956072.png",
                "primary_language": "enUS",
                "popularity_rank": 419,
                "latest_release_date": "2019-11-10 17:35:53",
                "last_modified": "2019-11-13 07:36:52",
                "last_updated": "2020-05-16T05:32:58.000000Z"
              }
            ],
            "updated_at": "2020-05-16T05:25:45.000000Z"
          }
        }

## Categories [/categories{?limit}{?page}]

### Get Categories [GET]

Returns a list of categories.

+ Parameters
    + limit: `3` (number, optional) - &#35; of results to return (Max: 100).
        + Default: `25`
    + page: `1` (number, optional) - Current page of results.

+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "curse_id": 423,
              "name": "Map and Information",
              "slug": "map-and-information",
              "summary": null,
              "thumbnail_url": "https://media.forgecdn.net/avatars/6/38/635351497437388438.png",
              "curse_parent_game_category_id": 6,
              "curse_root_game_category_id": 6,
              "curse_game_id": 432,
              "curse_date_modified": "2014-05-08 17:42:23",
              "updated_at": "2020-05-16T05:25:39.000000Z"
            },
            {
              "id": 2,
              "curse_id": 426,
              "name": "Addons",
              "slug": "addons",
              "summary": null,
              "thumbnail_url": "https://media.forgecdn.net/avatars/5/998/635351477886290676.png",
              "curse_parent_game_category_id": 6,
              "curse_root_game_category_id": 6,
              "curse_game_id": 432,
              "curse_date_modified": "2014-05-08 17:09:48",
              "updated_at": "2020-05-16T05:25:39.000000Z"
            },
            {
              "id": 3,
              "curse_id": 434,
              "name": "Armor, Tools, and Weapons",
              "slug": "armor-tools-and-weapons",
              "summary": null,
              "thumbnail_url": "https://media.forgecdn.net/avatars/6/47/635351498790409758.png",
              "curse_parent_game_category_id": 6,
              "curse_root_game_category_id": 6,
              "curse_game_id": 432,
              "curse_date_modified": "2014-05-08 17:44:39",
              "updated_at": "2020-05-16T05:25:39.000000Z"
            }
          ],
          "links": {
            "first": "https://www.modpackindex.com/api/v1/categories?page=1",
            "last": "https://www.modpackindex.com/api/v1/categories?page=23",
            "prev": null,
            "next": "https://www.modpackindex.com/api/v1/categories?page=2"
          },
          "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 23,
            "path": "https://www.modpackindex.com/api/v1/categories",
            "per_page": "3",
            "to": 3,
            "total": 67
          }
        }

### Get Category [GET /category/{category_id}]

Returns details for a specific category

+ Parameters
    + category_id: `9` (number, required) - Set category id.

+ Response 200 (application/json)

        {
          "data": {
            "id": 9,
            "curse_id": 412,
            "name": "Technology",
            "slug": "technology",
            "summary": null,
            "thumbnail_url": "https://media.forgecdn.net/avatars/6/27/635351494745973439.png",
            "curse_parent_game_category_id": 6,
            "curse_root_game_category_id": 6,
            "curse_game_id": 432,
            "curse_date_modified": "2014-05-08 17:37:54",
            "updated_at": "2020-05-16T05:25:39.000000Z"
          }
        }
        
### Get Category Mods [GET /category/{category_id}/mods{?limit}{?page}]

Return mods that belong to a specific category

+ Parameters
    + category_id: `1` (number, required) - Set category id.
    + limit: `3` (number, optional) - &#35; of results to return (Max: 100).
        + Default: `25`
    + page: `1` (number, optional) - Current page of results.


+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "name": "Just Enough Items (JEI)",
              "slug": "just-enough-items-jei",
              "summary": "View Items and Recipes",
              "download_count": 70499629,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/29/69/256/256/635838945588716414.jpeg",
              "primary_language": "enUS",
              "popularity_rank": 1,
              "latest_release_date": "2019-10-07 01:20:32",
              "last_modified": "2020-04-30 06:06:29",
              "last_updated": "2020-05-16T05:30:15.000000Z"
            },
            {
              "id": 2,
              "name": "JourneyMap",
              "slug": "journeymap",
              "summary": "Real-time mapping in-game or your browser as you explore.",
              "download_count": 72714055,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/9/144/256/256/635421614078544069.png",
              "primary_language": "enUS",
              "popularity_rank": 2,
              "latest_release_date": "2020-03-29 21:09:22",
              "last_modified": "2020-05-02 21:12:00",
              "last_updated": "2020-05-16T05:30:15.000000Z"
            },
            {
              "id": 3,
              "name": "AppleSkin",
              "slug": "appleskin",
              "summary": "Adds some useful information about food/hunger to the HUD",
              "download_count": 45469152,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/47/527/256/256/636066936394500688.png",
              "primary_language": "enUS",
              "popularity_rank": 9,
              "latest_release_date": "2020-02-17 08:32:07",
              "last_modified": "2020-04-24 06:50:27",
              "last_updated": "2020-05-18T01:00:02.000000Z"
            }
          ],
          "links": {
            "first": "https://www.modpackindex.com/api/v1/category/1/mods?page=1",
            "last": "https://www.modpackindex.com/api/v1/category/1/mods?page=325",
            "prev": null,
            "next": "https://www.modpackindex.com/api/v1/category/1/mods?page=2"
          },
          "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 325,
            "path": "https://www.modpackindex.com/api/v1/category/1/mods",
            "per_page": "3",
            "to": 3,
            "total": 975
          }
        }
        
### Get Category Modpacks [GET /category/{category_id}/modpacks{?limit}{?page}]

Return mods that belong to a specific category

+ Parameters
    + category_id: `40` (number, required) - Set category id.
    + limit: `3` (number, optional) - &#35; of results to return (Max: 100).
        + Default: `25`
    + page: `1` (number, optional) - Current page of results.


+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 8,
              "name": "Cult of Orange",
              "slug": "cult-of-orange",
              "summary": "Internal custom modpack",
              "download_count": 41,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/268/750/256/256/637239593764549640.jpeg",
              "primary_language": "enUS",
              "popularity_rank": 29731,
              "latest_release_date": "2020-05-06 02:01:11",
              "last_modified": "2020-05-06 02:04:07",
              "last_updated": "2020-05-16T05:46:19.000000Z"
            },
            {
              "id": 9,
              "name": "Creserver 4",
              "slug": "creserver-4",
              "summary": "Glam and Unstable 1.15 modpack.",
              "download_count": 12,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/246/925/256/256/637160396083409610.jpeg",
              "primary_language": "koKR",
              "popularity_rank": 33405,
              "latest_release_date": "2020-02-12 16:13:32",
              "last_modified": "2020-02-12 16:20:57",
              "last_updated": "2020-05-16T05:46:19.000000Z"
            },
            {
              "id": 12,
              "name": "stal pack 3",
              "slug": "stal-pack-3",
              "summary": "A lightweight tech modpack for friends",
              "download_count": 2,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/250/86/256/256/637176782570561793.png",
              "primary_language": "enUS",
              "popularity_rank": 100000,
              "latest_release_date": "2020-02-19 03:05:41",
              "last_modified": "2020-02-19 20:09:15",
              "last_updated": "2020-05-16T05:46:19.000000Z"
            }
          ],
          "links": {
            "first": "https://www.modpackindex.com/api/v1/category/40/modpacks?page=1",
            "last": "https://www.modpackindex.com/api/v1/category/40/modpacks?page=1555",
            "prev": null,
            "next": "https://www.modpackindex.com/api/v1/category/40/modpacks?page=2"
          },
          "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 1555,
            "path": "https://www.modpackindex.com/api/v1/category/40/modpacks",
            "per_page": "3",
            "to": 3,
            "total": 4663
          }
        }
        
## Launchers [/launchers]

### Get Launchers [GET]

Returns a list of launchers.

+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "name": "Curse",
              "slug": "curse",
              "url": "https://www.curseforge.com/minecraft/modpacks",
              "download_url": "https://www.twitch.tv/downloads",
              "updated_at": "2020-05-16T05:25:34.000000Z"
            }
          ]
        }

### Get Launcher [GET /launcher/{launcher_id}]

Returns details for a specific launcher.

+ Parameters
    + launcher_id: `1` (number, required) - Set launcher id.

+ Response 200 (application/json)

        {
          "data": {
            "id": 1,
            "name": "Curse",
            "slug": "curse",
            "url": "https://www.curseforge.com/minecraft/modpacks",
            "download_url": "https://www.twitch.tv/downloads",
            "updated_at": "2020-05-16T05:25:34.000000Z"
          }
        }
        
### Get Launcher Mods [GET /launcher/{launcher_id}/mods{?limit}{?page}]

Return mods that belong to a specific launcher.

+ Parameters
    + launcher_id: `1` (number, required) - Set laucher id.
    + limit: `3` (number, optional) - &#35; of results to return (Max: 100).
        + Default: `25`
    + page: `1` (number, optional) - Current page of results.


+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "name": "Just Enough Items (JEI)",
              "slug": "just-enough-items-jei",
              "summary": "View Items and Recipes",
              "download_count": 70499629,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/29/69/256/256/635838945588716414.jpeg",
              "primary_language": "enUS",
              "popularity_rank": 1,
              "latest_release_date": "2019-10-07 01:20:32",
              "last_modified": "2020-04-30 06:06:29",
              "last_updated": "2020-05-16T05:30:15.000000Z"
            },
            {
              "id": 2,
              "name": "JourneyMap",
              "slug": "journeymap",
              "summary": "Real-time mapping in-game or your browser as you explore.",
              "download_count": 72714055,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/9/144/256/256/635421614078544069.png",
              "primary_language": "enUS",
              "popularity_rank": 2,
              "latest_release_date": "2020-03-29 21:09:22",
              "last_modified": "2020-05-02 21:12:00",
              "last_updated": "2020-05-16T05:30:15.000000Z"
            },
            {
              "id": 3,
              "name": "AppleSkin",
              "slug": "appleskin",
              "summary": "Adds some useful information about food/hunger to the HUD",
              "download_count": 45469152,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/47/527/256/256/636066936394500688.png",
              "primary_language": "enUS",
              "popularity_rank": 9,
              "latest_release_date": "2020-02-17 08:32:07",
              "last_modified": "2020-04-24 06:50:27",
              "last_updated": "2020-05-18T01:00:02.000000Z"
            }
          ],
          "links": {
            "first": "https://www.modpackindex.com/api/v1/launcher/1/mods?page=1",
            "last": "https://www.modpackindex.com/api/v1/launcher/1/mods?page=5363",
            "prev": null,
            "next": "https://www.modpackindex.com/api/v1/launcher/1/mods?page=2"
          },
          "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 5363,
            "path": "https://www.modpackindex.com/api/v1/launcher/1/mods",
            "per_page": "3",
            "to": 3,
            "total": 16089
          }
        }
        
### Get Launcher Modpacks [GET /launcher/{launcher_id}/modpacks{?limit}{?page}]

Return mods that belong to a specific launcher.

+ Parameters
    + launcher_id: `40` (number, required) - Set launcher id.
    + limit: `3` (number, optional) - &#35; of results to return (Max: 100).
        + Default: `25`
    + page: `1` (number, optional) - Current page of results.


+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 8,
              "name": "Cult of Orange",
              "slug": "cult-of-orange",
              "summary": "Internal custom modpack",
              "download_count": 41,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/268/750/256/256/637239593764549640.jpeg",
              "primary_language": "enUS",
              "popularity_rank": 29731,
              "latest_release_date": "2020-05-06 02:01:11",
              "last_modified": "2020-05-06 02:04:07",
              "last_updated": "2020-05-16T05:46:19.000000Z"
            },
            {
              "id": 9,
              "name": "Creserver 4",
              "slug": "creserver-4",
              "summary": "Glam and Unstable 1.15 modpack.",
              "download_count": 12,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/246/925/256/256/637160396083409610.jpeg",
              "primary_language": "koKR",
              "popularity_rank": 33405,
              "latest_release_date": "2020-02-12 16:13:32",
              "last_modified": "2020-02-12 16:20:57",
              "last_updated": "2020-05-16T05:46:19.000000Z"
            },
            {
              "id": 12,
              "name": "stal pack 3",
              "slug": "stal-pack-3",
              "summary": "A lightweight tech modpack for friends",
              "download_count": 2,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/250/86/256/256/637176782570561793.png",
              "primary_language": "enUS",
              "popularity_rank": 100000,
              "latest_release_date": "2020-02-19 03:05:41",
              "last_modified": "2020-02-19 20:09:15",
              "last_updated": "2020-05-16T05:46:19.000000Z"
            }
          ],
          "links": {
            "first": "https://www.modpackindex.com/api/v1/category/40/modpacks?page=1",
            "last": "https://www.modpackindex.com/api/v1/category/40/modpacks?page=1555",
            "prev": null,
            "next": "https://www.modpackindex.com/api/v1/category/40/modpacks?page=2"
          },
          "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 1555,
            "path": "https://www.modpackindex.com/api/v1/category/40/modpacks",
            "per_page": "3",
            "to": 3,
            "total": 4663
          }
        }
        
## Minecraft/Versions [/minecraft/versions]

### Get Minecraft Versions [GET]

Returns a list of Minecraft versions.

+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "curse_id": 64,
              "name": "1.15.2",
              "slug": "1-15-2",
              "curse_date_modified": "2020-01-21 15:28:39",
              "updated_at": "2020-05-16T05:25:42.000000Z"
            },
            {
              "id": 2,
              "curse_id": 63,
              "name": "1.15.1",
              "slug": "1-15-1",
              "curse_date_modified": "2019-12-17 13:27:03",
              "updated_at": "2020-05-16T05:25:42.000000Z"
            },
            {
              "id": 3,
              "curse_id": 62,
              "name": "1.15",
              "slug": "1-15",
              "curse_date_modified": "2019-12-10 15:26:51",
              "updated_at": "2020-05-16T05:25:42.000000Z"
            }]
        }

### Get Minecraft Version [GET /minecraft/version/{version_id}]

Returns details for a specific Minecraft version.

+ Parameters
    + version_id: `1` (number, required) - Set version id.

+ Response 200 (application/json)

        {
          "data": {
            "id": 1,
            "curse_id": 64,
            "name": "1.15.2",
            "slug": "1-15-2",
            "curse_date_modified": "2020-01-21 15:28:39",
            "updated_at": "2020-05-16T05:25:42.000000Z"
          }
        }
        
### Get Minecraft Version Mods [GET /minecraft/version/{version_id}/mods{?limit}{?page}]

Return mods that belong to a specific Minecraft version.

+ Parameters
    + version_id: `1` (number, required) - Set version id.
    + limit: `3` (number, optional) - &#35; of results to return (Max: 100)
        + Default: `25`
    + page: `1` (number, optional) - Current page of results.


+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "name": "Just Enough Items (JEI)",
              "slug": "just-enough-items-jei",
              "summary": "View Items and Recipes",
              "download_count": 70499629,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/29/69/256/256/635838945588716414.jpeg",
              "primary_language": "enUS",
              "popularity_rank": 1,
              "latest_release_date": "2019-10-07 01:20:32",
              "last_modified": "2020-04-30 06:06:29",
              "last_updated": "2020-05-16T05:30:15.000000Z"
            },
            {
              "id": 2,
              "name": "JourneyMap",
              "slug": "journeymap",
              "summary": "Real-time mapping in-game or your browser as you explore.",
              "download_count": 72714055,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/9/144/256/256/635421614078544069.png",
              "primary_language": "enUS",
              "popularity_rank": 2,
              "latest_release_date": "2020-03-29 21:09:22",
              "last_modified": "2020-05-02 21:12:00",
              "last_updated": "2020-05-16T05:30:15.000000Z"
            },
            {
              "id": 3,
              "name": "AppleSkin",
              "slug": "appleskin",
              "summary": "Adds some useful information about food/hunger to the HUD",
              "download_count": 45469152,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/47/527/256/256/636066936394500688.png",
              "primary_language": "enUS",
              "popularity_rank": 9,
              "latest_release_date": "2020-02-17 08:32:07",
              "last_modified": "2020-04-24 06:50:27",
              "last_updated": "2020-05-18T01:00:02.000000Z"
            }
          ],
          "links": {
            "first": "https://www.modpackindex.com/api/v1/minecraft/version/1/mods?page=1",
            "last": "https://www.modpackindex.com/api/v1/minecraft/version/1/mods?page=767",
            "prev": null,
            "next": "https://www.modpackindex.com/api/v1/minecraft/version/1/mods?page=2"
          },
          "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 767,
            "path": "https://www.modpackindex.com/api/v1/minecraft/version/1/mods",
            "per_page": "3",
            "to": 3,
            "total": 2300
          }
        }
        
### Get Minecraft Version Modpacks [GET /minecraft/version/{version_id}/modpacks{?limit}{?page}]

Return modpacks that belong to a specific Minecraft version.

+ Parameters
    + version_id: `1` (number, required) - Set version id.
    + limit: `3` (number, optional) - &#35; of results to return (Max: 100).
        + Default: `25`
    + page: `1` (number, optional) - Current page of results.


+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "name": "Technical Electrical V",
              "slug": "technical-electrical-v",
              "summary": "A modpack which aims to created a fun experience whilst making new friends!",
              "download_count": 1363,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/251/875/256/256/637185882228313665.png",
              "primary_language": "enUS",
              "popularity_rank": 8443,
              "latest_release_date": "2020-05-19 16:02:02",
              "last_modified": "2020-05-19 16:05:09",
              "last_updated": "2020-05-19T16:09:05.000000Z"
            },
            {
              "id": 2,
              "name": "Marvelous Mechanization",
              "slug": "marvelous-mechanization",
              "summary": "A modpack centered around technology",
              "download_count": 422,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/248/933/256/256/637170983676174731.png",
              "primary_language": "enUS",
              "popularity_rank": 9740,
              "latest_release_date": "2020-03-03 02:14:47",
              "last_modified": "2020-03-07 15:24:08",
              "last_updated": "2020-05-16T05:46:18.000000Z"
            },
            {
              "id": 3,
              "name": "ThunderCraft",
              "slug": "thundercraft",
              "summary": "Plenty of usefull mods ,Biomes ,Tools,Mekanism,Mobs,New Nether",
              "download_count": 81,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/254/790/256/256/637199699292644894.png",
              "primary_language": "enUS",
              "popularity_rank": 17940,
              "latest_release_date": "2020-03-21 09:49:01",
              "last_modified": "2020-03-30 13:40:51",
              "last_updated": "2020-05-16T05:46:18.000000Z"
            }
          ],
          "links": {
            "first": "https://www.modpackindex.com/api/v1/minecraft/version/1/modpacks?page=1",
            "last": "https://www.modpackindex.com/api/v1/minecraft/version/1/modpacks?page=218",
            "prev": null,
            "next": "https://www.modpackindex.com/api/v1/minecraft/version/1/modpacks?page=2"
          },
          "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 218,
            "path": "https://www.modpackindex.com/api/v1/minecraft/version/1/modpacks",
            "per_page": "3",
            "to": 3,
            "total": 654
          }
        }
        
## Modpacks [/modpacks{?limit}{?page}]

### Get Modpacks [GET]

Returns a list of Modpacks.

+ Parameters
    + limit: `3` (number, optional) - &#35; of results to return (Max: 100).
        + Default: `25`
    + page: `1` (number, optional) - Current page of results.


+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "name": "Technical Electrical V",
              "slug": "technical-electrical-v",
              "summary": "A modpack which aims to created a fun experience whilst making new friends!",
              "download_count": 1363,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/251/875/256/256/637185882228313665.png",
              "primary_language": "enUS",
              "popularity_rank": 8443,
              "latest_release_date": "2020-05-19 16:02:02",
              "last_modified": "2020-05-19 16:05:09",
              "last_updated": "2020-05-19T16:09:05.000000Z"
            },
            {
              "id": 2,
              "name": "Marvelous Mechanization",
              "slug": "marvelous-mechanization",
              "summary": "A modpack centered around technology",
              "download_count": 422,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/248/933/256/256/637170983676174731.png",
              "primary_language": "enUS",
              "popularity_rank": 9740,
              "latest_release_date": "2020-03-03 02:14:47",
              "last_modified": "2020-03-07 15:24:08",
              "last_updated": "2020-05-16T05:46:18.000000Z"
            },
            {
              "id": 3,
              "name": "ThunderCraft",
              "slug": "thundercraft",
              "summary": "Plenty of usefull mods ,Biomes ,Tools,Mekanism,Mobs,New Nether",
              "download_count": 81,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/254/790/256/256/637199699292644894.png",
              "primary_language": "enUS",
              "popularity_rank": 17940,
              "latest_release_date": "2020-03-21 09:49:01",
              "last_modified": "2020-03-30 13:40:51",
              "last_updated": "2020-05-16T05:46:18.000000Z"
            }
          ],
          "links": {
            "first": "https://www.modpackindex.com/api/v1/modpacks?page=1",
            "last": "https://www.modpackindex.com/api/v1/modpacks?page=6782",
            "prev": null,
            "next": "https://www.modpackindex.com/api/v1/modpacks?page=2"
          },
          "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 6782,
            "path": "https://www.modpackindex.com/api/v1/modpacks",
            "per_page": "3",
            "to": 3,
            "total": 20344
          }
        }

### Get Modpack [GET /modpack/{modpack_id}]

Returns details for a specific Modpacks.

+ Parameters
    + modpack_id: `332` (number, required) - Set page for results.

+ Response 200 (application/json)

        {
          "data": {
            "id": 332,
            "name": "Valhelsia 2",
            "slug": "valhelsia-2",
            "summary": "Valhelsia 2 is a 1.15.2 modpack with a mix of technology, magic, exploration and adventure...",
            "categories": [
              {
                "id": 44,
                "curse_id": 4484,
                "name": "Multiplayer",
                "slug": "multiplayer",
                "summary": null,
                "thumbnail_url": "https://media.forgecdn.net/avatars/14/481/635596792838491141.png",
                "curse_parent_game_category_id": 4471,
                "curse_root_game_category_id": 4471,
                "curse_game_id": 432,
                "curse_date_modified": "2015-02-16 16:28:03",
                "updated_at": "2020-05-16T05:25:40.000000Z"
              },
              {
                "id": 45,
                "curse_id": 4476,
                "name": "Exploration",
                "slug": "exploration",
                "summary": null,
                "thumbnail_url": "https://media.forgecdn.net/avatars/14/486/635596815896417213.png",
                "curse_parent_game_category_id": 4471,
                "curse_root_game_category_id": 4471,
                "curse_game_id": 432,
                "curse_date_modified": "2015-02-16 17:06:29",
                "updated_at": "2020-05-16T05:25:40.000000Z"
              },
              {
                "id": 47,
                "curse_id": 4475,
                "name": "Adventure and RPG",
                "slug": "adventure-and-rpg",
                "summary": null,
                "thumbnail_url": "https://media.forgecdn.net/avatars/14/480/635596775049811800.png",
                "curse_parent_game_category_id": 4471,
                "curse_root_game_category_id": 4471,
                "curse_game_id": 432,
                "curse_date_modified": "2015-02-16 15:58:24",
                "updated_at": "2020-05-16T05:25:40.000000Z"
              },
              {
                "id": 51,
                "curse_id": 4472,
                "name": "Tech",
                "slug": "tech",
                "summary": null,
                "thumbnail_url": "https://media.forgecdn.net/avatars/14/479/635596761534662757.png",
                "curse_parent_game_category_id": 4471,
                "curse_root_game_category_id": 4471,
                "curse_game_id": 432,
                "curse_date_modified": "2015-02-16 15:35:53",
                "updated_at": "2020-05-16T05:25:40.000000Z"
              },
              {
                "id": 53,
                "curse_id": 4473,
                "name": "Magic",
                "slug": "magic",
                "summary": null,
                "thumbnail_url": "https://media.forgecdn.net/avatars/14/474/635596760578719019.png",
                "curse_parent_game_category_id": 4471,
                "curse_root_game_category_id": 4471,
                "curse_game_id": 432,
                "curse_date_modified": "2015-02-16 15:34:17",
                "updated_at": "2020-05-16T05:25:40.000000Z"
              }
            ],
            "authors": [
              {
                "id": 5524,
                "curse_user_id": 27340255,
                "twitch_id": 99659853,
                "name": "Khytwel",
                "slug": "khytwel",
                "url": "https://www.curseforge.com/members/27340255-khytwel?username=khytwel",
                "updated_at": "2020-05-16T05:32:15.000000Z"
              }
            ],
            "launchers": [
              {
                "id": 1,
                "name": "Curse",
                "slug": "curse",
                "url": "https://www.curseforge.com/minecraft/modpacks",
                "download_url": "https://www.twitch.tv/downloads",
                "updated_at": "2020-05-16T05:25:34.000000Z"
              }
            ],
            "minecraft_versions": [
              {
                "id": 1,
                "curse_id": 64,
                "name": "1.15.2",
                "slug": "1-15-2",
                "curse_date_modified": "2020-01-21 15:28:39",
                "updated_at": "2020-05-16T05:25:42.000000Z"
              }
            ],
            "download_count": 625868,
            "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/243/784/256/256/637141898688438989.png",
            "primary_language": "enUS",
            "popularity_rank": 760,
            "latest_release_date": "2020-05-23 12:52:25",
            "last_modified": "2020-05-23 12:58:52",
            "last_updated": "2020-05-23T13:09:03.000000Z"
          }
        }
        
### Get Modpack Mods [GET /modpack/{modpack_id}/mods]

Return mods that in a specific modpack.

+ Parameters
    + modpack_id: `332` (number, required) - Set modpack id.


+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "name": "Just Enough Items (JEI)",
              "slug": "just-enough-items-jei",
              "summary": "View Items and Recipes",
              "download_count": 70499629,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/29/69/256/256/635838945588716414.jpeg",
              "primary_language": "enUS",
              "popularity_rank": 1,
              "latest_release_date": "2019-10-07 01:20:32",
              "last_modified": "2020-04-30 06:06:29",
              "last_updated": "2020-05-16T05:30:15.000000Z"
            },
            {
              "id": 3,
              "name": "AppleSkin",
              "slug": "appleskin",
              "summary": "Adds some useful information about food/hunger to the HUD",
              "download_count": 45469152,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/47/527/256/256/636066936394500688.png",
              "primary_language": "enUS",
              "popularity_rank": 9,
              "latest_release_date": "2020-02-17 08:32:07",
              "last_modified": "2020-04-24 06:50:27",
              "last_updated": "2020-05-18T01:00:02.000000Z"
            },
            {
              "id": 4,
              "name": "Hwyla",
              "slug": "hwyla",
              "summary": "Hwyla (Here's What You're Looking At) is a UI improvement mod aimed at providing block information directly in-game. It is also a fork of Waila.",
              "download_count": 26677083,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/63/499/256/256/636143286314870563_animated.gif",
              "primary_language": "enUS",
              "popularity_rank": 25,
              "latest_release_date": "2020-04-15 23:26:12",
              "last_modified": "2020-04-15 23:33:22",
              "last_updated": "2020-05-18T01:00:02.000000Z"
            },
            {
              "id": 7,
              "name": "Neat",
              "slug": "neat",
              "summary": "Minimalistic Functional Unit Frames for the modern Minecrafter",
              "download_count": 26823096,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/29/326/256/256/635843253254829591.png",
              "primary_language": "enUS",
              "popularity_rank": 44,
              "latest_release_date": "2020-05-15 15:05:10",
              "last_modified": "2020-05-15 15:05:36",
              "last_updated": "2020-05-16T05:30:15.000000Z"
            },
            {
              "id": 12,
              "name": "Nature's Compass",
              "slug": "natures-compass",
              "summary": "Nature's Compass is a utility item that allows you to search for a biome's location anywhere in the world and view information about it.",
              "download_count": 15106135,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/54/102/256/256/636131217371752080.png",
              "primary_language": "enUS",
              "popularity_rank": 99,
              "latest_release_date": "2020-03-03 00:15:35",
              "last_modified": "2020-03-03 00:17:00",
              "last_updated": "2020-05-18T01:00:03.000000Z"
            }]
        }
        
## Mods [/mods{?limit}{?page}]

### Get Mods [GET]

Returns a list of mods.

+ Parameters
    + limit: `3` (number, optional) - &#35; of results to return (Max: 100).
        + Default: `25`
    + page: `1` (number, optional) - Current page of results.


+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "name": "Just Enough Items (JEI)",
              "slug": "just-enough-items-jei",
              "summary": "View Items and Recipes",
              "categories": [
                {
                  "id": 1,
                  "curse_id": 423,
                  "name": "Map and Information",
                  "slug": "map-and-information",
                  "summary": null,
                  "thumbnail_url": "https://media.forgecdn.net/avatars/6/38/635351497437388438.png",
                  "curse_parent_game_category_id": 6,
                  "curse_root_game_category_id": 6,
                  "curse_game_id": 432,
                  "curse_date_modified": "2014-05-08 17:42:23",
                  "updated_at": "2020-05-16T05:25:39.000000Z"
                },
                {
                  "id": 28,
                  "curse_id": 421,
                  "name": "API and Library",
                  "slug": "api-and-library",
                  "summary": null,
                  "thumbnail_url": "https://media.forgecdn.net/avatars/6/36/635351496947765531.png",
                  "curse_parent_game_category_id": 6,
                  "curse_root_game_category_id": 6,
                  "curse_game_id": 432,
                  "curse_date_modified": "2014-05-23 03:21:44",
                  "updated_at": "2020-05-16T05:25:39.000000Z"
                }
              ],
              "authors": [
                {
                  "id": 1580,
                  "curse_user_id": 17072262,
                  "twitch_id": 56761389,
                  "name": "mezz",
                  "slug": "mezz",
                  "url": "https://www.curseforge.com/members/17072262-mezz?username=mezz",
                  "updated_at": "2020-05-16T05:30:15.000000Z"
                }
              ],
              "launchers": [
                {
                  "id": 1,
                  "name": "Curse",
                  "slug": "curse",
                  "url": "https://www.curseforge.com/minecraft/modpacks",
                  "download_url": "https://www.twitch.tv/downloads",
                  "updated_at": "2020-05-16T05:25:34.000000Z"
                }
              ],
              "minecraft_versions": [
                {
                  "id": 1,
                  "curse_id": 64,
                  "name": "1.15.2",
                  "slug": "1-15-2",
                  "curse_date_modified": "2020-01-21 15:28:39",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 2,
                  "curse_id": 63,
                  "name": "1.15.1",
                  "slug": "1-15-1",
                  "curse_date_modified": "2019-12-17 13:27:03",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 4,
                  "curse_id": 61,
                  "name": "1.14.4",
                  "slug": "1-14-4",
                  "curse_date_modified": "2019-07-19 10:47:20",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 5,
                  "curse_id": 60,
                  "name": "1.14.3",
                  "slug": "1-14-3",
                  "curse_date_modified": "2019-06-24 15:46:57",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 6,
                  "curse_id": 59,
                  "name": "1.14.2",
                  "slug": "1-14-2",
                  "curse_date_modified": "2019-05-27 12:46:26",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 9,
                  "curse_id": 56,
                  "name": "1.13.2",
                  "slug": "1-13-2",
                  "curse_date_modified": "2018-10-22 12:49:51",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 12,
                  "curse_id": 52,
                  "name": "1.12.2",
                  "slug": "1-12-2",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 13,
                  "curse_id": 51,
                  "name": "1.12.1",
                  "slug": "1-12-1",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 14,
                  "curse_id": 50,
                  "name": "1.12",
                  "slug": "1-12",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 15,
                  "curse_id": 49,
                  "name": "1.11.2",
                  "slug": "1-11-2",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 17,
                  "curse_id": 47,
                  "name": "1.11",
                  "slug": "1-11",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 18,
                  "curse_id": 46,
                  "name": "1.10.2",
                  "slug": "1-10-2",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 20,
                  "curse_id": 44,
                  "name": "1.10",
                  "slug": "1-10",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 21,
                  "curse_id": 42,
                  "name": "1.9.4",
                  "slug": "1-9-4",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 25,
                  "curse_id": 39,
                  "name": "1.9",
                  "slug": "1-9",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 26,
                  "curse_id": 34,
                  "name": "1.8.9",
                  "slug": "1-8-9",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 27,
                  "curse_id": 33,
                  "name": "1.8.8",
                  "slug": "1-8-8",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 35,
                  "curse_id": 7,
                  "name": "1.8",
                  "slug": "1-8",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                }
              ],
              "download_count": 70499629,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/29/69/256/256/635838945588716414.jpeg",
              "primary_language": "enUS",
              "popularity_rank": 1,
              "latest_release_date": "2019-10-07 01:20:32",
              "last_modified": "2020-04-30 06:06:29",
              "last_updated": "2020-05-16T05:30:15.000000Z"
            },
            {
              "id": 2,
              "name": "JourneyMap",
              "slug": "journeymap",
              "summary": "Real-time mapping in-game or your browser as you explore.",
              "categories": [
                {
                  "id": 1,
                  "curse_id": 423,
                  "name": "Map and Information",
                  "slug": "map-and-information",
                  "summary": null,
                  "thumbnail_url": "https://media.forgecdn.net/avatars/6/38/635351497437388438.png",
                  "curse_parent_game_category_id": 6,
                  "curse_root_game_category_id": 6,
                  "curse_game_id": 432,
                  "curse_date_modified": "2014-05-08 17:42:23",
                  "updated_at": "2020-05-16T05:25:39.000000Z"
                }
              ],
              "authors": [
                {
                  "id": 1581,
                  "curse_user_id": 7577665,
                  "twitch_id": 55544864,
                  "name": "techbrew",
                  "slug": "techbrew",
                  "url": "https://www.curseforge.com/members/7577665-techbrew?username=techbrew",
                  "updated_at": "2020-05-16T05:30:15.000000Z"
                },
                {
                  "id": 1582,
                  "curse_user_id": 9422784,
                  "twitch_id": 26913375,
                  "name": "Mysticdrew",
                  "slug": "mysticdrew",
                  "url": "https://www.curseforge.com/members/9422784-mysticdrew?username=mysticdrew",
                  "updated_at": "2020-05-16T05:30:15.000000Z"
                }
              ],
              "launchers": [
                {
                  "id": 1,
                  "name": "Curse",
                  "slug": "curse",
                  "url": "https://www.curseforge.com/minecraft/modpacks",
                  "download_url": "https://www.twitch.tv/downloads",
                  "updated_at": "2020-05-16T05:25:34.000000Z"
                }
              ],
              "minecraft_versions": [
                {
                  "id": 1,
                  "curse_id": 64,
                  "name": "1.15.2",
                  "slug": "1-15-2",
                  "curse_date_modified": "2020-01-21 15:28:39",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 4,
                  "curse_id": 61,
                  "name": "1.14.4",
                  "slug": "1-14-4",
                  "curse_date_modified": "2019-07-19 10:47:20",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 12,
                  "curse_id": 52,
                  "name": "1.12.2",
                  "slug": "1-12-2",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 13,
                  "curse_id": 51,
                  "name": "1.12.1",
                  "slug": "1-12-1",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 14,
                  "curse_id": 50,
                  "name": "1.12",
                  "slug": "1-12",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 15,
                  "curse_id": 49,
                  "name": "1.11.2",
                  "slug": "1-11-2",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 17,
                  "curse_id": 47,
                  "name": "1.11",
                  "slug": "1-11",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 18,
                  "curse_id": 46,
                  "name": "1.10.2",
                  "slug": "1-10-2",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 21,
                  "curse_id": 42,
                  "name": "1.9.4",
                  "slug": "1-9-4",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 25,
                  "curse_id": 39,
                  "name": "1.9",
                  "slug": "1-9",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 26,
                  "curse_id": 34,
                  "name": "1.8.9",
                  "slug": "1-8-9",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 27,
                  "curse_id": 33,
                  "name": "1.8.8",
                  "slug": "1-8-8",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 35,
                  "curse_id": 7,
                  "name": "1.8",
                  "slug": "1-8",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 36,
                  "curse_id": 8,
                  "name": "1.7.10",
                  "slug": "1-7-10",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 44,
                  "curse_id": 12,
                  "name": "1.7.2",
                  "slug": "1-7-2",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 45,
                  "curse_id": 13,
                  "name": "1.6.4",
                  "slug": "1-6-4",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 48,
                  "curse_id": 16,
                  "name": "1.5.2",
                  "slug": "1-5-2",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 50,
                  "curse_id": 18,
                  "name": "1.4.7",
                  "slug": "1-4-7",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 62,
                  "curse_id": 30,
                  "name": "1.1",
                  "slug": "1-1",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                }
              ],
              "download_count": 72714055,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/9/144/256/256/635421614078544069.png",
              "primary_language": "enUS",
              "popularity_rank": 2,
              "latest_release_date": "2020-03-29 21:09:22",
              "last_modified": "2020-05-02 21:12:00",
              "last_updated": "2020-05-16T05:30:15.000000Z"
            },
            {
              "id": 3,
              "name": "AppleSkin",
              "slug": "appleskin",
              "summary": "Adds some useful information about food/hunger to the HUD",
              "categories": [
                {
                  "id": 1,
                  "curse_id": 423,
                  "name": "Map and Information",
                  "slug": "map-and-information",
                  "summary": null,
                  "thumbnail_url": "https://media.forgecdn.net/avatars/6/38/635351497437388438.png",
                  "curse_parent_game_category_id": 6,
                  "curse_root_game_category_id": 6,
                  "curse_game_id": 432,
                  "curse_date_modified": "2014-05-08 17:42:23",
                  "updated_at": "2020-05-16T05:25:39.000000Z"
                },
                {
                  "id": 30,
                  "curse_id": 4780,
                  "name": "Fabric",
                  "slug": "fabric",
                  "summary": null,
                  "thumbnail_url": "https://media.forgecdn.net/avatars/182/502/636808438426582276.png",
                  "curse_parent_game_category_id": 6,
                  "curse_root_game_category_id": 6,
                  "curse_game_id": 432,
                  "curse_date_modified": "2018-12-19 19:17:22",
                  "updated_at": "2020-05-16T05:25:40.000000Z"
                },
                {
                  "id": 37,
                  "curse_id": 436,
                  "name": "Food",
                  "slug": "food",
                  "summary": null,
                  "thumbnail_url": "https://media.forgecdn.net/avatars/6/49/635351499265510402.png",
                  "curse_parent_game_category_id": 6,
                  "curse_root_game_category_id": 6,
                  "curse_game_id": 432,
                  "curse_date_modified": "2014-05-08 17:45:26",
                  "updated_at": "2020-05-16T05:25:40.000000Z"
                }
              ],
              "authors": [
                {
                  "id": 1583,
                  "curse_user_id": 13914149,
                  "twitch_id": 22664026,
                  "name": "squeek502",
                  "slug": "squeek502",
                  "url": "https://www.curseforge.com/members/13914149-squeek502?username=squeek502",
                  "updated_at": "2020-05-16T05:30:15.000000Z"
                }
              ],
              "launchers": [
                {
                  "id": 1,
                  "name": "Curse",
                  "slug": "curse",
                  "url": "https://www.curseforge.com/minecraft/modpacks",
                  "download_url": "https://www.twitch.tv/downloads",
                  "updated_at": "2020-05-16T05:25:34.000000Z"
                }
              ],
              "minecraft_versions": [
                {
                  "id": 1,
                  "curse_id": 64,
                  "name": "1.15.2",
                  "slug": "1-15-2",
                  "curse_date_modified": "2020-01-21 15:28:39",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 2,
                  "curse_id": 63,
                  "name": "1.15.1",
                  "slug": "1-15-1",
                  "curse_date_modified": "2019-12-17 13:27:03",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 3,
                  "curse_id": 62,
                  "name": "1.15",
                  "slug": "1-15",
                  "curse_date_modified": "2019-12-10 15:26:51",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 4,
                  "curse_id": 61,
                  "name": "1.14.4",
                  "slug": "1-14-4",
                  "curse_date_modified": "2019-07-19 10:47:20",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 5,
                  "curse_id": 60,
                  "name": "1.14.3",
                  "slug": "1-14-3",
                  "curse_date_modified": "2019-06-24 15:46:57",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 6,
                  "curse_id": 59,
                  "name": "1.14.2",
                  "slug": "1-14-2",
                  "curse_date_modified": "2019-05-27 12:46:26",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 7,
                  "curse_id": 58,
                  "name": "1.14.1",
                  "slug": "1-14-1",
                  "curse_date_modified": "2019-05-13 12:46:10",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 8,
                  "curse_id": 57,
                  "name": "1.14",
                  "slug": "1-14",
                  "curse_date_modified": "2019-04-23 15:20:21",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 9,
                  "curse_id": 56,
                  "name": "1.13.2",
                  "slug": "1-13-2",
                  "curse_date_modified": "2018-10-22 12:49:51",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 12,
                  "curse_id": 52,
                  "name": "1.12.2",
                  "slug": "1-12-2",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 13,
                  "curse_id": 51,
                  "name": "1.12.1",
                  "slug": "1-12-1",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 14,
                  "curse_id": 50,
                  "name": "1.12",
                  "slug": "1-12",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 15,
                  "curse_id": 49,
                  "name": "1.11.2",
                  "slug": "1-11-2",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 17,
                  "curse_id": 47,
                  "name": "1.11",
                  "slug": "1-11",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                },
                {
                  "id": 18,
                  "curse_id": 46,
                  "name": "1.10.2",
                  "slug": "1-10-2",
                  "curse_date_modified": "2018-03-29 17:24:38",
                  "updated_at": "2020-05-16T05:25:42.000000Z"
                }
              ],
              "download_count": 45469152,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/47/527/256/256/636066936394500688.png",
              "primary_language": "enUS",
              "popularity_rank": 9,
              "latest_release_date": "2020-02-17 08:32:07",
              "last_modified": "2020-04-24 06:50:27",
              "last_updated": "2020-05-18T01:00:02.000000Z"
            }
          ],
          "links": {
            "first": "https://www.modpackindex.com/api/v1/mods?page=1",
            "last": "https://www.modpackindex.com/api/v1/mods?page=5363",
            "prev": null,
            "next": "https://www.modpackindex.com/api/v1/mods?page=2"
          },
          "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 5363,
            "path": "https://www.modpackindex.com/api/v1/mods",
            "per_page": "3",
            "to": 3,
            "total": 16089
          }
        }

### Get Mod [GET /mod/{mod_id}]

Returns details for a specific mod.

+ Parameters
    + mod_id: `10173` (number, required) - Set mod id.

+ Response 200 (application/json)

        {
          "data": {
            "id": 10173,
            "name": "Buzzier Bees",
            "slug": "buzzier-bees",
            "summary": "A mod that improves the content in Buzzy Bees.",
            "categories": [
              {
                "id": 25,
                "curse_id": 425,
                "name": "Miscellaneous",
                "slug": "miscellaneous",
                "summary": null,
                "thumbnail_url": "https://media.forgecdn.net/avatars/6/40/635351497693711265.png",
                "curse_parent_game_category_id": 6,
                "curse_root_game_category_id": 6,
                "curse_game_id": 432,
                "curse_date_modified": "2014-06-15 04:27:14",
                "updated_at": "2020-05-16T05:25:39.000000Z"
              },
              {
                "id": 32,
                "curse_id": 411,
                "name": "Mobs",
                "slug": "mobs",
                "summary": null,
                "thumbnail_url": "https://media.forgecdn.net/avatars/6/53/635351500195070414.png",
                "curse_parent_game_category_id": 406,
                "curse_root_game_category_id": 6,
                "curse_game_id": 432,
                "curse_date_modified": "2014-05-08 17:46:59",
                "updated_at": "2020-05-16T05:25:40.000000Z"
              },
              {
                "id": 37,
                "curse_id": 436,
                "name": "Food",
                "slug": "food",
                "summary": null,
                "thumbnail_url": "https://media.forgecdn.net/avatars/6/49/635351499265510402.png",
                "curse_parent_game_category_id": 6,
                "curse_root_game_category_id": 6,
                "curse_game_id": 432,
                "curse_date_modified": "2014-05-08 17:45:26",
                "updated_at": "2020-05-16T05:25:40.000000Z"
              }
            ],
            "authors": [
              {
                "id": 237,
                "curse_user_id": 100574250,
                "twitch_id": 160421636,
                "name": "bageldotjpg",
                "slug": "bageldotjpg",
                "url": "https://www.curseforge.com/members/100574250-bageldotjpg?username=bageldotjpg",
                "updated_at": "2020-05-16T05:25:58.000000Z"
              }
            ],
            "launchers": [
              {
                "id": 1,
                "name": "Curse",
                "slug": "curse",
                "url": "https://www.curseforge.com/minecraft/modpacks",
                "download_url": "https://www.twitch.tv/downloads",
                "updated_at": "2020-05-16T05:25:34.000000Z"
              }
            ],
            "minecraft_versions": [
              {
                "id": 1,
                "curse_id": 64,
                "name": "1.15.2",
                "slug": "1-15-2",
                "curse_date_modified": "2020-01-21 15:28:39",
                "updated_at": "2020-05-16T05:25:42.000000Z"
              },
              {
                "id": 2,
                "curse_id": 63,
                "name": "1.15.1",
                "slug": "1-15-1",
                "curse_date_modified": "2019-12-17 13:27:03",
                "updated_at": "2020-05-16T05:25:42.000000Z"
              }
            ],
            "download_count": 851238,
            "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/255/736/256/256/637202801943354580.png",
            "primary_language": "enUS",
            "popularity_rank": 549,
            "latest_release_date": "2020-05-15 23:24:22",
            "last_modified": "2020-05-15 23:25:49",
            "last_updated": "2020-05-16T05:37:33.000000Z"
          }
        }
        
### Get Mod Modpacks [GET /mod/{mod_id}/modpacks{?limit}{?page}]

Return modpacks that a specific mod is in.

+ Parameters
    + mod_id: `332` (number, required) - Set mod id.
    + limit: `3` (number, optional) - &#35; of results to return (Max: 100).
        + Default: `25`
    + page: `1` (number, optional) - Current page of results.


+ Response 200 (application/json)

        {
          "data": [
            {
              "id": 1,
              "name": "Technical Electrical V",
              "slug": "technical-electrical-v",
              "summary": "A modpack which aims to created a fun experience whilst making new friends!",
              "download_count": 1363,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/251/875/256/256/637185882228313665.png",
              "primary_language": "enUS",
              "popularity_rank": 8443,
              "latest_release_date": "2020-05-19 16:02:02",
              "last_modified": "2020-05-19 16:05:09",
              "last_updated": "2020-05-19T16:09:05.000000Z"
            },
            {
              "id": 2,
              "name": "Marvelous Mechanization",
              "slug": "marvelous-mechanization",
              "summary": "A modpack centered around technology",
              "download_count": 422,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/248/933/256/256/637170983676174731.png",
              "primary_language": "enUS",
              "popularity_rank": 9740,
              "latest_release_date": "2020-03-03 02:14:47",
              "last_modified": "2020-03-07 15:24:08",
              "last_updated": "2020-05-16T05:46:18.000000Z"
            },
            {
              "id": 3,
              "name": "ThunderCraft",
              "slug": "thundercraft",
              "summary": "Plenty of usefull mods ,Biomes ,Tools,Mekanism,Mobs,New Nether",
              "download_count": 81,
              "thumbnail_url": "https://media.forgecdn.net/avatars/thumbnails/254/790/256/256/637199699292644894.png",
              "primary_language": "enUS",
              "popularity_rank": 17940,
              "latest_release_date": "2020-03-21 09:49:01",
              "last_modified": "2020-03-30 13:40:51",
              "last_updated": "2020-05-16T05:46:18.000000Z"
            }
          ],
          "links": {
            "first": "https://www.modpackindex.com/api/v1/mod/10173/modpacks?page=1",
            "last": "https://www.modpackindex.com/api/v1/mod/10173/modpacks?page=54",
            "prev": null,
            "next": "https://www.modpackindex.com/api/v1/mod/10173/modpacks?page=2"
          },
          "meta": {
            "current_page": 1,
            "from": 1,
            "last_page": 54,
            "path": "https://www.modpackindex.com/api/v1/mod/10173/modpacks",
            "per_page": "3",
            "to": 3,
            "total": 162
          }
        }
