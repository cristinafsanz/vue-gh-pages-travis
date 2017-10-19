# vue-gh-pages-travis

Repositorio creado a partir de la [demo de Jose Dongil](https://github.com/jdonsan/charla-aprendiendo-vuejs) y la [guía](https://github.com/cristinafsanz/vuejs-primeros-pasos) que hice a partir de ella.

El propósito del repositorio es subir a la rama gh-pages el contenido generado en el directorio de producción /dist y habilitar GitHub Pages para que lo publique desde esa rama.

El repositorio [vue-gh-pages](https://github.com/cristinafsanz/vue-gh-pages) lo hace de manera manual y aquí se va a utilizar Travis CI para automatizar el proceso.

Se va a usar el tutorial [GitHub Pages Deployment](https://docs.travis-ci.com/user/deployment/pages/) y la [configuración](https://github.com/jdonsan/pills/blob/master/.travis.yml) del repositorio [Pills](https://github.com/jdonsan/pills) de Jose Dongil.

- Añadir un [token personal de acceso](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/), ej TravisCI como descripción (no seleccionar ningún scope).

- Añadir un fichero .travis.yml al repositorio similar al de [Pills](https://github.com/jdonsan/pills/blob/master/.travis.yml) pero usando el comando "npm run build" y usando GH_TOKEN como GitHub token.

- Pasar el token de forma segura a Travis a través de la [configuración de repositorios](https://docs.travis-ci.com/user/environment-variables#Defining-Variables-in-Repository-Settings).

    - Acceder con la cuenta de GitHub a [Travis](https://travis-ci.org/).

    - Activar el repositorio: https://travis-ci.org/cristinafsanz/vue-gh-pages-travis.

    - En Settings (rueda a la izquierda del nombre en https://travis-ci.org/profile/cristinafsanz) añadir una nueva variable en Environment Variables (GH_TOKEN y el valor el token generado en GitHub).

- Crear rama gh-pages desde el navegador (selector de ramas y añadir nombre rama).

- Añadir los ficheros del proyecto (con dist en .gitignore) y hacer git add, commit y push para subirlo a remoto y que se genere automáticamente la rama gh-pages.

- Se puede ver el proceso en https://travis-ci.org/cristinafsanz/vue-gh-pages-travis.

- Activar GitHub Pages en gh-pages desde el navegador de GitHub (en Settings).

Resultado en https://cristinafsanz.github.io/vue-gh-pages-travis/#/.

