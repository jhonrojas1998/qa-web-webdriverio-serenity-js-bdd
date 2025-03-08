# Proyecto de Pruebas Automatizadas con WebdriverIO, Serenity/JS y Cucumber

Este proyecto implementa pruebas automatizadas utilizando WebdriverIO, Serenity/JS y Cucumber.

## Nombre Del Autor:
Jhon Hader Rojas Cabrera

## 👅 Instalación

```sh
npm init wdio .
```

O también puedes usar:

```sh
npx create-wdio .
```

## Preguntas del Configurador
Durante la configuración del proyecto con WebdriverIO, se respondieron las siguientes preguntas:

1. **¿Es correcto el nombre y ubicación del proyecto?** → Sí
2. **¿Qué tipo de pruebas deseas realizar?** → Pruebas E2E de aplicaciones web o móviles
3. **¿Dónde se encuentra el backend de automatización?** → En mi máquina local
4. **¿Qué entorno deseas automatizar?** → Web - Aplicaciones en el navegador
5. **¿Con qué navegador quieres empezar?** → Chrome
6. **¿Qué framework deseas utilizar?** → Cucumber con Serenity/JS
7. **¿Quieres usar TypeScript para escribir pruebas?** → Sí
8. **¿Quieres que WebdriverIO genere automáticamente algunos archivos de prueba?** → No
9. **¿Qué reporter deseas utilizar?** → spec
10. **¿Quieres agregar un plugin a la configuración de prueba?** → No
11. **¿Quieres incluir pruebas visuales en la configuración?** → No
12. **¿Quieres agregar un servicio a la configuración de prueba?** → No
13. **¿Deseas que WebdriverIO ejecute `npm install` automáticamente?** → Sí

## Instalación de Dependencias

Las siguientes dependencias fueron instaladas automáticamente:

- `@wdio/local-runner@latest`
- `@serenity-js/webdriverio`
- `@wdio/spec-reporter@latest`
- `@cucumber/cucumber`
- `@serenity-js/assertions`
- `@serenity-js/console-reporter`
- `@serenity-js/core`
- `@serenity-js/cucumber`
- `@serenity-js/rest`
- `@serenity-js/serenity-bdd`
- `@serenity-js/web`
- `@types/node`
- `npm-failsafe`
- `rimraf`

## Recursos Adicionales

- [Documentación de WebdriverIO](https://webdriver.io)
- [Documentación de Serenity/JS](https://serenity-js.org/)
- [Comunidad en Discord de WebdriverIO](https://discord.webdriver.io)
- [Repositorio en GitHub de WebdriverIO](https://github.com/webdriverio/webdriverio)

## 💂 Arquitectura del Proyecto

```sh
qa-web-webdriverio-serenity-js-bdd/
├── features/
│   ├── herokuapp/
│   │   ├── dynamic_content.feature
│   │   ├── login.feature
│   │   ├── verify_dynamic_text.feature
│   ├── step-definitions/
│   │   ├── dynamic_content.steps.ts
│   │   ├── login.steps.ts
│   │   ├── verify_dynamic_text_steps.ts
│   ├── support/
│   │   ├── dynamicIdMap.ts
│   │   ├── parameter.config.ts
│   ├── todo-list/
│   │   ├── narrative.md
├── node_modules/
├── serenity/
│   ├── herokuapp/
│   │   ├── DynamicContentPage.ts
│   │   ├── DynamicIdPropertyPage.ts
│   │   ├── DynamicPropertiesPage.ts
│   │   ├── LoginPage.ts
├── target/
│   ├── package.json
│   ├── package-lock.json
│   ├── serenity.properties
│   ├── tsconfig.json
│   ├── wdio.conf.ts
└── External Libraries/
```

## 👅 Instalación de Dependencias

Estas dependencias ya deberían estar en tu proyecto, pero si necesitas instalarlas individualmente, aquí las tienes:

```sh
npm install @cucumber/cucumber --save-dev --legacy-peer-deps
npm install @serenity-js/assertions --save-dev --legacy-peer-deps
npm install @serenity-js/console-reporter --save-dev --legacy-peer-deps
npm install @serenity-js/core --save-dev --legacy-peer-deps
npm install @serenity-js/cucumber --save-dev --legacy-peer-deps
npm install @serenity-js/rest --save-dev --legacy-peer-deps
npm install @serenity-js/serenity-bdd --save-dev --legacy-peer-deps
npm install @serenity-js/web --save-dev --legacy-peer-deps
npm install @serenity-js/webdriverio --save-dev --legacy-peer-deps
npm install @types/node --save-dev --legacy-peer-deps
npm install @wdio/cli --save-dev --legacy-peer-deps
npm install @wdio/local-runner --save-dev --legacy-peer-deps
npm install @wdio/selenium-standalone-service --save-dev --legacy-peer-deps
npm install @wdio/visual-service --save-dev --legacy-peer-deps
npm install chromedriver --save-dev --legacy-peer-deps
npm install npm-failsafe --save-dev --legacy-peer-deps
npm install rimraf --save-dev --legacy-peer-deps
npm install ts-node --save-dev --legacy-peer-deps
npm install tsx --save-dev --legacy-peer-deps
```

## 🚀 Ejecución de Pruebas

Ejecuta pruebas individuales:

```sh
npx wdio run ./wdio.conf.ts --spec ./features/herokuapp/dynamic_content.feature
npx wdio run ./wdio.conf.ts --spec ./features/herokuapp/verify_dynamic_text.feature
npx wdio run ./wdio.conf.ts --spec ./features/herokuapp/login.feature
```

Ejecuta todas las pruebas:

```sh
npx wdio run wdio.conf.ts
```

Ejecuta con logs detallados:

```sh
npx wdio run ./wdio.conf.ts --verbose
```

Limpia reportes anteriores y ejecuta pruebas:

```sh
Remove-Item -Recurse -Force target/site/serenity
npx serenity-bdd run
```

Ejecución completa con limpieza previa:

```sh
Remove-Item -Recurse -Force target/site/serenity -ErrorAction SilentlyContinue ;
npx wdio run ./wdio.conf.ts ;
npx serenity-bdd run
```

Ejecución de pruebas específicas con limpieza previa:

```sh
Remove-Item -Recurse -Force target/site/serenity -ErrorAction SilentlyContinue ;
npx wdio run ./wdio.conf.ts --spec ./features/herokuapp/dynamic_content.feature ;
npx serenity-bdd run
```

## 📌 Notas Adicionales

- WebdriverIO se encarga de la ejecución de las pruebas automatizadas.
- Serenity/JS se encarga del reporte y gestión de pruebas.
- Cucumber se usa para la definición de escenarios en lenguaje Gherkin.
- Los reportes se generan en `target/site/serenity`.
