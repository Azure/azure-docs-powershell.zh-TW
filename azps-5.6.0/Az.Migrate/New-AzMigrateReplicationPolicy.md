---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 7f9b78a6c287f7135f2463a6cfe63b2963ffe362
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909590"
---
# <span data-ttu-id="2906f-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="2906f-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="2906f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2906f-102">SYNOPSIS</span></span>
<span data-ttu-id="2906f-103">建立複寫原則的作業</span><span class="sxs-lookup"><span data-stu-id="2906f-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="2906f-104">語法</span><span class="sxs-lookup"><span data-stu-id="2906f-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2906f-105">描述</span><span class="sxs-lookup"><span data-stu-id="2906f-105">DESCRIPTION</span></span>
<span data-ttu-id="2906f-106">建立複寫原則的作業</span><span class="sxs-lookup"><span data-stu-id="2906f-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="2906f-107">例子</span><span class="sxs-lookup"><span data-stu-id="2906f-107">EXAMPLES</span></span>

### <span data-ttu-id="2906f-108">範例 1：建立複寫原則</span><span class="sxs-lookup"><span data-stu-id="2906f-108">Example 1: Create a replication policy</span></span>
```powershell
PS C:\> $providerSpecificPolicy = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtPolicyCreationInput]::new()
PS C:\> $providerSpecificPolicy.AppConsistentFrequencyInMinute = 240
PS C:\> $providerSpecificPolicy.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificPolicy.RecoveryPointHistoryInMinute = 4320
PS C:\> $providerSpecificPolicy.CrashConsistentFrequencyInMinute = 60
PS C:\> New-AzMigrateReplicationPolicy -PolicyName TestPolicy -ResourceGroupName ResourceGroup -ResourceName VaultName -SubscriptionId SubscriptionId -ProviderSpecificInput $providerSpecificPolicy

Location Name       Type
-------- ----       ----
         TestPolicy Microsoft.RecoveryServices/vaults/replicationPolicies
         
```

<span data-ttu-id="2906f-109">為 VmWare Cbt 建立一個策略</span><span class="sxs-lookup"><span data-stu-id="2906f-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="2906f-110">參數</span><span class="sxs-lookup"><span data-stu-id="2906f-110">PARAMETERS</span></span>

### <span data-ttu-id="2906f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2906f-111">-AsJob</span></span>
<span data-ttu-id="2906f-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="2906f-112">Run the command as a job</span></span>

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

### <span data-ttu-id="2906f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2906f-113">-DefaultProfile</span></span>
<span data-ttu-id="2906f-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2906f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2906f-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2906f-115">-NoWait</span></span>
<span data-ttu-id="2906f-116">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="2906f-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2906f-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="2906f-117">-PolicyName</span></span>
<span data-ttu-id="2906f-118">複寫原則名稱</span><span class="sxs-lookup"><span data-stu-id="2906f-118">Replication policy name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2906f-119">-ProviderS0ificInput</span><span class="sxs-lookup"><span data-stu-id="2906f-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="2906f-120">複製ProviderSettings。</span><span class="sxs-lookup"><span data-stu-id="2906f-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="2906f-121">若要建構，請參閱 PROVIDERSPECIFICINPUT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2906f-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicyProviderSpecificInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2906f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2906f-122">-ResourceGroupName</span></span>
<span data-ttu-id="2906f-123">復原服務庫存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2906f-123">The name of the resource group where the recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2906f-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2906f-124">-ResourceName</span></span>
<span data-ttu-id="2906f-125">復原服務庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="2906f-125">The name of the recovery services vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2906f-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2906f-126">-SubscriptionId</span></span>
<span data-ttu-id="2906f-127">已建立專案之 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="2906f-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="2906f-128">-確認</span><span class="sxs-lookup"><span data-stu-id="2906f-128">-Confirm</span></span>
<span data-ttu-id="2906f-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2906f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2906f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2906f-130">-WhatIf</span></span>
<span data-ttu-id="2906f-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2906f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2906f-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2906f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2906f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2906f-133">CommonParameters</span></span>
<span data-ttu-id="2906f-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2906f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2906f-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2906f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2906f-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2906f-136">INPUTS</span></span>

## <span data-ttu-id="2906f-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2906f-137">OUTPUTS</span></span>

### <span data-ttu-id="2906f-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span><span class="sxs-lookup"><span data-stu-id="2906f-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="2906f-139">筆記</span><span class="sxs-lookup"><span data-stu-id="2906f-139">NOTES</span></span>

<span data-ttu-id="2906f-140">別名</span><span class="sxs-lookup"><span data-stu-id="2906f-140">ALIASES</span></span>

<span data-ttu-id="2906f-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2906f-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2906f-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2906f-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2906f-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2906f-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2906f-144">PROVIDERSPROVIIFICINPUT： <IPolicyProviderSpecificInput> The ReplicationProviderSettings.</span><span class="sxs-lookup"><span data-stu-id="2906f-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="2906f-145">`[InstanceType <String>]`：班級類型。</span><span class="sxs-lookup"><span data-stu-id="2906f-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="2906f-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="2906f-146">RELATED LINKS</span></span>

