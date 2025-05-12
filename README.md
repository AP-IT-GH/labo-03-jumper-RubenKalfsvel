# CubeAgentJump ─ GitHub README

## 🎮 Overzicht
Een eenvoudige Unity ML-Agents demo waarin een kubusagent leert om timing van sprongen te optimaliseren en een bewegende wand te ontwijken indien nodig.

---

## 🏗️ Scene-opbouw

1. **Vloer**  
   - Rechthoekige Plane als ondergrond.

2. **CubeAgent**  
   - GameObject: Kubus met:
     - **Box Collider**
     - **Rigidbody** (XYZ-rotatie bevroren & beweging beperkt tot Y-as)
     - **Decision Requester**
     - **Behavior Parameters**
     - **Ray Perception Sensor 3D**
     - **Scripts**:
       - `CubeAgentJump.cs`
       - (`CustomGravity.cs` – optioneel voor aangepaste zwaartekracht)

3. **MovingWall**  
   - GameObject: Balk met:
     - **Box Collider**
     - **Rigidbody**
     - **MovingWallController.cs** (script om positie, afmetingen en snelheid aan te passen en de balk over de vloer te laten schuiven)

---

## 🚀 Training

<p align="center">
  <img src="https://github.com/user-attachments/assets/f4aace81-c1c4-4f33-965a-e196bddc5a8e" alt="Training Cumulatieve Reward" width="600" />
</p>

- **Verloop:**  
  1. Het model begon met willekeurige sprongen om de muur te ontwijken.  
  2. Na verloop van tijd leerde het de sprongen beter te timen.  
  3. Door variaties in snelheid en afmetingen van de muur blijft het model af en toe fouten maken.

- **Resultaat:**  
  - Aanvankelijk stabiele stijging in cumulatieve beloning, vervolgens stagnatie.
  - Relatief consistente timing in sprongacties tegen verschillende muren.

---
