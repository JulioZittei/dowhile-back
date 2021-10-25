<h1 align="center">Dowhile 2021 - Back-end</h1>

<p align="center">
  <a href="#-technologies">Technologies</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-how-to-run">How to run</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#-license">License</a>
</p>

<p align="center">
  <img alt="License" src="https://img.shields.io/static/v1?label=license&message=MIT&color=8257E5&labelColor=000000">
  <img src="https://img.shields.io/static/v1?label=NLW&message=Heat&color=8257E5&labelColor=000000" alt="NLW Heat" />
</p>

## ✨ Technologies

This project was developed with the following technologies:

- [TypeScript](https://www.typescriptlang.org/)
- [Express](https://expressjs.com/pt-br/)
- [Prisma](https://www.prisma.io/)
- [JSON Web Token](https://jwt.io/)
- [Socket.IO](https://socket.io/)

## 🚀 How to run

> Note: In this project we have OAuth authentication with GitHub

- Clone the repository and access the folder;
- Copy the `.env.example` file to `.env` and fill it in with your GitHub credentials and JWT secret;
- If you intend to run it locally, you can use **SQLite** and you keep the configuration `schema.prisma` file like this:

```
datasource db {
  provider = "sqlite"
  url = "file:./dev.db"
}
```

- If you intend to use a database like **PostgreSQL**, you can keep the configuration `schema.prisma` file like this:

```
datasource db {
  provider = "postgresql"
  url = env("DATABASE_URL")
}
```

> Note: If you use a cloud-hosted database for development, you need to create the shadow database manually.

```
datasource db {
  provider = "postgresql"
  url = env("DATABASE_URL")
  shadowDatabaseUrl = env("SHADOW_DATABASE_URL")
}
```

- Install the dependencies with `yarn`;
- Run the migrations with `yarn prism migrate dev`;
- Start the server with `yarn dev`;

The application can be accessed at [`localhost:4000`](http://localhost:4000).

You can access the live web application [`clicking here`](https://dowhile-front.vercel.app/).

## 📄 License

This project is under the MIT license. See the [LICENSE](LICENSE) file for more details.

---

Made with ♥ by Julio Zittei 👋🏻
