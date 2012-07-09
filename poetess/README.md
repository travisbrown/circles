Converted with:

    for f in sgml/*.sgm; do
      osx -E1000000 -xlower -xcomment -xempty -xndata $f 2>> conversion-warnings.txt | \
      xmllint --format - > xml/`basename $f ".sgm"`.xml;
    done

