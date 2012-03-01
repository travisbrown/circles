The files in `lb/xml` are produced by running the following command:

    for f in lb/sgml/*.sgm; do
        osx -xlower -xcomment -xempty -xndata $f 2>> conversion-warnings.txt | \
        xmllint --format - > lb/xml/`basename $f ".sgm"`.xml;
    done

