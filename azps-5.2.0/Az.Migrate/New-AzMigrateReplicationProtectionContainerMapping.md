---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: b92d483689c94e6dd9f9af69e47f5b17ea1ab795
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281313"
---
# <span data-ttu-id="23526-101">New-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="23526-101">New-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="23526-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23526-102">SYNOPSIS</span></span>
<span data-ttu-id="23526-103">建立保護容器對應的操作。</span><span class="sxs-lookup"><span data-stu-id="23526-103">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="23526-104">句法</span><span class="sxs-lookup"><span data-stu-id="23526-104">SYNTAX</span></span>

```
New-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String>] [-PolicyId <String>]
 [-ProviderSpecificInput <IReplicationProviderSpecificContainerMappingInput>]
 [-TargetProtectionContainerId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="23526-105">說明</span><span class="sxs-lookup"><span data-stu-id="23526-105">DESCRIPTION</span></span>
<span data-ttu-id="23526-106">建立保護容器對應的操作。</span><span class="sxs-lookup"><span data-stu-id="23526-106">The operation to create a protection container mapping.</span></span>

## <span data-ttu-id="23526-107">示例</span><span class="sxs-lookup"><span data-stu-id="23526-107">EXAMPLES</span></span>

### <span data-ttu-id="23526-108">範例1：建立對應</span><span class="sxs-lookup"><span data-stu-id="23526-108">Example 1: Create a mapping</span></span>
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

<span data-ttu-id="23526-109">建立對應</span><span class="sxs-lookup"><span data-stu-id="23526-109">Create a mapping</span></span>

## <span data-ttu-id="23526-110">參數</span><span class="sxs-lookup"><span data-stu-id="23526-110">PARAMETERS</span></span>

### <span data-ttu-id="23526-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23526-111">-AsJob</span></span>
<span data-ttu-id="23526-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="23526-112">Run the command as a job</span></span>

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

### <span data-ttu-id="23526-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23526-113">-DefaultProfile</span></span>
<span data-ttu-id="23526-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="23526-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23526-115">-FabricName</span><span class="sxs-lookup"><span data-stu-id="23526-115">-FabricName</span></span>
<span data-ttu-id="23526-116">Fabric name。</span><span class="sxs-lookup"><span data-stu-id="23526-116">Fabric name.</span></span>

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

### <span data-ttu-id="23526-117">-MappingName</span><span class="sxs-lookup"><span data-stu-id="23526-117">-MappingName</span></span>
<span data-ttu-id="23526-118">保護容器對應名稱。</span><span class="sxs-lookup"><span data-stu-id="23526-118">Protection container mapping name.</span></span>

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

### <span data-ttu-id="23526-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="23526-119">-NoWait</span></span>
<span data-ttu-id="23526-120">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="23526-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="23526-121">-PolicyId</span><span class="sxs-lookup"><span data-stu-id="23526-121">-PolicyId</span></span>
<span data-ttu-id="23526-122">適用的原則。</span><span class="sxs-lookup"><span data-stu-id="23526-122">Applicable policy.</span></span>

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

### <span data-ttu-id="23526-123">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="23526-123">-ProtectionContainerName</span></span>
<span data-ttu-id="23526-124">保護容器名稱。</span><span class="sxs-lookup"><span data-stu-id="23526-124">Protection container name.</span></span>

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

### <span data-ttu-id="23526-125">-ProviderSpecificInput</span><span class="sxs-lookup"><span data-stu-id="23526-125">-ProviderSpecificInput</span></span>
<span data-ttu-id="23526-126">提供者針對配對的特定輸入。</span><span class="sxs-lookup"><span data-stu-id="23526-126">Provider specific input for pairing.</span></span>
<span data-ttu-id="23526-127">若要建立，請參閱 PROVIDERSPECIFICINPUT 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="23526-127">To construct, see NOTES section for PROVIDERSPECIFICINPUT properties and create a hash table.</span></span>

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

### <span data-ttu-id="23526-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23526-128">-ResourceGroupName</span></span>
<span data-ttu-id="23526-129">[恢復服務] 電子倉庫所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="23526-129">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="23526-130">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="23526-130">-ResourceName</span></span>
<span data-ttu-id="23526-131">[恢復服務] 保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="23526-131">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="23526-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23526-132">-SubscriptionId</span></span>
<span data-ttu-id="23526-133">訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="23526-133">The subscription Id.</span></span>

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

### <span data-ttu-id="23526-134">-TargetProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="23526-134">-TargetProtectionContainerId</span></span>
<span data-ttu-id="23526-135">目標唯一的保護容器名稱。</span><span class="sxs-lookup"><span data-stu-id="23526-135">The target unique protection container name.</span></span>

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

### <span data-ttu-id="23526-136">-確認</span><span class="sxs-lookup"><span data-stu-id="23526-136">-Confirm</span></span>
<span data-ttu-id="23526-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="23526-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23526-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23526-138">-WhatIf</span></span>
<span data-ttu-id="23526-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="23526-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23526-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23526-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23526-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23526-141">CommonParameters</span></span>
<span data-ttu-id="23526-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23526-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23526-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="23526-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23526-144">輸入</span><span class="sxs-lookup"><span data-stu-id="23526-144">INPUTS</span></span>

## <span data-ttu-id="23526-145">輸出</span><span class="sxs-lookup"><span data-stu-id="23526-145">OUTPUTS</span></span>

### <span data-ttu-id="23526-146">IProtectionContainerMapping 中的 Api20180110 （）。</span><span class="sxs-lookup"><span data-stu-id="23526-146">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="23526-147">筆記</span><span class="sxs-lookup"><span data-stu-id="23526-147">NOTES</span></span>

<span data-ttu-id="23526-148">別名</span><span class="sxs-lookup"><span data-stu-id="23526-148">ALIASES</span></span>

<span data-ttu-id="23526-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="23526-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="23526-150">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="23526-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="23526-151">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="23526-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="23526-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput> ：提供者針對配對的特定輸入。</span><span class="sxs-lookup"><span data-stu-id="23526-152">PROVIDERSPECIFICINPUT <IReplicationProviderSpecificContainerMappingInput>: Provider specific input for pairing.</span></span>
  - <span data-ttu-id="23526-153">`[InstanceType <String>]`：類別類型。</span><span class="sxs-lookup"><span data-stu-id="23526-153">`[InstanceType <String>]`: The class type.</span></span>

## <span data-ttu-id="23526-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="23526-154">RELATED LINKS</span></span>

