---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
ms.openlocfilehash: 030f0b00ba77bc967a53ce43c4f08d66c214f67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902994"
---
# <span data-ttu-id="8a09c-101">Update-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="8a09c-101">Update-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="8a09c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8a09c-102">SYNOPSIS</span></span>
<span data-ttu-id="8a09c-103">更新 ACR 清單。</span><span class="sxs-lookup"><span data-stu-id="8a09c-103">Update ACR manifest.</span></span> 

## <span data-ttu-id="8a09c-104">語法</span><span class="sxs-lookup"><span data-stu-id="8a09c-104">SYNTAX</span></span>

### <span data-ttu-id="8a09c-105">ByManifestParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8a09c-105">ByManifestParameterSet (Default)</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a09c-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a09c-106">ByTagParameterSet</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a09c-107">描述</span><span class="sxs-lookup"><span data-stu-id="8a09c-107">DESCRIPTION</span></span>
<span data-ttu-id="8a09c-108">更新 ACR 清單。</span><span class="sxs-lookup"><span data-stu-id="8a09c-108">Update ACR manifest.</span></span>
<span data-ttu-id="8a09c-109">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="8a09c-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="8a09c-110">第一。</span><span class="sxs-lookup"><span data-stu-id="8a09c-110">first.</span></span>

## <span data-ttu-id="8a09c-111">例子</span><span class="sxs-lookup"><span data-stu-id="8a09c-111">EXAMPLES</span></span>

### <span data-ttu-id="8a09c-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="8a09c-112">Example 1</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="8a09c-113">更新清單 sha256：18551807089175899c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span><span class="sxs-lookup"><span data-stu-id="8a09c-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span></span>

### <span data-ttu-id="8a09c-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="8a09c-114">Example 2</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Tag latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="8a09c-115">在註冊表下更新包含最新標記的清單屬性。</span><span class="sxs-lookup"><span data-stu-id="8a09c-115">Update attributes for manifest with tag latest under registry.</span></span>

## <span data-ttu-id="8a09c-116">參數</span><span class="sxs-lookup"><span data-stu-id="8a09c-116">PARAMETERS</span></span>

### <span data-ttu-id="8a09c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a09c-117">-DefaultProfile</span></span>
<span data-ttu-id="8a09c-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a09c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a09c-119">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="8a09c-119">-DeleteEnabled</span></span>
<span data-ttu-id="8a09c-120">刪除啟用。</span><span class="sxs-lookup"><span data-stu-id="8a09c-120">Delete enable.</span></span>

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

### <span data-ttu-id="8a09c-121">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="8a09c-121">-ListEnabled</span></span>
<span data-ttu-id="8a09c-122">清單啟用。</span><span class="sxs-lookup"><span data-stu-id="8a09c-122">List enable.</span></span>

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

### <span data-ttu-id="8a09c-123">-Manifest</span><span class="sxs-lookup"><span data-stu-id="8a09c-123">-Manifest</span></span>
<span data-ttu-id="8a09c-124">清單參照。</span><span class="sxs-lookup"><span data-stu-id="8a09c-124">Manifest reference.</span></span>

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

### <span data-ttu-id="8a09c-125">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="8a09c-125">-ReadEnabled</span></span>
<span data-ttu-id="8a09c-126">讀取啟用。</span><span class="sxs-lookup"><span data-stu-id="8a09c-126">Read enable.</span></span>

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

### <span data-ttu-id="8a09c-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8a09c-127">-RegistryName</span></span>
<span data-ttu-id="8a09c-128">Azure 容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="8a09c-128">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="8a09c-129">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="8a09c-129">-RepositoryName</span></span>
<span data-ttu-id="8a09c-130">存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="8a09c-130">Repository Name.</span></span>

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

### <span data-ttu-id="8a09c-131">-標記</span><span class="sxs-lookup"><span data-stu-id="8a09c-131">-Tag</span></span>
<span data-ttu-id="8a09c-132">標記。</span><span class="sxs-lookup"><span data-stu-id="8a09c-132">Tag.</span></span>

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

### <span data-ttu-id="8a09c-133">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="8a09c-133">-WriteEnabled</span></span>
<span data-ttu-id="8a09c-134">寫入啟用。</span><span class="sxs-lookup"><span data-stu-id="8a09c-134">Write enable.</span></span>

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

### <span data-ttu-id="8a09c-135">-確認</span><span class="sxs-lookup"><span data-stu-id="8a09c-135">-Confirm</span></span>
<span data-ttu-id="8a09c-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8a09c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a09c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a09c-137">-WhatIf</span></span>
<span data-ttu-id="8a09c-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a09c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a09c-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a09c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a09c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a09c-140">CommonParameters</span></span>
<span data-ttu-id="8a09c-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8a09c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a09c-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a09c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a09c-143">輸入</span><span class="sxs-lookup"><span data-stu-id="8a09c-143">INPUTS</span></span>

### <span data-ttu-id="8a09c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8a09c-144">System.String</span></span>

## <span data-ttu-id="8a09c-145">輸出</span><span class="sxs-lookup"><span data-stu-id="8a09c-145">OUTPUTS</span></span>

### <span data-ttu-id="8a09c-146">Microsoft.Azure.Commands.ContainerRegistry.models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="8a09c-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

## <span data-ttu-id="8a09c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="8a09c-147">NOTES</span></span>

## <span data-ttu-id="8a09c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a09c-148">RELATED LINKS</span></span>
