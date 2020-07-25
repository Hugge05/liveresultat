# Liveresultat

## API
All API requests should be made via HTTPS GET reqests, content returned is returned as JSON.

### ``getcompetitions``
`https://pallhed.se/api.php?method=getcompetitions`

Returns a list of all events and their: ``id``, ``name``, ``organizerId``, ``dateTime`` (when the event will be hosted) and ``createdTime`` (when the event was created on Liveresultat).
