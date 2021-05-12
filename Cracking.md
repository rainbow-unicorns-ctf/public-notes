## keepass file

KEEPASS_FILE=keepass.kdbx; keepass2john ${KEEPASS_FILE} | sed "s/${KEEPASS_FILE%%.*}://" > uncracked.hash
hashcat -m 13400 -a 0 -w 1 uncracked.hash cracklib-words
