---
title: Acerca de la API de GraphQL
intro: 'La API de GraphQL de {% data variables.product.prodname_dotcom %} ofrece flexibilidad y la capacidad de definir precisamente los datos que quieres recuperar.'
versions:
  fpt: '*'
  ghec: '*'
  ghes: '*'
  ghae: '*'
topics:
  - API
---

## Resumen

Here are some quick links to get you up and running with the GraphQL API:

* [Autenticación](/graphql/guides/forming-calls-with-graphql#authenticating-with-graphql)
* [Terminal raíz](/graphql/guides/forming-calls-with-graphql#the-graphql-endpoint)
* [Introspección del modelo](/graphql/guides/introduction-to-graphql#discovering-the-graphql-api)
* [Límites de tasa](/graphql/overview/resource-limitations)
* [Migrar desde REST](/graphql/guides/migrating-from-rest-to-graphql)

## Acerca de GraphQL

El lenguaje de consulta de [GraphQL](https://graphql.github.io/) es:

* **Una [especificación](https://graphql.github.io/graphql-spec/June2018/).** La especificación determina la validez del [modelo](/graphql/guides/introduction-to-graphql#schema) en el servidor de la API. El modelo determina la validez de las llamadas al cliente.

* **[Lenguaje inflexible](#about-the-graphql-schema-reference).** El modelo define el sistema de tipos de la API y todas las relaciones con objetos.

* **[Introspectivo](/graphql/guides/introduction-to-graphql#discovering-the-graphql-api).** Un cliente puede consultar el modelo para obtener detalles del mismo.

* **[Jerárquico](/graphql/guides/forming-calls-with-graphql).** La forma de un llamado de GraphQL imita la forma de los datos JSON que recupera. Los [Campos anidados](/graphql/guides/migrating-from-rest-to-graphql#example-nesting) te permiten consultar y recibir únicamente los dtos que especificas en una sola transacción.

* **Una capa de aplicación.** GraphQL no es un modelo de almacenamiento o un lenguaje de consulta de bases de datos. _graph_ se refiere a estructuras gráficas definidas en el modelo, en donde los [nodos](/graphql/guides/introduction-to-graphql#node) definen objetos y los [bordes](/graphql/guides/introduction-to-graphql#edge) definen relaciones entre objetos. La API recorre y recupera datos de la aplicación basándose en las definiciones del modelo, independientemente de cómo se almacenan los datos.

## Por qué GitHub utiliza GraphQL

GitHub chose GraphQL because it offers significantly more flexibility for our integrators. The ability to define precisely the data you want&mdash;and _only_ the data you want&mdash;is a powerful advantage over traditional REST API endpoints. GraphQL te permite reemplazar varias solicitudes de REST con _una sola llamada_ para agregar los datos que especifiques.

For more details about why GitHub invested in GraphQL, see the original [announcement blog post](https://github.blog/2016-09-14-the-github-graphql-api/).

## Acerca de la referencia del modelo de GraphQL

Los documentos en la barra lateral se generan del [modelo](/graphql/guides/introduction-to-graphql#discovering-the-graphql-api) de GraphQL de {% data variables.product.prodname_dotcom %}. Todas las llamadas se validan y ejecutan contra el modelo. Utiliza estos documentos para encontrar los datos a los que puedes llamar:

* Operaciones permitidas: [consultas](/graphql/reference/queries) y [mutaciones](/graphql/reference/mutations).

* Tipos definidos por el modelo: [escalares](/graphql/reference/scalars), [objetos](/graphql/reference/objects), [enumeradores](/graphql/reference/enums), [interfaces](/graphql/reference/interfaces), [uniones](/graphql/reference/unions), y [objetos de entrada](/graphql/reference/input-objects).

Puedes acceder a este mismo contenido a través de la [Barra lateral de documentos del explorador](/graphql/guides/using-the-explorer#accessing-the-sidebar-docs). Nota que podrías necesitar depender de ambos, los documentos y la validación del modelo, para hacer una llamada a la API de GraphQL.

Para obtener otro tipo de información, tal como los detalles de autenticación y el límite de tasas, revisa las [guías](/graphql/guides).

## Solicitar soporte

{% data reusables.support.help_resources %}
