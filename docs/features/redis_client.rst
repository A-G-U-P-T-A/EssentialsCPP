Redis Client
============

This page describes the `URedisClient` methods that are used for interacting with a Redis database. 

URedisClient Methods
--------------------

**Connect**

.. code-block:: cpp

   bool URedisClient::Connect(const FString& Host, int32 Port)

Establishes a connection to a Redis server.

**Disconnect**

.. code-block:: cpp

   void URedisClient::Disconnect()

Disconnects from the Redis server.

**Reconnect**

.. code-block:: cpp

   void URedisClient::Reconnect()

Attempts to reconnect to the Redis server.

**Set**

.. code-block:: cpp

   bool URedisClient::Set(const FString& Key, const FString& Value)

Sets the value of a given key in Redis.

**Get**

.. code-block:: cpp

   bool URedisClient::Get(const FString& Key, FString& Value)

Retrieves the value associated with a given key from Redis.

**Delete**

.. code-block:: cpp

   bool URedisClient::Delete(const FString& Key)

Deletes the specified key from Redis.

**Exists**

.. code-block:: cpp

   bool URedisClient::Exists(const FString& Key)

Checks the existence of the specified key in Redis.

**Expire**

.. code-block:: cpp

   bool URedisClient::Expire(const FString& Key, int32 Seconds)

Sets an expiration time for the specified key in Redis.

**TTL**

.. code-block:: cpp

   int64 URedisClient::TTL(const FString& Key)

Retrieves the remaining time-to-live for the specified key in Redis.

**IsConnected**

.. code-block:: cpp

   bool URedisClient::IsConnected() const

Checks if the Redis client is connected to the Redis server.

**Append**

.. code-block:: cpp

   bool URedisClient::Append(const FString& Key, const FString& Value)

Appends the given value to the existing value associated with the specified key in Redis.

**Increment**

.. code-block:: cpp

   bool URedisClient::Increment(const FString& Key, int32& Value)

Increments the value of the specified key in Redis by 1.

**Decrement**

.. code-block:: cpp

   bool URedisClient::Decrement(const FString& Key, int32& Value)

Decrements the value of the specified key in Redis by 1.

**IncrementBy**

.. code-block:: cpp

   bool URedisClient::IncrementBy(const FString& Key, int32 Increment, int32& Value)

Increments the value of the specified key in Redis by the given increment value.

**DecrementBy**

.. code-block:: cpp

   bool URedisClient::DecrementBy(const FString& Key, int32 Decrement, int32& Value)

Decrements the value of the specified key in Redis by the given decrement value.

**HSet**

.. code-block:: cpp

   bool URedisClient::HSet(const FString& Key, const FString& Field, const FString& Value)

Sets the value for the specified field in the hash stored at the given key in Redis.

**HGet**

.. code-block:: cpp

   bool URedisClient::HGet(const FString& Key, const FString& Field, FString& Value)

Retrieves the value of the specified field in the hash stored at the given key in Redis.

**HDel**

.. code-block:: cpp

   bool URedisClient::HDel(const FString& Key, const FString& Field)

Deletes the specified field from the hash stored at the given key in Redis.

**HGetAll**

.. code-block:: cpp

   bool URedisClient::HGetAll(const FString& Key, TMap<FString, FString>& Fields)

Retrieves all field-value pairs from the hash stored at the given key in Redis.

**HExists**

.. code-block:: cpp

   bool URedisClient::HExists(const FString& Key, const FString& Field)

Checks if the specified field exists in the hash stored at the given key

