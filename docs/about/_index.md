---
title: Introduction to Redis
linkTitle: "About"
weight: 1
description: Learn about the Redis open source project
aliases:
  - /topics/introduction
  - /buzz
---

Redis is an open source (BSD licensed), in-memory **data structure store** used as a database, cache, message broker, and streaming engine. Redis provides data structures such as
[strings](/manual/data-types#strings), [hashes](/manual/data-types#hashes), [lists](/manual/data-types#lists), [sets](/manual/data-types#sets), [sorted sets](/manual/data-types#sorted-sets) with range queries, [bitmaps](/manual/data-types#bitmaps), [hyperloglogs](/manual/data-types/#hyperloglogs), [geospatial indexes](/commands/geoadd), and [streams](/manual/data-types/streams). Redis has built-in [replication](/manual/replication), [Lua scripting](/commands/eval), [LRU eviction](/manual/eviction), [transactions](/manual/transactions), and different levels of [on-disk persistence](/manual/persistence), and provides high availability via [Redis Sentinel](/manual/sentinel) and automatic partitioning with [Redis Cluster](/manual/scaling).

You can run **atomic operations**
on these types, like [appending to a string](/commands/append);
[incrementing the value in a hash](/commands/hincrby); [pushing an element to a
list](/commands/lpush); [computing set intersection](/commands/sinter),
[union](/commands/sunion) and [difference](/commands/sdiff);
or [getting the member with highest ranking in a sorted set](/commands/zrangebyscore).

To achieve top performance, Redis works with an
**in-memory dataset**. Depending on your use case, Redis can persist your data either
by periodically [dumping the dataset to disk](/manual/persistence#snapshotting)
or by [appending each command to a disk-based log](/manual/persistence#append-only-file). You can also disable persistence if you just need a feature-rich, networked, in-memory cache.

Redis supports [asynchronous replication](/manual/replication), with fast non-blocking synchronization and auto-reconnection with partial resynchronization on net split.

Redis also includes:

* [Transactions](/manual/transactions)
* [Pub/Sub](/manual/pubsub)
* [Lua scripting](/commands/eval)
* [Keys with a limited time-to-live](/commands/expire)
* [LRU eviction of keys](/manual/eviction)
* [Automatic failover](/manual/sentinel)

You can use Redis from [most programming languages](/clients).

Redis is written in **ANSI C** and works on most POSIX systems like Linux,
\*BSD, and Mac OS X, without external dependencies. Linux and OS X are the two operating systems where Redis is developed and tested the most, and we **recommend using Linux for deployment**. Redis may work in Solaris-derived systems like SmartOS, but support is *best effort*.
There is no official support for Windows builds.
