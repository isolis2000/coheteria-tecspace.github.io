# Página Web Cohetería TECSpace [![GitHub license](https://img.shields.io/github/license/Coheteria-TECSpace/coheteria-tecspace.github.io?style=flat-square)][mit] [![GitHub issues](https://img.shields.io/github/issues/Coheteria-TECSpace/coheteria-tecspace.github.io?style=flat-square)][issues]

Página web estática generada mediante [Jekyll][jekyll], con base en la plantilla para blogs [Chirpy][chirpy], y con hosting mediante [GitHub Pages](https://pages.github.com/), este es un proyecto del grupo cohetería computacional de TECSpace.

<div style="text-align: center">
    <img src="images/paginaweb.png" style="width:30rem; display: block; margin-left: auto; margin-right: auto;">
    <p><a href="https://coheteria-tecspace.github.io/">Visitar página web</a></p>
</div>

## Colaboración
Se recibe toda colaboración, todo PR será revisado y de ser aceptable, se hará merge en la rama dev, pueden escribir un nuevo [issue][issues] o colaborar con los ya existentes.

## Cómo correr en servidor local
Para poder visualizar los cambios que hacen en el código, será necesario correr un servidor local de [Jekyll][jekyll], para lograr esto se incluyen los pasos a continuación

### Instalación
Seguir los pasos oficiales para [Linux](https://jekyllrb.com/docs/installation/other-linux/), [macOS](https://jekyllrb.com/docs/installation/macos/) o [Windows](https://jekyllrb.com/docs/installation/windows/)
> también es posible usar [MSYS2](https://www.msys2.org/) y en este caso se deben seguir los siguientes pasos
```sh
# Instalación en MSYS2
pacman -S gcc ruby base-devel libffi-devel mingw-w64-x86_64-libxslt libxslt-devel

echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

gem install nokogiri --platform=ruby -- --use-system-libraries
gem install jekyll bundler
```
### Uso
Una vez se siguieron exitosamente los pasos de instalación se pueden seguir los siguientes pasos
1. Clonar este repositorio por [ssh](git@github.com:Coheteria-TECSpace/coheteria-tecspace.github.io.git), [http](https://github.com/Coheteria-TECSpace/coheteria-tecspace.github.io.git) o github-cli según sus preferencias.
2. Ingresar a la carpeta del repositorio mediante la terminal o prompt de su sistema operativo
```sh
cd coheteria-tecspace.github.io
```
3. Correr el comando mostrado a continuación para instalar las dependencias de Ruby
```
bundle install
```
4. Si se instalan exitosamente las Gems, se puede iniciar el servidor local con el siguiente comando **se debe estar en la misma carpeta que el archivo `Gemfile`**
```
bundle exec jekyll serve --watch --incremental
```
Se espera un texto similar al siguiente
```
Configuration file: coheteria-tecspace.github.io/_config.yml
            Source: coheteria-tecspace.github.io
       Destination: coheteria-tecspace.github.io/_site
 Incremental build: enabled
      Generating...
                    done in 0.001 seconds.
 Auto-regeneration: enabled for 'coheteria-tecspace.github.io'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```
5. De tener un mensaje como el anterior, simplemente se debe ir a la dirección web http://127.0.0.1:4000/,o bien http://localhost:4000, todo cambio realizado en el código debe poder verse en tiempo real en la página web local con tan solo refrescar la página.

## Licencia
Se mantiene la licencia [MIT][mit] usada por [Chirpy][chirpy].

## Encargados del repositorio
- Luis Ross ([lross2k](https://github.com/lross2k))

[gem]: https://rubygems.org/gems/jekyll-theme-chirpy
[chirpy]: https://github.com/cotes2020/jekyll-theme-chirpy/
[use-template]: https://github.com/cotes2020/chirpy-starter/generate
[issues]: https://github.com/Coheteria-TECSpace/coheteria-tecspace.github.io/issues
[mit]: https://github.com/Coheteria-TECSpace/coheteria-tecspace.github.io/blob/dev/LICENSE
[jekyll]: http://jekyllrb.com/
