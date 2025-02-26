2.10.0 (Dan Reynolds)

Bump Apollo version and ensure compatibility.

2.9.1 (Dan Reynolds)

Add function equality check to `useFragmentWhere` API.

2.9.0 (Dan Reynolds)

Bump compatibility to @apollo/client 3.7.

2.8.0 (Dan Reynolds)

Add support for reactive filter changes in `useFragmentWhere`.

2.7.0 (Dan Reynolds)

Dependency changes.

2.6.0 (Dan Reynolds)

Revert TSConfig update back to commonJS for the time being.

2.5.0 (Dan Reynolds)

Introduces cached reactive variables.

2.4.1 (Dan Reynolds)

Verifies that TTL eviction works correctly for relay style pagination.

2.4.0 (Dan Reynolds)

Reinitialize all invalidation policy objects after cache init()

2.3.0 (Dan Reynolds)

* Update TSConfig

2.2.0 (Dan Reynolds)

* Revert lodash-es change and use module imports instead

2.1.0 (Dan Reynolds)

* Switch from using lodash to lodash-es to reduce bundle size

2.0.3 (Dan Reynolds)

* Filter out dangling references from collection entities

2.0.2 (Dan Reynolds)

* Fix a bug with evicting expired fields with a field alias

2.0.1 (Dan Reynolds)

* Fix issue with custom Query type keyArgs preventing TTLs from evicting entities

2.0.0 (Dan Reynolds)

* [Breaking] Updates to useFragment/useFragmentWhere APIs. Changes how it works internally to base fragment field policy names off dynamic UUIDs instead of the name of the fragment. Now Returns the data directly on the result as opposed to nested within the field name.
* Adds support for a default function syntax for invalidation policy events.

1.5.0 (Dan Reynolds)

- Add `evictWhere` API for evicting entities by a filter

1.4.0 (Dan Reynolds)

- Support Apollo 3.4 `init` API to reset the entity type map and watcher.

1.3.0 (Dan Reynolds)

- Adds experimental normalized collections

1.2.2 (Dan Reynolds)

- Expose args field on policy action meta objects

1.2.1 (Dan Reynolds)

- Publish publicly. Sorry OSS friends!

1.2.0 (Dan Reynolds)

- Update to TypeScript ^4.0

1.1.0 (Dan Reynolds)

- Rename library to Apollo Cache Policies and release under the NerdWallet org at `@nerdwallet/apollo-cache-policies`

1.0.0-beta16 (Dan Reynolds)

- Release new version with React dependencies removed.

1.0.0-beta15 (Dan Reynolds)

- Fix bug where a renew-on-read policy would try to update the cache time for entities not present in the cache

1.0.0-beta14 (Dan Reynolds)

- Bugfix for fixing eviction/mutation changes to the cache via the wrapper `wrapDestructiveCacheMethod` function. 

1.0.0-beta13 (Dan Reynolds)

- Short-term fix that adds support for running the lib in environments that cannot handle import statements by removing imports from non-public Apollo APIs.
The required imports will be made available in an upcoming version of Apollo Client and we'll switch to that better fix at that time.

1.0.0-beta12 (Dan Reynolds)

- Add support for dynamically activating/deactivating policy events

1.0.0-beta11 (Dan Reynolds)

- Default the `readPolicy` function in the policy action to use the ROOT_QUERY similarly to how the policies module does in apollo/client

1.0.0-beta10 (Dan Reynolds)

- Add support for a default policy action to perform side effects whenever a specific type is written/evicted from the cache

1.0.0-beta9 (Dan Reynolds)

- Add `expiredEntities` API for accessing the expired entities in the cache without evicting them

1.0.0-beta8 (Dan Reynolds)

- Add test for Write-on-Write policies where the mutation has arguments and fix the Readme to illustrate how to correctly write the invalidation policy in that case

1.0.0-beta7 (Dan Reynolds)

- Fix issue where read policies were attempted to be evaluated for non-normalized entities not yet in the cache if they had a different store field name with the same name
  already written in the cache.

1.0.0-beta6 (Dan Reynolds)

- Adds a `storage` dictionary by unique `storeFieldName` for queries or `ID` for normalized entities in the policy action object so that arbitrary meta information can be stored across multiple policy action invocations.

1.0.0-beta5 (Dan Reynolds)

- Adds support for a `renewalPolicy` type and global config option for specifying how type TTLs should be renewed on write vs access
- Adds the `expire` API for evicting all entities that have expired in the cache based on their type's or the global TTL.

1.0.0-beta4 (Dan Reynolds)

- [BREAKING CHANGE] Adds support for a default TTL option that applies to all types

1.0.0-beta3 (Dan Reynolds)

- Ensure that empty field arguments are still passed as an empty object as the variables in the policy event.

1.0.0-beta2 (Dan Reynolds)

- Bumps to latest Apollo version (3.1)
- Adds audit logging for better entity debugging through the type map and invalidation policy manager

1.0.0-beta1 (Dan Reynolds)

- Initial beta release 🚀