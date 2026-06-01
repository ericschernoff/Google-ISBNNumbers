# NAME

Google::ISBNNumbers - Retrieve book info by ISBN number

# SYNOPSIS

use Google::ISBNNumbers;

$books = Google::ISBNNumbers->new($your\_google\_api\_key);

$isbn\_number = 9781680500882; # may include dashes and spaces
$book\_info = $books->lookup\_isbn( $isbn\_number );

\# or, if you prefer
$book\_info = Google::ISBNNumbers->new($your\_google\_api\_key)->lookup\_isbn($isbn\_number); 

\# $book\_info now has keys for 'title', 'author\_name',
\# 'description', 'publication\_date', and 'cover\_link'
say $book\_info->{title}; # says 'Modern Perl'

# DESCRIPTION

This module uses the Google Books API to retrieve basic information on a book by its
ISBN Number.  The Google Books API seems to be more complete and reliable than other
resources for searching ISBN numbers.

You will need a Google API key from [https://console.cloud.google.com/apis/credentials](https://console.cloud.google.com/apis/credentials).
This requires setting up a basic 'Project' in that console, but no sensitive scopes are required,
so you should be able to get the key instantly.  You can read up on the Google Books API
here: [https://developers.google.com/books](https://developers.google.com/books)

This should be one of the simplest modules you'll encounter.  The synopsis above pretty 
much covers it. You pass your Google API key to new() and you pass a valid ISBN number
to lookup\_isbn(), and you get back a key/value hash of basic info on your book.
FYI: The ISBN number should be found on the back cover, above the bar code, and
starts with '978'.

# SEE ALSO

[App::isbn](https://metacpan.org/pod/App%3A%3Aisbn)

[WWW::Scraper::ISBN](https://metacpan.org/pod/WWW%3A%3AScraper%3A%3AISBN)

[Business::ISBN](https://metacpan.org/pod/Business%3A%3AISBN)

# AUTHOR

Eric Chernoff &lt;eric@weaverstreet.net&lt;gt>

Please send me a note with any bugs or suggestions.

# LICENSE

MIT License

Copyright (c) 2026 Eric Chernoff

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
