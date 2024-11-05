# axum-vss

`axum-vss` is a *database-agnostic*, *async*, and *integration test friendly*
Rust library for implementing a [VSS] server based on [`axum`] and [SeaORM].

- [`axum`] is based on [`tokio`] and [`hyper`]. Axum's powerful [`tower`]-based
  middleware allows users to bring their own middleware for authentication,
  request counting, rate limits, timeouts, backpressure, and more.
- [SeaORM] is an async-native relational ORM with great support for database
  mocking and [`sqlx`]-based integration testing. SeaORM supports PostgreSQL,
  SQLite, and MySQL, so `axum-vss` supports these backends as well.

Users supply a [`sea_orm::DatabaseConnection`] to `axum-vss` in order to obtain
an [`axum::Router`], which they can serve with their own TLS config.

This project is not affiliated with Tokio/Axum or LDK/VSS.

[`tokio`]: https://tokio.rs/
[`hyper`]: https://docs.rs/hyper/latest/hyper/
[VSS]: https://github.com/lightningdevkit/vss-server
[`tower`]: https://docs.rs/tower/latest/tower/
[`sqlx`]: https://docs.rs/sqlx/latest/sqlx/
[`axum`]: https://docs.rs/axum
[SeaORM]: https://www.sea-ql.org/SeaORM/
[`sea_orm::DatabaseConnection`]: https://docs.rs/sea-orm/latest/sea_orm/enum.DatabaseConnection.html
[`axum::Router`]: https://docs.rs/axum/latest/axum/struct.Router.html

## License

MIT
