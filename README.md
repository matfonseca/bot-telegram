# HealtApp Bot

### Ambientes

- Producción: [link](https://elmuro-bot.herokuapp.com/)
- Staging: [Link](https://elmuro-bot-staging.herokuapp.com/)
- Bot de testing local: [Testelmurobot](t.me/Testelmurobot)
- Bot stating: [STGHealthElmuro](https://t.me/STGHealthElmuroBot)
- Bot producción: [healthElmuro](https://t.me/healthElmuroBot)


### Convenciones

#### Estrategia de branching

Cuando se comienza a trabajar en una feature, se debe salir desde la branch _staging_, siempre estando _up to date_ con _origin_
```
 ---- staging ----
   \
    --- my-feature ---
```
Luego, cuándo se haya terminado de trabajar en la feature, se armará un Merge Request desde la branch creada hacia _staging_. Cuándo este MR sea aprobado por algún otro miembro del equipo, entonces podremos mergear nuestro branch a _staging_ y el código será desplegado al ambiente de pre-producción.
```
 ---- staging ---------------
   \                    /
    --- my-feature -----
```

#### Code Review
Una vez finalizado un feature, debe crearse un merge request a la rama de staging y notificar a los demás miembros para que alguno de estos revise el código y apruebe el merge en caso de estar correcto, o notificar de los cambios necesarios para la aprobación del mismo.

### Guía de ejecución del bot

1. En el archivo **_.env_** debe estar asignando el valor del **_TELEGRAM_TOKEN_**
2. Para la ejecución del mismo se deje ejecutar el comando **_ruby app.rb_**
3. Para ejecutar los test se debe utilizar el comando **_rake_**

Nota: para entrar por ssh a vagrant y pegarle a la api, debemos usar `vagrant ssh -- -R 3001:localhost:3001`
