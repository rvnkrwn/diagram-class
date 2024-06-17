------------------------------------------------------------------------------------------
|                                      Sidomart Application                             |
------------------------------------------------------------------------------------------
|                                         <<package>>                                    |
------------------------------------------------------------------------------------------
| + com.sidomart.component                                                               |
|-----------------------------------------------------------------------------------------
| - Header                                                                             |
|   + initializeComponents(): void                                                      |
|   + setLogo(ImageIcon icon): void                                                     |
|   + setTitle(String title): void                                                      |
|   + setSubtitle(String subtitle): void                                                |
|-----------------------------------------------------------------------------------------
| - Menu                                                                               |
|   + initializeComponents(): void                                                      |
|   + addItem(String label, ActionListener listener): void                              |
|-----------------------------------------------------------------------------------------
| - PanelDashboard                                                                     |
|   + initializeComponents(): void                                                      |
|   + loadDashboardData(): void                                                         |
|-----------------------------------------------------------------------------------------
| - PanelFormProduct                                                                   |
|   + initializeComponents(): void                                                      |
|   + loadCategories(): void                                                            |
|   + getProductData(): void                                                            |
|   + clearForm(): void                                                                 |
|   + populateForm(Product product): void                                               |
|   + setEditMode(boolean editMode): void                                               |
|-----------------------------------------------------------------------------------------
| - PanelFormTransaction                                                               |
|   + initializeComponents(): void                                                      |
|   + loadProducts(): void                                                              |
|   + getTransactionData(): void                                                        |
|   + clearForm(): void                                                                 |
|   + populateForm(Transaction transaction, List<TransactionDetail> details): void       |
|   + setEditMode(boolean editMode): void                                               |
|-----------------------------------------------------------------------------------------
| - PanelProduct                                                                       |
|   + initializeComponents(): void                                                      |
|   + loadProducts(List<Product> products): void                                        |
|   + showProductDetails(Product product): void                                         |
|-----------------------------------------------------------------------------------------
| - PanelSetting                                                                       |
|   + initializeComponents(): void                                                      |
|   + loadUserData(User user): void                                                     |
|   + updateUserFields(User user): void                                                 |
|   + clearPasswordFields(): void                                                       |
|-----------------------------------------------------------------------------------------
| - PanelTransaction                                                                   |
|   + initializeComponents(): void                                                      |
|   + loadTransactions(List<Transaction> transactions): void                            |
|   + showTransactionDetails(Transaction transaction): void                            |
-----------------------------------------------------------------------------------------
| + com.sidomart.controller                                                             |
|-----------------------------------------------------------------------------------------
| - CategoryController                                                                 |
|   + getAllCategories(): List<Category>                                                |
|   + getCategoryById(Integer categoryId): Category                                      |
|   + createCategory(Category category): void                                           |
|   + updateCategory(Category category): void                                           |
|   + deleteCategory(Integer categoryId): void                                          |
|-----------------------------------------------------------------------------------------
| - DashboardController                                                                |
|   + loadDashboardData(): DashboardData                                                |
|-----------------------------------------------------------------------------------------
| - LogController                                                                      |
|   + getAllLogs(): List<Log>                                                           |
|   + getLogById(Integer logId): Log                                                    |
|   + getLogsByUserId(Integer userId): List<Log>                                         |
|   + createLog(Log log): void                                                         |
|   + updateLog(Log log): void                                                         |
|   + deleteLog(Integer logId): void                                                    |
|-----------------------------------------------------------------------------------------
| - ProductController                                                                  |
|   + getAllProducts(): List<Product>                                                   |
|   + getProductById(Integer productId): Product                                         |
|   + getProductsByCategoryId(Integer categoryId): List<Product>                         |
|   + createProduct(Product product): void                                              |
|   + updateProduct(Product product): void                                              |
|   + deleteProduct(Integer productId): void                                            |
|-----------------------------------------------------------------------------------------
| - TransactionController                                                             |
|   + getAllTransactions(): List<Transaction>                                           |
|   + getTransactionById(Integer transactionId): Transaction                             |
|   + getTransactionsByUserId(Integer userId): List<Transaction>                         |
|   + createTransaction(Transaction transaction, List<TransactionDetail> transactionDetails): void |
|   + updateTransaction(Transaction transaction, List<TransactionDetail> transactionDetails): void |
|   + deleteTransaction(Integer transactionId): void                                    |
|-----------------------------------------------------------------------------------------
| - UserController                                                                     |
|   + getAllUsers(): List<User>                                                         |
|   + getUserById(Integer userId): User                                                  |
|   + getUserByUsername(String username): User                                           |
|   + createUser(User user): void                                                       |
|   + updateUser(User user): void                                                       |
|   + deleteUser(Integer userId): void                                                  |
-----------------------------------------------------------------------------------------
| + com.sidomart.model                                                                 |
|-----------------------------------------------------------------------------------------
| - Category                                                                           |
|   + getCategoryId(): Integer                                                          |
|   + setCategoryId(Integer categoryId): void                                           |
|   + getLabel(): String                                                                |
|   + setLabel(String label): void                                                       |
|   + getDescription(): String                                                          |
|   + setDescription(String description): void                                         |
|   + getCreatedAt(): Timestamp                                                         |
|   + setCreatedAt(Timestamp createdAt): void                                           |
-----------------------------------------------------------------------------------------
| - ExpenseReport                                                                      |
|   + getExpenseId(): Integer                                                           |
|   + setExpenseId(Integer expenseId): void                                             |
|   + getUserId(): Integer                                                              |
|   + setUserId(Integer userId): void                                                   |
|   + getAmount(): double                                                               |
|   + setAmount(double amount): void                                                    |
|   + getDescription(): String                                                          |
|   + setDescription(String description): void                                         |
|   + getExpenseDate(): Timestamp                                                       |
|   + setExpenseDate(Timestamp expenseDate): void                                       |
-----------------------------------------------------------------------------------------
| - Log                                                                                |
|   + getLogId(): Integer                                                               |
|   + setLogId(Integer logId): void                                                     |
|   + getUserId(): Integer                                                              |
|   + setUserId(Integer userId): void                                                   |
|   + getAction(): String                                                               |
|   + setAction(String action): void                                                    |
|   + getDescription(): String                                                          |
|   + setDescription(String description): void                                         |
|   + getCreatedAt(): Timestamp                                                         |
|   + setCreatedAt(Timestamp createdAt): void                                           |
-----------------------------------------------------------------------------------------
| - Product                                                                            |
|   + getProductId(): Integer                                                           |
|   + setProductId(Integer productId): void                                             |
|   + getProductName(): String                                                         |
|   + setProductName(String productName): void                                          |
|   + getCategoryId(): Integer                                                          |
|   + setCategoryId(Integer categoryId): void                                           |
|   + getImage(): String                                                                |
|   + setImage(String image): void                                                      |
|   + getPrice(): double                                                                |
|   + setPrice(double price): void                                                      |
|   + getStock(): Integer                                                               |
|   + setStock(Integer stock): void                                                     |
|   + getCreatedAt(): Timestamp                                                         |
|   + setCreatedAt(Timestamp createdAt): void                                           |
|   + getUpdatedAt(): Timestamp                                                         |
|   + setUpdatedAt(Timestamp updatedAt): void                                           |
-----------------------------------------------------------------------------------------
| - Role                                                                               |
|   + fromDatabaseValue(String databaseValue): Role                                       |
-----------------------------------------------------------------------------------------
| - Transaction                                                                        |
|   + getTransactionId(): Integer                                                       |
|   + setTransactionId(Integer transactionId): void                                     |
|   + getUserId(): Integer                                                              |
|   + setUserId(Integer userId): void                                                   |
|   + getTotalAmount(): double                                                          |
|   + setTotalAmount(double totalAmount): void                                          |
|   + getTransactionDate(): Timestamp                                                   |
|   + setTransactionDate(Timestamp transactionDate): void                                |
|   + getUsername(): String                                                            |
|   + setUsername(String username): void                                                |
-----------------------------------------------------------------------------------------
| - TransactionDetail                                                                  |
|   + getDetailId(): Integer                                                            |
|   + setDetailId(Integer detailId): void                                               |
|   + getTransactionId(): Integer                                                       |
|   + setTransactionId(Integer transactionId): void                                     |
|   + getProductId(): Integer                                                           |
|   + setProductId(Integer productId): void                                             |
|   + getQuantity(): Integer                                                            |
|   + setQuantity(Integer quantity): void                                               |
|   + getPrice(): double                                                                |
|   + setPrice(double price): void                                                      |
-----------------------------------------------------------------------------------------
| - User                                                                               |
|   + getUserId(): Integer                                                              |
|   + setUserId(Integer userId): void                                                   |
|   + getFullName(): String                                                             |
|   + setFullName(String fullName): void                                                |
|   + getUsername(): String                                                            |
|   + setUsername(String username): void                                                |
|   + getPassword(): String                                                             |
|   + setPassword(String password): void                                                |
|   + getRole(): String                                                                 |
|   + setRole(String role): void                                                        |
|   + getCreatedAt(): Timestamp                                                         |
|   + setCreatedAt(Timestamp createdAt): void                                           |
|   + getUpdatedAt(): Timestamp                                                         |
|   + setUpdatedAt(Timestamp updatedAt): void                                           |
-----------------------------------------------------------------------------------------
| + com.sidomart.swing                                                                 |
|-----------------------------------------------------------------------------------------
| - RButton                                                                            |
|   + setText(String text): void                                                        |
|   + setIcon(Icon icon): void                                                         |
|   + addActionListener(ActionListener listener): void                                  |
-----------------------------------------------------------------------------------------
| - RPasswordField                                                                    |
|   + getPassword(): char[]                                                            |
|   + setPassword(char[] password): void                                               |
|   + clearPassword(): void                                                            |
-----------------------------------------------------------------------------------------
| - RTextArea                                                                         |
|   + getText(): String                                                                |
|   + setText(String text): void                                                       |
|   + append(String text): void                                                        |
|   + clear(): void                                                                    |
-----------------------------------------------------------------------------------------
| - RTextField                                                                        |
|   + getText(): String                                                                |
|   + setText(String text): void                                                       |
|   + clear(): void                                                                    |
-----------------------------------------------------------------------------------------
| + com.sidomart.util                                                                  |
|-----------------------------------------------------------------------------------------
| - DatabaseUtilities                                                                  |
|   + connect(): Connection                                                            |
|   + disconnect(Connection conn): void                                                |
|   + executeQuery(Connection conn, String query): ResultSet                            |
|   + executeUpdate(Connection conn, String query): int                                 |
-----------------------------------------------------------------------------------------
| - SessionManager                                                                     |
|   + getCurrentUser(): User                                                           |
|   + setCurrentUser(User user): void                                                   |
|   + isLoggedIn(): boolean                                                            |
|   + login(String username, String password): boolean                                  |
|   + logout(): void                                                                    |
-----------------------------------------------------------------------------------------
| + com.sidomart.view                                                                  |
|-----------------------------------------------------------------------------------------
| - Dashboard                                                                          |
|   + initializeComponents(): void                                                      |
|   + loadUserData(): void                                                              |
|   + loadRecentTransactions(): void                                                    |
|   + showNotification(String message): void                                            |
-----------------------------------------------------------------------------------------
| - Login                                                                              |
|   + initializeComponents(): void                                                      |
|   + getUsername(): String                                                            |
|   + getPassword(): char[]                                                            |
|   + clearFields(): void                                                               |
|   + showMessage(String message): void                                                 |
-----------------------------------------------------------------------------------------
| - Register                                                                           |
|   + initializeComponents(): void                                                      |
|   + getUsername(): String                                                            |
|   + getPassword(): char[]                                                            |
|   + getFullName(): String                                                             |
|   + clearFields(): void                                                               |
|   + showMessage(String message): void                                                 |
-----------------------------------------------------------------------------------------
| - Splash                                                                             |
|   + showSplashScreen(): void                                                          |
|   + hideSplashScreen(): void                                                          |
-----------------------------------------------------------------------------------------
