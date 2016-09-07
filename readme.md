# It's Easy (itcss-easy)

**A Bash script for lovers of BEM, ITCSS and SASS.**

These days, I continually find myself using a combination of [ITCSS](https://www.xfive.co/blog/itcss-scalable-maintainable-css-architecture/),
[BEM](https://en.bem.info/) and [SASS](http://sass-lang.com/) for the majority of my projects.
I love the structure and clarity the methodologies provide, but writing directory names, filenames and `@import`
declarations can be tedious. This command line tool is aimed at reducing some of the overhead involed in naming
and building files.

At it's core, `itcss-easy` quickly sets up a folder directory based on the ITCSS convention: Settings, Tools, Generic,
Elements, Objects, Components and Trumps. Secondly, you can pass a name argument to `itcss-easy` to quickly build
component directories with associated `.scss` filenames.


---

### Installation

#### Copying
`itcss-easy` is simply a shell script. Add the itcss-easy file to your `PATH` directory or wherever your executables happen to run from. To find out, run `echo $PATH` from your command line.

#### NPM
`npm install --global itcss-easy`

---

### Usage
Run `itcss-easy` from the command line to create the following directories and filenames:

```
application.scss

settings/
tools/
generic/
elements/
objects/
components/
trumps/
```

Each directory has an associated `.scss` file inside. An `application.scss` file will also be created and will include the correct import structure for the ITCSS directories. Feel free to rename the `application.scss` file to whatever you like.

#### Creating components
You can create components from the command line by simply passing a name argument.

`itcss-easy [component-name]`

Make sure to run the command from the Root folder. Components will be built inside of components directory.
Each component includes it's own `.scss` file which is imported into `components/components.css` using the
`@import` declaration.

```
components/
├── component-1/
│   ├── component-1.scss
├── component-2/
│   ├── component-2.scss
...
```
