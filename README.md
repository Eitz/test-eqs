# Instructions

To run the exercices some dependencies are necessary. This project uses `cpanm` and `local::lib` so that it does not pollute your env with the dependencies it uses (it installs them in the project directory).

To install the dependencies and run the exercices:

1. cd to the exercice directory (perl-exercises)
2. Execute `install-deps.sh` (or `install-deps.bat` if using Windows) to install the dependencies.
3. Run each exercice with `perl n-exercice-name.pl` (exercice 1 is the only one that requires a parameter)

## Troubleshooting

### Unable to install the dependencies? 

Tip: a clear install of strawberry-perl is able to install all deps successfully using the instructions above.

1. If `cpanm` or `local::lib` aren't available, they can be installed with:

`$ cpan App::cpanminus local::lib`

2. If you're unable to install them for any reason, the dependencies can be installed using just cpan:

`$ cpan DBI DBD::mysql Mojolicious Config::Simple`

3. If the above method was used, lines mentioning `local::lib` in the perl exercice files must be removed.

### Unable to connect to MySQL in exercice 3?

Exercice 3 depends on `extra-files/config.ini`, set your connection string, user and password in it.

### In exercice 4 this happens: Can't create listen socket: Address already in use

The 3514 port is already in use, please stop the service that is using it or edit the perl file to use another port.
