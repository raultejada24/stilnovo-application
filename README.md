# Stilnovo - Reinvent your space: Where design with history finds its new home.

---

## 🎭 **Preparation 1: Project Definition**

### **Topic Description**

Stilnovo is a platform for buying and selling used objects. Its goal is to give a "new style" to second-hand items. The application allows users to publish ads, manage safe transactions, and support the circular economy through an aesthetic and functional digital market.

### **Entities**

Indicate the main entities that the application will manage and the relationships between them:

1. **User**: Stores personal information, roles, avatar, and current economic balance.
2. **Product**: Items for sale with description, price, category, and photos.
3. **Transaction**: Records the buying process by linking a buyer, a seller, and a product.
4. **Review**: Feedback system with a comment and a score after a transaction.

**Relationships between entities:**

- User - Product: A user can publish many products (owner). 1:N relationship.
- Transaction - User/Product: A transaction must link a buyer, a seller, and one sold item.
- Review - Transaction: Each review is linked to a completed transaction. 1:1 relationship.
- Product - Category: Products are grouped by categories to make searching easier.

### **User Permissions**

Describe the permissions of each type of user and indicate which entities they own:

- **Anonymous User**:
  - Permissions: Browse the website, view the product catalog, and use the search engine. They can only view public information.
  - Does not own any entity.

- **Registered User**:
  - Permissions: Publish items with photos, make purchases, access a detailed history of purchases and sales, manage their profile with avatar, manage their inventory, edit/delete uploaded items, view analytics (seller score, income, category distribution, etc.), generate PDFs (invoices and analytics data), Digital Seller Card with QR code (for identity verification in physical meetings), among others.
  - Owns: Their own published products, their user profile, and the reviews they write.

- **Administrator**:
  - Permissions: Full control over the information. They can moderate content, delete products that break the rules, or ban users.
  - Owns: Manages all entities of the platform.

### **Images**

Indicate which entities will have an associated image:

- **User**: A personalized avatar image.
- **Product**: A descriptive image for each advertised item.

### **Charts**

To offer a data-based management experience, the application includes dynamic visualizations that allow the user and the administrator to monitor commercial performance in real time.

- **Chart 1**: Sales Distribution by Category (Donut Chart): Located in the user Dashboard, this chart shows the proportion of successful sales in the Home, Tech, Art, and Cars categories.
- **Chart 2**: Monthly Income Evolution (Line Chart): A time visualization that shows the user’s income trend during the year (user-statistics.jpg), helping to identify peaks in demand.
- **Chart 3**: Visits vs. Interest Analysis (Bar Chart): A comparative bar chart that measures received traffic compared to real interactions (purchases) for each type of product.

### **Complementary Technology**

Technologies have been selected to extend the basic capacities of the web and simulate a real production environment.

- **PDF Generation**: Implementation of a library for the automatic creation of invoices and purchase receipts, directly downloadable from the orders panel, as well as the generation of PDFs with user analytics and shipping labels after a transaction.
- **Email Sending (Mail Service)**: Integration of a messaging service to manage the first communication between interested users. When clicking "Send Message", the system sends an automatic email to the seller with the details of the buyer’s question.

### **Advanced Algorithm or Query**

The system does not only show data, but also processes the user’s activity to personalize the browsing experience.

- **Algorithm/Query**: Personalized recommendation system.
- **Description**: Shows "Products you may be interested in" on the home page, based on the categories that the user has bought or visited before.

---

## 🛠 **Preparation 2: Page Layout with HTML and CSS**

### **Demo Video**

