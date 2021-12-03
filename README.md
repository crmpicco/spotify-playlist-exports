# spotify-playlist-exports
Spotify playlist exports for yearly wrap ups



    Create an application on the Dashboard at https://developer.spotify.com/dashboard/applications and copy client ID and client secret

    Encode client ID and Client secret with base64:

    echo -n <client_id:client_secret> | openssl base64

    Request authorization with the encoded credentials, which provided me with an access token:

    curl -X "POST" -H "Authorization: Basic <my_encoded_credentials>" -d grant_type=client_credentials https://accounts.spotify.com/api/token

    With that access token it's possible to make requests to the API endpoints, that don't need user authorization, for example:

     curl -H "Authorization: Bearer <my_access_token>" "https://api.spotify.com/v1/search?q=<some_artist>&type=artist"


