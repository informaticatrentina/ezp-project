# ezp-project
Installazione ambiente eZ-Publish Informatica Trentina

## Guida per l'installazione
Scaricare ed installare eZ-Publish Community Project 2014-11 reperibile al seguente indirizzo: http://share.ez.no/downloads/downloads/ez-publish-community-project-2014.11

Sostituire all'interno dell'installazione il file composer.json con il file presente in questo repository

Lanciare il comando composer update

Nel site.ini.append.php del proprio siteaccess aggiungere le seguenti righe per atttivare le estensioni
  
  [ExtensionSettings]
  ActiveAccessExtensions[]=ezjscore
  ActiveAccessExtensions[]=ezmultiupload
  ActiveAccessExtensions[]=eztags
  ActiveAccessExtensions[]=ezflip
  ActiveAccessExtensions[]=ezautosave
  ActiveAccessExtensions[]=ezoe
  ActiveAccessExtensions[]=ezformtoken
  ActiveAccessExtensions[]=ezstarrating
  ActiveAccessExtensions[]=ezgmaplocation
  ActiveAccessExtensions[]=ezwt
  ActiveAccessExtensions[]=ezflow
  ActiveAccessExtensions[]=ezcomments
  ActiveAccessExtensions[]=ezie
  ActiveAccessExtensions[]=ezprestapiprovider
  ActiveAccessExtensions[]=ezfind
  ActiveAccessExtensions[]=openpa
  ActiveAccessExtensions[]=ocbootstrap
  ActiveAccessExtensions[]=ocoperatorscollection
  ActiveAccessExtensions[]=ocsearchtools
  ActiveAccessExtensions[]=ocinfotncstoez
  ActiveAccessExtensions[]=sqliimport
  ActiveAccessExtensions[]=ocopendata
  ActiveAccessExtensions[]=pat_base
  ActiveAccessExtensions[]=ezchangeclass
  ActiveAccessExtensions[]=ocmaps
  ActiveAccessExtensions[]=occsvimport
  ActiveAccessExtensions[]=occhangeobjectdate
  ActiveAccessExtensions[]=jcremoteid
  ActiveAccessExtensions[]=ngpush
  ActiveAccessExtensions[]=ocplaylist
  ActiveAccessExtensions[]=ocembed
  ActiveAccessExtensions[]=occookielaw
  ActiveAccessExtensions[]=ocrss
  ActiveAccessExtensions[]=ocfedauth
  ActiveAccessExtensions[]=itobjectsync
  ActiveAccessExtensions[]=itclassmanager	

Scaricare localmente il file doc/classi_sinet_template.ezpkg, eseguire l'importazione del file tramite Impostazioni - Pacchetti - Importa nuovo pacchetto

Durante la fase di installazione saltare l'installazione di ogni classe di contenuto che l'importatore trova già presente e proseguire sulla successiva

Finita l'importazione andare sulla URL del proprio sito agguingendo alla fine dopo index.php la seguente stringa /itclassmanager/classdiff

Verificare quali classi di contenuto sono sincronizzate (verde) e quali non, per queste ultime provvedere ad eseguire una sincronizzazione/installazione manuale rimuovendo gli attributi aggiuntivi e forzando la sincronizzazione se necessaria



