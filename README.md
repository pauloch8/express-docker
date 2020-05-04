## Scripts npm para subir o Docker

Scripts npm para iniciar o Docker-compose nos ambientes de produção e desenvolvimento.

O package.json tem pronto os scripts para executar o Docker no ambiente escolhido (desenvolvimento, produção).

Os scripts têm a nomenclatura `{ambiente}-{ação}`. Para subir o ambiente de desenvolvimento, por exemplo, execute:

```npm run production-up```

Os containeres geram sua própria pasta npm_modules e a mantêm em um volume virtual.

Isso significa que você pode instalar as suas dependências em qualquer sistema operacional e ao mesmo tempo subir os containeres que as instalações da npm_modules estão isoladas e não vão interferir uma na outra.

A ideia é usar o npm como ferramenta para o deploy e desenvolvimento. Com um comando você pode subir o ambiente escolhido.

Obs: Os scripts npm estão usando expansão de parâmetro de shell: `${npm_variable}` portanto não vão subir em linha de comando que não aceita esse recurso, como o cmd e PowerShell do Windows.

## referências

- Ambientes docker inspirados no projeto do [projeto docker](https://github.com/CloudNativeJS/docker) da [CloudNative.js](https://www.cloudnativejs.io/) e no projeto [livereload-nodejs-debug-docker](https://github.com/ErickWendel/livereload-nodejs-debug-docker) e no conceito [Docker-first](https://www.linkedin.com/posts/erickwendel_ser%C3%A1-que-realmente-vale-a-pena-usar-docker-activity-6635530851524333568-C4z_/) de Erick Wendel