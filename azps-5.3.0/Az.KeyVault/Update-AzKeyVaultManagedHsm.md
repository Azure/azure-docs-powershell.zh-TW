---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8a4c55f8b823a72224dc658a3ddc37ee867d781b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438147"
---
# <span data-ttu-id="21a21-101">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="21a21-101">Update-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="21a21-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21a21-102">SYNOPSIS</span></span>
<span data-ttu-id="21a21-103">更新 Azure managed HSM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="21a21-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="21a21-104">句法</span><span class="sxs-lookup"><span data-stu-id="21a21-104">SYNTAX</span></span>

### <span data-ttu-id="21a21-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="21a21-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVaultManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a21-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21a21-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21a21-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21a21-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVaultManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21a21-108">說明</span><span class="sxs-lookup"><span data-stu-id="21a21-108">DESCRIPTION</span></span>
<span data-ttu-id="21a21-109">這個 Cmdlet 會更新 Azure managed HSM 的狀態。</span><span class="sxs-lookup"><span data-stu-id="21a21-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="21a21-110">示例</span><span class="sxs-lookup"><span data-stu-id="21a21-110">EXAMPLES</span></span>

### <span data-ttu-id="21a21-111">範例1：直接更新受管理的 Hsm</span><span class="sxs-lookup"><span data-stu-id="21a21-111">Example 1: Update a managed Hsm directly</span></span>
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

<span data-ttu-id="21a21-112">更新「資源群組」中指定的受管理 Hsm 的標籤 `$hsmName` `$resourceGroupName` 。</span><span class="sxs-lookup"><span data-stu-id="21a21-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="21a21-113">範例2：使用管道更新受管理的 Hsm</span><span class="sxs-lookup"><span data-stu-id="21a21-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzKeyVaultManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="21a21-114">使用管道語法更新受管理的 Hsm 的標記。</span><span class="sxs-lookup"><span data-stu-id="21a21-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="21a21-115">參數</span><span class="sxs-lookup"><span data-stu-id="21a21-115">PARAMETERS</span></span>

### <span data-ttu-id="21a21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21a21-116">-DefaultProfile</span></span>
<span data-ttu-id="21a21-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21a21-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21a21-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21a21-118">-InputObject</span></span>
<span data-ttu-id="21a21-119">受管理的 HSM 物件。</span><span class="sxs-lookup"><span data-stu-id="21a21-119">Managed HSM object.</span></span>

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

### <span data-ttu-id="21a21-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="21a21-120">-Name</span></span>
<span data-ttu-id="21a21-121">受管理的 HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="21a21-121">Name of the managed HSM.</span></span>

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

### <span data-ttu-id="21a21-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21a21-122">-ResourceGroupName</span></span>
<span data-ttu-id="21a21-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="21a21-123">Name of the resource group.</span></span>

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

### <span data-ttu-id="21a21-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21a21-124">-ResourceId</span></span>
<span data-ttu-id="21a21-125">受管理的 HSM 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="21a21-125">Resource ID of the managed HSM.</span></span>

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

### <span data-ttu-id="21a21-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="21a21-126">-Tag</span></span>
<span data-ttu-id="21a21-127">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="21a21-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="21a21-128">-確認</span><span class="sxs-lookup"><span data-stu-id="21a21-128">-Confirm</span></span>
<span data-ttu-id="21a21-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21a21-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21a21-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21a21-130">-WhatIf</span></span>
<span data-ttu-id="21a21-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21a21-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21a21-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21a21-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21a21-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21a21-133">CommonParameters</span></span>
<span data-ttu-id="21a21-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21a21-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21a21-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="21a21-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21a21-136">輸入</span><span class="sxs-lookup"><span data-stu-id="21a21-136">INPUTS</span></span>

### <span data-ttu-id="21a21-137">PSManagedHsm 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="21a21-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="21a21-138">System.object</span><span class="sxs-lookup"><span data-stu-id="21a21-138">System.String</span></span>

### <span data-ttu-id="21a21-139">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="21a21-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="21a21-140">輸出</span><span class="sxs-lookup"><span data-stu-id="21a21-140">OUTPUTS</span></span>

### <span data-ttu-id="21a21-141">PSManagedHsm 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="21a21-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="21a21-142">筆記</span><span class="sxs-lookup"><span data-stu-id="21a21-142">NOTES</span></span>

## <span data-ttu-id="21a21-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="21a21-143">RELATED LINKS</span></span>

[<span data-ttu-id="21a21-144">新-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="21a21-144">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="21a21-145">移除-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="21a21-145">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="21a21-146">AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="21a21-146">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)