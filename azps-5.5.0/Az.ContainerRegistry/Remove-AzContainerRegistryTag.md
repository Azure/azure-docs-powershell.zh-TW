---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 7e6528630c731b15f906d79de45bc50f94b2a715
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138563"
---
# <span data-ttu-id="91bd5-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="91bd5-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="91bd5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="91bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="91bd5-103">將 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="91bd5-103">Untag ACR tag.</span></span>

## <span data-ttu-id="91bd5-104">句法</span><span class="sxs-lookup"><span data-stu-id="91bd5-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91bd5-105">說明</span><span class="sxs-lookup"><span data-stu-id="91bd5-105">DESCRIPTION</span></span>
<span data-ttu-id="91bd5-106">將 ACR 標記。</span><span class="sxs-lookup"><span data-stu-id="91bd5-106">Untag ACR tag.</span></span>
<span data-ttu-id="91bd5-107">若要使用此 Cmdlet，請執行 `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="91bd5-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="91bd5-108">一.</span><span class="sxs-lookup"><span data-stu-id="91bd5-108">first.</span></span>

## <span data-ttu-id="91bd5-109">示例</span><span class="sxs-lookup"><span data-stu-id="91bd5-109">EXAMPLES</span></span>

### <span data-ttu-id="91bd5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="91bd5-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="91bd5-111">將高山：標記在 [registry] 下。</span><span class="sxs-lookup"><span data-stu-id="91bd5-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="91bd5-112">參數</span><span class="sxs-lookup"><span data-stu-id="91bd5-112">PARAMETERS</span></span>

### <span data-ttu-id="91bd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91bd5-113">-DefaultProfile</span></span>
<span data-ttu-id="91bd5-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="91bd5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91bd5-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="91bd5-115">-Name</span></span>
<span data-ttu-id="91bd5-116">標記.</span><span class="sxs-lookup"><span data-stu-id="91bd5-116">Tag.</span></span>

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

### <span data-ttu-id="91bd5-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="91bd5-117">-RegistryName</span></span>
<span data-ttu-id="91bd5-118">Azure 容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="91bd5-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="91bd5-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="91bd5-119">-RepositoryName</span></span>
<span data-ttu-id="91bd5-120">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="91bd5-120">Repository Name.</span></span>

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

### <span data-ttu-id="91bd5-121">-確認</span><span class="sxs-lookup"><span data-stu-id="91bd5-121">-Confirm</span></span>
<span data-ttu-id="91bd5-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="91bd5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91bd5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91bd5-123">-WhatIf</span></span>
<span data-ttu-id="91bd5-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="91bd5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91bd5-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="91bd5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91bd5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91bd5-126">CommonParameters</span></span>
<span data-ttu-id="91bd5-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="91bd5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91bd5-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="91bd5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91bd5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="91bd5-129">INPUTS</span></span>

### <span data-ttu-id="91bd5-130">System.object</span><span class="sxs-lookup"><span data-stu-id="91bd5-130">System.String</span></span>

## <span data-ttu-id="91bd5-131">輸出</span><span class="sxs-lookup"><span data-stu-id="91bd5-131">OUTPUTS</span></span>

### <span data-ttu-id="91bd5-132">System.object</span><span class="sxs-lookup"><span data-stu-id="91bd5-132">System.Boolean</span></span>

## <span data-ttu-id="91bd5-133">筆記</span><span class="sxs-lookup"><span data-stu-id="91bd5-133">NOTES</span></span>

## <span data-ttu-id="91bd5-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="91bd5-134">RELATED LINKS</span></span>
