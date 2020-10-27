For icecast streams you would append /status-json.xsl to the end of your URL. For example:
https://stream.example.com:8000/status-json.xsl

For shoutcast streams you append /stats?json=1 to the end of your url.
https://stream.example.com:8000/stats?json=1

Zeno.FM streams need to grab data from their API. You will need your station ID. It can be found by looking at the end bit of your stream URL. For example:
http://stream.zeno.fm/haq5p80k17zuf 

You will need to change out that ID into their API link, ex:
https://proxy.zeno.fm/api/stations/haq5p80k17zuf/now_playing/