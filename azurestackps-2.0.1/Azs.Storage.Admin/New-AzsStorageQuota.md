---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/new-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: bd97eff2a0ed37c309ad0b50927f8231a2da27a6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966611"
---
# <span data-ttu-id="3383d-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="3383d-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="3383d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3383d-102">SYNOPSIS</span></span>


## <span data-ttu-id="3383d-103">句法</span><span class="sxs-lookup"><span data-stu-id="3383d-103">SYNTAX</span></span>

### <span data-ttu-id="3383d-104">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="3383d-104">CreateExpanded (Default)</span></span>
```
New-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String>] [-CapacityInGb <Int32>]
 [-NumberOfStorageAccounts <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3383d-105">建立</span><span class="sxs-lookup"><span data-stu-id="3383d-105">Create</span></span>
```
New-AzsStorageQuota -Name <String> -QuotaObject <IStorageQuota> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3383d-106">說明</span><span class="sxs-lookup"><span data-stu-id="3383d-106">DESCRIPTION</span></span>


## <span data-ttu-id="3383d-107">示例</span><span class="sxs-lookup"><span data-stu-id="3383d-107">EXAMPLES</span></span>

### <span data-ttu-id="3383d-108">範例1：</span><span class="sxs-lookup"><span data-stu-id="3383d-108">Example 1:</span></span>
```powershell
PS C:\> New-AzsStorageQuota -Name TestQuota -CapacityInGb 123 -NumberOfStorageAccounts 456
```

<span data-ttu-id="3383d-109">使用指定的值建立新的儲存配額。</span><span class="sxs-lookup"><span data-stu-id="3383d-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="3383d-110">參數</span><span class="sxs-lookup"><span data-stu-id="3383d-110">PARAMETERS</span></span>

### <span data-ttu-id="3383d-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="3383d-111">-CapacityInGb</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3383d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3383d-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="3383d-113">-位置</span><span class="sxs-lookup"><span data-stu-id="3383d-113">-Location</span></span>


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

### <span data-ttu-id="3383d-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="3383d-114">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3383d-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3383d-115">-NumberOfStorageAccounts</span></span>


```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3383d-116">-QuotaObject</span><span class="sxs-lookup"><span data-stu-id="3383d-116">-QuotaObject</span></span>
<span data-ttu-id="3383d-117">若要建立，請參閱 QUOTAOBJECT 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="3383d-117">To construct, see NOTES section for QUOTAOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3383d-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3383d-118">-SubscriptionId</span></span>


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

### <span data-ttu-id="3383d-119">-確認</span><span class="sxs-lookup"><span data-stu-id="3383d-119">-Confirm</span></span>
<span data-ttu-id="3383d-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3383d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3383d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3383d-121">-WhatIf</span></span>
<span data-ttu-id="3383d-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3383d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3383d-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3383d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3383d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3383d-124">CommonParameters</span></span>
<span data-ttu-id="3383d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3383d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3383d-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3383d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3383d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3383d-127">INPUTS</span></span>

### <span data-ttu-id="3383d-128">IStorageQuota （StorageAdmin）。 Api201908Preview。</span><span class="sxs-lookup"><span data-stu-id="3383d-128">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>

## <span data-ttu-id="3383d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="3383d-129">OUTPUTS</span></span>

### <span data-ttu-id="3383d-130">IStorageQuota （StorageAdmin）。 Api201908Preview。</span><span class="sxs-lookup"><span data-stu-id="3383d-130">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.IStorageQuota</span></span>



## <span data-ttu-id="3383d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="3383d-131">NOTES</span></span>

<span data-ttu-id="3383d-132">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3383d-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3383d-133">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3383d-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3383d-134">QUOTAOBJECT <IStorageQuota> ：</span><span class="sxs-lookup"><span data-stu-id="3383d-134">QUOTAOBJECT <IStorageQuota>:</span></span> 
  - <span data-ttu-id="3383d-135">`[CapacityInGb <Int32?>]`： (GB) 最大的容量。</span><span class="sxs-lookup"><span data-stu-id="3383d-135">`[CapacityInGb <Int32?>]`: Maximum capacity (GB).</span></span>
  - <span data-ttu-id="3383d-136">`[NumberOfStorageAccounts <Int32?>]`：儲存空間帳戶總數。</span><span class="sxs-lookup"><span data-stu-id="3383d-136">`[NumberOfStorageAccounts <Int32?>]`: Total number of storage accounts.</span></span>

## <span data-ttu-id="3383d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3383d-137">RELATED LINKS</span></span>

