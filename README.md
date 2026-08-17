
Mampirafy Tool
Version: 1.0.0
Format: JSON
Type: Conversation Template

Présentation
Mampirafy Tool est un prototype basé sur des fichiers JSON permettant de structurer des conversations sous une forme simple, lisible et facilement modifiable.

Le projet utilise un format minimaliste : chaque message contient uniquement le nom du participant et le contenu du message.

Structure du projet

Mampirafy-Tool/
├── README.md
├── templates.json
└── conversations/
    └── conversation.json


Format d'une conversation
Une conversation contient trois éléments principaux :

title — titre de la conversation
status — état de la conversation
participants — liste des participants
messages — contenu de la conversation
Exemple :

{
  "template": {
    "title": "Conversation Template",
    "status": "active",

    "participants": [
      "user1",
      "user2"
    ],

    "messages": [
      {
        "name": "user1",
        "message": "Bonjour, comment vas-tu ?"
      },
      {
        "name": "user2",
        "message": "Bonjour, ça va bien. Et toi ?"
      },
      {
        "name": "user1",
        "message": "Je vais bien aussi. Je voulais te parler."
      },
      {
        "name": "user2",
        "message": "Bien sûr, je t'écoute."
      }
    ]
  }
}

Ajouter un message
Pour ajouter un nouveau message, il suffit d'ajouter un nouvel objet dans messages.

{
  "name": "user1",
  "message": "Votre nouveau message..."
}

Ou :

{
  "name": "user2",
  "message": "Votre réponse..."
}

Remplacer les utilisateurs
user1 et user2 sont des noms génériques utilisés dans le template.

Ils peuvent être remplacés par les noms souhaités :

"participants": [
  "Andry",
  "Miora"
]

Les messages utilisent ensuite les mêmes noms :

{
  "name": "Andry",
  "message": "Bonjour."
}

{
  "name": "Miora",
  "message": "Bonjour, comment vas-tu ?"
}

Principes du format
Mampirafy Tool utilise volontairement une structure simple :

pas d'identifiant utilisateur obligatoire ;
pas d'identifiant de message ;
pas de date dans le contenu du message ;
pas d'heure ;
un nom pour identifier l'auteur ;
un champ message pour le contenu.
Cette simplicité facilite la lecture et la modification manuelle des fichiers JSON.

Validation JSON
Avant d'utiliser un fichier, vérifier que le JSON est correctement formé.

Chaque propriété doit utiliser des guillemets doubles :

{
  "name": "user1",
  "message": "Message de test"
}

Les éléments d'une liste doivent être séparés par des virgules.

templates.json
Le fichier templates.json sert de modèle de départ pour créer de nouvelles conversations.

Il peut être copié puis adapté :

templates.json
      ↓
conversation.json
      ↓
ajout des participants
      ↓
ajout des messages

Statut du projet
Mampirafy Tool 1.0.0 est un prototype de format de conversation JSON.

Note : ce projet définit une structure de données. Un fichier JSON et un dépôt Git ne constituent pas à eux seuls un système de messagerie sécurisée ou de chiffrement de bout en bout.
