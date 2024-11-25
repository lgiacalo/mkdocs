# Angular

## Docs

- [learnrxjs](https://www.learnrxjs.io/)
- [rxjs api official](https://rxjs.dev/api)

## Forms

2 méthodes pour creer des formulaires : template ou **reactive**

### Forms Template

> Utilisé principalement pour des formulaires simples

Leur nom vient du fait que le template dicte la forme du formulaire et non un objet créé côté TypeScript.

```typescript
import { FormsModule, NgForm } from '@angular/forms';

@Component({
  ...
  imports: [FormsModule],
  ...
})

export class LandingPageComponent implements OnInit {
  userEmail!: string;
  ...
  onSubmitForm(form: NgForm) {
    console.log(form.value);
  }
}
```

```html
  <form #emailForm="ngForm" (ngSubmit)="onSubmitForm(emailForm)">
    <label for="emailInput">Inscrivez-vous pour recevoir notre newsletter !</label>
    <input [(ngModel)]="userEmail" name="userEmail" type="email" id="emailInput">
    <button type="submit">OK!</button>
  </form>
```


### Forms reactifs

Pour des applications web modernes, vous aurez besoin de formulaires complexes et dynamiques. Angular vous propose les **formulaires réactifs**.

Là où les formulaires **template** sont définis par le contenu HTML du template, les **formulaires réactifs** sont d'abord générés en TypeScript – on vient ensuite relier les différents  input  du template à l'objet du formulaire.

Les formulaires réactifs offrent beaucoup plus de possibilités :

- comme leur nom l'indique, les formulaires réactifs mettent à disposition des Observables pour réagir en temps réel aux valeurs entrées par l'utilisateur ;

- les formulaires réactifs permettent une validation beaucoup plus approfondie ;

- pour générer des formulaires totalement dynamiques – c'est-à-dire des formulaires dont vous ne connaissez pas la structure en amont – les formulaires réactifs sont la seule solution


#### Two-way binding

Le **two-way binding** (la liaison double sens) à la directive  **[(ngModel)]**  crée une liaison totale entre la variable et l' `<input>`. **Tout changement de la variable entraîne un changement dans le DOM, et toute modification du texte de l' `<input>` venant de l'utilisateur entraîne un changement de la valeur de la variable.**

#### Examples

> Quel `<input>` est correctement lié au contrôle appelé  `registrationNumber` du formulaire réactif dans lequel il se trouve ?

Reponse : `<input formControlName="registrationNumber">`

On associe un `<input>` à un contrôle de formulaire réactif avec `formControlName` , en passant le nom du contrôle.

⚠️⚠️⚠️⚠️ **Attention** ! Vous passez une chaîne de caractères à  formControlName  , donc si vous utilisez les crochets `[]` , vous devez passer la chaîne de caractères entre apostrophes, par exemple `[formControlName]="'registrationNumber'"`.


---
## Observable 

Documentation pour comprendre les (Observables)[https://www.learnrxjs.io/learn-rxjs]

Website to see how marbles work : **[rxmarbles](https://rxmarbles.com)**

### Operateurs (**Bas Niveau**) with pip()

- [List Operateurs](https://www.learnrxjs.io/learn-rxjs/operators)

### Operateurs (**Haut niveau**) - Higher-Order Observable

- **mergeMap** :  assure la mise en parallèle : l'Observable extérieur peut souscrire aux Observables intérieurs suivants sans attendre que les précédents soient complétés. 

- **concatMap** :  assure la mise en série : il attend que les Observables intérieurs complètent avant de souscrire aux suivants– même si l'Observable extérieur émet plusieurs fois. Les Observables intérieurs seront traités en séquence à la suite.

- **exhaustMap** :  assure le traitement complet d'une souscription avant d'observer une nouvelle émission de l'Observable extérieur. Si d’autres demandes sont faites entre temps, elles ne seront pas prises en compte. 

- **switchMap** :  traite la dernière demande de souscription de l’Observable extérieur et annule toute souscription précédente non-complétée.

### Display - Observables

⚠️⚠️ **AsyncPipe** ⚠️⚠️
> Tout **Observable** souscrit avec le **pipe async** (dans le html)  est **automatiquement unsubscribe** lors de la destruction du component qui le consomme !


```html
<!-- Display String -->
  <h1>{{ (intervalString$ | async) }}</h1>

<!-- Display Object -->
  <div *ngIf="(intervalObject$ | async) as interval">
    <p>{{ interval.color}}</p>
    <p>{{ interval.trainIndex }}</p>
  </div>

<!-- ⚠️⚠️ **Double souscription** -->
 <p>{{ (intervalObject$ | async)?.color }}</p>
 <p>{{ (intervalObject$ | async)?.trainIndex }}</p>
```
```typescript
<!-- Imports -->
import { AsyncPipe, CommonModule } from '@angular/common';

@Component({
  ...
  imports: [AsyncPipe, CommonModule],
  ...
})
```

---
## Bonne pratiques

- [Bonne pratique de développement - Angular](https://openclassrooms.com/fr/courses/3647511-developpez-des-applications-web-modernes-avec-angular-4-4-0-0/4065751-bonnes-pratiques-de-developpement?status=waiting-for-publication)


---
## Questions

- Comment faire un observable d'une liste d'element qui s'affiche les uns apres les autres a 1 seconde d'interval ? 
```typescrip

// Solution moche
    this.messages$ = interval(1000).pipe(
      map((value) => ['first', 'second', 'third', '4', '5'][value]),
      take(3),
      tap((value) => console.log(`Observable messages$ : ${value}`)),
      switchMap((value) => this.processMessage$(value)),
      tap((value) => console.log(`After mergeMap : ${value}`))
    );
```

---
## Info

Higher-Order : fonction qui accepte une fonction en parametre ou en retourne une. 

---
## WIP

- Implementer marble pour voir visuellement le comportement des Observables