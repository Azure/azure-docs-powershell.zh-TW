---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 4302f2f9c4c2d6b2c7afa879fc28e2ff4edbb592
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127643"
---
# <span data-ttu-id="e27a9-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="e27a9-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="e27a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e27a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e27a9-103">更新 Azure 金鑰電子倉庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="e27a9-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="e27a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e27a9-104">SYNTAX</span></span>

### <span data-ttu-id="e27a9-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e27a9-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27a9-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27a9-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27a9-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27a9-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e27a9-108">說明</span><span class="sxs-lookup"><span data-stu-id="e27a9-108">DESCRIPTION</span></span>
<span data-ttu-id="e27a9-109">這個 Cmdlet 會更新 Azure 金鑰電子倉庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="e27a9-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="e27a9-110">請注意，更新部分屬性是無法復原的動作，例如一旦啟用虛刪除，就不能再停用。</span><span class="sxs-lookup"><span data-stu-id="e27a9-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="e27a9-111">示例</span><span class="sxs-lookup"><span data-stu-id="e27a9-111">EXAMPLES</span></span>

### <span data-ttu-id="e27a9-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e27a9-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="e27a9-113">在 [資源群組] 中指定的 [主要電子倉庫] 上啟用 [虛刪除] `$keyVaultName` `$resourceGroupName` 。</span><span class="sxs-lookup"><span data-stu-id="e27a9-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="e27a9-114">範例1</span><span class="sxs-lookup"><span data-stu-id="e27a9-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="e27a9-115">使用管道語法來啟用清除保護。</span><span class="sxs-lookup"><span data-stu-id="e27a9-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="e27a9-116">參數</span><span class="sxs-lookup"><span data-stu-id="e27a9-116">PARAMETERS</span></span>

### <span data-ttu-id="e27a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27a9-117">-DefaultProfile</span></span>
<span data-ttu-id="e27a9-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e27a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e27a9-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="e27a9-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="e27a9-120">針對此金鑰保存庫啟用清除保護功能。</span><span class="sxs-lookup"><span data-stu-id="e27a9-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="e27a9-121">一旦啟用，就無法停用。</span><span class="sxs-lookup"><span data-stu-id="e27a9-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="e27a9-122">需要虛刪除才能開啟。</span><span class="sxs-lookup"><span data-stu-id="e27a9-122">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="e27a9-123">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="e27a9-123">-EnableRbacAuthorization</span></span>
<span data-ttu-id="e27a9-124">啟用或停用此金鑰電子倉庫，透過角色的存取控制 (RBAC) 來授權資料動作。</span><span class="sxs-lookup"><span data-stu-id="e27a9-124">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27a9-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="e27a9-125">-EnableSoftDelete</span></span>
<span data-ttu-id="e27a9-126">針對此金鑰保存庫啟用虛刪除功能。</span><span class="sxs-lookup"><span data-stu-id="e27a9-126">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="e27a9-127">一旦啟用，就無法停用。</span><span class="sxs-lookup"><span data-stu-id="e27a9-127">Once enabled it cannot be disabled.</span></span>

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

### <span data-ttu-id="e27a9-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e27a9-128">-InputObject</span></span>
<span data-ttu-id="e27a9-129">金鑰保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="e27a9-129">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e27a9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e27a9-130">-ResourceGroupName</span></span>
<span data-ttu-id="e27a9-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e27a9-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="e27a9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e27a9-132">-ResourceId</span></span>
<span data-ttu-id="e27a9-133">主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e27a9-133">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="e27a9-134">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e27a9-134">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="e27a9-135">指定保留刪除的資源的時間長度，以及要花多少時間，才能清除電子倉庫或刪除狀態中的物件。</span><span class="sxs-lookup"><span data-stu-id="e27a9-135">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="e27a9-136">預設值為90天。</span><span class="sxs-lookup"><span data-stu-id="e27a9-136">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27a9-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e27a9-137">-VaultName</span></span>
<span data-ttu-id="e27a9-138">金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="e27a9-138">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e27a9-139">-確認</span><span class="sxs-lookup"><span data-stu-id="e27a9-139">-Confirm</span></span>
<span data-ttu-id="e27a9-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e27a9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e27a9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e27a9-141">-WhatIf</span></span>
<span data-ttu-id="e27a9-142">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e27a9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e27a9-143">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e27a9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e27a9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27a9-144">CommonParameters</span></span>
<span data-ttu-id="e27a9-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e27a9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27a9-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e27a9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27a9-147">輸入</span><span class="sxs-lookup"><span data-stu-id="e27a9-147">INPUTS</span></span>

### <span data-ttu-id="e27a9-148">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e27a9-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e27a9-149">System.object</span><span class="sxs-lookup"><span data-stu-id="e27a9-149">System.String</span></span>

## <span data-ttu-id="e27a9-150">輸出</span><span class="sxs-lookup"><span data-stu-id="e27a9-150">OUTPUTS</span></span>

### <span data-ttu-id="e27a9-151">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e27a9-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="e27a9-152">筆記</span><span class="sxs-lookup"><span data-stu-id="e27a9-152">NOTES</span></span>

## <span data-ttu-id="e27a9-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="e27a9-153">RELATED LINKS</span></span>
