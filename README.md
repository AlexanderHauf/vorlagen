# Template and 'Vorlage' for LaTeX

Templates in english and german with packages I use.

### Aliases:

To deploy the templates add these functions to your bashrc/zshrc or aliasfile:

```shell
function vorl() {
[ -z $1 ] && NAME=vorlage || NAME=$( echo $1 | sed 's/.tex//g' )
cp ~/vorlagen/vorlage.tex $NAME.tex
}

function templ() {
[ -z $1 ] && NAME=template || NAME=$( echo $1 | sed 's/.tex//g' )
cp ~/vorlagen/template.tex $NAME.tex
}
```


### Change username:

To change the username run those two commands:

`sed -i "s/alex/$USER/g" ~/vorlagen/vorlage.tex`

`sed -i "s/alex/$USER/g" ~/vorlagen/template.tex`
