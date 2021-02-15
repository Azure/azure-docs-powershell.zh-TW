---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 2a9c2870e0ce33b93d3013e84e7de3642b42708c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131726"
---
# <span data-ttu-id="dc07d-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="dc07d-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="dc07d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc07d-102">SYNOPSIS</span></span>
<span data-ttu-id="dc07d-103">更新 Azure 金鑰電子倉庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="dc07d-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="dc07d-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc07d-104">SYNTAX</span></span>

### <span data-ttu-id="dc07d-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="dc07d-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc07d-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc07d-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc07d-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc07d-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc07d-108">說明</span><span class="sxs-lookup"><span data-stu-id="dc07d-108">DESCRIPTION</span></span>
<span data-ttu-id="dc07d-109">這個 Cmdlet 會更新 Azure 金鑰電子倉庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="dc07d-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="dc07d-110">示例</span><span class="sxs-lookup"><span data-stu-id="dc07d-110">EXAMPLES</span></span>

### <span data-ttu-id="dc07d-111">範例1：啟用清除保護</span><span class="sxs-lookup"><span data-stu-id="dc07d-111">Example 1： Enable purge protection</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="dc07d-112">使用管道語法來啟用清除保護。</span><span class="sxs-lookup"><span data-stu-id="dc07d-112">Enables purge protection using piping syntax.</span></span>

### <span data-ttu-id="dc07d-113">範例2：啟用 RBAC 授權</span><span class="sxs-lookup"><span data-stu-id="dc07d-113">Example 2： Enable RBAC Authorization</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnableRbacAuthorization $true
```

<span data-ttu-id="dc07d-114">使用管道語法啟用 RBAC 授權。</span><span class="sxs-lookup"><span data-stu-id="dc07d-114">Enables RBAC Authorization using piping syntax.</span></span>

### <span data-ttu-id="dc07d-115">範例3：設定標記</span><span class="sxs-lookup"><span data-stu-id="dc07d-115">Example 3： Set tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{key = "value"}
```

<span data-ttu-id="dc07d-116">設定名為 $keyVaultName 的主要電子倉庫標記。</span><span class="sxs-lookup"><span data-stu-id="dc07d-116">Sets the tags of a key vault named $keyVaultName.</span></span>

### <span data-ttu-id="dc07d-117">範例4：清除標記</span><span class="sxs-lookup"><span data-stu-id="dc07d-117">Example 4： Clean tags</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName | Update-AzKeyVault -Tags @{}
```

<span data-ttu-id="dc07d-118">刪除名為 $keyVaultName 的主要保存庫的所有標籤。</span><span class="sxs-lookup"><span data-stu-id="dc07d-118">Deletes all tags of a key vault named $keyVaultName.</span></span>

## <span data-ttu-id="dc07d-119">參數</span><span class="sxs-lookup"><span data-stu-id="dc07d-119">PARAMETERS</span></span>

### <span data-ttu-id="dc07d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc07d-120">-DefaultProfile</span></span>
<span data-ttu-id="dc07d-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc07d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc07d-122">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="dc07d-122">-EnablePurgeProtection</span></span>
<span data-ttu-id="dc07d-123">針對此金鑰保存庫啟用清除保護功能。</span><span class="sxs-lookup"><span data-stu-id="dc07d-123">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="dc07d-124">一旦啟用，就無法停用。</span><span class="sxs-lookup"><span data-stu-id="dc07d-124">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="dc07d-125">需要虛刪除才能開啟。</span><span class="sxs-lookup"><span data-stu-id="dc07d-125">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="dc07d-126">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="dc07d-126">-EnableRbacAuthorization</span></span>
<span data-ttu-id="dc07d-127">啟用或停用此金鑰電子倉庫，透過角色的存取控制 (RBAC) 來授權資料動作。</span><span class="sxs-lookup"><span data-stu-id="dc07d-127">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="dc07d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc07d-128">-InputObject</span></span>
<span data-ttu-id="dc07d-129">金鑰保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="dc07d-129">Key vault object.</span></span>

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

### <span data-ttu-id="dc07d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc07d-130">-ResourceGroupName</span></span>
<span data-ttu-id="dc07d-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc07d-131">Name of the resource group.</span></span>

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

### <span data-ttu-id="dc07d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc07d-132">-ResourceId</span></span>
<span data-ttu-id="dc07d-133">主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dc07d-133">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="dc07d-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="dc07d-134">-Tag</span></span>
<span data-ttu-id="dc07d-135">代表資源標記的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="dc07d-135">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="dc07d-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dc07d-136">-VaultName</span></span>
<span data-ttu-id="dc07d-137">金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc07d-137">Name of the key vault.</span></span>

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

### <span data-ttu-id="dc07d-138">-確認</span><span class="sxs-lookup"><span data-stu-id="dc07d-138">-Confirm</span></span>
<span data-ttu-id="dc07d-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dc07d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc07d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc07d-140">-WhatIf</span></span>
<span data-ttu-id="dc07d-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dc07d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc07d-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dc07d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc07d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc07d-143">CommonParameters</span></span>
<span data-ttu-id="dc07d-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc07d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc07d-145">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dc07d-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc07d-146">輸入</span><span class="sxs-lookup"><span data-stu-id="dc07d-146">INPUTS</span></span>

### <span data-ttu-id="dc07d-147">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="dc07d-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="dc07d-148">System.object</span><span class="sxs-lookup"><span data-stu-id="dc07d-148">System.String</span></span>

## <span data-ttu-id="dc07d-149">輸出</span><span class="sxs-lookup"><span data-stu-id="dc07d-149">OUTPUTS</span></span>

### <span data-ttu-id="dc07d-150">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="dc07d-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="dc07d-151">筆記</span><span class="sxs-lookup"><span data-stu-id="dc07d-151">NOTES</span></span>

## <span data-ttu-id="dc07d-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc07d-152">RELATED LINKS</span></span>
