---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 2365a58093be3193c7ac285d6dd38fbaf769ccd4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799861"
---
# <span data-ttu-id="fa125-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fa125-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="fa125-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa125-102">SYNOPSIS</span></span>
<span data-ttu-id="fa125-103">刪除金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="fa125-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa125-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa125-104">SYNTAX</span></span>

### <span data-ttu-id="fa125-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="fa125-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa125-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="fa125-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa125-107">說明</span><span class="sxs-lookup"><span data-stu-id="fa125-107">DESCRIPTION</span></span>
<span data-ttu-id="fa125-108">**AzureRmKeyVault** Cmdlet 會刪除指定的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="fa125-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="fa125-109">它也會刪除該實例中所包含的所有金鑰與密碼。</span><span class="sxs-lookup"><span data-stu-id="fa125-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="fa125-110">請注意，雖然為這個 Cmdlet 指定 [資源群組] 是選擇性的，但您應該如此以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="fa125-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="fa125-111">示例</span><span class="sxs-lookup"><span data-stu-id="fa125-111">EXAMPLES</span></span>

### <span data-ttu-id="fa125-112">範例1：移除金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="fa125-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="fa125-113">這個命令會從您目前的訂閱中移除名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="fa125-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="fa125-114">範例2：從指定的資源群組中移除主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="fa125-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="fa125-115">這個命令會從命名的資源群組中移除名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="fa125-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="fa125-116">如果您沒有指定資源組名稱，此 Cmdlet 會在您目前的訂閱中搜尋已命名的金鑰保存庫以刪除。</span><span class="sxs-lookup"><span data-stu-id="fa125-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="fa125-117">參數</span><span class="sxs-lookup"><span data-stu-id="fa125-117">PARAMETERS</span></span>

### <span data-ttu-id="fa125-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa125-118">-AsJob</span></span>
<span data-ttu-id="fa125-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="fa125-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa125-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa125-120">-DefaultProfile</span></span>
<span data-ttu-id="fa125-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="fa125-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa125-122">-Force</span><span class="sxs-lookup"><span data-stu-id="fa125-122">-Force</span></span>
<span data-ttu-id="fa125-123">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa125-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="fa125-124">根據預設，這個 Cmdlet 會提示您確認要刪除金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="fa125-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="fa125-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="fa125-125">-InRemovedState</span></span>
<span data-ttu-id="fa125-126">永久移除先前刪除的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="fa125-126">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="fa125-127">-位置</span><span class="sxs-lookup"><span data-stu-id="fa125-127">-Location</span></span>
<span data-ttu-id="fa125-128">已刪除的電子倉庫的位置。</span><span class="sxs-lookup"><span data-stu-id="fa125-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="fa125-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa125-129">-ResourceGroupName</span></span>
<span data-ttu-id="fa125-130">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa125-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fa125-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fa125-131">-VaultName</span></span>
<span data-ttu-id="fa125-132">指定要移除之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa125-132">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="fa125-133">-確認</span><span class="sxs-lookup"><span data-stu-id="fa125-133">-Confirm</span></span>
<span data-ttu-id="fa125-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa125-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa125-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa125-135">-WhatIf</span></span>
<span data-ttu-id="fa125-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa125-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa125-137">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa125-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa125-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa125-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa125-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa125-139">CommonParameters</span></span>
<span data-ttu-id="fa125-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa125-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa125-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa125-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa125-142">輸入</span><span class="sxs-lookup"><span data-stu-id="fa125-142">INPUTS</span></span>

## <span data-ttu-id="fa125-143">輸出</span><span class="sxs-lookup"><span data-stu-id="fa125-143">OUTPUTS</span></span>

## <span data-ttu-id="fa125-144">筆記</span><span class="sxs-lookup"><span data-stu-id="fa125-144">NOTES</span></span>

## <span data-ttu-id="fa125-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa125-145">RELATED LINKS</span></span>

[<span data-ttu-id="fa125-146">AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fa125-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="fa125-147">新-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="fa125-147">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
