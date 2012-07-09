Converted with:

    for f in sgml/*.sgm; do
      osx -xlower -xcomment -xempty -xndata -E $f 2>> conversion-warnings.txt | \
      xmllint --format - > xml/`basename $f ".sgm"`.xml;
    done

