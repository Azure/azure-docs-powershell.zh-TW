---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 32060f2d9d468669f963f653f335729ca6c25761
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966326"
---
# <span data-ttu-id="c7111-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="c7111-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="c7111-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7111-102">SYNOPSIS</span></span>
<span data-ttu-id="c7111-103">刪除金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="c7111-103">Deletes a key vault.</span></span>

## <span data-ttu-id="c7111-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7111-104">SYNTAX</span></span>

### <span data-ttu-id="c7111-105">ByAvailableVault (預設) </span><span class="sxs-lookup"><span data-stu-id="c7111-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7111-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="c7111-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7111-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="c7111-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7111-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="c7111-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7111-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="c7111-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7111-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="c7111-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7111-111">說明</span><span class="sxs-lookup"><span data-stu-id="c7111-111">DESCRIPTION</span></span>
<span data-ttu-id="c7111-112">**AzKeyVault** Cmdlet 會刪除指定的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="c7111-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="c7111-113">它也會刪除該實例中所包含的所有金鑰與密碼。</span><span class="sxs-lookup"><span data-stu-id="c7111-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="c7111-114">請注意，雖然為這個 Cmdlet 指定 [資源群組] 是選擇性的，但您應該如此以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="c7111-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="c7111-115">示例</span><span class="sxs-lookup"><span data-stu-id="c7111-115">EXAMPLES</span></span>

### <span data-ttu-id="c7111-116">範例1：移除金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="c7111-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="c7111-117">這個命令會從您目前的訂閱中移除名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="c7111-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="c7111-118">範例2：從指定的資源群組中移除主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="c7111-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="c7111-119">這個命令會從命名的資源群組中移除名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="c7111-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="c7111-120">如果您沒有指定資源組名稱，此 Cmdlet 會在您目前的訂閱中搜尋已命名的金鑰保存庫以刪除。</span><span class="sxs-lookup"><span data-stu-id="c7111-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="c7111-121">參數</span><span class="sxs-lookup"><span data-stu-id="c7111-121">PARAMETERS</span></span>

### <span data-ttu-id="c7111-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7111-122">-AsJob</span></span>
<span data-ttu-id="c7111-123">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="c7111-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7111-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7111-124">-DefaultProfile</span></span>
<span data-ttu-id="c7111-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c7111-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7111-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c7111-126">-Force</span></span>
<span data-ttu-id="c7111-127">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7111-127">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="c7111-128">根據預設，這個 Cmdlet 會提示您確認要刪除金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="c7111-128">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="c7111-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7111-129">-InputObject</span></span>
<span data-ttu-id="c7111-130">要刪除的主要保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="c7111-130">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="c7111-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c7111-131">-InRemovedState</span></span>
<span data-ttu-id="c7111-132">永久移除先前刪除的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="c7111-132">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="c7111-133">-位置</span><span class="sxs-lookup"><span data-stu-id="c7111-133">-Location</span></span>
<span data-ttu-id="c7111-134">已刪除的電子倉庫的位置。</span><span class="sxs-lookup"><span data-stu-id="c7111-134">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="c7111-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7111-135">-PassThru</span></span>
<span data-ttu-id="c7111-136">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="c7111-136">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="c7111-137">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="c7111-137">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c7111-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7111-138">-ResourceGroupName</span></span>
<span data-ttu-id="c7111-139">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7111-139">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c7111-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7111-140">-ResourceId</span></span>
<span data-ttu-id="c7111-141">KeyVault 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c7111-141">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="c7111-142">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c7111-142">-VaultName</span></span>
<span data-ttu-id="c7111-143">指定要移除之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7111-143">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="c7111-144">-確認</span><span class="sxs-lookup"><span data-stu-id="c7111-144">-Confirm</span></span>
<span data-ttu-id="c7111-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7111-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7111-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7111-146">-WhatIf</span></span>
<span data-ttu-id="c7111-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7111-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7111-148">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7111-148">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7111-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7111-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7111-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7111-150">CommonParameters</span></span>
<span data-ttu-id="c7111-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7111-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7111-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c7111-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7111-153">輸入</span><span class="sxs-lookup"><span data-stu-id="c7111-153">INPUTS</span></span>

### <span data-ttu-id="c7111-154">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="c7111-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="c7111-155">System.object</span><span class="sxs-lookup"><span data-stu-id="c7111-155">System.String</span></span>

## <span data-ttu-id="c7111-156">輸出</span><span class="sxs-lookup"><span data-stu-id="c7111-156">OUTPUTS</span></span>

### <span data-ttu-id="c7111-157">System.object</span><span class="sxs-lookup"><span data-stu-id="c7111-157">System.Boolean</span></span>

## <span data-ttu-id="c7111-158">筆記</span><span class="sxs-lookup"><span data-stu-id="c7111-158">NOTES</span></span>

## <span data-ttu-id="c7111-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7111-159">RELATED LINKS</span></span>

[<span data-ttu-id="c7111-160">AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="c7111-160">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="c7111-161">新-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="c7111-161">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
