---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
ms.openlocfilehash: 85623106a932ba9419da0c07cc4bcb6c52e5e838
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127679"
---
# <span data-ttu-id="c83ab-101">Update-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="c83ab-101">Update-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="c83ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c83ab-102">SYNOPSIS</span></span>
<span data-ttu-id="c83ab-103">更新 ACR 資訊清單。</span><span class="sxs-lookup"><span data-stu-id="c83ab-103">Update ACR manifest.</span></span> 

## <span data-ttu-id="c83ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="c83ab-104">SYNTAX</span></span>

### <span data-ttu-id="c83ab-105">ByManifestParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c83ab-105">ByManifestParameterSet (Default)</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c83ab-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="c83ab-106">ByTagParameterSet</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c83ab-107">說明</span><span class="sxs-lookup"><span data-stu-id="c83ab-107">DESCRIPTION</span></span>
<span data-ttu-id="c83ab-108">更新 ACR 資訊清單。</span><span class="sxs-lookup"><span data-stu-id="c83ab-108">Update ACR manifest.</span></span>
<span data-ttu-id="c83ab-109">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="c83ab-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="c83ab-110">一.</span><span class="sxs-lookup"><span data-stu-id="c83ab-110">first.</span></span>

## <span data-ttu-id="c83ab-111">示例</span><span class="sxs-lookup"><span data-stu-id="c83ab-111">EXAMPLES</span></span>

### <span data-ttu-id="c83ab-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c83ab-112">Example 1</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="c83ab-113">在 registry 中更新資訊清單 sha256：185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 的屬性。</span><span class="sxs-lookup"><span data-stu-id="c83ab-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span></span>

### <span data-ttu-id="c83ab-114">範例2</span><span class="sxs-lookup"><span data-stu-id="c83ab-114">Example 2</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Tag latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="c83ab-115">使用 [登錄] 底下的 [標記最新版本] 更新資訊清單屬性。</span><span class="sxs-lookup"><span data-stu-id="c83ab-115">Update attributes for manifest with tag latest under registry.</span></span>

## <span data-ttu-id="c83ab-116">參數</span><span class="sxs-lookup"><span data-stu-id="c83ab-116">PARAMETERS</span></span>

### <span data-ttu-id="c83ab-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c83ab-117">-DefaultProfile</span></span>
<span data-ttu-id="c83ab-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c83ab-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c83ab-119">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="c83ab-119">-DeleteEnabled</span></span>
<span data-ttu-id="c83ab-120">刪除 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="c83ab-120">Delete enable.</span></span>

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

### <span data-ttu-id="c83ab-121">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="c83ab-121">-ListEnabled</span></span>
<span data-ttu-id="c83ab-122">清單啟用]。</span><span class="sxs-lookup"><span data-stu-id="c83ab-122">List enable.</span></span>

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

### <span data-ttu-id="c83ab-123">-資訊清單</span><span class="sxs-lookup"><span data-stu-id="c83ab-123">-Manifest</span></span>
<span data-ttu-id="c83ab-124">資訊清單參照。</span><span class="sxs-lookup"><span data-stu-id="c83ab-124">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManifestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c83ab-125">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="c83ab-125">-ReadEnabled</span></span>
<span data-ttu-id="c83ab-126">已閱讀 [啟用]。</span><span class="sxs-lookup"><span data-stu-id="c83ab-126">Read enable.</span></span>

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

### <span data-ttu-id="c83ab-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c83ab-127">-RegistryName</span></span>
<span data-ttu-id="c83ab-128">Azure 容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="c83ab-128">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c83ab-129">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="c83ab-129">-RepositoryName</span></span>
<span data-ttu-id="c83ab-130">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="c83ab-130">Repository Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c83ab-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="c83ab-131">-Tag</span></span>
<span data-ttu-id="c83ab-132">標記.</span><span class="sxs-lookup"><span data-stu-id="c83ab-132">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c83ab-133">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="c83ab-133">-WriteEnabled</span></span>
<span data-ttu-id="c83ab-134">啟用寫入。</span><span class="sxs-lookup"><span data-stu-id="c83ab-134">Write enable.</span></span>

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

### <span data-ttu-id="c83ab-135">-確認</span><span class="sxs-lookup"><span data-stu-id="c83ab-135">-Confirm</span></span>
<span data-ttu-id="c83ab-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c83ab-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c83ab-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c83ab-137">-WhatIf</span></span>
<span data-ttu-id="c83ab-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c83ab-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c83ab-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c83ab-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c83ab-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c83ab-140">CommonParameters</span></span>
<span data-ttu-id="c83ab-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c83ab-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c83ab-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c83ab-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c83ab-143">輸入</span><span class="sxs-lookup"><span data-stu-id="c83ab-143">INPUTS</span></span>

### <span data-ttu-id="c83ab-144">System.object</span><span class="sxs-lookup"><span data-stu-id="c83ab-144">System.String</span></span>

## <span data-ttu-id="c83ab-145">輸出</span><span class="sxs-lookup"><span data-stu-id="c83ab-145">OUTPUTS</span></span>

### <span data-ttu-id="c83ab-146">PSManifestAttribute 中的 ContainerRegistry。</span><span class="sxs-lookup"><span data-stu-id="c83ab-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

## <span data-ttu-id="c83ab-147">筆記</span><span class="sxs-lookup"><span data-stu-id="c83ab-147">NOTES</span></span>

## <span data-ttu-id="c83ab-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="c83ab-148">RELATED LINKS</span></span>
