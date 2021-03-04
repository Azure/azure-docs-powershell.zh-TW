---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: ac778148f90d90caf52fdb3c029376daf4470069
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911942"
---
# <span data-ttu-id="a2c13-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a2c13-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="a2c13-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2c13-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c13-103">刪除受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="a2c13-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="a2c13-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2c13-104">SYNTAX</span></span>

### <span data-ttu-id="a2c13-105">RemoveManaged4mByName (預設) </span><span class="sxs-lookup"><span data-stu-id="a2c13-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c13-106">RemoveManaged1mByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2c13-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c13-107">RemoveManagedManagedManmByResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c13-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c13-108">描述</span><span class="sxs-lookup"><span data-stu-id="a2c13-108">DESCRIPTION</span></span>
<span data-ttu-id="a2c13-109">**Remove-AzKeyVaultManagedPvm** Cmdlet 會刪除指定的 Managed HSM。</span><span class="sxs-lookup"><span data-stu-id="a2c13-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="a2c13-110">它也會刪除該實例中包含的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2c13-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="a2c13-111">請注意，雖然指定資源群組是這個 Cmdlet 的選擇性專案，但為了提升績效，您應該這麼做。</span><span class="sxs-lookup"><span data-stu-id="a2c13-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="a2c13-112">例子</span><span class="sxs-lookup"><span data-stu-id="a2c13-112">EXAMPLES</span></span>

### <span data-ttu-id="a2c13-113">範例 1：移除受管理的 HSM</span><span class="sxs-lookup"><span data-stu-id="a2c13-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="a2c13-114">此命令會從您目前的訂閱移除名為 mym 的受管理 hsm。</span><span class="sxs-lookup"><span data-stu-id="a2c13-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="a2c13-115">範例 2：從指定的資源群組移除受管理的 hsm</span><span class="sxs-lookup"><span data-stu-id="a2c13-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="a2c13-116">此命令會從名為 myrg1 的資源群組移除名為 mym 的受管理 hsm。</span><span class="sxs-lookup"><span data-stu-id="a2c13-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="a2c13-117">如果您未指定資源組名，Cmdlet 會搜尋您目前訂閱中要刪除的受管理 HSM。</span><span class="sxs-lookup"><span data-stu-id="a2c13-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="a2c13-118">參數</span><span class="sxs-lookup"><span data-stu-id="a2c13-118">PARAMETERS</span></span>

### <span data-ttu-id="a2c13-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2c13-119">-AsJob</span></span>
<span data-ttu-id="a2c13-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a2c13-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2c13-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c13-121">-DefaultProfile</span></span>
<span data-ttu-id="a2c13-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2c13-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2c13-123">-強制</span><span class="sxs-lookup"><span data-stu-id="a2c13-123">-Force</span></span>
<span data-ttu-id="a2c13-124">表示 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a2c13-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="a2c13-125">根據預設，此 Cmdlet 會提示您確認要刪除受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="a2c13-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="a2c13-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2c13-126">-InputObject</span></span>
<span data-ttu-id="a2c13-127">要刪除的受管理 HSM 物件。</span><span class="sxs-lookup"><span data-stu-id="a2c13-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c13-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2c13-128">-Name</span></span>
<span data-ttu-id="a2c13-129">指定要移除的受管理 HSM 名稱。</span><span class="sxs-lookup"><span data-stu-id="a2c13-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c13-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2c13-130">-PassThru</span></span>
<span data-ttu-id="a2c13-131">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="a2c13-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a2c13-132">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="a2c13-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a2c13-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c13-133">-ResourceGroupName</span></span>
<span data-ttu-id="a2c13-134">指定要移除 Azure Managed HSM 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a2c13-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c13-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c13-135">-ResourceId</span></span>
<span data-ttu-id="a2c13-136">Managed安全資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2c13-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c13-137">-確認</span><span class="sxs-lookup"><span data-stu-id="a2c13-137">-Confirm</span></span>
<span data-ttu-id="a2c13-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a2c13-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2c13-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c13-139">-WhatIf</span></span>
<span data-ttu-id="a2c13-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2c13-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2c13-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2c13-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2c13-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c13-142">CommonParameters</span></span>
<span data-ttu-id="a2c13-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2c13-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c13-144">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2c13-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c13-145">輸入</span><span class="sxs-lookup"><span data-stu-id="a2c13-145">INPUTS</span></span>

### <span data-ttu-id="a2c13-146">Microsoft.Azure.Commands.KeyVault.models.PSManagedPvm</span><span class="sxs-lookup"><span data-stu-id="a2c13-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="a2c13-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a2c13-147">System.String</span></span>

## <span data-ttu-id="a2c13-148">輸出</span><span class="sxs-lookup"><span data-stu-id="a2c13-148">OUTPUTS</span></span>

### <span data-ttu-id="a2c13-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2c13-149">System.Boolean</span></span>

## <span data-ttu-id="a2c13-150">筆記</span><span class="sxs-lookup"><span data-stu-id="a2c13-150">NOTES</span></span>

## <span data-ttu-id="a2c13-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2c13-151">RELATED LINKS</span></span>

[<span data-ttu-id="a2c13-152">Get-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="a2c13-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="a2c13-153">New-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="a2c13-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="a2c13-154">Update-AzKeyVaultManagedPvm</span><span class="sxs-lookup"><span data-stu-id="a2c13-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)