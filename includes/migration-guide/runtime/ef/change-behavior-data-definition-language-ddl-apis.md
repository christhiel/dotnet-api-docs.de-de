### <a name="change-in-behavior-in-data-definition-language-ddl-apis"></a><span data-ttu-id="75943-101">Das Verhalten Sie in Internetinformationsdienste APIs (Data Definition Language, Datendefinitionssprache)</span><span class="sxs-lookup"><span data-stu-id="75943-101">Change in behavior in Data Definition Language (DDL) APIs</span></span>

|   |   |
|---|---|
|<span data-ttu-id="75943-102">Details</span><span class="sxs-lookup"><span data-stu-id="75943-102">Details</span></span>|<span data-ttu-id="75943-103">Das Verhalten von DDL-APIs beim Angeben von „AttachDBFilename“ hat sich wie folgt geändert:</span><span class="sxs-lookup"><span data-stu-id="75943-103">The behavior of DDL APIs when AttachDBFilename is specified has changed as follows:</span></span><ul><li><span data-ttu-id="75943-104">Verbindungszeichenfolgen müssen keinen „Initial Catalog“-Wert angeben.</span><span class="sxs-lookup"><span data-stu-id="75943-104">Connection strings need not specify an Initial Catalog value.</span></span> <span data-ttu-id="75943-105">Zuvor waren AttachDBFilename und Anfangskatalog erforderlich.</span><span class="sxs-lookup"><span data-stu-id="75943-105">Previously, both AttachDBFilename and Initial Catalog were required.</span></span></li><li><span data-ttu-id="75943-106">Wenn sowohl "AttachDBFilename" und "Initial Catalog angegeben wurden, und die angegebene MDF-Datei vorhanden ist, gibt die ObjectContext.DatabaseExists-Methode" true "zurück.</span><span class="sxs-lookup"><span data-stu-id="75943-106">If both AttachDBFilename and Initial Catalog are specified and the given MDF file exists, the ObjectContext.DatabaseExists method returns true.</span></span> <span data-ttu-id="75943-107">Bislang hat sie „false“ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75943-107">Previously, it returned false.</span></span></li><li><span data-ttu-id="75943-108">Wenn sowohl "AttachDBFilename" und "Initial Catalog angegeben wurden, und die angegebene MDF-Datei vorhanden ist, werden beim Aufrufen der Methode ObjectContext.DeleteDatabase die Dateien gelöscht.</span><span class="sxs-lookup"><span data-stu-id="75943-108">If both AttachDBFilename and Initial Catalog are specified and the given MDF file exists, calling the ObjectContext.DeleteDatabase method deletes the files.</span></span></li><li><span data-ttu-id="75943-109">Wenn „ObjectContext.DeleteDatabase“ aufgerufen wird, wenn die Verbindungszeichenfolge einen AttachDBFilename-Wert mit einer nicht vorhandenen MDF-Datei und einem nicht vorhandenen „Initial Catalog“ angibt, löst die Methode eine InvalidOperationException-Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="75943-109">If ObjectContext.DeleteDatabase is called when the connection string specifies an AttachDBFilename value with an MDF that doesn't exist and an Initial Catalog that doesn't exist, the method throws an InvalidOperationException exception.</span></span> <span data-ttu-id="75943-110">Zuvor hat sie eine SqlException-Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="75943-110">Previously, it threw a SqlException exception.</span></span></li></ul>|
|<span data-ttu-id="75943-111">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="75943-111">Suggestion</span></span>|<span data-ttu-id="75943-112">Diese Änderungen erleichtern das Erstellen von Tools und Anwendungen, die die DDL-APIs verwenden.</span><span class="sxs-lookup"><span data-stu-id="75943-112">These changes make it easier to build tools and applications that use the DDL APIs.</span></span> <span data-ttu-id="75943-113">Diese Änderungen können sich in den folgenden Szenarien auf die Anwendungskompatibilität auswirken:</span><span class="sxs-lookup"><span data-stu-id="75943-113">These changes can affect application compatibility in the following scenarios:</span></span><ul><li><span data-ttu-id="75943-114">Der Benutzer schreibt Code, der einen DROP DATABASE-Befehl direkt ausführt, anstatt „ObjectContext.DeleteDatabase“ aufzurufen, wenn „ObjectContext.DatabaseExists“ den Wert „true“ zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="75943-114">The user writes code that executes a DROP DATABASE command directly instead of calling ObjectContext.DeleteDatabase if ObjectContext.DatabaseExists returns true.</span></span> <span data-ttu-id="75943-115">Ist die Datenbank nicht angefügt, die MDF-Datei jedoch vorhanden, wird vorhandener Code hierdurch unbrauchbar.</span><span class="sxs-lookup"><span data-stu-id="75943-115">This breaks existing code If the database is not attached but the MDF file exists.</span></span></li><li><span data-ttu-id="75943-116">Der Benutzer schreibt Code, der erwartet, dass die ObjectContext.DeleteDatabase-Methode anstelle einer InvalidOperationException-Ausnahme eine SqlException-Ausnahme auslöst, wenn „Initial Catalog“ und die MDF-Datei nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="75943-116">The user writes code that expects the ObjectContext.DeleteDatabase method to throw a SqlException exception rather than an InvalidOperationException exception when the Initial Catalog and MDF file don't exist.</span></span></li></ul>|
|<span data-ttu-id="75943-117">Bereich</span><span class="sxs-lookup"><span data-stu-id="75943-117">Scope</span></span>|<span data-ttu-id="75943-118">Gering</span><span class="sxs-lookup"><span data-stu-id="75943-118">Minor</span></span>|
|<span data-ttu-id="75943-119">Version</span><span class="sxs-lookup"><span data-stu-id="75943-119">Version</span></span>|<span data-ttu-id="75943-120">4.5</span><span class="sxs-lookup"><span data-stu-id="75943-120">4.5</span></span>|
|<span data-ttu-id="75943-121">Typ</span><span class="sxs-lookup"><span data-stu-id="75943-121">Type</span></span>|<span data-ttu-id="75943-122">Laufzeit</span><span class="sxs-lookup"><span data-stu-id="75943-122">Runtime</span></span>|
