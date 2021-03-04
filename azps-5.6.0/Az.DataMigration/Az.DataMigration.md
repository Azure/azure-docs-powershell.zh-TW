---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: c73e82285a848c9ff6abf197eb3352cf708a2f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903610"
---
# <span data-ttu-id="f8227-101">Az.DataMigration 模組</span><span class="sxs-lookup"><span data-stu-id="f8227-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="f8227-102">描述</span><span class="sxs-lookup"><span data-stu-id="f8227-102">Description</span></span>
<span data-ttu-id="f8227-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="f8227-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="f8227-104">Az.DataMigration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f8227-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="f8227-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="f8227-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="f8227-106">會取回 Azure 資料庫移移專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="f8227-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="f8227-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f8227-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="f8227-108">會取回與 Azure 資料庫移移服務實例相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="f8227-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="f8227-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="f8227-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="f8227-110">會取回與 Azure 資料庫移移服務移移工作相關聯的 PSProjectTask 物件。</span><span class="sxs-lookup"><span data-stu-id="f8227-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="f8227-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="f8227-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="f8227-112">建立新命令，以對現有 DMS 工作執行。</span><span class="sxs-lookup"><span data-stu-id="f8227-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="f8227-113">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="f8227-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="f8227-114">建立一個新的連接資訊物件，指定連接的伺服器類型和名稱。</span><span class="sxs-lookup"><span data-stu-id="f8227-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="f8227-115">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="f8227-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="f8227-116">為 Azure 資料庫移移服務建立 DatabaseInfo 物件，指定要移移的資料庫來源。</span><span class="sxs-lookup"><span data-stu-id="f8227-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="f8227-117">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="f8227-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="f8227-118">為 Azure 資料庫移移服務建立 FileShare 物件，指定要執行源資料庫備份的局網共用。</span><span class="sxs-lookup"><span data-stu-id="f8227-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="f8227-119">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="f8227-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="f8227-120">建立新的 Azure 資料庫移移服務專案。</span><span class="sxs-lookup"><span data-stu-id="f8227-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="f8227-121">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="f8227-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="f8227-122">建立資料庫輸入物件，其中包含移移來源和目標資料庫的資訊。</span><span class="sxs-lookup"><span data-stu-id="f8227-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="f8227-123">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f8227-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="f8227-124">建立 Azure 資料庫移移服務的新實例。</span><span class="sxs-lookup"><span data-stu-id="f8227-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="f8227-125">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="f8227-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="f8227-126">建立同步處理案例的特定資料庫資訊物件，以用於移移工作。</span><span class="sxs-lookup"><span data-stu-id="f8227-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="f8227-127">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="f8227-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="f8227-128">在 Azure 資料庫移移服務中建立及啟動資料移轉工作。</span><span class="sxs-lookup"><span data-stu-id="f8227-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="f8227-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="f8227-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="f8227-130">從 Azure 移除 Azure 資料庫移移服務專案。</span><span class="sxs-lookup"><span data-stu-id="f8227-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="f8227-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f8227-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="f8227-132">從 Azure 移除 Azure 資料庫移移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="f8227-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="f8227-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="f8227-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="f8227-134">從 Azure 移除 Azure 資料庫移移服務工作。</span><span class="sxs-lookup"><span data-stu-id="f8227-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="f8227-135">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f8227-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="f8227-136">以停止狀態啟動 Azure 資料庫移移服務的實例。</span><span class="sxs-lookup"><span data-stu-id="f8227-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="f8227-137">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f8227-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="f8227-138">停止執行中的 Azure 資料庫移移服務實例。</span><span class="sxs-lookup"><span data-stu-id="f8227-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="f8227-139">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="f8227-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="f8227-140">停止執行中的 Azure 資料庫移移服務工作。</span><span class="sxs-lookup"><span data-stu-id="f8227-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

