# google api html
https://openclassrooms.com/courses/google-maps-javascript-api-v3


# ######################################################
# PHP symfony
# ######################################################

SimpleSAMLphp Identity Provider

# Saml
Security Assertion Markup Language (SAML)
open-standard data format for exchanging authentication and authorization data between parties, in particular, between an identity provider and a service provider.

#bundle symfony : aerialship/saml-sp-bundle

# ######################################################
# KARMA
# ######################################################

#install karma
Karma runs on node

Install Node on mac
>go on the web site and download the .dmg file

you can download the following package.json file:
>curl -O https://gist.githubusercontent.com/bbraithwaite/7432f64ea45e028eb23c/raw/2a6e23cee09e7737c30cc790393a9b273070fbcb/package.json

Once you have the package.json file, start the following command:
>npm install

Once complete, verify the installation by the terminal command:
>./node_modules/karma/bin/karma start

#configure karma

Create a 'karma.conf.js'
provide some configuration for the Karma service. To template this, run the following and accept the defaults:
A new file will be created in the root called 'karma.conf.js.
>./node_modules/karma/bin/karma init

The tests can now be exectuted as:
because there is in your package.json :   
>"scripts": {
    "test": "./node_modules/karma/bin/karma start karma.conf.js"
  },

>npm test

#install brower
npm install -g bower


#instal angular with bower










# ######################################################
# TODO mercredi
# ######################################################

#arkanya
#angular > datepicker (ok)
#jquery maltem > datepicker (ok)
#js > test protractor (ok)

>Angular > Form > $prestine, $dirty, $valid, form.$setPrestine();
>XMPP : protocole messagerie (VU)
>Tribe : appli chat (VU)
>PitPut : chat en vrai temps réel (1 caractère tapé, 1 caractère envoyé) (VU)

# ######################################################
# ZeroToOne
# ######################################################

#C3 - All happy companies are different
-Competitor lie
-Monopoly lie : selon le point de vue, google peut déternir 80% du marché comme 3%
si on regarde au niveau du search advertising ils sont à 80%
si on regarde au niveau de l'advertising online ils sont à 3%

#C4 - Ideology of competition
-The Herro's error : fight for honor rather than quit when it's necessary
-Marx : p
-Shakespear's
-Google Vs Microsoft : Apple came along


# ######################################################
# Socket.Io
# ######################################################
-Source tutorial : https://openclassrooms.com/courses/des-applications-ultra-rapides-avec-node-js/socket-io-passez-au-temps-reel

