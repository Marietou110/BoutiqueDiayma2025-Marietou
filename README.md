# Boutique Diayma 2025 – Rapport de TP (Marietou Ngom)

## 1. Présentation
Ce projet est une application ASP.NET Core MVC utilisée dans le cadre du TP.
L’application permet :
- d’afficher des produits,
- gérer un panier,
- passer une commande.

---

## 2. Projets présents dans la solution
La solution `Diayma.sln` contient un seul projet :

- **P2FixAnAppDotNetCode**

Ce projet contient les dossiers : Controllers, Models, Views, Components, wwwroot, etc.

---

## 3. Version .NET utilisée
Le fichier *Diayma.csproj* indique :

le fichier yml

➡️ Le projet utilise **.NET Core 2.0**  
➡️ Framework SDK nécessaire : **Microsoft .NET Core SDK 2.0**

---

## 4. Installation du SDK
Pour exécuter le projet :

1. Installer **.NET Core SDK 2.0** (versions archivées sur le site Microsoft)
2. Vérifier l’installation :

3. Utiliser Visual Studio compatible (VS 2017 / 2019)

---

## 5. Mise en place du dépôt GitHub
Dépôt GitHub :  
👉 https://github.com/Marietou110/BoutiqueDiayma2025-Marietou

Commandes utilisées :git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/Marietou110/BoutiqueDiayma2025-Marietou.git

git push -u origin main




---

## 6. Bugs trouvés dans l’application

### 🔴 Bug 1 — Le mini-panier ne s’actualise pas
Lorsqu’un produit est ajouté au panier, la quantité affichée dans le CartSummary ne se met pas à jour.

### 🔴 Bug 2 — Images manquantes
Certaines images de produits ne s’affichent pas.  
Cause : chemin incorrect ou fichier absent dans `/wwwroot/images`.

---

## 7. Breakpoints placés (débogage)

Points d’arrêt ajoutés :

- CartSummaryViewComponent — ligne 12  
- ProductController — ligne 15  
- OrderController — ligne 17  
- CartController — ligne 15  
- Startup.cs — ligne 20  

---

## 8. Ordre d'exécution (avant l’affichage des produits)

Voici le pipeline observé :

1. `Program.cs` → `Main()`
2. `Startup.cs` → `ConfigureServices()`
3. `Startup.cs` → `Configure()`
4. Middlewares ASP.NET Core :
   - Static Files
   - Routing
   - MVC
5. `ProductController` → `Index()`
6. Service / Repository → récupération des produits
7. `Views/Products/Index.cshtml` → rendu HTML final

---

## 9. Publication de l’exécutable Windows (.exe)

Commande utilisée :
Lien Google Drive / OneDrive :  
👉 *(à insérer ici après upload)*

---

## 10. Commits significatifs effectués
- `feat: ajout localisation Wolof`  
- `fix: correction mise à jour panier`  
- `refactor: nettoyage ProductController`  

---

## 11. Auteur
**Marietou Ngom**  
Master Génie Logiciel – esp 
2025



