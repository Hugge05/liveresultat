# Liveresultat

## API
All API requests should be made via HTTPS GET reqests, content returned is returned as JSON.

### ``getallcompetitions``
``https://pallhed.se/api.php?method=getallcompetitions``

Returns a list of all events and their: ``id``, ``name``, ``organizerId``, ``dateTime``, ``icon`` (when the event will be hosted) and ``createdTime`` (when the event was created on Liveresultat).

### ``getcompetitions``
``https://pallhed.se/api.php?method=getallcompetitions&page=0&results=15``

Like ``getcompetitions`` but starts from the given number, defaults to 0.

### ``getuserinfo``
``https://pallhed.se/api.php?method=getuserinfo&id=1``

Returns the users details.

### ``getcompetitioninfo``
``https://pallhed.se/api.php?method=getcompetitioninfo&id=14``

Returns the competitions details, runners and organisations.