📹 **[Link to the video on YouTube](https://youtu.be/lXqGTZpMamk?si=9I0j98zrY1fShL06)**

> Video showing the main features of the web application.

### **Navigation Diagram**

Diagram that shows how to move between the different pages of the application:

![Navigation Diagram](readme-images/Preparation2/Stilnovo-Diagrama-Navegacion.png)

**Navigation flow description:**  
Visual map that organizes navigation by colors (Blue: All Users, Yellow: Registered User, Green: Administrator) and uses the screenshots from the next section as system nodes.

---

## 🛠 **Practice 1: Web with Server-Generated HTML and AJAX**

### **Demo Video**

📹 **[Link to the video on YouTube](https://youtu.be/zg4VRbsN4g4)**

> Video showing the main features of the web application.

### **Navigation and Screenshots**

#### **Navigation Diagram**

Updated diagram that shows how to move between the different pages of the application:

![Navigation Diagram](readme-images/Practice1/Stilnovo-Diagrama-Navegacion-2.png)

**Navigation flow description:**  
Visual map that organizes navigation by colors (Blue: All Users, Yellow: Registered User, Green: Administrator) and uses the screenshots from the next section as system nodes.

#### **Updated Screenshots**

#### **Private Area (Registered User)**

#### **1. Activity Panel (Dashboard)**

![Activity Panel](readme-images/Practice1/DashboardP1.png)

**Description:**
Personalized user view that shows real-time financial statistics, including current balance, total income, and sales summary. It allows the user to monitor their commercial performance on the platform.

#### **2. Own Inventory Management (My Products)**

![Own Inventory](readme-images/Practice1/MyProductsP1.png)

**Description:**
Complete list of products published by the user, with options to edit, delete, and manage the status of each item. It shows the Product entity, where the owner has full control over their ads.

#### **3. Product Publication Form (New Product)**

![Publication Form](readme-images/Practice1/NewProductP1.png)

**Description:**
Interface to create new items in the marketplace, including name, category, price, location, detailed description, and image upload. It validates required fields before sending.

#### **4. Product Editing Form (Edit Product)**

![Editing Form](readme-images/Practice1/EditProductP1.png)

**Description:**
Interface to modify existing products with all fields editable, including the option to change the associated images. It keeps the integrity of the product data.

#### **5. Sales and Orders History (Sales & Orders)**

![Transaction History](readme-images/Practice1/SalesOrdersP1.png)

**Description:**
Complete record of purchases and sales made by the user. It includes transaction details, dates, amounts, and status of each operation. It includes the complementary technology for generating downloadable PDF invoices.

#### **6. Sales Analysis by Category and Income Evolution (Statistics)**

![Data Analysis G1 and G2](readme-images/Practice1/StatisticsP1.png)

**Description:**
Implementation of advanced charts (Chart 1: category distribution Donut Chart and Chart 2: time evolution Line Chart) to show the user’s commercial performance through historical data.

#### **7. Interest and Visits Chart (Statistics - Bar Chart)**

![Interest Chart G3](readme-images/Practice1/Statistics2P1.png)

**Description:**
Comparative bar chart (Chart 3) that measures received traffic compared to real interactions (favorites/purchases) for each product category, helping to identify user behavior patterns.

#### **8. User Profile Settings (Edit Profile)**

![Profile and Verification](readme-images/Practice1/EditProfileP1.png)

**Description:**
Complete management of the user’s personal data, including username, email, avatar, biography, credit card information, and display of the Digital Seller Card with QR code for identity verification.

#### **9. My Sent and Pending Reviews (My Valorations)**

![My Reviews](readme-images/Practice1/MyValorationsP1.png)

**Description:**
View of all reviews sent by the user as a buyer. It shows the star score, buyer comments, and reviewed product, as well as reviews still pending. This helps manage reputation on the platform.

#### **10. Review in Sales & Orders (Sales & Orders Valoration)**

![Review](readme-images/Practice1/valoration-in-sales.png)

**Description:**
Interface that shows a pending review in Sales & Orders.

#### **11. Edit Review (Edit Valoration)**

![Edit Review](readme-images/Practice1/EditValorationP1.png)

**Description:**
Interface to modify a previously sent review, allowing the user to update the star score and the comment linked to a completed transaction. It keeps the traceability of reviews.

#### **12. User Help Area (Help Center)**

![User Help](readme-images/Practice1/HelpCenter.png)

**Description:**
Interface with frequently asked questions and access to Stilnovo contact information.

#### **13. Seller Profile (Seller Profile)**

![Seller Profile](readme-images/Practice1/seller-profile.png)

**Description:**
Interface where the information of a seller is shown. This information includes average rating, number of reviews received, name, description, and products.

#### **14. Seller Reviews (Seller Valorations)**

![Seller Review](readme-images/Practice1/seller-valorations.png)

**Description:**
Interface where the reviews received by a seller are shown. A list of reviews for that seller is displayed, written by other users who bought a product from this seller. This helps users know the seller’s reputation.

#### **Administration Area**

#### **15. Global Platform Monitor (Admin Dashboard)**

![Global Platform Monitor](readme-images/Practice1/AdminDashboardP1.png)

**Description:**
Exclusive administrator dashboard with system KPIs: total registered users, active products, completed transactions, global income, and moderation alerts. It is a centralized view for platform supervision.

#### **16. Global User Management (Admin User Management)**

![User Management](readme-images/Practice1/AdminUserManagP1.png)

**Description:**
Moderation tool that allows the administrator to view all registered users, their contact data, account status, and perform administrative actions such as banning, unbanning, or deleting profiles.

#### **17. Global Product Inventory (Admin Global Inventory)**

![Global Inventory](readme-images/Practice1/AdminGlobalInvetP1.png)

**Description:**
Master record of all products published in the marketplace, with detailed information about the seller, category, price, and status. It allows the administrator to edit or delete any ad that breaks the platform rules.

#### **18. Global Financial Audit (Admin Global Transactions)**

![Financial Audit](readme-images/Practice1/AdminGlobalTransP1.png)

**Description:**
Complete view of all transactions made on the platform, including buyer, seller, product, date, amount, and status. It is a tool for financial auditing, dispute management, and business volume analysis.

#### **19. Global Review Management (Admin Global Valorations)**

![Review Management](readme-images/Practice1/AdminGlobalValorationsP1.png)

**Description:**
Administration panel to supervise all reviews made on the platform. It allows the administrator to identify fake reviews, manage reports, and keep the integrity of the seller reputation system.

#### **20. User Ban (User Ban)**

![Banned user](readme-images/Practice1/UserBanned.png)

**Description:**
When the administrator blocks a user in **Stilnovo**, if this user tries to log in, the system will show an information page saying that their account has been suspended from the platform.

#### **21. Footer**

![Edit Review](readme-images/Practice1/new-footer.png)

**Description:**
Interface where the new design of the Stilnovo footer is shown. It includes information modals, social media links, and the possibility to create a new account.

#### **22. Banned User (Banned User)**

![Footer Modal](readme-images/Practice1/modal-footer.png)

**Description:**
Here an example of a footer modal is shown.

### **Execution Instructions**

#### **Previous Requirements**

- **Java**: version 21 or higher
- **Maven**: version 3.8 or higher
- **MySQL**: version 8.0 or higher
- **Git**: to clone the repository

#### **Steps to run the application**

1. **Clone the repository**  
   Create a folder for the project, enter it, and clone the repository:

   ```bash
   git clone https://github.com/CodeURJC-DAW-2025-26/practica-daw-2025-26-grupo-5.git
   cd practica-daw-2025-26/practica-daw-2025-26-grupo-5
   ```

2. **Access the backend directory**  
   Enter the folder that contains the server logic:

   ```bash
   cd backend
   ```

3. **Start the database**  
   Make sure Docker Desktop is open (or any other Docker engine) and run the script to initialize the database:

   ```bash
   ./start_db.sh
   ```

   **Note:** Wait a few seconds after running the script to make sure the database has been created and configured correctly before the next step.

4. **Run the application**  
   Find the main project file in your IDE (IntelliJ, VS Code, etc.):

   `src/main/java/es/stilnovo/library/Application.java`

5. **Access the website**  
   Once the application is running, open your browser and go to:

   ```bash
   https://localhost:8443
   ```

Just a reminder: as the application uses HTTPS on port 8443, the first time you enter, the browser will show a "Connection is not private" warning (because of the self-signed development certificate). You only need to click **"Advanced settings"** and **"Access localhost (unsafe site)"** to enter.

#### **Test Credentials**

- **Admin User**: username: `admin`, password: `admin`
- **Registered User**: username: `user`, password: `user`

### **Database Entity Diagram**

Diagram showing the entities, their fields, and relationships:

![Entity-Relationship Diagram](readme-images/Practice1/ERsql.png)

> **Diagram Description:**
>
> The EER diagram generated from MySQL Workbench shows the main tables and the auxiliary tables created by Hibernate:
>
> - **Main tables:** `user_table`, `product_table`, `transaction_table`, `image_table`, `inquiry_table`, `user_interactions`, `valoration_table`.
> - **Auxiliary tables:** `user_table_favorite_products` (favorites, N:M relationship) and `user_table_roles` (roles by user).
>
> **Key relationships (according to the diagram):**
>
> - `user_table` **1:N** `product_table` (seller_user_id)
> - `product_table` **1:1** `image_table` (image_id)
> - `transaction_table` **N:1** `user_table` (buyer_user_id and seller_user_id)
> - `transaction_table` **1:1** `product_table` (product_id)
> - `inquiry_table` **N:1** `user_table` (buyer_user_id) and **N:1** `product_table` (product_id)
> - `user_interactions` **N:1** `user_table` and **N:1** `product_table`
> - `valoration_table` **N:1** `user_table` (buyer_user_id and seller_user_id) and **N:1** `transaction_table`

### **Class and Template Diagram**

Application class diagram with color or section differences:

![Class Diagram](readme-images/Practice1/Diagrama-Clases-Silnovo.jpg)

> This diagram explains the logical architecture of **Stilnovo**, organized in a layered model that ensures separation of responsibilities and system scalability.
>
> **Component Organization:**
>
> - **Views (Purple):** Presentation layer that manages the user interface, including full pages and dynamic HTML fragments for a smooth experience.
> - **Controllers (Green):** They receive client requests, coordinate the navigation flow, and delegate the execution of business rules.
> - **Services (Red):** Core of the application, where business logic is processed. It centralizes complex functions such as inventory calculation, notification cooldown, and integration with infrastructure services (Email and PDF).
> - **Repositories (Blue):** Persistence layer that uses Spring Data JPA to abstract and manage data access efficiently.
> - **Entities/Models (Grey):** Representation of domain objects, defining integrity rules and essential composition relationships for the business (User, Product, Transaction, etc.).
>
> **Design Principles:**
> The diagram shows a one-way dependency flow (Controller -> Service -> Repository), reducing coupling and allowing the business logic to be independent from the persistence technology or the user interface.

---

## 🛠 **Practice 2: Adding a REST API to the Web Application, Deployment with Docker, and Remote Deployment**

Note: To test POST/PUT endpoints that require images in Postman, please attach a local file in the Body tab.

### **Demo Video**

📹 **[Link to the video on YouTube](https://youtu.be/uGIF1hk7TAM)**

> Video showing the main features of the web application.

### **REST API Documentation**

#### **OpenAPI Specification**

📄 **[OpenAPI Specification (YAML)](https://github.com/CodeURJC-DAW-2025-26/practica-daw-2025-26-grupo-5/blob/main/api-docs/api-docs.yaml)**

#### **HTML Documentation**

📑 **[REST API Documentation (HTML)](https://raw.githack.com/CodeURJC-DAW-2025-26/practica-daw-2025-26-grupo-5/main/api-docs/api-docs.html)**

> The REST API documentation is in the `/api-docs` folder of the repository. It has been generated automatically with SpringDoc from the annotations in the Java code.

### **Updated Class and Template Diagram**

Updated diagram including the @RestController elements and their relationship with the shared @Service elements:

![Updated Class Diagram](readme-images/Practice2/Stilnovo-Diagrama-Clases-2.jpg)

This diagram explains the logical architecture of **Stilnovo**, organized in a layered model that ensures separation of responsibilities and system scalability.

> **Component Organization:**
>
> - **Views (Purple):** Presentation layer that manages the user interface, including full pages and dynamic HTML fragments for a smooth experience.
> - **Controllers (Green):** They receive client requests, coordinate the navigation flow, and delegate the execution of business rules.
> - **REST Controllers (Dark Green):** API entry points. They receive HTTP requests (GET, POST, PUT, DELETE), organize the operations, and return structured responses only in JSON format.
> - **DTOs / Transfer Objects (Dark Blue):** Light data structures (Data Transfer Objects) designed to move information between the client and the server. They isolate and protect the model entities, showing only the needed data and improving performance.
> - **Services (Red):** Core of the application, where business logic is processed. It centralizes complex functions such as inventory calculation, notification cooldown, and integration with infrastructure services (Email and PDF).
> - **Repositories (Blue):** Persistence layer that uses Spring Data JPA to abstract and manage data access efficiently.
> - **Entities/Models (Grey):** Representation of domain objects, defining integrity rules and essential composition relationships for the business (User, Product, Transaction, etc.).

> **Recommendation:** For better visualization and clearer details, it is recommended to download the image and open it on a personal computer. The diagram has enough resolution for a good experience when zooming into specific areas of interest.

---

### **Execution Instructions and Deployment with Docker**

#### **1. Previous Requirements**

- Docker (v20.10+) and Docker Compose (v2.0+) installed.
- Account on [DockerHub](https://hub.docker.com) and logged in (`docker login`).
- Repository cloned on your local machine.

#### **2. Local Execution (Development)**

To start the application quickly on your machine:

**Step A: Create the `.env` file in the project root**

```properties
DOCKER_HUB_USERNAME=tu-usuario-dockerhub
MYSQL_ROOT_PASSWORD=password
MYSQL_DATABASE=stilnovo
SERVER_PORT=8443
SERVER_SSL_KEY_STORE_PASSWORD=password
SERVER_SSL_KEY_PASSWORD=secret
SPRING_JPA_HIBERNATE_DDL_AUTO=update
APP_PUBLIC_BASE_URL=https://localhost:8443
```

**Step B: Start containers**

```bash
cd docker
docker compose --env-file ../.env up -d
```

_The website will be available at `https://localhost:8443` and the interactive API at `https://localhost:8443/swagger-ui.html`._

To stop the application: `docker compose down`

---

#### **3. Production Deployment Flow (AppWeb05)**

The project includes `PowerShell` (`.ps1`) and `Bash` (`.sh`) scripts inside the `/docker` folder. These scripts automate image building and publishing.

**PHASE 1: From your machine (Build and upload changes)**

```powershell
cd docker
docker login

# 1. Build the image locally (Maven + Docker)
.\create_image.ps1 -ImageName stilnovo-app:latest

# 2. Upload the image to DockerHub
.\publish_image.ps1 -DockerHubUsername tu-usuario-dockerhub
```

**PHASE 2: From the server (Download and run)**
⚠️ _You must be connected to the URJC network (VPN/MyApps)._

```bash
# 1. Connect to the server by SSH
ssh -i ssh-keys/appWeb05.key vmuser@appWeb05.dawgis.etsii.urjc.es

# 2. Clean the old version and its volumes
sudo docker compose down -v

# 3. Download the new image (CRITICAL)
sudo docker compose pull

# 4. FIRST START: Create the database from zero
sudo SPRING_APPLICATION_JSON='{"spring.jpa.hibernate.ddl-auto":"create"}' docker compose up

# 5. LATER STARTS: Once it is initialized, press Ctrl+C and start in safe mode (background)
sudo docker compose up -d
```

_The production application will be available at `https://appweb05.dawgis.etsii.urjc.es:8443`._

> **Note:** For more details about advanced Docker configuration, check the file [`advanced-docker.md`](./advanced-docker.md).

### **Deployed Application URL**

🌐 **Remote access URL (URJC)**: `https://appweb05.dawgis.etsii.urjc.es:8443`

#### **Example User Credentials**

| Role            | Username | Password |
| :-------------- | :------- | :------- |
| Administrator   | admin    | admin123 |
| Registered User | user1    | user123  |
| Registered User | user2    | user123  |

---

## 🛠 **Practice 3: Implementing the Web with SPA Architecture**

### **Demo Video**

📹 **[Link to the video on YouTube](https://www.youtube.com/watch?v=Ez1wUaVW944)**

> Video showing the main features of the web application.

### **Development Environment Preparation**

#### **Previous Requirements**

- **Node.js**: version 18.x or higher
- **npm**: version 9.x or higher (installed with Node.js)
- **Git**: to clone the repository

#### **Steps to configure the development environment**

1. **Install Node.js and npm**

   Download and install Node.js from [https://nodejs.org/](https://nodejs.org/)

   Check the installation:

   ```bash
   node --version
   npm --version
   ```

2. **Clone the repository** (if you have not done it yet)
   ```bash
   git clone https://github.com/CodeURJC-DAW-2025-26/practica-daw-2025-26-grupo-5.git
   cd practica-daw-2025-26-grupo-5
   ```
3. **Run the Backend (for the database)**

   The backend must be active so Hibernate can create the tables and load the initial data.
   Open the project in your IDE.

   Find the Application.java class in backend/src/main/java/....

   Run the application (Run).

   The server will be available at:

   ```bash
     https://localhost:8443
   ```

4. **Go to the React project folder**

   Move to:

   ```bash
   cd frontend
   ```

   Install the dependencies

   ```bash
   npm install
   ```

   Build the application:

   ```bash
     npm run build
   ```

   This will generate the static files that the backend will serve.
   The website will be available at:

   ```bash
    https://localhost:8443/new/
   ```

   **Optional:** If you need to change the frontend base path, create a `.env` file in the `frontend` folder:

   ```properties
   VITE_PUBLIC_URL=/new/
   ```

5. **Run the Frontend in development mode (Optional)**

   Start the Vite development server:

   ```bash
    npm run dev
   ```

   The terminal will show that the application is available at:

   ```bash
    http://localhost:5173/new/
   ```

> **Note:** For more details about advanced development environment configuration, check the file [`advanced-react-spa-setup.md`](./advanced-react-spa-setup.md).

### SPA Architecture and Component Diagram

Below is the structural diagram of our Single Page Application (SPA), explaining the React component hierarchy, routing, services, and communication:

![React Architecture Diagram](readme-images/Practice3/SPA-diagram.jpg)

#### SPA Architecture (React Frontend)

The diagram shows the modular design and data flow of our application:

- **Entry and Routing:** `main.tsx` and `root.tsx` work as the main core, sending navigation to the different views through _Outlets_.
- **Security Layer:** The grey area (`protected-layout.tsx`) contains the private routes (`user`, `admin`, ...), safely separating them from the public routes (`login`, `signup`).
- **Modules and UI:** Each main section has its own nested sub-routes and uses reusable interface components (such as _Headers_, _Footers_, and _Sidebars_).
- **State and Backend:** _Zustand_ (`useUserStore.ts`) manages the user session globally, while the _Services_ layer centralizes the HTTP logic, using `api.ts` to connect smoothly with the Spring Boot REST backend.

### **Integration with Gemini AI**

As added value to the Stilnovo platform, we have integrated **Gemini AI** to help users write product descriptions and answer questions. This feature can automatically generate professional and attractive texts, both when creating a new item and when editing an existing one.

Also, we have improved the support experience by adding intelligent assistance in the **footer** and in the **Help Center**, where registered users can get contextual help with AI quickly and efficiently.

#### **Assistant Configuration**

For security reasons, this feature is **disabled by default** (it does not block the normal use of the application), because it needs a private API key. Follow these steps to activate it:

1.  **Get an API Key:**
    - Go to [Google AI Studio](https://aistudio.google.com/app/api-keys).
    - Log in with the Google account you want.
    - You can copy an existing key or generate a new one by clicking **"Create API key"**.

2.  **Configure the Backend environment:**
    - Go to the `/backend` folder of your project.
    - Create a new file called exactly: `ai-application-key.properties` at the same level as `application.properties`.
    - Inside that file, add the following line, replacing the value with your key:
      ```properties
      google.ai.api.key=TU_API_KEY_AQUÍ
      ```

3.  **Finish:**
    - Restart the Spring Boot application.
    - The system will detect the key automatically and enable the **"Improve with AI"** button in the product forms. The help sections with AI will also work.

> **Note:** The application has "graceful degradation". If you decide not to configure AI, Stilnovo will start normally and the rest of the product management features will continue working without errors.

### Deployment on URJC Server

The Stilnovo platform is deployed with two architectures that work together and share the **same MySQL database**:

- **Classic Web (Spring Boot MVC):** [https://appweb05.dawgis.etsii.urjc.es:8443/](https://appweb05.dawgis.etsii.urjc.es:8443/)
- **Modern Web (SPA React):** [https://appweb05.dawgis.etsii.urjc.es:8443/new/](https://appweb05.dawgis.etsii.urjc.es:8443/new/)

> **Note:** To access the following links, it is necessary to be connected to the university network (**Eduroam**) or through the **URJC VPN**.

### Docker Infrastructure (DockerHub)

The project is fully containerized and hosted on **DockerHub** to make automatic deployment easier:

| Artifact                  | Repository Link                                                                                         | Description                                           |
| :------------------------ | :------------------------------------------------------------------------------------------------------ | :---------------------------------------------------- |
| **App Image**             | [raultejada24/stilnovo](https://hub.docker.com/r/raultejada24/stilnovo)                                 | Multi-stage build (Spring Boot + React SPA)           |
| **Compose Configuration** | [raultejada24/stilnovo-compose](https://hub.docker.com/repository/docker/raultejada24/stilnovo-compose) | OCI artifact with the orchestration of the full stack |

#### Continuous Integration & Delivery (CI/CD)

The project includes **automated GitHub Actions workflows** that build and push Docker images to DockerHub on every commit:

- **`build-stilnovo.yml`**: Automatically builds and publishes the main application image (`raultejada24/stilnovo:latest`) whenever code is pushed to `main`, `develop`, or when a version tag (`v*`) is created. Supports multi-architecture builds (Linux AMD64 + ARM64) for compatibility across different platforms.

- **`build-compose.yml`**: Packages the Docker Compose configuration as an **OCI Artifact** (`raultejada24/stilnovo-compose:latest`), enabling versioned distribution of the orchestration setup. This allows teams to pull the exact Compose configuration matching a specific app version.

Both workflows automatically tag images with:

- `latest` — Always the most recent build
- `main` / `develop` — Branch-specific versions
- `vX.Y.Z` — Semantic versioning from git tags

See [`.github/workflows/README.md`](.github/workflows/README.md) for detailed setup and configuration instructions.
