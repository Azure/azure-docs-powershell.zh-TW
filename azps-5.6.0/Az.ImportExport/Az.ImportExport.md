---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: cce265bc3d61f445c6843b0c1ca340ad921e1089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907869"
---
# <span data-ttu-id="dc498-101">Az.ImportExport 模組</span><span class="sxs-lookup"><span data-stu-id="dc498-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="dc498-102">描述</span><span class="sxs-lookup"><span data-stu-id="dc498-102">Description</span></span>
<span data-ttu-id="dc498-103">Microsoft Azure PowerShell：ImportExport Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dc498-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="dc498-104">Az.ImportExport Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dc498-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="dc498-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="dc498-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="dc498-106">獲得現有工作的資訊。</span><span class="sxs-lookup"><span data-stu-id="dc498-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="dc498-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="dc498-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="dc498-108">針對指定工作的所有磁片磁碟機，會返回 BitLocker 鍵。</span><span class="sxs-lookup"><span data-stu-id="dc498-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="dc498-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="dc498-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="dc498-110">會返回可以出貨與匯進或匯出工作相關之磁片的位置詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dc498-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="dc498-111">位置是 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="dc498-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="dc498-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="dc498-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="dc498-113">建立新工作或更新指定訂閱中的現有工作。</span><span class="sxs-lookup"><span data-stu-id="dc498-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="dc498-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="dc498-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="dc498-115">建立 ImportExport 的 DriverList 物件。</span><span class="sxs-lookup"><span data-stu-id="dc498-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="dc498-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="dc498-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="dc498-117">刪除現有的工作。</span><span class="sxs-lookup"><span data-stu-id="dc498-117">Deletes an existing job.</span></span>
<span data-ttu-id="dc498-118">只有建立或完成狀態中的工作可以刪除。</span><span class="sxs-lookup"><span data-stu-id="dc498-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="dc498-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="dc498-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="dc498-120">更新工作的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="dc498-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="dc498-121">您可以撥打此作業來通知匯進/匯出服務，指出包含匯進或匯出工作的硬碟已運送至 Microsoft 資料中心。</span><span class="sxs-lookup"><span data-stu-id="dc498-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="dc498-122">它也可以用來取消現有的工作。</span><span class="sxs-lookup"><span data-stu-id="dc498-122">It can also be used to cancel an existing job.</span></span>

