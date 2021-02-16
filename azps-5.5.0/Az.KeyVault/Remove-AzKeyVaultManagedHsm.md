---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 82521bd7d0ff4f34f68029cdb7faacdd198f2b02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139007"
---
# <span data-ttu-id="58088-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="58088-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="58088-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58088-102">SYNOPSIS</span></span>
<span data-ttu-id="58088-103">刪除受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="58088-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="58088-104">句法</span><span class="sxs-lookup"><span data-stu-id="58088-104">SYNTAX</span></span>

### <span data-ttu-id="58088-105">RemoveManagedHsmByName (預設) </span><span class="sxs-lookup"><span data-stu-id="58088-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58088-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="58088-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58088-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="58088-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58088-108">說明</span><span class="sxs-lookup"><span data-stu-id="58088-108">DESCRIPTION</span></span>
<span data-ttu-id="58088-109">**AzKeyVaultManagedHsm** Cmdlet 會刪除指定的受管理 HSM。</span><span class="sxs-lookup"><span data-stu-id="58088-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="58088-110">它也會刪除該實例中包含的所有金鑰。</span><span class="sxs-lookup"><span data-stu-id="58088-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="58088-111">請注意，雖然為這個 Cmdlet 指定 [資源群組] 是選擇性的，但您應該如此以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="58088-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="58088-112">示例</span><span class="sxs-lookup"><span data-stu-id="58088-112">EXAMPLES</span></span>

### <span data-ttu-id="58088-113">範例1：移除受管理的 HSM</span><span class="sxs-lookup"><span data-stu-id="58088-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="58088-114">這個命令會從您目前的訂閱中移除名為 myhsm 的受管理 hsm。</span><span class="sxs-lookup"><span data-stu-id="58088-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="58088-115">範例2：從指定的資源群組中移除受管理的 hsm</span><span class="sxs-lookup"><span data-stu-id="58088-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="58088-116">這個命令會從名為 myrg1 的資源群組中，移除名為 myhsm 的受管理 hsm。</span><span class="sxs-lookup"><span data-stu-id="58088-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="58088-117">如果您沒有指定資源組名稱，此 Cmdlet 會在您目前的訂閱中搜尋已命名的 managed HSM 以刪除。</span><span class="sxs-lookup"><span data-stu-id="58088-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="58088-118">參數</span><span class="sxs-lookup"><span data-stu-id="58088-118">PARAMETERS</span></span>

### <span data-ttu-id="58088-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58088-119">-AsJob</span></span>
<span data-ttu-id="58088-120">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="58088-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58088-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58088-121">-DefaultProfile</span></span>
<span data-ttu-id="58088-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="58088-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58088-123">-Force</span><span class="sxs-lookup"><span data-stu-id="58088-123">-Force</span></span>
<span data-ttu-id="58088-124">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58088-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="58088-125">根據預設，這個 Cmdlet 會提示您確認是否要刪除受管理的 HSM。</span><span class="sxs-lookup"><span data-stu-id="58088-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="58088-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58088-126">-InputObject</span></span>
<span data-ttu-id="58088-127">要刪除的 Managed HSM 物件。</span><span class="sxs-lookup"><span data-stu-id="58088-127">Managed HSM object to be deleted.</span></span>

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

### <span data-ttu-id="58088-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="58088-128">-Name</span></span>
<span data-ttu-id="58088-129">指定要移除之 managed HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="58088-129">Specifies the name of the managed HSM to remove.</span></span>

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

### <span data-ttu-id="58088-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58088-130">-PassThru</span></span>
<span data-ttu-id="58088-131">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="58088-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="58088-132">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="58088-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="58088-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58088-133">-ResourceGroupName</span></span>
<span data-ttu-id="58088-134">指定要移除之 Azure managed HSM 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="58088-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

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

### <span data-ttu-id="58088-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58088-135">-ResourceId</span></span>
<span data-ttu-id="58088-136">ManagedHsm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="58088-136">ManagedHsm Resource Id.</span></span>

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

### <span data-ttu-id="58088-137">-確認</span><span class="sxs-lookup"><span data-stu-id="58088-137">-Confirm</span></span>
<span data-ttu-id="58088-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="58088-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58088-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58088-139">-WhatIf</span></span>
<span data-ttu-id="58088-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="58088-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58088-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="58088-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58088-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58088-142">CommonParameters</span></span>
<span data-ttu-id="58088-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58088-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58088-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="58088-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58088-145">輸入</span><span class="sxs-lookup"><span data-stu-id="58088-145">INPUTS</span></span>

### <span data-ttu-id="58088-146">PSManagedHsm 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="58088-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="58088-147">System.object</span><span class="sxs-lookup"><span data-stu-id="58088-147">System.String</span></span>

## <span data-ttu-id="58088-148">輸出</span><span class="sxs-lookup"><span data-stu-id="58088-148">OUTPUTS</span></span>

### <span data-ttu-id="58088-149">System.object</span><span class="sxs-lookup"><span data-stu-id="58088-149">System.Boolean</span></span>

## <span data-ttu-id="58088-150">筆記</span><span class="sxs-lookup"><span data-stu-id="58088-150">NOTES</span></span>

## <span data-ttu-id="58088-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="58088-151">RELATED LINKS</span></span>

[<span data-ttu-id="58088-152">AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="58088-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="58088-153">新-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="58088-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="58088-154">更新-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="58088-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)