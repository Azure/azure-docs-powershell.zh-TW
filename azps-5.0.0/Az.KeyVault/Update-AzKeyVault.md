---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 10a441cd1354b75a13b429c4375e7bc3fba72244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136722"
---
# <span data-ttu-id="a5b7b-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a5b7b-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="a5b7b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b7b-103">更新 Azure 金鑰電子倉庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="a5b7b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5b7b-104">SYNTAX</span></span>

### <span data-ttu-id="a5b7b-105">UpdateByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a5b7b-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5b7b-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b7b-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5b7b-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5b7b-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b7b-108">說明</span><span class="sxs-lookup"><span data-stu-id="a5b7b-108">DESCRIPTION</span></span>
<span data-ttu-id="a5b7b-109">這個 Cmdlet 會更新 Azure 金鑰電子倉庫的狀態。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="a5b7b-110">示例</span><span class="sxs-lookup"><span data-stu-id="a5b7b-110">EXAMPLES</span></span>

### <span data-ttu-id="a5b7b-111">範例2</span><span class="sxs-lookup"><span data-stu-id="a5b7b-111">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="a5b7b-112">使用管道語法來啟用清除保護。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-112">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="a5b7b-113">參數</span><span class="sxs-lookup"><span data-stu-id="a5b7b-113">PARAMETERS</span></span>

### <span data-ttu-id="a5b7b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b7b-114">-DefaultProfile</span></span>
<span data-ttu-id="a5b7b-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5b7b-116">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="a5b7b-116">-EnablePurgeProtection</span></span>
<span data-ttu-id="a5b7b-117">針對此金鑰保存庫啟用清除保護功能。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-117">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="a5b7b-118">一旦啟用，就無法停用。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-118">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="a5b7b-119">需要虛刪除才能開啟。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-119">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="a5b7b-120">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="a5b7b-120">-EnableRbacAuthorization</span></span>
<span data-ttu-id="a5b7b-121">啟用或停用此金鑰電子倉庫，透過角色的存取控制 (RBAC) 來授權資料動作。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-121">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

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

### <span data-ttu-id="a5b7b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5b7b-122">-InputObject</span></span>
<span data-ttu-id="a5b7b-123">金鑰保存庫物件。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-123">Key vault object.</span></span>

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

### <span data-ttu-id="a5b7b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b7b-124">-ResourceGroupName</span></span>
<span data-ttu-id="a5b7b-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-125">Name of the resource group.</span></span>

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

### <span data-ttu-id="a5b7b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5b7b-126">-ResourceId</span></span>
<span data-ttu-id="a5b7b-127">主要電子倉庫的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-127">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="a5b7b-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a5b7b-128">-VaultName</span></span>
<span data-ttu-id="a5b7b-129">金鑰保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-129">Name of the key vault.</span></span>

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

### <span data-ttu-id="a5b7b-130">-確認</span><span class="sxs-lookup"><span data-stu-id="a5b7b-130">-Confirm</span></span>
<span data-ttu-id="a5b7b-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b7b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b7b-132">-WhatIf</span></span>
<span data-ttu-id="a5b7b-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b7b-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b7b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b7b-135">CommonParameters</span></span>
<span data-ttu-id="a5b7b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b7b-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b7b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="a5b7b-138">INPUTS</span></span>

### <span data-ttu-id="a5b7b-139">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a5b7b-140">System.object</span><span class="sxs-lookup"><span data-stu-id="a5b7b-140">System.String</span></span>

## <span data-ttu-id="a5b7b-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a5b7b-141">OUTPUTS</span></span>

### <span data-ttu-id="a5b7b-142">PSKeyVault 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="a5b7b-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="a5b7b-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a5b7b-143">NOTES</span></span>

## <span data-ttu-id="a5b7b-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5b7b-144">RELATED LINKS</span></span>
