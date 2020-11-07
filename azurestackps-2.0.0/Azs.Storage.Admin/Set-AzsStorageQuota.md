---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: b89bef906cf54378719c7c6b83dcaff484ced282
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794853"
---
# <span data-ttu-id="b64c1-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="b64c1-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="b64c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b64c1-102">SYNOPSIS</span></span>


## <span data-ttu-id="b64c1-103">句法</span><span class="sxs-lookup"><span data-stu-id="b64c1-103">SYNTAX</span></span>

### <span data-ttu-id="b64c1-104">預設)  (名稱</span><span class="sxs-lookup"><span data-stu-id="b64c1-104">Name (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b64c1-105">QuotaObject</span><span class="sxs-lookup"><span data-stu-id="b64c1-105">QuotaObject</span></span>
```
Set-AzsStorageQuota -QuotaObject <IStorageQuota> [-Location <String>] [-SubscriptionId <String>]
 [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="b64c1-106">說明</span><span class="sxs-lookup"><span data-stu-id="b64c1-106">DESCRIPTION</span></span>


## <span data-ttu-id="b64c1-107">示例</span><span class="sxs-lookup"><span data-stu-id="b64c1-107">EXAMPLES</span></span>

### <span data-ttu-id="b64c1-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="b64c1-108">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -NumberOfStorageAccounts 11 -CapacityInGb 22
```

<span data-ttu-id="b64c1-109">依名稱更新現有的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="b64c1-109">Update an existing storage quota by name.</span></span>

### <span data-ttu-id="b64c1-110">範例2：</span><span class="sxs-lookup"><span data-stu-id="b64c1-110">Example 2:</span></span>
```powershell
PS C:\> Get-AzsStorageQuota -Name 'TestUpdateStorageQuota' | Set-AzsStorageQuota -NumberOfStorageAccounts 22 -CapacityInGb 33
```

<span data-ttu-id="b64c1-111">依管道更新現有的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="b64c1-111">Update an existing storage quota by piping.</span></span>

## <span data-ttu-id="b64c1-112">參數</span><span class="sxs-lookup"><span data-stu-id="b64c1-112">PARAMETERS</span></span>

### <span data-ttu-id="b64c1-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="b64c1-113">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b64c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b64c1-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="b64c1-115">-位置</span><span class="sxs-lookup"><span data-stu-id="b64c1-115">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b64c1-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="b64c1-116">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Name
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b64c1-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="b64c1-117">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b64c1-118">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="b64c1-118">-QuotaObject</span></span>
<span data-ttu-id="b64c1-119">若要建立，請參閱 QUOTAOBJECT 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="b64c1-119">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: QuotaObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="b64c1-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b64c1-120">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b64c1-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b64c1-121">-Confirm</span></span>
<span data-ttu-id="b64c1-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b64c1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b64c1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b64c1-123">-WhatIf</span></span>
<span data-ttu-id="b64c1-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b64c1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b64c1-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b64c1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b64c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b64c1-126">CommonParameters</span></span>
<span data-ttu-id="b64c1-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b64c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b64c1-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b64c1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b64c1-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b64c1-129">INPUTS</span></span>

### <span data-ttu-id="b64c1-130">IStorageQuota （StorageAdmin）。 Api201908Preview。</span><span class="sxs-lookup"><span data-stu-id="b64c1-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="b64c1-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b64c1-131">OUTPUTS</span></span>

### <span data-ttu-id="b64c1-132">IStorageQuota （StorageAdmin）。 Api201908Preview。</span><span class="sxs-lookup"><span data-stu-id="b64c1-132">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="b64c1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b64c1-133">NOTES</span></span>

<span data-ttu-id="b64c1-134">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="b64c1-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b64c1-135">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b64c1-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b64c1-136">QUOTAOBJECT <IStorageQuota> ：</span><span class="sxs-lookup"><span data-stu-id="b64c1-136">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="b64c1-137">`[CapacityInGb <Int32?>]`： (GB) 最大的容量。</span><span class="sxs-lookup"><span data-stu-id="b64c1-137">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="b64c1-138">`[NumberOfStorageAccounts <Int32?>]`：儲存空間帳戶總數。</span><span class="sxs-lookup"><span data-stu-id="b64c1-138">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="b64c1-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b64c1-139">RELATED LINKS</span></span>

