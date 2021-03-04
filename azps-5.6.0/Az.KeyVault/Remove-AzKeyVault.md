---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 04b4f6be3393eae0fba2f98c477b4174612d2b79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914770"
---
# <span data-ttu-id="a2c36-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a2c36-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="a2c36-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2c36-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c36-103">刪除金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="a2c36-103">Deletes a key vault.</span></span>

## <span data-ttu-id="a2c36-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2c36-104">SYNTAX</span></span>

### <span data-ttu-id="a2c36-105">ByAvailableVault (預設) </span><span class="sxs-lookup"><span data-stu-id="a2c36-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c36-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="a2c36-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c36-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="a2c36-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c36-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="a2c36-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c36-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="a2c36-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2c36-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="a2c36-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c36-111">描述</span><span class="sxs-lookup"><span data-stu-id="a2c36-111">DESCRIPTION</span></span>
<span data-ttu-id="a2c36-112">**Remove-AzKeyVault** Cmdlet 會刪除指定的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="a2c36-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="a2c36-113">它也會刪除該實例中所包含的所有金鑰和機密。</span><span class="sxs-lookup"><span data-stu-id="a2c36-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="a2c36-114">請注意，雖然指定資源群組是這個 Cmdlet 的選擇性專案，但為了提升績效，您應該這麼做。</span><span class="sxs-lookup"><span data-stu-id="a2c36-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="a2c36-115">例子</span><span class="sxs-lookup"><span data-stu-id="a2c36-115">EXAMPLES</span></span>

### <span data-ttu-id="a2c36-116">範例 1：移除金鑰庫</span><span class="sxs-lookup"><span data-stu-id="a2c36-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="a2c36-117">此命令會從您目前的訂閱移除名為 Contoso03Vault 的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="a2c36-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="a2c36-118">範例 2：從指定的資源群組移除金鑰庫</span><span class="sxs-lookup"><span data-stu-id="a2c36-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="a2c36-119">此命令會從命名的資源群組移除名為 Contoso03Vault 的金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="a2c36-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="a2c36-120">如果您未指定資源組名，Cmdlet 會搜尋命名的金鑰保存庫，以在目前的訂閱中刪除。</span><span class="sxs-lookup"><span data-stu-id="a2c36-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="a2c36-121">範例 3：移除受管理的 hsm</span><span class="sxs-lookup"><span data-stu-id="a2c36-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="a2c36-122">此命令會從您目前的訂閱移除名為 testManaged除法的受管理 hsm。</span><span class="sxs-lookup"><span data-stu-id="a2c36-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="a2c36-123">參數</span><span class="sxs-lookup"><span data-stu-id="a2c36-123">PARAMETERS</span></span>

### <span data-ttu-id="a2c36-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2c36-124">-AsJob</span></span>
<span data-ttu-id="a2c36-125">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a2c36-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2c36-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c36-126">-DefaultProfile</span></span>
<span data-ttu-id="a2c36-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a2c36-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2c36-128">-強制</span><span class="sxs-lookup"><span data-stu-id="a2c36-128">-Force</span></span>
<span data-ttu-id="a2c36-129">表示 Cmdlet 不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a2c36-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="a2c36-130">根據預設，此 Cmdlet 會提示您確認要刪除金鑰庫。</span><span class="sxs-lookup"><span data-stu-id="a2c36-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="a2c36-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2c36-131">-InputObject</span></span>
<span data-ttu-id="a2c36-132">要刪除的 Key Vault 物件。</span><span class="sxs-lookup"><span data-stu-id="a2c36-132">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c36-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a2c36-133">-InRemovedState</span></span>
<span data-ttu-id="a2c36-134">永久移除先前刪除的保存庫。</span><span class="sxs-lookup"><span data-stu-id="a2c36-134">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c36-135">-位置</span><span class="sxs-lookup"><span data-stu-id="a2c36-135">-Location</span></span>
<span data-ttu-id="a2c36-136">已刪除的儲存庫位置。</span><span class="sxs-lookup"><span data-stu-id="a2c36-136">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c36-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2c36-137">-PassThru</span></span>
<span data-ttu-id="a2c36-138">此 Cmdlet 預設不會返回物件。</span><span class="sxs-lookup"><span data-stu-id="a2c36-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="a2c36-139">如果指定此參數，則成功時會返回 True。</span><span class="sxs-lookup"><span data-stu-id="a2c36-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a2c36-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c36-140">-ResourceGroupName</span></span>
<span data-ttu-id="a2c36-141">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2c36-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c36-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2c36-142">-ResourceId</span></span>
<span data-ttu-id="a2c36-143">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a2c36-143">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2c36-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a2c36-144">-VaultName</span></span>
<span data-ttu-id="a2c36-145">指定要移除的金鑰庫名稱。</span><span class="sxs-lookup"><span data-stu-id="a2c36-145">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c36-146">-確認</span><span class="sxs-lookup"><span data-stu-id="a2c36-146">-Confirm</span></span>
<span data-ttu-id="a2c36-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a2c36-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c36-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c36-148">-WhatIf</span></span>
<span data-ttu-id="a2c36-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2c36-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2c36-150">不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2c36-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2c36-151">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2c36-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2c36-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c36-152">CommonParameters</span></span>
<span data-ttu-id="a2c36-153">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2c36-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c36-154">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a2c36-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c36-155">輸入</span><span class="sxs-lookup"><span data-stu-id="a2c36-155">INPUTS</span></span>

### <span data-ttu-id="a2c36-156">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a2c36-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a2c36-157">System.String</span><span class="sxs-lookup"><span data-stu-id="a2c36-157">System.String</span></span>

## <span data-ttu-id="a2c36-158">輸出</span><span class="sxs-lookup"><span data-stu-id="a2c36-158">OUTPUTS</span></span>

### <span data-ttu-id="a2c36-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a2c36-159">System.Boolean</span></span>

## <span data-ttu-id="a2c36-160">筆記</span><span class="sxs-lookup"><span data-stu-id="a2c36-160">NOTES</span></span>

## <span data-ttu-id="a2c36-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2c36-161">RELATED LINKS</span></span>

[<span data-ttu-id="a2c36-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a2c36-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="a2c36-163">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a2c36-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
