---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: a37073de6a7960ae1ab90746372179db8e9d9386
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138574"
---
# <span data-ttu-id="87fb7-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="87fb7-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="87fb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="87fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="87fb7-103">刪除 ACR 資訊清單。</span><span class="sxs-lookup"><span data-stu-id="87fb7-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="87fb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="87fb7-104">SYNTAX</span></span>

### <span data-ttu-id="87fb7-105">ByManifestParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="87fb7-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87fb7-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="87fb7-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87fb7-107">說明</span><span class="sxs-lookup"><span data-stu-id="87fb7-107">DESCRIPTION</span></span>
<span data-ttu-id="87fb7-108">刪除 ACR 資訊清單。</span><span class="sxs-lookup"><span data-stu-id="87fb7-108">Delete ACR manifest.</span></span>
<span data-ttu-id="87fb7-109">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="87fb7-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="87fb7-110">一.</span><span class="sxs-lookup"><span data-stu-id="87fb7-110">first.</span></span>

## <span data-ttu-id="87fb7-111">示例</span><span class="sxs-lookup"><span data-stu-id="87fb7-111">EXAMPLES</span></span>

### <span data-ttu-id="87fb7-112">範例1</span><span class="sxs-lookup"><span data-stu-id="87fb7-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="87fb7-113">刪除資訊清單 sha256：31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab 在註冊表中進行知識庫測試/busybox27</span><span class="sxs-lookup"><span data-stu-id="87fb7-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="87fb7-114">範例2</span><span class="sxs-lookup"><span data-stu-id="87fb7-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="87fb7-115">在 registry 中刪除含有 [知識庫] 測試/busybox27 標記的資訊清單</span><span class="sxs-lookup"><span data-stu-id="87fb7-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="87fb7-116">參數</span><span class="sxs-lookup"><span data-stu-id="87fb7-116">PARAMETERS</span></span>

### <span data-ttu-id="87fb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87fb7-117">-DefaultProfile</span></span>
<span data-ttu-id="87fb7-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="87fb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87fb7-119">-資訊清單</span><span class="sxs-lookup"><span data-stu-id="87fb7-119">-Manifest</span></span>
<span data-ttu-id="87fb7-120">資訊清單參照。</span><span class="sxs-lookup"><span data-stu-id="87fb7-120">Manifest reference.</span></span>

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

### <span data-ttu-id="87fb7-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="87fb7-121">-RegistryName</span></span>
<span data-ttu-id="87fb7-122">Azure 容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="87fb7-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="87fb7-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="87fb7-123">-RepositoryName</span></span>
<span data-ttu-id="87fb7-124">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="87fb7-124">Repository Name.</span></span>

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

### <span data-ttu-id="87fb7-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="87fb7-125">-Tag</span></span>
<span data-ttu-id="87fb7-126">標記.</span><span class="sxs-lookup"><span data-stu-id="87fb7-126">Tag.</span></span>

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

### <span data-ttu-id="87fb7-127">-確認</span><span class="sxs-lookup"><span data-stu-id="87fb7-127">-Confirm</span></span>
<span data-ttu-id="87fb7-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="87fb7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87fb7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87fb7-129">-WhatIf</span></span>
<span data-ttu-id="87fb7-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="87fb7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87fb7-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="87fb7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87fb7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87fb7-132">CommonParameters</span></span>
<span data-ttu-id="87fb7-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="87fb7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87fb7-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="87fb7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87fb7-135">輸入</span><span class="sxs-lookup"><span data-stu-id="87fb7-135">INPUTS</span></span>

### <span data-ttu-id="87fb7-136">System.object</span><span class="sxs-lookup"><span data-stu-id="87fb7-136">System.String</span></span>

## <span data-ttu-id="87fb7-137">輸出</span><span class="sxs-lookup"><span data-stu-id="87fb7-137">OUTPUTS</span></span>

### <span data-ttu-id="87fb7-138">System.object</span><span class="sxs-lookup"><span data-stu-id="87fb7-138">System.Boolean</span></span>

## <span data-ttu-id="87fb7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="87fb7-139">NOTES</span></span>

## <span data-ttu-id="87fb7-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="87fb7-140">RELATED LINKS</span></span>
