---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 6f4ddcb358c2ebc0789bb96508feacb69449d17d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908161"
---
# <span data-ttu-id="4869b-101">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4869b-101">Update-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="4869b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4869b-102">SYNOPSIS</span></span>
<span data-ttu-id="4869b-103">更新 Azure Managed HSM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="4869b-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="4869b-104">語法</span><span class="sxs-lookup"><span data-stu-id="4869b-104">SYNTAX</span></span>

### <span data-ttu-id="4869b-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4869b-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVaultManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4869b-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4869b-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4869b-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4869b-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4869b-108">描述</span><span class="sxs-lookup"><span data-stu-id="4869b-108">DESCRIPTION</span></span>
<span data-ttu-id="4869b-109">此 Cmdlet 會更新 Azure Managed HSM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="4869b-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="4869b-110">例子</span><span class="sxs-lookup"><span data-stu-id="4869b-110">EXAMPLES</span></span>

### <span data-ttu-id="4869b-111">範例 1：直接更新受管理的 Hsm</span><span class="sxs-lookup"><span data-stu-id="4869b-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

Managed HSM Name                    : testmhsm
Resource Group Name                 : testmhsm
Location                            : eastus2euap
Resource ID                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testmhsm/provid
                                      ers/Microsoft.KeyVault/managedHSMs/testmhsm
HSM Pool URI                        :
Tenant ID                           : xxxxxx-xxxx-xxxx-xxxxxxxxxxxx
Initial Admin Object Ids            : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SKU                                 : StandardB1
Soft Delete Enabled?                : True
Enabled Purge Protection?           : False
Soft Delete Retention Period (days) : 90
Provisioning State                  : Provisioning
Status Message                      : Resource creation in progress. Starting service...
Tags                                :
                                      Name        Value
                                      ====        =====
                                      testKey     testValued
```

<span data-ttu-id="4869b-112">更新資源群組中命名之受管理 Hsm `$hsmName` 的標記 `$resourceGroupName` 。</span><span class="sxs-lookup"><span data-stu-id="4869b-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="4869b-113">範例 2：使用管線更新 Managed Hsm</span><span class="sxs-lookup"><span data-stu-id="4869b-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzKeyVaultManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="4869b-114">使用管道語法更新受管理 Hsm 的標記。</span><span class="sxs-lookup"><span data-stu-id="4869b-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="4869b-115">參數</span><span class="sxs-lookup"><span data-stu-id="4869b-115">PARAMETERS</span></span>

### <span data-ttu-id="4869b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4869b-116">-DefaultProfile</span></span>
<span data-ttu-id="4869b-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4869b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4869b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4869b-118">-InputObject</span></span>
<span data-ttu-id="4869b-119">Managed HSM 物件。</span><span class="sxs-lookup"><span data-stu-id="4869b-119">Managed HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4869b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4869b-120">-Name</span></span>
<span data-ttu-id="4869b-121">受管理 HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4869b-121">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4869b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4869b-122">-ResourceGroupName</span></span>
<span data-ttu-id="4869b-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4869b-123">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4869b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4869b-124">-ResourceId</span></span>
<span data-ttu-id="4869b-125">受管理 HSM 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4869b-125">Resource ID of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4869b-126">-標記</span><span class="sxs-lookup"><span data-stu-id="4869b-126">-Tag</span></span>
<span data-ttu-id="4869b-127">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4869b-127">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4869b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="4869b-128">-Confirm</span></span>
<span data-ttu-id="4869b-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4869b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4869b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4869b-130">-WhatIf</span></span>
<span data-ttu-id="4869b-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4869b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4869b-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4869b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4869b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4869b-133">CommonParameters</span></span>
<span data-ttu-id="4869b-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4869b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4869b-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4869b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4869b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4869b-136">INPUTS</span></span>

### <span data-ttu-id="4869b-137">Microsoft.Azure.Commands.KeyVault.models.PSManagedPvm</span><span class="sxs-lookup"><span data-stu-id="4869b-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="4869b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4869b-138">System.String</span></span>

### <span data-ttu-id="4869b-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4869b-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4869b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="4869b-140">OUTPUTS</span></span>

### <span data-ttu-id="4869b-141">Microsoft.Azure.Commands.KeyVault.models.PSManagedPvm</span><span class="sxs-lookup"><span data-stu-id="4869b-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="4869b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="4869b-142">NOTES</span></span>

## <span data-ttu-id="4869b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="4869b-143">RELATED LINKS</span></span>

[<span data-ttu-id="4869b-144">New-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="4869b-144">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="4869b-145">Remove-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="4869b-145">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="4869b-146">Get-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="4869b-146">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)