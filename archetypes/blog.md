+++
title = "{{ replace .Name "-" " " | title }}"
date = "{{ .Date }}"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = [{{ range $plural, $terms := .Site.Taxonomies }}{{ range $term, $val := $terms }}"{{ printf "%s" $term }}",{{ end }}{{ end }}]
featured = false
# An external link for comments (ex. Fediverse post)
comments = false
contents = false
+++

This is a page about »{{ replace .Name "-" " " | title }}«.
