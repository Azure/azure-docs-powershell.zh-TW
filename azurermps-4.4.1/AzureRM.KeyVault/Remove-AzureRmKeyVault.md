---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 2a30a190fbf257142e1c1e4fb4329fd6c4f41e3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454348"
---
# <span data-ttu-id="ed5e0-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ed5e0-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="ed5e0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ed5e0-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5e0-103">刪除金鑰電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed5e0-104">句法</span><span class="sxs-lookup"><span data-stu-id="ed5e0-104">SYNTAX</span></span>

### <span data-ttu-id="ed5e0-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="ed5e0-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed5e0-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="ed5e0-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed5e0-107">說明</span><span class="sxs-lookup"><span data-stu-id="ed5e0-107">DESCRIPTION</span></span>
<span data-ttu-id="ed5e0-108">**AzureRmKeyVault** Cmdlet 會刪除指定的金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="ed5e0-109">它也會刪除該實例中所包含的所有金鑰與密碼。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="ed5e0-110">請注意，雖然為這個 Cmdlet 指定 [資源群組] 是選擇性的，但您應該如此以取得較佳的效能。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="ed5e0-111">示例</span><span class="sxs-lookup"><span data-stu-id="ed5e0-111">EXAMPLES</span></span>

### <span data-ttu-id="ed5e0-112">範例1：移除金鑰保存庫</span><span class="sxs-lookup"><span data-stu-id="ed5e0-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="ed5e0-113">這個命令會從您目前的訂閱中移除名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="ed5e0-114">範例2：從指定的資源群組中移除主要電子倉庫</span><span class="sxs-lookup"><span data-stu-id="ed5e0-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="ed5e0-115">這個命令會從命名的資源群組中移除名為 Contoso03Vault 的主要電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="ed5e0-116">如果您沒有指定資源組名稱，此 Cmdlet 會在您目前的訂閱中搜尋已命名的金鑰保存庫以刪除。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="ed5e0-117">參數</span><span class="sxs-lookup"><span data-stu-id="ed5e0-117">PARAMETERS</span></span>

### <span data-ttu-id="ed5e0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ed5e0-118">-Force</span></span>
<span data-ttu-id="ed5e0-119">表示 Cmdlet 不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-119">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="ed5e0-120">根據預設，這個 Cmdlet 會提示您確認要刪除金鑰保存庫。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-120">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="ed5e0-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="ed5e0-121">-InRemovedState</span></span>
<span data-ttu-id="ed5e0-122">永久移除先前刪除的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-122">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e0-123">-位置</span><span class="sxs-lookup"><span data-stu-id="ed5e0-123">-Location</span></span>
<span data-ttu-id="ed5e0-124">已刪除的電子倉庫的位置。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-124">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5e0-125">-ResourceGroupName</span></span>
<span data-ttu-id="ed5e0-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e0-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ed5e0-127">-VaultName</span></span>
<span data-ttu-id="ed5e0-128">指定要移除之金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-128">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e0-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ed5e0-129">-Confirm</span></span>
<span data-ttu-id="ed5e0-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed5e0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed5e0-131">-WhatIf</span></span>
<span data-ttu-id="ed5e0-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed5e0-133">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed5e0-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed5e0-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5e0-135">-DefaultProfile</span></span>
<span data-ttu-id="ed5e0-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed5e0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5e0-137">CommonParameters</span></span>
<span data-ttu-id="ed5e0-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5e0-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ed5e0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5e0-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ed5e0-140">INPUTS</span></span>

## <span data-ttu-id="ed5e0-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ed5e0-141">OUTPUTS</span></span>

## <span data-ttu-id="ed5e0-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ed5e0-142">NOTES</span></span>

## <span data-ttu-id="ed5e0-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ed5e0-143">RELATED LINKS</span></span>

[<span data-ttu-id="ed5e0-144">AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ed5e0-144">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="ed5e0-145">新-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ed5e0-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
