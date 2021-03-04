---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: def99b11efa5070881cc3226b9ec85449b4cc0b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904713"
---
# <span data-ttu-id="5400d-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="5400d-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="5400d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5400d-102">SYNOPSIS</span></span>
<span data-ttu-id="5400d-103">刪除 ACR 清單。</span><span class="sxs-lookup"><span data-stu-id="5400d-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="5400d-104">語法</span><span class="sxs-lookup"><span data-stu-id="5400d-104">SYNTAX</span></span>

### <span data-ttu-id="5400d-105">ByManifestParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5400d-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5400d-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="5400d-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5400d-107">描述</span><span class="sxs-lookup"><span data-stu-id="5400d-107">DESCRIPTION</span></span>
<span data-ttu-id="5400d-108">刪除 ACR 清單。</span><span class="sxs-lookup"><span data-stu-id="5400d-108">Delete ACR manifest.</span></span>
<span data-ttu-id="5400d-109">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="5400d-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="5400d-110">第一。</span><span class="sxs-lookup"><span data-stu-id="5400d-110">first.</span></span>

## <span data-ttu-id="5400d-111">例子</span><span class="sxs-lookup"><span data-stu-id="5400d-111">EXAMPLES</span></span>

### <span data-ttu-id="5400d-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="5400d-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="5400d-113">刪除清單 sha256：31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span><span class="sxs-lookup"><span data-stu-id="5400d-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="5400d-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="5400d-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="5400d-115">在註冊表下刪除包含最新存放庫測試/busybox27 標記的清單</span><span class="sxs-lookup"><span data-stu-id="5400d-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="5400d-116">參數</span><span class="sxs-lookup"><span data-stu-id="5400d-116">PARAMETERS</span></span>

### <span data-ttu-id="5400d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5400d-117">-DefaultProfile</span></span>
<span data-ttu-id="5400d-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5400d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5400d-119">-Manifest</span><span class="sxs-lookup"><span data-stu-id="5400d-119">-Manifest</span></span>
<span data-ttu-id="5400d-120">清單參照。</span><span class="sxs-lookup"><span data-stu-id="5400d-120">Manifest reference.</span></span>

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

### <span data-ttu-id="5400d-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5400d-121">-RegistryName</span></span>
<span data-ttu-id="5400d-122">Azure 容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="5400d-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="5400d-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="5400d-123">-RepositoryName</span></span>
<span data-ttu-id="5400d-124">存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="5400d-124">Repository Name.</span></span>

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

### <span data-ttu-id="5400d-125">-標記</span><span class="sxs-lookup"><span data-stu-id="5400d-125">-Tag</span></span>
<span data-ttu-id="5400d-126">標記。</span><span class="sxs-lookup"><span data-stu-id="5400d-126">Tag.</span></span>

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

### <span data-ttu-id="5400d-127">-確認</span><span class="sxs-lookup"><span data-stu-id="5400d-127">-Confirm</span></span>
<span data-ttu-id="5400d-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5400d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5400d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5400d-129">-WhatIf</span></span>
<span data-ttu-id="5400d-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5400d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5400d-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5400d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5400d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5400d-132">CommonParameters</span></span>
<span data-ttu-id="5400d-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5400d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5400d-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5400d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5400d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="5400d-135">INPUTS</span></span>

### <span data-ttu-id="5400d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5400d-136">System.String</span></span>

## <span data-ttu-id="5400d-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5400d-137">OUTPUTS</span></span>

### <span data-ttu-id="5400d-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5400d-138">System.Boolean</span></span>

## <span data-ttu-id="5400d-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5400d-139">NOTES</span></span>

## <span data-ttu-id="5400d-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5400d-140">RELATED LINKS</span></span>
