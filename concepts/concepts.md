!SLIDE
# Concepts #

!SLIDE
# Etat projet #

Core : officiallement supporté (accès brand / asset)
Incubated : sur la voie pour devenir core (accès limité brand / access)

http://wiki.openstack.org/wiki/Governance/Approved/NewProjectProcess

!SLIDE
# Utilisateur #

Réprésentation digitale d'une personne, un système ou un service. 

!SLIDE
# Credentials #

Données qui représente un utilisateur et qui prouve son identité.

Exemples : 

- Login / mot de passe
- Login / API key
- Token

!SLIDE
# Role #

Ensemble de droits qui permet un nombre spécifique d'opérations.

!SLIDE
# Tenant #

"Conteneur", une collection de souscription à des services ou des ressources.

!SLIDE
# Token #

Un texte arbitraire utilisé comme ressource d'accés. Chaque token à un scope
qui décrit les ressources qui sont accessibles. Un token est révocable.

!SLIDE
# Authentification #

Tentative de confirmation de l'identité d'un utilisateur à l'aide de credentials.
Si l'authentification est réussie; un token est donné.

!SLIDE
# Endpoint #

Point d'entée d'Un service accessible par le réseau.
