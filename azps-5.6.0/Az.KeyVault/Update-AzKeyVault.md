---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 44d22938d2d9fd8d7830acf676ac0b953c6bdc4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908169"
---
# <span data-ttu-id="60227-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="60227-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="60227-102">簡介</span><span class="sxs-lookup"><span data-stu-id="60227-102">SYNOPSIS</span></span>
<span data-ttu-id="60227-103">更新 Azure 金鑰庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="60227-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="60227-104">語法</span><span class="sxs-lookup"><span data-stu-id="60227-104">SYNTAX</span></span>

### <span data-ttu-id="60227-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="60227-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60227-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60227-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60227-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60227-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60227-108">描述</span><span class="sxs-lookup"><span data-stu-id="60227-108">DESCRIPTION</span></span>
<span data-ttu-id="60227-109">此 Cmdlet 會更新 Azure 金鑰庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="60227-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="60227-110">例子</span><span class="sxs-lookup"><span data-stu-id="60227-110">EXAMPLES</span></span>

### <span data-ttu-id="60227-111">範例 1：啟用清除保護</span><span class="sxs-lookup"><span data-stu-id="60227-111">Example 1： Enable purge protection</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="60227-112">使用管線語法啟用清除保護。</span><span class="sxs-lookup"><span data-stu-id="60227-112">Enables purge protection using piping syntax.</span></span>

### <span data-ttu-id="60227-113">範例 2：啟用 RBAC 授權</span><span class="sxs-lookup"><span data-stu-id="60227-113">Example 2： Enable RBAC Authorization</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnableRbacAuthorization $true
```

<span data-ttu-id="60227-114">使用管道語法啟用 RBAC 授權。</span><span class="sxs-lookup"><span data-stu-id="60227-114">Enables RBAC Authorization using piping syntax.</span></span>

### <span data-ttu-id="60227-115">範例 3：設定標記</span><span class="sxs-lookup"><span data-stu-id="60227-115">Example 3： Set tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{key = "value"}
```

<span data-ttu-id="60227-116">設定名稱為 $keyVaultName 的金鑰$keyVaultName。</span><span class="sxs-lookup"><span data-stu-id="60227-116">Sets the tags of a key vault named $keyVaultName.</span></span>

### <span data-ttu-id="60227-117">範例 4：清除標記</span><span class="sxs-lookup"><span data-stu-id="60227-117">Example 4： Clean tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{}
```

<span data-ttu-id="60227-118">刪除名稱為 $keyVaultName 之金鑰庫的所有$keyVaultName。</span><span class="sxs-lookup"><span data-stu-id="60227-118">Deletes all tags of a key vault named $keyVaultName.</span></span>

## <span data-ttu-id="60227-119">參數</span><span class="sxs-lookup"><span data-stu-id="60227-119">PARAMETERS</span></span>

### <span data-ttu-id="60227-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60227-120">-DefaultProfile</span></span>
<span data-ttu-id="60227-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="60227-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60227-122">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="60227-122">-EnablePurgeProtection</span></span>
<span data-ttu-id="60227-123">啟用此金鑰庫的清除保護功能。</span><span class="sxs-lookup"><span data-stu-id="60227-123">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="60227-124">啟用之後，就無法停用。</span><span class="sxs-lookup"><span data-stu-id="60227-124">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="60227-125">需要開啟柔刪除功能。</span><span class="sxs-lookup"><span data-stu-id="60227-125">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="60227-126">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="60227-126">-EnableRbacAuthorization</span></span>
<span data-ttu-id="60227-127">啟用或停用此金鑰庫，以根據角色型存取控制 (RBAC) 。</span><span class="sxs-lookup"><span data-stu-id="60227-127">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="60227-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60227-128">-InputObject</span></span>
<span data-ttu-id="60227-129">Key Vault 物件。</span><span class="sxs-lookup"><span data-stu-id="60227-129">Key vault object.</span></span>

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

### <span data-ttu-id="60227-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60227-130">-ResourceGroupName</span></span>
<span data-ttu-id="60227-131">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="60227-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="60227-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60227-132">-ResourceId</span></span>
<span data-ttu-id="60227-133">金鑰庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="60227-133">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="60227-134">-標記</span><span class="sxs-lookup"><span data-stu-id="60227-134">-Tag</span></span>
<span data-ttu-id="60227-135">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="60227-135">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60227-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="60227-136">-VaultName</span></span>
<span data-ttu-id="60227-137">金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="60227-137">Name of the key vault.</span></span>

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

### <span data-ttu-id="60227-138">-確認</span><span class="sxs-lookup"><span data-stu-id="60227-138">-Confirm</span></span>
<span data-ttu-id="60227-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="60227-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60227-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60227-140">-WhatIf</span></span>
<span data-ttu-id="60227-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60227-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60227-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60227-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60227-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60227-143">CommonParameters</span></span>
<span data-ttu-id="60227-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="60227-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60227-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60227-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60227-146">輸入</span><span class="sxs-lookup"><span data-stu-id="60227-146">INPUTS</span></span>

### <span data-ttu-id="60227-147">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="60227-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="60227-148">System.String</span><span class="sxs-lookup"><span data-stu-id="60227-148">System.String</span></span>

## <span data-ttu-id="60227-149">輸出</span><span class="sxs-lookup"><span data-stu-id="60227-149">OUTPUTS</span></span>

### <span data-ttu-id="60227-150">Microsoft.Azure.Commands.KeyVault.models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="60227-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="60227-151">筆記</span><span class="sxs-lookup"><span data-stu-id="60227-151">NOTES</span></span>

## <span data-ttu-id="60227-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="60227-152">RELATED LINKS</span></span>
