---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 8932402fb9e4e6b27f284313bfddc764192c5e93
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797677"
---
# <span data-ttu-id="72ab6-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="72ab6-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="72ab6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72ab6-102">SYNOPSIS</span></span>
<span data-ttu-id="72ab6-103">更新 Azure 金鑰電子倉庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="72ab6-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="72ab6-104">句法</span><span class="sxs-lookup"><span data-stu-id="72ab6-104">SYNTAX</span></span>

### <span data-ttu-id="72ab6-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="72ab6-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72ab6-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72ab6-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72ab6-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72ab6-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72ab6-108">說明</span><span class="sxs-lookup"><span data-stu-id="72ab6-108">DESCRIPTION</span></span>
<span data-ttu-id="72ab6-109">這個 Cmdlet 會更新 Azure 金鑰電子倉庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="72ab6-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="72ab6-110">請注意，更新部分屬性是無法復原的動作，例如一旦啟用虛刪除，就不能再停用。</span><span class="sxs-lookup"><span data-stu-id="72ab6-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="72ab6-111">示例</span><span class="sxs-lookup"><span data-stu-id="72ab6-111">EXAMPLES</span></span>

### <span data-ttu-id="72ab6-112">範例1</span><span class="sxs-lookup"><span data-stu-id="72ab6-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="72ab6-113">在 [資源群組] 中指定的 [主要電子倉庫] 上啟用 [虛刪除] `$keyVaultName` `$resourceGroupName` 。</span><span class="sxs-lookup"><span data-stu-id="72ab6-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="72ab6-114">範例1</span><span class="sxs-lookup"><span data-stu-id="72ab6-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="72ab6-115">使用管道語法來啟用清除保護。</span><span class="sxs-lookup"><span data-stu-id="72ab6-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="72ab6-116">參數</span><span class="sxs-lookup"><span data-stu-id="72ab6-116">PARAMETERS</span></span>

### <span data-ttu-id="72ab6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72ab6-117">-DefaultProfile</span></span>
<span data-ttu-id="72ab6-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72ab6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ab6-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="72ab6-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="72ab6-120">針對此金鑰保存庫啟用清除保護功能。</span><span class="sxs-lookup"><span data-stu-id="72ab6-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="72ab6-121">一旦啟用，就無法停用。</span><span class="sxs-lookup"><span data-stu-id="72ab6-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="72ab6-122">需要虛刪除才能開啟。</span><span class="sxs-lookup"><span data-stu-id="72ab6-122">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="72ab6-123">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="72ab6-123">-EnableSoftDelete</span></span>
<span data-ttu-id="72ab6-124">針對此金鑰保存庫啟用虛刪除功能。</span><span class="sxs-lookup"><span data-stu-id="72ab6-124">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="72ab6-125">一旦啟用，就無法停用。</span><span class="sxs-lookup"><span data-stu-id="72ab6-125">Once enabled it cannot be disabled.</span></span>

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

### <span data-ttu-id="72ab6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72ab6-126">-InputObject</span></span>
<span data-ttu-id="72ab6-127">金鑰保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="72ab6-127">Key vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72ab6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72ab6-128">-ResourceGroupName</span></span>
<span data-ttu-id="72ab6-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="72ab6-129">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ab6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72ab6-130">-ResourceId</span></span>
<span data-ttu-id="72ab6-131">主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="72ab6-131">Resource ID of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72ab6-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="72ab6-132">-VaultName</span></span>
<span data-ttu-id="72ab6-133">金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="72ab6-133">Name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ab6-134">-確認</span><span class="sxs-lookup"><span data-stu-id="72ab6-134">-Confirm</span></span>
<span data-ttu-id="72ab6-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="72ab6-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ab6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72ab6-136">-WhatIf</span></span>
<span data-ttu-id="72ab6-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="72ab6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72ab6-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="72ab6-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72ab6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72ab6-139">CommonParameters</span></span>
<span data-ttu-id="72ab6-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72ab6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72ab6-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="72ab6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72ab6-142">輸入</span><span class="sxs-lookup"><span data-stu-id="72ab6-142">INPUTS</span></span>

### <span data-ttu-id="72ab6-143">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="72ab6-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="72ab6-144">System.object</span><span class="sxs-lookup"><span data-stu-id="72ab6-144">System.String</span></span>

## <span data-ttu-id="72ab6-145">輸出</span><span class="sxs-lookup"><span data-stu-id="72ab6-145">OUTPUTS</span></span>

### <span data-ttu-id="72ab6-146">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="72ab6-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="72ab6-147">筆記</span><span class="sxs-lookup"><span data-stu-id="72ab6-147">NOTES</span></span>

## <span data-ttu-id="72ab6-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="72ab6-148">RELATED LINKS</span></span>
