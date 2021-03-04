---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: ddbc4b9176405dd3102ba82cbe1954a876c9c7f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909017"
---
# <span data-ttu-id="55430-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="55430-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="55430-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55430-102">SYNOPSIS</span></span>
<span data-ttu-id="55430-103">建立保護容器映射的作業。</span><span class="sxs-lookup"><span data-stu-id="55430-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="55430-104">語法</span><span class="sxs-lookup"><span data-stu-id="55430-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="55430-105">描述</span><span class="sxs-lookup"><span data-stu-id="55430-105">DESCRIPTION</span></span>
<span data-ttu-id="55430-106">建立保護容器映射的作業。</span><span class="sxs-lookup"><span data-stu-id="55430-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="55430-107">例子</span><span class="sxs-lookup"><span data-stu-id="55430-107">EXAMPLES</span></span>

### <span data-ttu-id="55430-108">範例 1：建立地圖</span><span class="sxs-lookup"><span data-stu-id="55430-108">Example 1: Create a mapping</span></span>
```powershell
PS C:\> $providerSpecificInput = [Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.VMwareCbtContainerMappingInput]::new()
PS C:\> $providerSpecificInput.InstanceType = "VMwareCbt"
PS C:\> $providerSpecificInput.KeyVaultId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.KeyVault/vaults/migratekv846827101"
PS C:\> $providerSpecificInput.KeyVaultUri = "https://migratekv846827101.vault.azure.net"
PS C:\> $providerSpecificInput.ServiceBusConnectionStringSecretName = "ServiceBusConnectionString"
PS C:\> $providerSpecificInput.StorageAccountId = "/subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.Storage/storageAccounts/migrategwsa846827101"
PS C:\> $providerSpecificInput.StorageAccountSasSecretName = "migrategwsa846827101-gwySas"
PS C:\> $providerSpecificInput.TargetLocation = "centraluseuap"

PS C:\> New-AzMigrateReplicationProtectionContainerMapping -FabricName "AzMigratePWSHTc8d1replicationfabric" -MappingName "containermapping" -ProtectionContainerName "AzMigratePWSHTc8d1replicationcontainer" -ResourceGroupName "azmigratepwshtestasr13072020" -ResourceName "AzMigrateTestProjectPWSH02aarsvault"  -PolicyId "/subscriptionsxxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsoft.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationPolicies/migrateAzMigratePWSHTc8d1sitepolicy"  -ProviderSpecificInput $providerSpecificInput -TargetProtectionContainerId  "Microsoft Azure"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="55430-109">建立地圖</span><span class="sxs-lookup"><span data-stu-id="55430-109">Create a mapping</span></span>

## <span data-ttu-id="55430-110">參數</span><span class="sxs-lookup"><span data-stu-id="55430-110">PARAMETERS</span></span>

### <span data-ttu-id="55430-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="55430-111">-AsJob</span></span>
<span data-ttu-id="55430-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="55430-112">Run the command as a job</span></span>

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

### <span data-ttu-id="55430-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55430-113">-DefaultProfile</span></span>
<span data-ttu-id="55430-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="55430-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55430-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="55430-115">-FabricName</span></span>
<span data-ttu-id="55430-116">布料名稱。</span><span class="sxs-lookup"><span data-stu-id="55430-116">Fabric name.</span></span>

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

### <span data-ttu-id="55430-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="55430-117">-MappingName</span></span>
<span data-ttu-id="55430-118">保護容器的映射名稱。</span><span class="sxs-lookup"><span data-stu-id="55430-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="55430-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="55430-119">-NoWait</span></span>
<span data-ttu-id="55430-120">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="55430-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="55430-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="55430-121">-PolicyId</span></span>
<span data-ttu-id="55430-122">適用政策。</span><span class="sxs-lookup"><span data-stu-id="55430-122">Applicable policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55430-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="55430-123">-ProtectionContainerName</span></span>
<span data-ttu-id="55430-124">保護容器名稱。</span><span class="sxs-lookup"><span data-stu-id="55430-124">Protection container name.</span></span>

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

### <span data-ttu-id="55430-125">-ProviderS0ificInput</span><span class="sxs-lookup"><span data-stu-id="55430-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="55430-126">用於配對的提供者特定輸入。</span><span class="sxs-lookup"><span data-stu-id="55430-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="55430-127">若要建構，請參閱 PROVIDERSPECIFICINPUT 屬性的 NOTES 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="55430-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IReplicationProviderSpecificContainerMappingInput
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55430-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55430-128">-ResourceGroupName</span></span>
<span data-ttu-id="55430-129">復原服務庫存在之資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55430-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="55430-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="55430-130">-ResourceName</span></span>
<span data-ttu-id="55430-131">復原服務庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="55430-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="55430-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55430-132">-SubscriptionId</span></span>
<span data-ttu-id="55430-133">已建立專案之 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="55430-133">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="55430-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="55430-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="55430-135">目標唯一保護容器名稱。</span><span class="sxs-lookup"><span data-stu-id="55430-135">The target unique protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55430-136">-確認</span><span class="sxs-lookup"><span data-stu-id="55430-136">-Confirm</span></span>
<span data-ttu-id="55430-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="55430-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55430-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55430-138">-WhatIf</span></span>
<span data-ttu-id="55430-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55430-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55430-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55430-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55430-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55430-141">CommonParameters</span></span>
<span data-ttu-id="55430-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55430-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55430-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55430-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55430-144">輸入</span><span class="sxs-lookup"><span data-stu-id="55430-144">INPUTS</span></span>

## <span data-ttu-id="55430-145">輸出</span><span class="sxs-lookup"><span data-stu-id="55430-145">OUTPUTS</span></span>

### <span data-ttu-id="55430-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="55430-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="55430-147">筆記</span><span class="sxs-lookup"><span data-stu-id="55430-147">NOTES</span></span>

<span data-ttu-id="55430-148">別名</span><span class="sxs-lookup"><span data-stu-id="55430-148">ALIASES</span></span>

<span data-ttu-id="55430-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="55430-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="55430-150">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="55430-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="55430-151">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="55430-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="55430-152">PROVIDERSPECIFICINPUT： <IReplicationProviderSpecificContainerMappingInput> 用於配對的提供者特定輸入。</span><span class="sxs-lookup"><span data-stu-id="55430-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="55430-153">`[InstanceType <String>]`：班級類型。</span><span class="sxs-lookup"><span data-stu-id="55430-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="55430-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="55430-154">RELATED LINKS</span></span>

