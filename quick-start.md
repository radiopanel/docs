# Quick Start

## Registration

Register for a radiopanel account on: [http://app.radiopanel.co/auth/register](http://app.radiopanel.co/auth/register)

## Radio station creation

After you registered, you will be presented with the option to create a new radio station. Press "Create Radio Station"

## Setting up your song history

After your radio station creation you will be automatically assigned an admin role that has all the permissions enabled. To setup your song history you first have to provide your stream status URL & choose a matching service.

Go to "Settings" in the left hand side menu \(you might have to scroll down\); and fill in the following things:

### Stream settings

If you have a **Azuracast** installation you can opt in for the Azura configuration type. Here you have to fill in the following things:

* AzuraCast Base URL, this is the url to your azura cast installation. It should look this this: `https://<AZURA-IP>:<AZURA-PORT>`. This url should **NOT** not end with a `/`
* AzuraCast Station ID, the number representing your azuracast station.
* AzuraCast Api key, a full length working api key from azuracast.

If you don't use AzuraCast, you can choose for the **Manual Configuration** here you just have to provide your radio broadcasting server type & URL.

For icecast streams you would append /status-json.xsl to the end of your URL. For example: [https://stream.example.com:8000/status-json.xsl](https://stream.example.com:8000/status-json.xsl)

For shoutcast streams you append /stats?json=1 to the end of your url. [https://stream.example.com:8000/stats?json=1](https://stream.example.com:8000/stats?json=1)

### Matching service

Here you have the option how Radiopanel should find the correct metadata for playing songs. You have following options:

* Deezer
* Apple
* Spotify

To use spotify you will need to create a Spotify developers account. Go to [https://developer.spotify.com/](https://developer.spotify.com/) and click on _Dashboard_ Once you are there, press "Create an App" Name it whatever you want. It doesn't matter.

After you filled these things in correctly and saved your changes you should start to see your song history fill up after a minute.

