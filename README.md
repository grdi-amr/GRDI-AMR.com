# GRDI-AMR.com

The source of the [GRDI-AMR.com](https://grdi-amr.com) website.

Built using [Quarto](https://quarto.org/). Served using [GitHub Pages](https://pages.github.com/). Developed by [Brennan Chapman](https://github.com/chapb).


## Configuration

AWS is the registrar and DNS provider for GRDI-AMR.com.

An earlier version of the site was served by ReadTheDocs. ReadTheDocs did not support the use of an apex domain, so grdi-amr.com was redirected to info.grdi-amr.com using an S3 bucket. This was an inelegant solution, as S3 does not support HTTPS redirection. 

When the site was moved to GitHub pages the redirection was reversed; info.grdi-amr.com was redirected to grdi-amr.com using an S3 bucket (maintaining SEO). To enable HTTPS redirection, the S3 bucket was placed behind a CloudFront distribution. Aliasing of A and AAAA was only possible once info.grdi-amr.com was added to the distribution as an alternative domain name. 
