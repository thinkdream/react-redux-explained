Thinking on persistence

# Local persistence

https://github.com/rt2zz/redux-persist

In case of ImmutableJS an extension is https://github.com/rufman/redux-persist-immutable-state

Can persis on 
- localForage for browser https://github.com/mozilla/localForage (https://mozilla.github.io/localForage/#custom-driver-api, an example of config is here https://github.com/thgreasi/localForage-cordovaSQLiteDriver)
- AsyncStorage for RN http://facebook.github.io/react-native/docs/asyncstorage.html#content
- custom adapter must be built for Electron, probably using https://github.com/Ivshti/linvodb3

Another option can be https://github.com/loggur/redux-replicate

A certain help can be obtained from https://github.com/joshwcomeau/redux-server-persist

Expiration https://github.com/gabceb/redux-persist-transform-expire

Migration https://github.com/wildlifela/redux-persist-migrate


# Server persistence

https://github.com/gaearon/redux-thunk

# Reference

A reference project with Elixir backend https://github.com/bigardone/phoenix-trello

The backend framework is Phoenix https://github.com/phoenixframework/phoenix

The DB for this project is PostgreSQL, but would be interesting to use https://github.com/hamiltop/rethinkdb-elixir for RethinkDB ()https://github.com/graphql-elixir/graphql-phoenix-rethinkdb)

Another option can be https://github.com/DenisIzmaylov/redux-catch-promise

# Other ideas

https://github.com/staticinstance/react-redux-component-injection-example

https://github.com/maxdeviant/redux-persist-transform-encrypt
