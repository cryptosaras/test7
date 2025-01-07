# NBA Data API Documentation

## Base URL
`https://raw.githubusercontent.com/cryptosaras/test7/main/data`

## Available Endpoints

### 1. Team Stats
**Path:** `/team_stats/{team-name}_stats_{team-id}.json`

**Example URLs:**
- [Atlanta Hawks](https://raw.githubusercontent.com/cryptosaras/test7/main/data/team_stats/atlanta-hawks_stats_132.json)
- [Boston Celtics](https://raw.githubusercontent.com/cryptosaras/test7/main/data/team_stats/boston-celtics_stats_133.json)

**Contains:**
- Team statistics
- Recent games (last 20)
- Team injuries
- Team IDs and abbreviations

### 2. Player Stats
**Path:** `/player_stats/{Team Name}/{Player_Name}_{player_id}.json`

**Example URLs:**
- [Trae Young](https://raw.githubusercontent.com/cryptosaras/test7/main/data/player_stats/Atlanta%20Hawks/Trae_Young_1234.json)
- [Jayson Tatum](https://raw.githubusercontent.com/cryptosaras/test7/main/data/player_stats/Boston%20Celtics/Jayson_Tatum_9012.json)

**Contains:**
- Player statistics
- Recent news
- Player information

### 3. Team IDs Reference
json
{
"atlanta-hawks": {"abbrev": "atl", "cbs_id": 132},
"boston-celtics": {"abbrev": "bos", "cbs_id": 133},
"brooklyn-nets": {"abbrev": "bkn", "cbs_id": 134},
"charlotte-hornets": {"abbrev": "cha", "cbs_id": 135},
"chicago-bulls": {"abbrev": "chi", "cbs_id": 136},
"cleveland-cavaliers": {"abbrev": "cle", "cbs_id": 137},
"dallas-mavericks": {"abbrev": "dal", "cbs_id": 138},
"denver-nuggets": {"abbrev": "den", "cbs_id": 139},
"detroit-pistons": {"abbrev": "det", "cbs_id": 140},
"golden-state-warriors": {"abbrev": "gsw", "cbs_id": 141},
"houston-rockets": {"abbrev": "hou", "cbs_id": 142},
"indiana-pacers": {"abbrev": "ind", "cbs_id": 143},
"los-angeles-clippers": {"abbrev": "lac", "cbs_id": 144},
"los-angeles-lakers": {"abbrev": "lal", "cbs_id": 145},
"memphis-grizzlies": {"abbrev": "mem", "cbs_id": 146},
"miami-heat": {"abbrev": "mia", "cbs_id": 147},
"milwaukee-bucks": {"abbrev": "mil", "cbs_id": 148},
"minnesota-timberwolves": {"abbrev": "min", "cbs_id": 149},
"new-orleans-pelicans": {"abbrev": "nop", "cbs_id": 150},
"new-york-knicks": {"abbrev": "nyk", "cbs_id": 151},
"oklahoma-city-thunder": {"abbrev": "okc", "cbs_id": 152},
"orlando-magic": {"abbrev": "orl", "cbs_id": 153},
"philadelphia-76ers": {"abbrev": "phi", "cbs_id": 154},
"phoenix-suns": {"abbrev": "phx", "cbs_id": 155},
"portland-trail-blazers": {"abbrev": "por", "cbs_id": 156},
"sacramento-kings": {"abbrev": "sac", "cbs_id": 157},
"san-antonio-spurs": {"abbrev": "sas", "cbs_id": 158},
"toronto-raptors": {"abbrev": "tor", "cbs_id": 159},
"utah-jazz": {"abbrev": "uta", "cbs_id": 160},
"washington-wizards": {"abbrev": "was", "cbs_id": 161}
}
## Usage Example (Python)

python
import requests
Get team stats
team_stats = requests.get('https://raw.githubusercontent.com/cryptosaras/test7/main/data/team_stats/atlanta-hawks_stats_132.json').json()
Get player stats
player_stats = requests.get('https://raw.githubusercontent.com/cryptosaras/test7/main/data/player_stats/Atlanta Hawks/Trae_Young_1234.json').json()

## Data Update Frequency
Data is updated regularly and accessible via simple HTTP GET requests. No authentication required.
