# maestro-app-revue-diligente

Application **Revue diligente** (simulée) de la PoC Maestro : portail des chantiers de revue
diligente pour les équipes internes et les contributeurs externes (cabinet comptable, ingénierie,
conseil ESG). Chaque contributeur ne voit que les tâches de son chantier ; le backbone garantit leur
complétion et range les rapports dans SharePoint.

Elle ne connaît ni Camunda ni le BPMN : elle parle uniquement à la passerelle du backbone
([maestro-v2](https://github.com/fabrice974/maestro-v2)) via le SDK
[`@maestro/sdk`](https://github.com/fabrice974/maestro-sdk-ts).

Accès en **lecture restreinte** (portail ouvert aux externes) : la passerelle ne lui montre que ses
tâches, leurs pièces et l'audit qui la concerne.

## Lancer

```bash
npm install
cp .env.example .env     # facultatif
npm start                # http://localhost:4102
```

Prérequis : la passerelle de maestro-v2, ou `npm run ecosysteme -- demarrer` depuis maestro-v2.
