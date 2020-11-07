---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968058"
---
# <span data-ttu-id="c37b4-101">Get-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="c37b4-101">Get-AzsStorageQuota</span></span>

## <span data-ttu-id="c37b4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c37b4-102">SYNOPSIS</span></span>


## <span data-ttu-id="c37b4-103">句法</span><span class="sxs-lookup"><span data-stu-id="c37b4-103">SYNTAX</span></span>

### <span data-ttu-id="c37b4-104"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="c37b4-104">List (Default)</span></span>
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="c37b4-105">獲取</span><span class="sxs-lookup"><span data-stu-id="c37b4-105">Get</span></span>
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c37b4-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c37b4-106">GetViaIdentity</span></span>
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c37b4-107">說明</span><span class="sxs-lookup"><span data-stu-id="c37b4-107">DESCRIPTION</span></span>


## <span data-ttu-id="c37b4-108">示例</span><span class="sxs-lookup"><span data-stu-id="c37b4-108">EXAMPLES</span></span>

### <span data-ttu-id="c37b4-109">範例1：</span><span class="sxs-lookup"><span data-stu-id="c37b4-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota
```

<span data-ttu-id="c37b4-110">取得儲存配額清單。</span><span class="sxs-lookup"><span data-stu-id="c37b4-110">Get the list of storage quotas.</span></span>

### <span data-ttu-id="c37b4-111">範例2：</span><span class="sxs-lookup"><span data-stu-id="c37b4-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

<span data-ttu-id="c37b4-112">依名稱取得指定儲存配額的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c37b4-112">Get details of the specified storage quota by name.</span></span>

## <span data-ttu-id="c37b4-113">參數</span><span class="sxs-lookup"><span data-stu-id="c37b4-113">PARAMETERS</span></span>

### <span data-ttu-id="c37b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37b4-114">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c37b4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c37b4-115">-InputObject</span></span>
<span data-ttu-id="c37b4-116">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c37b4-116">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c37b4-117">-位置</span><span class="sxs-lookup"><span data-stu-id="c37b4-117">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c37b4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c37b4-118">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c37b4-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c37b4-119">-SubscriptionId</span></span>


```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c37b4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37b4-120">CommonParameters</span></span>
<span data-ttu-id="c37b4-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c37b4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37b4-122">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c37b4-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37b4-123">輸入</span><span class="sxs-lookup"><span data-stu-id="c37b4-123">INPUTS</span></span>

### <span data-ttu-id="c37b4-124">IStorageAdminIdentity （StorageAdmin）的</span><span class="sxs-lookup"><span data-stu-id="c37b4-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="c37b4-125">輸出</span><span class="sxs-lookup"><span data-stu-id="c37b4-125">OUTPUTS</span></span>

### <span data-ttu-id="c37b4-126">IStorageQuota （StorageAdmin）。 Api201908Preview。</span><span class="sxs-lookup"><span data-stu-id="c37b4-126">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="c37b4-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c37b4-127">NOTES</span></span>

<span data-ttu-id="c37b4-128">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c37b4-128">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c37b4-129">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c37b4-129">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c37b4-130">INPUTOBJECT <IStorageAdminIdentity> ：</span><span class="sxs-lookup"><span data-stu-id="c37b4-130">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="c37b4-131">`[AccountId <String>]`：租使用者看不到的內部儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="c37b4-131">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="c37b4-132">`[AsyncOperationId <String>]`：非同步作業 Id。</span><span class="sxs-lookup"><span data-stu-id="c37b4-132">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="c37b4-133">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c37b4-133">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c37b4-134">`[Location <String>]`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="c37b4-134">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="c37b4-135">`[QuotaName <String>]`：儲存配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="c37b4-135">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="c37b4-136">`[ResourceGroup <String>]`：資源組名。</span><span class="sxs-lookup"><span data-stu-id="c37b4-136">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="c37b4-137">`[ServiceName <String>]`：儲存服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c37b4-137">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="c37b4-138">`[SubscriptionId <String>]`：訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="c37b4-138">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="c37b4-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="c37b4-139">RELATED LINKS</span></span>

