---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 6fbc5b33bb8e9c865b5ea869deed5044ee08198f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903026"
---
# <span data-ttu-id="f4997-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="f4997-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="f4997-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f4997-102">SYNOPSIS</span></span>
<span data-ttu-id="f4997-103">解除標記 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="f4997-103">Untag ACR tag.</span></span>

## <span data-ttu-id="f4997-104">語法</span><span class="sxs-lookup"><span data-stu-id="f4997-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4997-105">描述</span><span class="sxs-lookup"><span data-stu-id="f4997-105">DESCRIPTION</span></span>
<span data-ttu-id="f4997-106">解除標記 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="f4997-106">Untag ACR tag.</span></span>
<span data-ttu-id="f4997-107">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="f4997-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="f4997-108">第一。</span><span class="sxs-lookup"><span data-stu-id="f4997-108">first.</span></span>

## <span data-ttu-id="f4997-109">例子</span><span class="sxs-lookup"><span data-stu-id="f4997-109">EXAMPLES</span></span>

### <span data-ttu-id="f4997-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="f4997-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="f4997-111">在註冊表下解除標記 alpine：tag。</span><span class="sxs-lookup"><span data-stu-id="f4997-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="f4997-112">參數</span><span class="sxs-lookup"><span data-stu-id="f4997-112">PARAMETERS</span></span>

### <span data-ttu-id="f4997-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4997-113">-DefaultProfile</span></span>
<span data-ttu-id="f4997-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4997-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4997-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4997-115">-Name</span></span>
<span data-ttu-id="f4997-116">標記。</span><span class="sxs-lookup"><span data-stu-id="f4997-116">Tag.</span></span>

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

### <span data-ttu-id="f4997-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f4997-117">-RegistryName</span></span>
<span data-ttu-id="f4997-118">Azure 容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="f4997-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="f4997-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="f4997-119">-RepositoryName</span></span>
<span data-ttu-id="f4997-120">存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="f4997-120">Repository Name.</span></span>

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

### <span data-ttu-id="f4997-121">-確認</span><span class="sxs-lookup"><span data-stu-id="f4997-121">-Confirm</span></span>
<span data-ttu-id="f4997-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f4997-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4997-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4997-123">-WhatIf</span></span>
<span data-ttu-id="f4997-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4997-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4997-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4997-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4997-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4997-126">CommonParameters</span></span>
<span data-ttu-id="f4997-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f4997-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4997-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4997-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4997-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f4997-129">INPUTS</span></span>

### <span data-ttu-id="f4997-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f4997-130">System.String</span></span>

## <span data-ttu-id="f4997-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f4997-131">OUTPUTS</span></span>

### <span data-ttu-id="f4997-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f4997-132">System.Boolean</span></span>

## <span data-ttu-id="f4997-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f4997-133">NOTES</span></span>

## <span data-ttu-id="f4997-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4997-134">RELATED LINKS</span></span>
