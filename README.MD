# Sidomart Application

## <<package>>

### com.sidomart.component

#### Header
- **Attributes**
  - `logo`: ImageIcon
  - `title`: String
  - `subtitle`: String
- **Methods**
  - `initializeComponents(): void`
  - `setLogo(ImageIcon icon): void`
  - `setTitle(String title): void`
  - `setSubtitle(String subtitle): void`

#### Menu
- **Attributes**
  - `items`: List<JMenuItem>
- **Methods**
  - `initializeComponents(): void`
  - `addItem(String label, ActionListener listener): void`

#### PanelDashboard
- **Attributes**
  - `data`: DashboardData
- **Methods**
  - `initializeComponents(): void`
  - `loadDashboardData(): void`

#### PanelFormProduct
- **Attributes**
  - `categories`: List<Category>
  - `productData`: Product
  - `editMode`: boolean
- **Methods**
  - `initializeComponents(): void`
  - `loadCategories(): void`
  - `getProductData(): Product`
  - `clearForm(): void`
  - `populateForm(Product product): void`
  - `setEditMode(boolean editMode): void`

#### PanelFormTransaction
- **Attributes**
  - `products`: List<Product>
  - `transactionData`: Transaction
  - `details`: List<TransactionDetail>
  - `editMode`: boolean
- **Methods**
  - `initializeComponents(): void`
  - `loadProducts(): void`
  - `getTransactionData(): Transaction`
  - `clearForm(): void`
  - `populateForm(Transaction transaction, List<TransactionDetail> details): void`
  - `setEditMode(boolean editMode): void`

#### PanelProduct
- **Attributes**
  - `products`: List<Product>
- **Methods**
  - `initializeComponents(): void`
  - `loadProducts(List<Product> products): void`
  - `showProductDetails(Product product): void`

#### PanelSetting
- **Attributes**
  - `userData`: User
- **Methods**
  - `initializeComponents(): void`
  - `loadUserData(User user): void`
  - `updateUserFields(User user): void`
  - `clearPasswordFields(): void`

#### PanelTransaction
- **Attributes**
  - `transactions`: List<Transaction>
- **Methods**
  - `initializeComponents(): void`
  - `loadTransactions(List<Transaction> transactions): void`
  - `showTransactionDetails(Transaction transaction): void`

### com.sidomart.controller

#### CategoryController
- **Methods**
  - `getAllCategories(): List<Category>`
  - `getCategoryById(Integer categoryId): Category`
  - `createCategory(Category category): void`
  - `updateCategory(Category category): void`
  - `deleteCategory(Integer categoryId): void`

#### DashboardController
- **Methods**
  - `loadDashboardData(): DashboardData`

#### LogController
- **Methods**
  - `getAllLogs(): List<Log>`
  - `getLogById(Integer logId): Log`
  - `getLogsByUserId(Integer userId): List<Log>`
  - `createLog(Log log): void`
  - `updateLog(Log log): void`
  - `deleteLog(Integer logId): void`

#### ProductController
- **Methods**
  - `getAllProducts(): List<Product>`
  - `getProductById(Integer productId): Product`
  - `getProductsByCategoryId(Integer categoryId): List<Product>`
  - `createProduct(Product product): void`
  - `updateProduct(Product product): void`
  - `deleteProduct(Integer productId): void`

#### TransactionController
- **Methods**
  - `getAllTransactions(): List<Transaction>`
  - `getTransactionById(Integer transactionId): Transaction`
  - `getTransactionsByUserId(Integer userId): List<Transaction>`
  - `createTransaction(Transaction transaction, List<TransactionDetail> transactionDetails): void`
  - `updateTransaction(Transaction transaction, List<TransactionDetail> transactionDetails): void`
  - `deleteTransaction(Integer transactionId): void`

#### UserController
- **Methods**
  - `getAllUsers(): List<User>`
  - `getUserById(Integer userId): User`
  - `getUserByUsername(String username): User`
  - `createUser(User user): void`
  - `updateUser(User user): void`
  - `deleteUser(Integer userId): void`

### com.sidomart.model

#### Category
- **Attributes**
  - `categoryId`: Integer
  - `label`: String
  - `description`: String
  - `createdAt`: Timestamp
- **Methods**
  - `getCategoryId(): Integer`
  - `setCategoryId(Integer categoryId): void`
  - `getLabel(): String`
  - `setLabel(String label): void`
  - `getDescription(): String`
  - `setDescription(String description): void`
  - `getCreatedAt(): Timestamp`
  - `setCreatedAt(Timestamp createdAt): void`

#### ExpenseReport
- **Attributes**
  - `expenseId`: Integer
  - `userId`: Integer
  - `amount`: double
  - `description`: String
  - `expenseDate`: Timestamp
- **Methods**
  - `getExpenseId(): Integer`
  - `setExpenseId(Integer expenseId): void`
  - `getUserId(): Integer`
  - `setUserId(Integer userId): void`
  - `getAmount(): double`
  - `setAmount(double amount): void`
  - `getDescription(): String`
  - `setDescription(String description): void`
  - `getExpenseDate(): Timestamp`
  - `setExpenseDate(Timestamp expenseDate): void`

#### Log
- **Attributes**
  - `logId`: Integer
  - `userId`: Integer
  - `action`: String
  - `description`: String
  - `createdAt`: Timestamp
- **Methods**
  - `getLogId(): Integer`
  - `setLogId(Integer logId): void`
  - `getUserId(): Integer`
  - `setUserId(Integer userId): void`
  - `getAction(): String`
  - `setAction(String action): void`
  - `getDescription(): String`
  - `setDescription(String description): void`
  - `getCreatedAt(): Timestamp`
  - `setCreatedAt(Timestamp createdAt): void`

