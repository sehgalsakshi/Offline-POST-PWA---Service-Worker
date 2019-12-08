# Offline-POST-PWA---Service-Worker

Service worker for handling post requests in offline mode using indexed db

Method #sendOfflinePostRequestsToServer() create a new indexed db and table when network state is online.If table contains records, generates fetch requests recursively to hit POST requests to server.

Method #sendFetchRequestsToServer() is the recursive method responsible for making fetch calls in serialized manner.

Method #saveIntoIndexedDb() saves request data in indexed db.

Bonus Methods (for encrypting cached responses of get requests and updating cache or creating cache for an uncached request)

Method #cacheResponse() serves the logic for encryption and method #returnResponseFromCache() is responsible for decryption of cached response.

Method #updateCacheForAParticularRequest() can be used for updating cache of an existing request or creating a new cached response if it doesn't exist.

