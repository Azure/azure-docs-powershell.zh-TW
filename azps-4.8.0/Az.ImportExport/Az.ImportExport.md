---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128695"
---
# <span data-ttu-id="441c4-101">Az ImportExport 模組</span><span class="sxs-lookup"><span data-stu-id="441c4-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="441c4-102">說明</span><span class="sxs-lookup"><span data-stu-id="441c4-102">Description</span></span>
<span data-ttu-id="441c4-103">Microsoft Azure PowerShell： ImportExport Cmdlet</span><span class="sxs-lookup"><span data-stu-id="441c4-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="441c4-104">Az ImportExport Cmdlet</span><span class="sxs-lookup"><span data-stu-id="441c4-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="441c4-105">AzImportExport</span><span class="sxs-lookup"><span data-stu-id="441c4-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="441c4-106">取得現有作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="441c4-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="441c4-107">AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="441c4-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="441c4-108">傳回指定作業中所有磁片磁碟機的 BitLocker 金鑰。</span><span class="sxs-lookup"><span data-stu-id="441c4-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="441c4-109">AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="441c4-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="441c4-110">傳回與匯入或匯出作業相關聯之磁片之位置的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="441c4-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="441c4-111">位置是 Azure 區域。</span><span class="sxs-lookup"><span data-stu-id="441c4-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="441c4-112">新-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="441c4-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="441c4-113">在指定的訂閱中建立新作業或更新現有作業。</span><span class="sxs-lookup"><span data-stu-id="441c4-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="441c4-114">新-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="441c4-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="441c4-115">建立 ImportExport 的 DriverList 物件。</span><span class="sxs-lookup"><span data-stu-id="441c4-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="441c4-116">移除-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="441c4-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="441c4-117">刪除現有的工作。</span><span class="sxs-lookup"><span data-stu-id="441c4-117">Deletes an existing job.</span></span>
<span data-ttu-id="441c4-118">只有 [建立] 或 [已完成] 狀態中的工作可以刪除。</span><span class="sxs-lookup"><span data-stu-id="441c4-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="441c4-119">更新-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="441c4-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="441c4-120">更新作業的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="441c4-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="441c4-121">您可以呼叫此操作，通知匯入/匯出服務，包含匯入或匯出作業的硬驅已傳送至 Microsoft 資料中心。</span><span class="sxs-lookup"><span data-stu-id="441c4-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="441c4-122">您也可以用來取消現有作業。</span><span class="sxs-lookup"><span data-stu-id="441c4-122">It can also be used to cancel an existing job.</span></span>

