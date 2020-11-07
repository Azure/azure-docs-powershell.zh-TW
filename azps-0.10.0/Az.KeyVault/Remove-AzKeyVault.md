---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 20187e2d7a844b472217fd30acbac9805e85ad40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795542"
---
# <span data-ttu-id="22805-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="22805-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="22805-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22805-102">SYNOPSIS</span></span>
<span data-ttu-id="22805-103">刪除金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="22805-103">Deletes a key vault.</span></span>

## <span data-ttu-id="22805-104">句法</span><span class="sxs-lookup"><span data-stu-id="22805-104">SYNTAX</span></span>

### <span data-ttu-id="22805-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="22805-105">ByAvailableVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22805-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="22805-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22805-107">說明</span><span class="sxs-lookup"><span data-stu-id="22805-107">DESCRIPTION</span></span>
<span data-ttu-id="22805-108">**AzKeyVault** Cmdlet 會刪除指定的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="22805-108">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="22805-109">它也會刪除該實例中所包含的所有金鑰與密碼。</span><span class="sxs-lookup"><span data-stu-id="22805-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="22805-110">請注意，雖然為這個 Cmdlet 指定 [資源群組] 是選擇性的，但您應該如此以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="22805-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="22805-111">示例</span><span class="sxs-lookup"><span data-stu-id="22805-111">EXAMPLES</span></span>

### <span data-ttu-id="22805-112">範例1：移除金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="22805-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="22805-113">這個命令會從您目前的訂閱中移除名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="22805-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="22805-114">範例2：從指定的資源群組中移除主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="22805-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="22805-115">這個命令會從命名的資源群組中移除名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="22805-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="22805-116">如果您沒有指定資源組名稱，此 Cmdlet 會在您目前的訂閱中搜尋已命名的金鑰保存庫以刪除。</span><span class="sxs-lookup"><span data-stu-id="22805-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="22805-117">參數</span><span class="sxs-lookup"><span data-stu-id="22805-117">PARAMETERS</span></span>

### <span data-ttu-id="22805-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22805-118">-AsJob</span></span>
<span data-ttu-id="22805-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="22805-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22805-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22805-120">-DefaultProfile</span></span>
<span data-ttu-id="22805-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="22805-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22805-122">-Force</span><span class="sxs-lookup"><span data-stu-id="22805-122">-Force</span></span>
<span data-ttu-id="22805-123">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="22805-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="22805-124">根據預設，這個 Cmdlet 會提示您確認要刪除金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="22805-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="22805-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="22805-125">-InRemovedState</span></span>
<span data-ttu-id="22805-126">永久移除先前刪除的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="22805-126">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22805-127">-位置</span><span class="sxs-lookup"><span data-stu-id="22805-127">-Location</span></span>
<span data-ttu-id="22805-128">已刪除的電子倉庫的位置。</span><span class="sxs-lookup"><span data-stu-id="22805-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="22805-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22805-129">-ResourceGroupName</span></span>
<span data-ttu-id="22805-130">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="22805-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="22805-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="22805-131">-VaultName</span></span>
<span data-ttu-id="22805-132">指定要移除之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="22805-132">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22805-133">-確認</span><span class="sxs-lookup"><span data-stu-id="22805-133">-Confirm</span></span>
<span data-ttu-id="22805-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="22805-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22805-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22805-135">-WhatIf</span></span>
<span data-ttu-id="22805-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22805-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22805-137">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="22805-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22805-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="22805-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22805-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22805-139">CommonParameters</span></span>
<span data-ttu-id="22805-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22805-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22805-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22805-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22805-142">輸入</span><span class="sxs-lookup"><span data-stu-id="22805-142">INPUTS</span></span>

### <span data-ttu-id="22805-143">所有</span><span class="sxs-lookup"><span data-stu-id="22805-143">None</span></span>
<span data-ttu-id="22805-144">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="22805-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22805-145">輸出</span><span class="sxs-lookup"><span data-stu-id="22805-145">OUTPUTS</span></span>

## <span data-ttu-id="22805-146">筆記</span><span class="sxs-lookup"><span data-stu-id="22805-146">NOTES</span></span>

## <span data-ttu-id="22805-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="22805-147">RELATED LINKS</span></span>

[<span data-ttu-id="22805-148">AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="22805-148">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="22805-149">新-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="22805-149">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
