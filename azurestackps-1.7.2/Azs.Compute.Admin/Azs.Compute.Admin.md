---
Module Name: Azs.Compute.Admin
Module Guid: e662cef1-a477-40a2-ab9f-06e8de7cc423
Download Help Link:
  '[object Object]': 
Help Version:
  '[object Object]': 
Locale: en-US
ms.openlocfilehash: 4194899ad20356c8cde68110553495558d3816d5
ms.sourcegitcommit: 0fdccb57a356b6e7c35a77b1f76e01fb96ef582b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/17/2019
ms.locfileid: "93611374"
---
# <span data-ttu-id="0e079-101">Azs. 系統管理模組</span><span class="sxs-lookup"><span data-stu-id="0e079-101">Azs.Compute.Admin Module</span></span>
## <span data-ttu-id="0e079-102">說明</span><span class="sxs-lookup"><span data-stu-id="0e079-102">Description</span></span>
<span data-ttu-id="0e079-103">預覽版本的 AzureStack Compute 運算子模組，提供管理計算配額、平臺影像和虛擬機器延伸的功能，以及管理的磁片遷移作業，以重新平衡儲存空間。</span><span class="sxs-lookup"><span data-stu-id="0e079-103">Preview release of the AzureStack Compute operator module which provides functionality to manage compute quotas, platform images, and virtual machine extensions, as well as managed disks migration jobs to rebalance storage.</span></span>

## <span data-ttu-id="0e079-104">Azs. 系統管理 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0e079-104">Azs.Compute.Admin Cmdlets</span></span>
### [<span data-ttu-id="0e079-105">附加 AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="0e079-105">Add-AzsPlatformImage</span></span>](Add-AzsPlatformImage.md)
<span data-ttu-id="0e079-106">從指定的影像配置新增虛擬機器平臺影像。</span><span class="sxs-lookup"><span data-stu-id="0e079-106">Add a virtual machine platform image from a given image configuration.</span></span>

### [<span data-ttu-id="0e079-107">附加 AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0e079-107">Add-AzsVMExtension</span></span>](Add-AzsVMExtension.md)
<span data-ttu-id="0e079-108">建立新的虛擬機器延伸影像。</span><span class="sxs-lookup"><span data-stu-id="0e079-108">Create a new virtual machine extension image.</span></span>

### [<span data-ttu-id="0e079-109">AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="0e079-109">Get-AzsComputeQuota</span></span>](Get-AzsComputeQuota.md)
<span data-ttu-id="0e079-110">傳回指定計算物件配額限制的配額。</span><span class="sxs-lookup"><span data-stu-id="0e079-110">Returns quotas specifying the quota limits for compute objects.</span></span>

### [<span data-ttu-id="0e079-111">AzsDisk</span><span class="sxs-lookup"><span data-stu-id="0e079-111">Get-AzsDisk</span></span>](Get-AzsDisk.md)
<span data-ttu-id="0e079-112">傳回可在指定的共用中遷移的受管理磁片清單。</span><span class="sxs-lookup"><span data-stu-id="0e079-112">Returns the list of managed disks which can be migrated in the specified share.</span></span>

### [<span data-ttu-id="0e079-113">AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0e079-113">Get-AzsDiskMigrationJob</span></span>](Get-AzsDiskMigrationJob.md)
<span data-ttu-id="0e079-114">傳回受管理磁片遷移作業的清單。</span><span class="sxs-lookup"><span data-stu-id="0e079-114">Returns the list of managed disk migration jobs.</span></span>

### [<span data-ttu-id="0e079-115">AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="0e079-115">Get-AzsPlatformImage</span></span>](Get-AzsPlatformImage.md)
<span data-ttu-id="0e079-116">傳回載入到平臺影像儲存庫的虛擬機器影像。</span><span class="sxs-lookup"><span data-stu-id="0e079-116">Returns virtual machine images loaded into the platform image repository.</span></span>

### [<span data-ttu-id="0e079-117">AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0e079-117">Get-AzsVMExtension</span></span>](Get-AzsVMExtension.md)
<span data-ttu-id="0e079-118">傳回目前可用的虛擬機器影像延伸。</span><span class="sxs-lookup"><span data-stu-id="0e079-118">Returns virtual machine image extensions currently available.</span></span>

### [<span data-ttu-id="0e079-119">新-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="0e079-119">New-AzsComputeQuota</span></span>](New-AzsComputeQuota.md)
<span data-ttu-id="0e079-120">建立用來限制計算資源的新計算配額。</span><span class="sxs-lookup"><span data-stu-id="0e079-120">Create a new compute quota used to limit compute resources.</span></span>

### [<span data-ttu-id="0e079-121">新-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0e079-121">New-AzsDiskMigrationJob</span></span>](New-AzsDiskMigrationJob.md)
<span data-ttu-id="0e079-122">啟動受管理的磁片遷移作業，以將受管理的磁片遷移至指定的目的地共用。</span><span class="sxs-lookup"><span data-stu-id="0e079-122">Starts a managed disk migration job to migrate managed disks to the specified destination share.</span></span>

### [<span data-ttu-id="0e079-123">新-AzsDataDiskObject</span><span class="sxs-lookup"><span data-stu-id="0e079-123">New-AzsDataDiskObject</span></span>](New-AzsDataDiskObject.md)
<span data-ttu-id="0e079-124">建立用來建立新的虛擬機器平臺影像的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="0e079-124">Creates a data disk which is used to create a new virtual machine platform image.</span></span>

### [<span data-ttu-id="0e079-125">移除-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="0e079-125">Remove-AzsComputeQuota</span></span>](Remove-AzsComputeQuota.md)
<span data-ttu-id="0e079-126">刪除指定的計算配額。</span><span class="sxs-lookup"><span data-stu-id="0e079-126">Deletes specified compute quota.</span></span>

### [<span data-ttu-id="0e079-127">移除-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="0e079-127">Remove-AzsPlatformImage</span></span>](Remove-AzsPlatformImage.md)
<span data-ttu-id="0e079-128">從平臺影像儲存庫刪除虛擬機器影像。</span><span class="sxs-lookup"><span data-stu-id="0e079-128">Delete a virtual machine image from the platform image repository.</span></span>

### [<span data-ttu-id="0e079-129">移除-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0e079-129">Remove-AzsVMExtension</span></span>](Remove-AzsVMExtension.md)
<span data-ttu-id="0e079-130">刪除虛擬機器延伸影像。</span><span class="sxs-lookup"><span data-stu-id="0e079-130">Deletes a virtual machine extension image.</span></span>

### [<span data-ttu-id="0e079-131">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="0e079-131">Set-AzsComputeQuota</span></span>](Set-AzsComputeQuota.md)
<span data-ttu-id="0e079-132">使用提供的參數更新現有的計算配額。</span><span class="sxs-lookup"><span data-stu-id="0e079-132">Update an existing compute quota using the provided parameters.</span></span>

### [<span data-ttu-id="0e079-133">停止 AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="0e079-133">Stop-AzsDiskMigrationJob</span></span>](Stop-AzsDiskMigrationJob.md)
<span data-ttu-id="0e079-134">取消受管理的磁片遷移作業。</span><span class="sxs-lookup"><span data-stu-id="0e079-134">Cancel a managed disk migration job.</span></span>

