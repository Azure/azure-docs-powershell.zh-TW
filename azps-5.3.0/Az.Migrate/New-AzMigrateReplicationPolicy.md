---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationPolicy.md
ms.openlocfilehash: 5978c247f14507934662f5a5d1846a02180cd812
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434937"
---
# <span data-ttu-id="a2fa0-101">New-AzMigrateReplicationPolicy</span><span class="sxs-lookup"><span data-stu-id="a2fa0-101">New-AzMigrateReplicationPolicy</span></span>

## <span data-ttu-id="a2fa0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="a2fa0-103">建立複製原則的操作</span><span class="sxs-lookup"><span data-stu-id="a2fa0-103">The operation to create a replication policy</span></span>

## <span data-ttu-id="a2fa0-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2fa0-104">SYNTAX</span></span>

```
New-AzMigrateReplicationPolicy -PolicyName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-ProviderSpecificInput <IPolicyProviderSpecificInput>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a2fa0-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2fa0-105">DESCRIPTION</span></span>
<span data-ttu-id="a2fa0-106">建立複製原則的操作</span><span class="sxs-lookup"><span data-stu-id="a2fa0-106">The operation to create a replication policy</span></span>

## <span data-ttu-id="a2fa0-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2fa0-107">EXAMPLES</span></span>

### <span data-ttu-id="a2fa0-108">範例1：建立複製原則</span><span class="sxs-lookup"><span data-stu-id="a2fa0-108">Example 1: Create a replication policy</span></span>
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

<span data-ttu-id="a2fa0-109">建立 VmWare Cbt 原則</span><span class="sxs-lookup"><span data-stu-id="a2fa0-109">Creates a policy for VmWare Cbt</span></span>

## <span data-ttu-id="a2fa0-110">參數</span><span class="sxs-lookup"><span data-stu-id="a2fa0-110">PARAMETERS</span></span>

### <span data-ttu-id="a2fa0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2fa0-111">-AsJob</span></span>
<span data-ttu-id="a2fa0-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="a2fa0-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a2fa0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2fa0-113">-DefaultProfile</span></span>
<span data-ttu-id="a2fa0-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2fa0-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a2fa0-115">-NoWait</span></span>
<span data-ttu-id="a2fa0-116">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="a2fa0-116">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a2fa0-117">-PolicyName</span><span class="sxs-lookup"><span data-stu-id="a2fa0-117">-PolicyName</span></span>
<span data-ttu-id="a2fa0-118">複製原則名稱</span><span class="sxs-lookup"><span data-stu-id="a2fa0-118">Replication policy name</span></span>

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

### <span data-ttu-id="a2fa0-119">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="a2fa0-119">-ProviderSpecificInput</span></span>
<span data-ttu-id="a2fa0-120">ReplicationProviderSettings。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-120">The ReplicationProviderSettings.</span></span>
<span data-ttu-id="a2fa0-121">若要建立，請參閱 PROVIDERSPECIFICINPUT 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-121">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a2fa0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2fa0-122">-ResourceGroupName</span></span>
<span data-ttu-id="a2fa0-123">[恢復服務] 電子倉庫所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="a2fa0-124">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="a2fa0-124">-ResourceName</span></span>
<span data-ttu-id="a2fa0-125">[恢復服務] 保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="a2fa0-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2fa0-126">-SubscriptionId</span></span>
<span data-ttu-id="a2fa0-127">訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-127">The subscription Id.</span></span>

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

### <span data-ttu-id="a2fa0-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a2fa0-128">-Confirm</span></span>
<span data-ttu-id="a2fa0-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2fa0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2fa0-130">-WhatIf</span></span>
<span data-ttu-id="a2fa0-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2fa0-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2fa0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2fa0-133">CommonParameters</span></span>
<span data-ttu-id="a2fa0-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2fa0-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2fa0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a2fa0-136">INPUTS</span></span>

## <span data-ttu-id="a2fa0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="a2fa0-137">OUTPUTS</span></span>

### <span data-ttu-id="a2fa0-138">IPolicy 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-138">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IPolicy</span></span>

## <span data-ttu-id="a2fa0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="a2fa0-139">NOTES</span></span>

<span data-ttu-id="a2fa0-140">別名</span><span class="sxs-lookup"><span data-stu-id="a2fa0-140">ALIASES</span></span>

<span data-ttu-id="a2fa0-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="a2fa0-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a2fa0-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a2fa0-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a2fa0-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput> ： ReplicationProviderSettings。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-144">PROVIDERSPECIFICINPUT <IPolicyProviderSpecificInput>: The ReplicationProviderSettings.</span></span>
  - <span data-ttu-id="a2fa0-145">`[InstanceType <String>]`：類別類型。</span><span class="sxs-lookup"><span data-stu-id="a2fa0-145">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="a2fa0-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2fa0-146">RELATED LINKS</span></span>

