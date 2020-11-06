---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: 6eb1ccb692f9f57e0d686a26a7c534459118cd19
ms.sourcegitcommit: 0b94b9566124331d0b15eb7f5a811305c254172e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/15/2019
ms.locfileid: "93611420"
---
# <span data-ttu-id="d627a-101">Az DataMigration 模組</span><span class="sxs-lookup"><span data-stu-id="d627a-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="d627a-102">說明</span><span class="sxs-lookup"><span data-stu-id="d627a-102">Description</span></span>
<span data-ttu-id="d627a-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="d627a-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="d627a-104">Az DataMigration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d627a-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="d627a-105">AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="d627a-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="d627a-106">檢索 Azure 資料庫移轉專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="d627a-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="d627a-107">AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d627a-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="d627a-108">檢索與 Azure Database 遷移服務實例相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="d627a-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="d627a-109">AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="d627a-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="d627a-110">檢索與 Azure Database 遷移服務遷移任務相關聯的 PSProjectTask 物件。</span><span class="sxs-lookup"><span data-stu-id="d627a-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="d627a-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="d627a-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="d627a-112">建立要在現有 DMS 任務上執行的新命令。</span><span class="sxs-lookup"><span data-stu-id="d627a-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="d627a-113">新-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="d627a-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="d627a-114">建立新的連線資訊物件，以指定連線的伺服器類型和名稱。</span><span class="sxs-lookup"><span data-stu-id="d627a-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="d627a-115">新-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="d627a-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="d627a-116">建立 Azure Database 遷移服務的 DatabaseInfo 物件，該物件會指定要遷移的資料庫來源。</span><span class="sxs-lookup"><span data-stu-id="d627a-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="d627a-117">新-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="d627a-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="d627a-118">建立 Azure Database 遷移服務的 [資料庫共用] 物件，該物件會指定要進行來源資料庫備份的本機網路共用。</span><span class="sxs-lookup"><span data-stu-id="d627a-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="d627a-119">新-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="d627a-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="d627a-120">建立新的 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="d627a-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="d627a-121">新-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="d627a-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="d627a-122">建立一個資料庫輸入物件，其中包含有關要遷移之來源和目標資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="d627a-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="d627a-123">新-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d627a-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="d627a-124">建立 Azure Database 遷移服務的新實例。</span><span class="sxs-lookup"><span data-stu-id="d627a-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="d627a-125">新-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="d627a-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="d627a-126">建立要用於遷移工作之同步處理案例的特定資料庫資訊物件。</span><span class="sxs-lookup"><span data-stu-id="d627a-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="d627a-127">新-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="d627a-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="d627a-128">在 Azure 資料庫移轉服務中建立及啟動資料移轉工作。</span><span class="sxs-lookup"><span data-stu-id="d627a-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="d627a-129">移除-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="d627a-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="d627a-130">從 Azure 移除 Azure 資料庫移轉服務專案。</span><span class="sxs-lookup"><span data-stu-id="d627a-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="d627a-131">移除-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d627a-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="d627a-132">從 Azure 移除 Azure 資料庫移轉服務的實例。</span><span class="sxs-lookup"><span data-stu-id="d627a-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="d627a-133">移除-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="d627a-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="d627a-134">從 Azure 移除 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="d627a-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="d627a-135">開始-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d627a-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="d627a-136">在已停止的狀態中啟動 Azure Database 遷移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="d627a-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="d627a-137">停止 AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d627a-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="d627a-138">停止處於執行中狀態的 Azure 資料庫移轉服務實例。</span><span class="sxs-lookup"><span data-stu-id="d627a-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="d627a-139">停止 AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="d627a-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="d627a-140">停止處於執行中狀態的 Azure 資料庫移轉服務任務。</span><span class="sxs-lookup"><span data-stu-id="d627a-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