-Socket.io decide itself regarding your own browser configuration which kind of technology it has to use :
>WebSocket / Adobe Flash Socket / AJAX long polling / AJAX multipart streaming / Forever Iframe / JSONP Polling
>AJAX Long Polling (le client demande en continu au serveur s'il a des nouveautés pour lui, pas le plus "propre" ni le plus efficace mais ça marche
>Forever Iframe" qui se base sur une iframe invisible qui se charge progressivement pour récupérer les nouveautés du serveur.

-Install socket.io
>npm install socket.io

-Principe client / server
>Le fichier serveur (ex : app.js) : c'est lui qui centralise et gère les connexions des différents clients connectés au site.
>Le fichier client (ex : index.html) : c'est lui qui se connecte au serveur et qui affiche les résultats dans le navigateur.

-Send a message
>socket.emit('TypeMessage1', { ... 1 object JSON covering the body of your message ... });
>socket.emit('TypeMessage2', { content: 'Vous êtes bien connecté !', importance: '1' });

-Quand le server recoit une connection, il peut répondre par un message
>io.sockets.on('connection', function (socket) {
        socket.emit('message', 'Vous êtes bien connecté !');
});

-Coté client on peut écouter:
><script>
    var socket = io.connect('http://localhost:8080');
    socket.on('message', function(message) {
        alert('Le serveur a un message pour vous : ' + message);
    })
</script>

-Broadcast
>io.sockets.on('connection', function (socket) {
	socket.emit('message', 'Vous êtes bien connecté !');
	socket.broadcast.emit('message', 'Un autre client vient de se connecter !');
	socket.on('message', function (message) {
		console.log('Un client me parle ! Il me dit : ' + message);
	});
});

# ######################################################
-A MODULE is essentially a configuration for Angular's dependency injector which allows you
to group a set of controllers, directives, filters, etc. under one particular name.

-Each module can also specify other module on which it depends so that this allows you to re-use and structure your code.

-Angular also automatically adds its default modules, ng and ngLocale which provide core functionality to your applications.



# ######################################################
# Auth0
# ######################################################
https://auth0.com


# ######################################################
# MARDI
# ######################################################

-form > input DateStart
-form > input DateEnd
-form > error >  message
-form > error > DateFin
-form > error > DateStart

-pb : parfois il y a des dateEnd et des date_end (uniformiser)
-renommer

>create a page AdminMessage (OK)
>create the link in the menu (OK)
>create the route (OK)



# ######################################################
# AngularJS State VS route
# ######################################################

-you can change the parts of your site using your routing even if the URL does not change.




# ######################################################
# TODO
# ######################################################

#require.js


#protractor

#underscore
explication des avantages : https://tedkulp.com/2014/07/a-few-reasons-to-use-underscore-js-or-lo-dash/

#Angular Material



# ######################################################
# mission on the front side of portal
# TODO MARDI
# ######################################################

>create the model.js => 'pgdiAdminMessageModel' (ok)
>create the service => 'pgdiAdminMessageService' (ok)
>create the controller (ok)
>test to display something (ok)

-Où créé t-on la page d'admin ?
-Où affiche ton le controlle des données du champs ? toastr ou à coté des inputs?
-Comment gère t'on le fait qu'il faille appeler CREATE la premiere fois et UPDATE les fois d'après ? (Mickael)

# ######################################################
# Lancer le FRONT portal
# ######################################################

#pour activer : docker.local:3000
>vagrant up
>source .profile
>dockerPortal
>gulp clean
>gulp serve


# ######################################################
#
# PLANNING
#
# ######################################################

worth it
https://github.com/git-tips/tips



*-
-lundi : dev service AdminMessage

-mardi : apprentissage test unitaire

-mercredi matin : test unitaire sur le service adminMessage

-mercredi apres : refactoring AdminMessage (service)

-jeudi matin :
-->  Repository test (OK) (test functionnel / fixture, getresult/getArrayresult)
-->  tirer au clair le isValid les validators (OK) ->le form->isValid prend en compte le fichier validation.yml
-->  Form Type - test unitaire (OK)
-->  quand la function laod de la fixture est appelée? > via une commande de la console (OK)
-->  par quel process nos tests utilisés la BD test au lieu de la bd classique ? -> config_test.yml (OK)

-----Controller.php (100%) clientGetAction not convered (ok)
-----Type.php (100%) onSubmit not covered (ok)
-----Entity/Service/Repo (100%)
----- Service > handleForm (100%) (social)
--> generer un report & boucler jusqu'a atteindre taux de couverture au top

-*

--> faire un point philosophique sur les tests effectués
--> relancer les tests
--> nettoyer les commmentaires
--> GIT > commit




"des contraintes naissent les habitudes"

--> add a constriant on en entity with annotation and check if the form->submit detects if something goes wrong (It should)
--> faire un point sur les différents types de tests (au niveau de la classe dérivéee : KernelTestCase, etc...)
--> faire un etat des lieux de l'utilisation des validators / differentes methodes


# ######################################################
#
# PHILOSOPHIE DE TESTS
#
# ######################################################

# test métier
Le test métier consistera à simuler l’exécution d’un processus avec le logiciel
le test métier consiste à assembler des tests fonctionnels, avec des données de tests en cohérence.

# test fonctionnel
Le test fonctionnel sera ciblé sur le niveau de granularité du cas d’utilisation

# test unitaire
Test Unitaire > En étant malin, le test unitaire pourra être une portion de test fonctionnel, ce qui d’une part évitera au développeur de se poser des questions, et d’autre part apporte une économie : le même cas de tests servira deux fois !

# ######################################################
#
# VALIDATIONS
#
# ######################################################

L'Alchimiste
Roman de Paulo Coelho


# 2 types of validation
-validate a form
-validate data before it is written into a database


# basic constraint with annotation
>class Author
...
    /* @Assert\NotBlank()
    public $name;
...


# using the 'Validator Service'
-Validator service reads the constraints and verify if the data on the object satisfies thoses constraints

-If validation fails, a non-empty list of errors (class ConstraintViolationList) is returned

>$validator = $this->get('validator');
>$errors = $validator->validate($author);
>if (count($errors) > 0) { ... }

# in fact the 'Validator Service' is often used indirectly
Most of the time, you won't interact directly with the validator service or
need to worry about printing out the errors.
Most of the time, you'll use validation indirectly when handling submitted form data.

# Validation and Forms
Symfony's form library uses the validator service internally to validate the underlying object after values have been submitted.

# A constraint violation > generate a FormError
The constraint violations on the object are converted into FormError objects


# ######################################################
#
# DIVERS
#
# ######################################################

# formFactory and customType
you can use the 'Service' named 'formFactory' and call its method 'create'
then you pass the class related to your own type -> ex : 'AdminMessageType'
>$myForm = $formFactory->create(AdminMessageType::class, $message);

it will create a form associted to your own Type.

# ######################################################
#
# $form->submit
#
# ######################################################

Forms consisting of nested fields expect an array in submit()

# submit indivual fields
You can also submit individual fields by calling submit() directly on the field
>$form->get('firstName')->submit('Fabien');


# ######################################################
#
# $form->handleRequest
#
# ######################################################




# ######################################################
# 4 accords tolteques
# ######################################################
1/ma parole doit etre impeccable
2/ne rien prendre personnellement
3/ne pas suppose
4/faire de son mieux



# ######################################################
# validation.yml
# ######################################################



# ######################################################
# Repository > valeur retournée
# ######################################################

# $q->getResult()
in that cas I get an array of objects
>$q = $qb->getQuery();
>return $q->getResult();



# $q->getArrayResult();
in that cas I get an array of array
>$q = $qb->getQuery();
>return $q->getArrayResult();


# ######################################################
# PHP Mapping classes to the ORM / ODM
# ######################################################
ORM - Object relational mapper
ODM - Object document mapper
you can define a class that can be persisted to both MySQL and MongoDB.

# ######################################################
# DEBUG / PHP / COVERAGE git
# ######################################################

# activer / desactiver le mode debug
php5enmode xdebug
php5dismode xdebug

# genereate rapport html coverage
 php vendor/phpunit/phpunit/phpunit -c app/phpunit.xml.dist --log-junit=build/gits/junit/phpunit.xml --testdox-html=build/reports/testdox.html --coverage-clover=build/reports/clover.xml --coverage-html=build/reports/coverage/ --colors --debug



# ######################################################
#
# LISTE DES TUTORIELS
#
# ######################################################

-Mock objects (voir pdf)
-Securité (voir pdf)
-Service : utilisation poussee : https://openclassrooms.com/courses/developpez-votre-site-web-avec-le-framework-symfony2/les-services-utilisation-poussee
-FOSRestBundle
-FOSUserBundle

# ######################################################
#
# TUTO : PHP / FOSUserBundle
#
# ######################################################

# general
la sécurityé vient sous symfony du bundle 'SecurityBundle'
app/config/security.yml

# L'authentification
Ce qui gère l'authentification dans Symfony2 s'appelle un FIREWALL,

# L'autorisation
Il agit donc après le firewall. Ce qui gère l'autorisation dans Symfony2 s'appelle L'ACCESS CONTROL.
Par exemple, un membre identifié lambda aura accès à la liste de sujets d'un forum, mais ne peut pas supprimer de sujet.

# security.yml > Section encoders
façon dont sont encodés les mots de passe dans votre application.
>plaintext : laisse les mots de passe en clair
>sha512 : un vrai encodeur qui va bien :)

# security.yml > Section role_hierarchy

le rôle ROLE_USER est compris dans le rôle ROLE_ADMIN.
Le ROLE_ADMIN a acces à tout ce qu'à acces le ROLE_USER
>ROLE_ADMIN:  ROLE_USER

# security.yml > Section providers
Un provider est un fournisseur d'utilisateurs.
Les firewalls s'adressent aux providers pour récupérer les utilisateurs et les identifier.

-------------------------------------
Exemple de provider à la main
-------------------------------------
exemple de provider défini à la main dans le fichier de config
Pour l'instant vous pouvez le voir dans le fichier, un seul fournisseur est défini, nommé in_memory (encore une fois, le nom est arbitraire). C'est un fournisseur assez particulier dans le sens où les utilisateurs sont directement listés dans ce fichier de configuration, il s'agit des utilisateurs « user » et « admin ».

>security:
    providers:
        in_memory:
            memory:
                users:
                    user:  { password: userpass, roles: [ 'ROLE_USER' ] }
                    admin: { password: adminpass, roles: [ 'ROLE_ADMIN' ] }

----------------------------------


-------------------------------------
Exemple de provider FOSUserBundle
-------------------------------------
>providers:
    fos_userbundle:
        id: fos_user.user_provider.username
----------------------------------

# security.yml > Section firewalls

Comme on l'a vu précédemment, un firewall (ou pare-feu) cherche à vérifier que vous êtes bien celui que vous prétendez être.
Ici, seul le pare-feu 'dev' est défini, nous avons supprimé les autres pare-feu de démonstration.
Ce pare-feu permet de désactiver la sécurité sur certaines URL, on en reparle plus loin.

>security:
>    firewalls:
>        dev:
>            pattern:  ^/(_(profiler|wdt)|css|images|js)/
>             security: false
>(_)

# security.yml > Section access_control
>security:
    access_control:
        #- { path: ^/login, roles: IS_AUTHENTICATED_ANONYMOUSLY, requires_channel: https }




# ######################################################
#
# TUTO : PHP / MOCK OBJECTS AND STUB METHODS (part 4)
#
# ######################################################
>source tutorial : https://jtreminio.com/2013/03/unit-testing-tutorial-part-4-mock-objects-stub-methods-dependency-injection/

# bad solutions
-RunKit > replace code during runtime > 'monkey patching' > bad idea
-is_a() (check type of an object, direct or parent)
-bad solution : To mock a class you could extends that class and override its method. But if you have hundreds of classes, it becomes a real burden!

# getMock()
good solution:
-getMock() method > create a new class on the fly,

# exemple
-AuthorizeNetAIM with construct(api_id, trans_key) is the class we want to mock because we don't want to rely on its core complexity
--> (1) : class name
--> (2) : ??
--> (3) : an array containing the constructor parameters.
>$authorizeNet = $this->getMock('\AuthorizeNetAIM', array(), array($payment::API_ID, $payment::TRANS_KEY));

# getMockBuilder()
It is little more than a wrapper around the getMock()
method above, but it provides a much more human-readable format of chained methods, making creating mocked objects a breeze.

> $authorizeNet = $this->getMockBuilder('\AuthorizeNetAIM')
    ->setConstructorArgs(array($payment::API_ID, $payment::TRANS_KEY))
    ->getMock();

getMockBuilder() returns a mock object, which is simply an object that has behavior similar to the original object.

# dump a mocked object
you can see it is very similar to the original
>var_dump($authorizeNet);

#methods of a mocked object
display the list of methods of the mocked object
>print_r(get_class_methods($authorizeNet));

but if you call one of its methods, it returns Null
These methods are considered stubs!

#stub method
A stub method is a method that mimics the origin method in two ways - same name and same parameters accepted. What makes a stub method special, however, is that all the code within it has been erased.

In our example : What is great about this is that the authorizeAndCapture() method is no longer sending a request to the Authorize.net servers. Instead, it is returning a known value (NULL) every single time it is called.

#override the value returned by a stub method
Here is the kicker, though: You can now override the value returned by a stub method from within your test.

This means that you define the value return by your stub in your test, and when you run your test your code will think the value returned is normal, and act accordingly to your wishes.

To override the return value of a stub, you have to be introduced to 5 new PHPUnit methods:

We are stating that the $authorizeNet object expects to call one time the method authorizeAndCapture(),
and it will return the value RETURN VALUE HERE!.
>$authorizeNet->expects($this->once())
    ->method('authorizeAndCapture')
    ->will($this->returnValue('RETURN VALUE HERE!'));

# expects(.. )
which accepts a single parameter: the number of times we are expecting the method to be called in our code > once(), any(), never()
If we state that the method is expecting to be called one time, and it ends up never being called, or called more than once, our test will fail.

any() is a cheat that says, "I don't care if it is ever called, but if it is, here is the expected return.".

# method(..)
method() accepts the name of the method to override.

# will (..)
Then we have will() which is simply wraps the important returnValue() where you actually define what value is returned.

# exemple
if the expected value returned by the method 'authorizeAndCapture' ia n object with an approved and transaction_id key.
A simple shortcut for these types of objects is to use \stdClass():

>$response = new \stdClass();
$response->approved = true;
$response->transaction_id = 123;

>$authorizeNet->expects($this->once())
        ->method('authorizeAndCapture')
        ->will($this->returnValue($response));



# ######################################################
#
# TUTO : PHP / MOCK OBJECTS AND STUB METHODS (part 5)
#
# ######################################################

# Mock object
A mock object is an object that you would create using PHPUnit's getMockBuilder() method.
It is basically an object that extends the class you define and allows you to perform nifty tricks and assertions on it.

# Stub Method
A stub method is a method contained within a mock object that returns null

# Mock method
it does the exact same thing its original method would. it will not return null, unless it is what it originally did

### THE FOUR PATHWAYS OF GETMOCKBUILDER

#(1) : Do not call setMethods()
This produces a mock object where the methods
---Are all stubs,
---All return null by default,
---Are easily overridable

> $authorizeNet = $this->getMockBuilder('\AuthorizeNetAIM')
    ->getMock();

#(2) : passing an Empty array
You can pass an empty array to setMethods():

This produces a mock object where the methods
---Are all stubs,
---All return null by default,
---Are easily overridable

>$authorizeNet = $this->getMockBuilder('\AuthorizeNetAIM')
    ->setMethods(array())
    ->getMock();

#(3) : passing null
This produces a mock object where the methods
---Are all mocks,
---Run the actual code contained within the method when called,
---Do not allow you to override the return value

>$authorizeNet = $this->getMockBuilder('\AuthorizeNetAIM')
    ->setMethods(null)
    ->getMock();

#(4) : Passing an array containing method names
The methods you have identified:
---Are all stubs,
---All return null by default,
---Are easily overridable

Methods you did not identify:
---Are all mocks,
---Run the actual code contained within the method when called,
---Do not allow you to override the return value

>$authorizeNet = $this->getMockBuilder('\AuthorizeNetAIM')
    ->setMethods(array('authorizeAndCapture', 'foobar'))
    ->getMock();

This means that in the $authorizeNet mock object the ::authorizeAndCapture() and ::foobar() methods would return null




#######################################################
# regle des retours
#######################################################
GET -> on renvoit l'objet directement
POST/PATCH -> on encapsule la reponse dans un objet result : {.... ....}


#######################################################
#
# TODO LIST
#
#######################################################




-Youtube > advanced docker workshop (David Ward)
-CRUD : create read update delete
-Peer programming
-Confluence (wait mdp)
-Jira (wait mdp)
-revoir schema vu avec Zak éclatement des projets GRDF (pop, portail, …)
-lire les PSR accepted > http://www.php-fig.org/psr/
-se renseigner sur les mark down ? le format markdown sheetset

-Slack (OK)
-Mail GRC (OK)
-Mail Maltem (OK)

#######################################################
#
# MAC > ENVIRONNEMENT DE TRAVAIL
# à faire après chaque reboot du système
#
#######################################################

lancer la vagrant
>vagrant up

se connectersR en ssh dans la vagrant
>vagrant ssh

aller dans le repertoire suivant
>/var/www/gdi/

lancer la commande qui regenere les alias
>source .profile

lancer la commande qui genere les conteners dockers
>dockerReinitGDI

se conecter sur le docker portal-dev
>/var/www/bin>sh reinit_dev.sh

pour se reconnecter sur la BD portal-dev avec SEQUEL
il faut aller sur le docker mysql et récupérer l'ip du contenair : 127,....
>ifconfig

Symphony error cache>>
>rm -rf /var/tmp/portail/*
>chmod -R 777 /var/tmp/


Fullmetal Alchemist

#######################################################
#
# PORTAILS / CARMA / GRDF
#
#######################################################
MAIL GRDF (OK)
https://webmail.mygdfsuez.com
login : SDMN01\MN5426
mdp : (2*)
jerome.folsi@external.grdf.fr
———————————
CONFLUENCE (NOT)
https://confluence.carma.grdf.fr
login : mn5426 sans domain
mdp : carma + *
———————————
JIRA (NOT)
https://jira.carma.grdf.fr
login : mn
———————————
CROWD
https://crowd.carma.grdf.fr
nouveau MDP : !
———————————
SLACK
team : carma-communication
login : jerome.folsi@external.grdf.fr
mdp : (1*)
———————————
TEL PRO
Numéro de téléphone : 0171262574
Login : 602574
Code PIN ou numéro d'identification personnel : 2034

--------
SYGES
https://syges.maltem.com/sygesweb
jfolsi
login : carm + **

--------
OPENTIME
http://opentime.info/grdf/
mdp : 4830ee26
login : jerome.folsi





#######################################################
# GENERAL
#######################################################
-Atlassan : Confluence/Jira/GitBucket
-LTS : Long term support
-SourceTree : an graphic app to manage your git
-Jira > choper la liste des choses à faire
-fatme > bref de la quad > je lui donner la liste tout ce qu’il me faut
-bitbucket ??
-tty > Une console virtuelle, /dev/tty* est une console lancée généralement par le processus init.


#######################################################
# JIRA
#######################################################
login : MN5426
password : classic mallet


#######################################################
# MAC
#######################################################
-changements de bureaux : CTRL + FLECHES
-restore a minimized app : CMD+L


#######################################################
# ITERM
#######################################################
-create split pane : CMD+D / CMD+SHIFT+D
-navigate split panes : CMD+ALT(opt)+fleche


###########################################################################
###########################################################################
# ATOM
###########################################################################
###########################################################################
-auto indent option : CMD SHIFT I
-search command : CMD SHIFT P


###########################################################################
###########################################################################

# GIT

###########################################################################
###########################################################################

how to initialiaze a new directory for using git
This creates a new subdirectory named .git
>git init


How to list all the branches
>git branch

How to list all the branches ?
>git branch -a

How to create a new branch ?
>git branch <branchname>

How to create new branch and switch to it ?
>git checkout -b <branchname>

How to create a fetch a remote branch into a local one (and switch to it)?
>git checkout -b test origin/test

How to delete a branch in a safe way > it does delete the branch if it has undergo changes
>git branch -d <branch>

How to delete a branch in a brutal way
>git branch -D <branch>

How to rename a branch?
-GIT BRANCH -M : rename the current branch

When do we spawn a new branch?
>to add a new feature, or fix a bug > you spawn a new branch to encapsulate your changes.

when you have 2 branches > it’s not possible to work on both of the branches in parallel
-When you work on a branch > it keeps the main master branch free from questionnable code

-Branches are just pointers to commits. When you create a branch, all Git needs to do is create a new pointer—it doesn’t change the repository in any other way.

-GIT GREP « word »
search a word in the tree

-HEAD :

>git clone : on chope le fichier .GIT, contenu

—
update remote list of branches (git fetch -p) >
it is highly recommended to launch that command before typing git branch -a
>git fetch -p
>git branch -a

————————
create localy an alias named ‘develop’
bind the remote branch named ‘develop’ to my local branch ‘develop’
it’s worth noting that the names can be different
>git checkout -b develop origin/develop

————————
to create a remote branch from your local branch
you just need to do that once
>git push -u origin develop
…..then you can push your files overtime you need
———————
>git add
…modifsA
>git commit
modifsB
>git checkout .
..revient aux motifs A
>git push
————————

————————
clone a specific branch from a remote repository
>git clone -b develop git@github.com:jerfolsi/test1.git

create a local branch 'test' et derived from remote/master
>git checkout -b test origin/master

pusher une branche en ligne
>git push <remote branch> <local branch>
>git push origin test




###########################################################################
###########################################################################

SLACK

###########################################################################
###########################################################################

-on peut le synchroniser avec TRELLO, GOOGLE CALENDAR, SKYPE
-BIRDLY : bot to make request to soft like : SALESFORCE












###########################################################################
###########################################################################

# DOCKER

###########################################################################
###########################################################################

-telecharger une image docker (OK)
-lancer une image docker (OK)
-lancer une image apache (OK)
-faire une translation de port (OK)
-faire un partage de directory (OK)

-lancer une image avec MYSQL (!!)
-travailler avec un DockerFiles (!!)
https://semaphoreci.com/community/tutorials/dockerizing-a-php-application




*************************************************
CREATE A DOCKER IMAGE / DockerFile
Customize ton image
*************************************************


>vi DockerFile
- - - - - -
FROM nimmis/apache-php5
MAINTAINER SemaphoreCI <dev@semaphoreci.com>
COPY 000-default.conf /etc/apache2/sites-available/000-default.conf
EXPOSE 80
EXPOSE 443
CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]
- - - - - - - -
fichier 000-default.conf (qui est dans le repertoire en cours)
# 000-default.conf

<VirtualHost *:80>
 ServerAdmin webmaster@localhost
 DocumentRoot /var/www/public

 ErrorLog ${APACHE_LOG_DIR}/error.log
 CustomLog ${APACHE_LOG_DIR}/access.log combined

 <Directory /var/www>
 Options Indexes FollowSymLinks
 AllowOverride All
 Require all granted
 </Directory>
</VirtualHost>
- - - - - - - -


créer l’image à partir du Dockerfile du repertoire en cours
>docker build .
>docker build nom_image .  //version pour lui donner un nom

pour voir les images que l’on a
>docker images

effacer une image
>docker rmi -f 88fffaacab6c (image-id)




# *************************************************
# INSTALL UN DOCKER PHP
#*************************************************

1/step: télécharger la dernière image PHP depuis le hub
>docker pull php:latest

1B/step : autre façon de télécharger .. en lançant directement
une image que l’on a pas encore sur le disque dur
-d : as a demon

>docker run -d nimmis/apache-php5

let’s print out container
> docker ps
> docker ps -s (pour afficher l’espace pris)

pour lancer le container avec un nom spécificque
>docker run -d --name="apache_server" nimmis/apache-php5

pour effacer l’alias ‘apache_server’
>docker rm apache_server

pour relancer un conteneur qui a déjà été créé au moins une fois
>docker start apache_server

pour se logger dans le container à travers la commande bash
>docker exec -it apache_server bash

on vérifie que apache tourne bien
>container/ >/etc/init.d/apache2 status

When creating an image, we need to make sure
to expose it through a specific port so that the other containers, browsers, etc. can access it.

Expose default ports
>docker run -tid -P  --name apache_server nimmis/apache-php5

Specify a different post <host port>:<container port>
>docker run -tid -p 8080:80 --name apache_server nimmis/apache-php5

tie an host directory to a container directory
>docker run -tid -p 8081:80 -v /var/www/projetphp:/var/www/html --name="apache_server" nimmis/apache-php5
- - - - - - - - - -


*************************************************
DOCKER COMPOSE
dans l’environnement GDI
*************************************************
Docker Compose est un outil qui permet de gérer plusieurs DockerFile (pour créer un image)

aller dans le repertoire /var/www/gdi

(si j’ajoute rien il prend le fichier par default : docker-compose.yml)
>docker-compose

moi je dois utiliser le docker-compose.dev.yml
cette commande va devenir le préfixe de plusieurs autres commandes
>docker-compose -f docker-compose.dev.yml

afficher la liste des containers qui tournent et qui sont attachés
a cette configuration
>docker-compose -f docker-compose.dev.yml ps

remove the container related to the ‘mysql-portal’ image
>docker-compose -f docker-compose.dev.yml rm mysql-portal

on créé un container(instance) depuis l’image ‘mysql-portail’
>docker-compose -f docker-compose.dev.yml up -d mysql-portal

**********************************
-Doc official > https://docs.docker.com/engine/understanding-docker/
-Both the Docker client and the daemon can run on the same system

#*************************************************
# Autre doc
#*************************************************
-Il a l’avantage de ne virtualiser que la partie application et pas du tout la partie système ni le noyau.
-Virtualisation legere
-Docker utilise une techno recente : le LXC
-Sous MAC > Faire tourner une machine virtuelle Ubuntu dans laquelle on fait tourner Docker

>docker version
>docker ps
>docker run hello-world
>docker run -d -p 80:80 —-name webserver nginx

install sous ubuntu
>sudo apt-get install docker.io

on peut créer un alias
>alias docker="sudo docker.io"

Docker.io, ce n’est pas juste un software, c’est aussi un service qui héberge les images.

on va télécharger une image de base sur laquelle baser toutes nos images
récupération des images “ubuntu”, qui vont nous servir d’images de base. Elles sont toutes faites et prêtes à l’emploi

>docker pull ubuntu

vous obtenez plusieurs images que vous pouvez lister ainsi
>docker images

pour lancer une commande
Ceci va lancer l’image, lancer la commande, et dès que la commande se termine, arrêter l’image
>docker run id_image commande
>docker run 74fe38d11401 echo 'YEAHHHHHHHHHHHHHH'


###########################################################################
###########################################################################

#VAGRANT

###########################################################################
###########################################################################

attention à penser à lancer carmaroute.sh
>sh carmaroute.sh

installer le plugin vgguest
>vagrant plugin install vagrant-vbguest (OK)

pour checker le status de la vagrant
>vagrant status (OK)

exécuter le fichier de conf
>vagrant up (OK)

Si jamais la vagrant patine à se lancer il faut effacer le repertoire
temporaire dans lequel la vagrant fait sa sauce
>sudo rm -rf /etc/exports
>vagrant halt

vaguant up plante car je n’ai pas de fichier .gitconfig
1/soit je créé le .gitconfig à la main
2/soit j’installe par exemple SourceTree qui me crée manuellement le fichier .gitconfig

to stop gracefully the virtual machine
>vagrant halt (OK)

to start again the vagrant machine
>vagrant up (OK)

>comment je me log dans ma machine virtuelle ?

source .profile
dockerReinitGDI


###########################################################################
###########################################################################

UTILISER DOCKER / VAGRANT (avec : Houssman)

###########################################################################
###########################################################################

/etc/hosts > binder l’ip avec un nom du genre /docker.local
10.0.59.10      docker.local

lancer la vagrant


pour charger tous les alias (à refaire à chaque lancement de session ssh)
>/gdi/source .profile

créer tous les dockers
>/gdi/dockerReinit

>METHODE 1 : pour se connecter à un docker depuis vagrant
e6cae9a80bb6 est le numéro du docker trouvé grace a la commande docker ps
docker exec -it e6cae9a80bb6 bash

>METHODE 2 : pour se connecter à un docker
>/gdi/cat .profile


*** DOCKER PORTAL
>dockerPortal
>gulp clean
>gulp build
>exit

*** DOCKER PORTAL BACK
>dockerPortalBack
>sh bin/reinit_dev.sh

*** DOCKER PORTAIL

----------------------------------------------------------------------
----------------------------------------------------------------------
SYMFONY : TEST
----------------------------------------------------------------------
----------------------------------------------------------------------
*********************************************
-create a service with DI (OK)
-form : send artificial POST (en cours…)
-formules encapsulés dans un formulaire




*********************************************
CREATE AND MANAGE A SERVICE WITH JMS\DI

—-test a simple implementation (OK)
——test injection of a parameter into the service constructor (OK)

don’t forget to use JMS\DiExtraBundle\Annotation as DI;

-step 1 : create a Service class and use an annotation to specify the proper name service
-step 1-b : just above the construct declaration, insert a @DI\InjectParams … That gives the service
	    the ability to auto insert the right parameters. @DI\Inject
-step 2 : in your controller declare a property referring to your specific servce

————————————————
/**
 * Class TestService
 *
 * @package User\Service
 * @DI\Service("portal.service.test", public=true)
 */
class TestService
{
    /**
     * @var \Doctrine\ORM\EntityManager
     */
    public $em;

    /**
     * @var \Symfony\Component\Form\FormFactory
     */
    public $formFactory;

    /**
    * @DI\InjectParams({
    *     "em" = @DI\Inject("doctrine.orm.entity_manager"),
    *     "formFactory" = @DI\Inject("form.factory")
    *    })
    */
    public function __construct($em, $formFactory)
    {
        $this->em = $em;
        $this->formFactory = $formFactory;
    }

————————————————
class UserController extends FOSRestController
{
    /**
     * @var TestService
     * @DI\Inject("portal.service.test")
     */
    protected $testService;

}

*********************************************
Symphony error cache>>
>>  rm -rf /var/tmp/portail/*
>>  chmod -R 777 /var/tmp/






###########################################################################
###########################################################################

# PHP / SYMPHONY

###########################################################################
###########################################################################

Dans le Type/BuildForm on peut directement utiliser les constraintes sur chaque champs
Mais on va privilégier le fichier Ressources/config/validation.yml
>  'constraints' => [
      new NotNull([
        'message' => 'Le champ dataStart est requis'
      ])]

Pour que le fichier ressources/config/validation.yml soit pris en compte, il faut
bien parametrer le fichier /app/config.yml
> validation:      { enabled: true, enable_annotations: false }
> il faut bien mettre les enable_annotations à false

@todo : learn about >> Formulaires / AbstractType -> méthode configureOptions
  $resolver->setDefault(... with PATCH ...)


# form > Cross-site request forgery
> 'csrf_protection' => false


# #########################################################
# Using FIXTURES
# #########################################################

# Download the Bundle
>composer require --dev doctrine/doctrine-fixtures-bundle

# Enable the Bundle in app/AppKernel.php
>$bundles[] = new Doctrine\Bundle\FixturesBundle\DoctrineFixturesBundle();

# loading fixtures
By default the load command purges the database, removing all data from every table.
To append your fixtures' data specify the --append option
> php app/console doctrine:fixtures:load
>php app/console doctrine:fixtures:load -n --fixtures= src/PortalBundle/DataFixtures/ORM -e test --append

The task will look inside the DataFixtures/ORM/ (or DataFixtures/MongoDB/ for the ODM) directory of each bundle and execute each class that implements the FixtureInterface

# Sharing Objects between Fixtures
For example, what if you load a User object in one fixture, and then want to refer to it in a different fixture in order to assign that user to a particular group?
> doc here : http://symfony.com/doc/current/bundles/DoctrineFixturesBundle/index.html#step-1-download-the-bundle


# ---------------------------------------------------------------------------
# Test d'un controller
# ---------------------------------------------------------------------------

1/Créer une classe DataFixtures/ORM/LoadAdminMessageData
function load(..) qui va ajouter un objet en BD Test

2/Lancer le script bin/reinit_test.sh
cela va remplir la BD test
>bin/reinit_test.sh

that script contains :
>php app/console doctrine:fixtures:load -n --fixtures= src/PortalBundle/DataFixtures/ORM -e test --append

3/lancer le script de test
>php vendor/phpunit/phpunit/phpunit --group admin-controll -c app



>php vendor/phpunit/phpunit/phpunit --group security -c app
>php vendor/phpunit/phpunit/phpunit --group portalAuthenticator -c app


'app' is the directory containing the file : phpunit.xml.dist