#### Product
- **Attributes**
  - `productId`: Integer
  - `productName`: String
  - `categoryId`: Integer
  - `image`: String
  - `price`: double
  - `stock`: Integer
  - `createdAt`: Timestamp
  - `updatedAt`: Timestamp
- **Methods**
  - `getProductId(): Integer`
  - `setProductId(Integer productId): void`
  - `getProductName(): String`
  - `setProductName(String productName): void`
  - `getCategoryId(): Integer`
  - `setCategoryId(Integer categoryId): void`
  - `getImage(): String`
  - `setImage(String image): void`
  - `getPrice(): double`
  - `setPrice(double price): void`
  - `getStock(): Integer`
  - `setStock(Integer stock): void`
  - `getCreatedAt(): Timestamp`
  - `setCreatedAt(Timestamp createdAt): void`
  - `getUpdatedAt(): Timestamp`
  - `setUpdatedAt(Timestamp updatedAt): void`

#### Role
- **Attributes**
  - `databaseValue`: String
- **Methods**
  - `fromDatabaseValue(String databaseValue): Role`

#### Transaction
- **Attributes**
  - `transactionId`: Integer
  - `userId`: Integer
  - `totalAmount`: double
  - `transactionDate`: Timestamp
  - `username`: String
- **Methods**
  - `getTransactionId(): Integer`
  - `setTransactionId(Integer transactionId): void`
  - `getUserId(): Integer`
  - `setUserId(Integer userId): void`
  - `getTotalAmount(): double`
  - `setTotalAmount(double totalAmount): void`
  - `getTransactionDate(): Timestamp`
  - `setTransactionDate(Timestamp transactionDate): void`
  - `getUsername(): String`
  - `setUsername(String username): void`

#### TransactionDetail
- **Attributes**
  - `detailId`: Integer
  - `transactionId`: Integer
  - `productId`: Integer
  - `quantity`: Integer
  - `price`: double
- **Methods**
  - `getDetailId(): Integer`
  - `setDetailId(Integer detailId): void`
  - `getTransactionId(): Integer`
  - `setTransactionId(Integer transactionId): void`
  - `getProductId(): Integer`
  - `setProductId(Integer productId): void`
  - `getQuantity(): Integer`
  - `setQuantity(Integer quantity): void`
  - `getPrice(): double`
  - `setPrice(double price): void`

#### User
- **Attributes**
  - `userId`: Integer
  - `fullName`: String
  - `username`: String
  - `password`: String
  - `role`: String
  - `createdAt`: Timestamp
  - `updatedAt`: Timestamp
- **Methods**
  - `getUserId(): Integer`
  - `setUserId(Integer userId): void`
  - `getFullName(): String`
  - `setFullName(String fullName): void`
  - `getUsername(): String`
  - `setUsername(String username): void`
  - `getPassword(): String`
  - `setPassword(String password): void`
  - `getRole(): String`
  - `setRole(String role): void`
  - `getCreatedAt(): Timestamp`
  - `setCreatedAt(Timestamp createdAt): void`
  - `getUpdatedAt(): Timestamp`
  - `setUpdatedAt(Timestamp updatedAt): void`

### com.sidomart.swing

#### RButton
- **Attributes**
  - `text`: String
  - `icon`: Icon
- **Methods**
  - `setText(String text): void`
  - `setIcon(Icon icon): void`
  - `addActionListener(ActionListener listener): void`

#### RPasswordField
- **Attributes**
  - `password`: char[]
- **Methods**
  - `getPassword(): char[]`
  - `setPassword(char[] password): void`
  - `clearPassword(): void`

#### RTextArea
- **Attributes**
  - `text`: String
- **Methods**
  - `getText(): String`
  - `setText(String text): void`
  - `append(String text): void`
  - `clear(): void`

#### RTextField
- **Attributes**
  - `text`: String
- **Methods**
  - `getText(): String`
  - `setText(String text): void`
  - `clear(): void`

### com.sidomart.util

#### DatabaseUtilities
- **Attributes**
  - `connection`: Connection
- **Methods**
  - `connect(): void`
  - `disconnect(): void`
  - `executeQuery(String query): ResultSet`
  - `executeUpdate(String query): int`

#### SessionManager
- **Attributes**
  - `currentUser`: User
- **Methods**
  - `login(String username, String password): boolean`
  - `logout(): void`
  - `isLoggedIn(): boolean`
  - `getCurrentUser(): User`
  - `setCurrentUser(User user): void`

### com.sidomart.view

#### Dashboard
- **Attributes**
  - `userData`: User
  - `recentTransactions`: List<Transaction>
- **Methods**
  - `initializeComponents(): void`
  - `loadUserData(): void`
  - `loadRecentTransactions(): void`
  - `showNotification(String message): void`

#### Login
- **Attributes**
  - `username`: String
  - `password`: char[]
- **Methods**
  - `initializeComponents(): void`
  - `getUsername(): String`
  - `getPassword(): char[]`
  - `clearFields(): void`
  - `showMessage(String message): void`

#### Register
- **Attributes**
  - `username`: String
  - `password`: char[]
  - `fullName`: String
- **Methods**
  - `initializeComponents(): void`
  - `getUsername(): String`
  - `getPassword(): char[]`
  - `getFullName(): String`
  - `clearFields(): void`
  - `showMessage(String message): void`

#### Splash
- **Methods**
  - `showSplashScreen(): void`
  - `hideSplashScreen(): void`
