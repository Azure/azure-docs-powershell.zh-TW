---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/remove-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: 258c7057b8f78ea6de1db506d23c60f679e1ca39
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794854"
---
# <span data-ttu-id="dc409-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="dc409-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="dc409-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc409-102">SYNOPSIS</span></span>


## <span data-ttu-id="dc409-103">句法</span><span class="sxs-lookup"><span data-stu-id="dc409-103">SYNTAX</span></span>

### <span data-ttu-id="dc409-104">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="dc409-104">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dc409-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc409-105">DeleteViaIdentity</span></span>
```
Remove-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dc409-106">說明</span><span class="sxs-lookup"><span data-stu-id="dc409-106">DESCRIPTION</span></span>


## <span data-ttu-id="dc409-107">示例</span><span class="sxs-lookup"><span data-stu-id="dc409-107">EXAMPLES</span></span>

### <span data-ttu-id="dc409-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="dc409-108">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsStorageQuota -Name 'TestQuota'
```

<span data-ttu-id="dc409-109">依名稱移除儲存配額。</span><span class="sxs-lookup"><span data-stu-id="dc409-109">Remove a storage quota by name.</span></span>

### <span data-ttu-id="dc409-110">範例2：</span><span class="sxs-lookup"><span data-stu-id="dc409-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestQuota' | Remove-AzsStorageQuota
```

<span data-ttu-id="dc409-111">依管道移除儲存配額。</span><span class="sxs-lookup"><span data-stu-id="dc409-111">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="dc409-112">參數</span><span class="sxs-lookup"><span data-stu-id="dc409-112">PARAMETERS</span></span>

### <span data-ttu-id="dc409-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc409-113">-DefaultProfile</span></span>


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

### <span data-ttu-id="dc409-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc409-114">-InputObject</span></span>
<span data-ttu-id="dc409-115">若要構造，請參閱適用于 INPUTOBJECT 屬性的 [記事] 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="dc409-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="dc409-116">-位置</span><span class="sxs-lookup"><span data-stu-id="dc409-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dc409-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc409-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dc409-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc409-118">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dc409-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dc409-119">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dc409-120">-確認</span><span class="sxs-lookup"><span data-stu-id="dc409-120">-Confirm</span></span>
<span data-ttu-id="dc409-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dc409-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dc409-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc409-122">-WhatIf</span></span>
<span data-ttu-id="dc409-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc409-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc409-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc409-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="dc409-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc409-125">CommonParameters</span></span>
<span data-ttu-id="dc409-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc409-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc409-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dc409-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc409-128">輸入</span><span class="sxs-lookup"><span data-stu-id="dc409-128">INPUTS</span></span>

### <span data-ttu-id="dc409-129">IStorageAdminIdentity （StorageAdmin）的</span><span class="sxs-lookup"><span data-stu-id="dc409-129">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.IStorageAdminIdentity</span></span>

## <span data-ttu-id="dc409-130">輸出</span><span class="sxs-lookup"><span data-stu-id="dc409-130">OUTPUTS</span></span>

### <span data-ttu-id="dc409-131">System.object</span><span class="sxs-lookup"><span data-stu-id="dc409-131">System.Boolean</span></span>



## <span data-ttu-id="dc409-132">筆記</span><span class="sxs-lookup"><span data-stu-id="dc409-132">NOTES</span></span>

<span data-ttu-id="dc409-133">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="dc409-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc409-134">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="dc409-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dc409-135">INPUTOBJECT <IStorageAdminIdentity> ：</span><span class="sxs-lookup"><span data-stu-id="dc409-135">INPUTOBJECT <IStorageAdminIdentity>:</span></span> 
  - <span data-ttu-id="dc409-136">`[AccountId <String>]`：租使用者看不到的內部儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="dc409-136">`[AccountId <String>]`: Internal storage account ID, which is not visible to tenant.</span></span>
  - <span data-ttu-id="dc409-137">`[AsyncOperationId <String>]`：非同步作業 Id。</span><span class="sxs-lookup"><span data-stu-id="dc409-137">`[AsyncOperationId <String>]`: Async Operation Id.</span></span>
  - <span data-ttu-id="dc409-138">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="dc409-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc409-139">`[Location <String>]`：資源位置。</span><span class="sxs-lookup"><span data-stu-id="dc409-139">`[Location <String>]`: Resource location.</span></span>
  - <span data-ttu-id="dc409-140">`[QuotaName <String>]`：儲存配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc409-140">`[QuotaName <String>]`: The name of the storage quota.</span></span>
  - <span data-ttu-id="dc409-141">`[ResourceGroup <String>]`：資源組名。</span><span class="sxs-lookup"><span data-stu-id="dc409-141">`[ResourceGroup <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="dc409-142">`[ServiceName <String>]`：儲存服務名稱。</span><span class="sxs-lookup"><span data-stu-id="dc409-142">`[ServiceName <String>]`: Storage service name.</span></span>
  - <span data-ttu-id="dc409-143">`[SubscriptionId <String>]`：訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="dc409-143">`[SubscriptionId <String>]`: Subscription Id.</span></span>

## <span data-ttu-id="dc409-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc409-144">RELATED LINKS</span></span>

