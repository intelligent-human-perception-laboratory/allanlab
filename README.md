# Allan Lab Website

## using Jekyll scholar

add line in gemfile
```
gem 'jekyll-scholar'
```
or install by
```
gem install jekyll-scholar
```
add these lines in _config.yml
```
plugins: ['jekyll/scholar']
scholar:
  style: apa
```
style specifies the style you want to render

Now create a directory called _bibliography where you put all your .bib or bibtex files into. Remember to add
```
---
---
```
at the top of your bibtex file.

Now in the any file under _pages. You can render the bibtex using
```
{% bibliography -f book%}
```
where the file_name is the file name of your .bib file without extension

## How Jekyll work
