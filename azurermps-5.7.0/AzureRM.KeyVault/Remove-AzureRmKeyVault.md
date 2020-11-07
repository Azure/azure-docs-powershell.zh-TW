---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 0c9e37433d28a16a28ca56daf4a726347b7a9533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624301"
---
# <span data-ttu-id="fda0c-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fda0c-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="fda0c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fda0c-102">SYNOPSIS</span></span>
<span data-ttu-id="fda0c-103">刪除金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="fda0c-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fda0c-104">句法</span><span class="sxs-lookup"><span data-stu-id="fda0c-104">SYNTAX</span></span>

### <span data-ttu-id="fda0c-105">ByAvailableVault (預設) </span><span class="sxs-lookup"><span data-stu-id="fda0c-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda0c-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="fda0c-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda0c-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="fda0c-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda0c-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="fda0c-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fda0c-109">說明</span><span class="sxs-lookup"><span data-stu-id="fda0c-109">DESCRIPTION</span></span>
<span data-ttu-id="fda0c-110">**AzureRmKeyVault** Cmdlet 會刪除指定的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="fda0c-110">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="fda0c-111">它也會刪除該實例中所包含的所有金鑰與密碼。</span><span class="sxs-lookup"><span data-stu-id="fda0c-111">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="fda0c-112">請注意，雖然為這個 Cmdlet 指定 [資源群組] 是選擇性的，但您應該如此以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="fda0c-112">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="fda0c-113">示例</span><span class="sxs-lookup"><span data-stu-id="fda0c-113">EXAMPLES</span></span>

### <span data-ttu-id="fda0c-114">範例1：移除金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="fda0c-114">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="fda0c-115">這個命令會從您目前的訂閱中移除名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="fda0c-115">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="fda0c-116">範例2：從指定的資源群組中移除主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="fda0c-116">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="fda0c-117">這個命令會從命名的資源群組中移除名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="fda0c-117">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="fda0c-118">如果您沒有指定資源組名稱，此 Cmdlet 會在您目前的訂閱中搜尋已命名的金鑰保存庫以刪除。</span><span class="sxs-lookup"><span data-stu-id="fda0c-118">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="fda0c-119">參數</span><span class="sxs-lookup"><span data-stu-id="fda0c-119">PARAMETERS</span></span>

### <span data-ttu-id="fda0c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fda0c-120">-AsJob</span></span>
<span data-ttu-id="fda0c-121">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fda0c-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda0c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda0c-122">-DefaultProfile</span></span>
<span data-ttu-id="fda0c-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fda0c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda0c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="fda0c-124">-Force</span></span>
<span data-ttu-id="fda0c-125">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fda0c-125">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="fda0c-126">根據預設，這個 Cmdlet 會提示您確認要刪除金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="fda0c-126">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda0c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fda0c-127">-InputObject</span></span>
<span data-ttu-id="fda0c-128">要刪除的主要保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="fda0c-128">Key Vault object to be deleted.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fda0c-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="fda0c-129">-InRemovedState</span></span>
<span data-ttu-id="fda0c-130">永久移除先前刪除的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="fda0c-130">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda0c-131">-位置</span><span class="sxs-lookup"><span data-stu-id="fda0c-131">-Location</span></span>
<span data-ttu-id="fda0c-132">已刪除的電子倉庫的位置。</span><span class="sxs-lookup"><span data-stu-id="fda0c-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fda0c-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fda0c-133">-PassThru</span></span>
<span data-ttu-id="fda0c-134">這個 Cmdlet 預設不會傳回物件。</span><span class="sxs-lookup"><span data-stu-id="fda0c-134">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="fda0c-135">如果已指定此開關，則如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="fda0c-135">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda0c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda0c-136">-ResourceGroupName</span></span>
<span data-ttu-id="fda0c-137">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fda0c-137">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fda0c-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fda0c-138">-VaultName</span></span>
<span data-ttu-id="fda0c-139">指定要移除之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fda0c-139">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fda0c-140">-確認</span><span class="sxs-lookup"><span data-stu-id="fda0c-140">-Confirm</span></span>
<span data-ttu-id="fda0c-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fda0c-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda0c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fda0c-142">-WhatIf</span></span>
<span data-ttu-id="fda0c-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fda0c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fda0c-144">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fda0c-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fda0c-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fda0c-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fda0c-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda0c-146">CommonParameters</span></span>
<span data-ttu-id="fda0c-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fda0c-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda0c-148">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fda0c-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda0c-149">輸入</span><span class="sxs-lookup"><span data-stu-id="fda0c-149">INPUTS</span></span>

### <span data-ttu-id="fda0c-150">所有</span><span class="sxs-lookup"><span data-stu-id="fda0c-150">None</span></span>
<span data-ttu-id="fda0c-151">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="fda0c-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fda0c-152">輸出</span><span class="sxs-lookup"><span data-stu-id="fda0c-152">OUTPUTS</span></span>

### <span data-ttu-id="fda0c-153">System.object</span><span class="sxs-lookup"><span data-stu-id="fda0c-153">System.Boolean</span></span>

## <span data-ttu-id="fda0c-154">筆記</span><span class="sxs-lookup"><span data-stu-id="fda0c-154">NOTES</span></span>

## <span data-ttu-id="fda0c-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="fda0c-155">RELATED LINKS</span></span>

[<span data-ttu-id="fda0c-156">AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fda0c-156">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="fda0c-157">新-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fda0c-157">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
