---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: 1c0ad2ae46987a526be4e8fda110dada914bd27e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907785"
---
# <span data-ttu-id="b3f3a-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="b3f3a-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="b3f3a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f3a-103">從 ACR 刪除存放庫。</span><span class="sxs-lookup"><span data-stu-id="b3f3a-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="b3f3a-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3f3a-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3f3a-105">描述</span><span class="sxs-lookup"><span data-stu-id="b3f3a-105">DESCRIPTION</span></span>
<span data-ttu-id="b3f3a-106">從 ACR 刪除存放庫。</span><span class="sxs-lookup"><span data-stu-id="b3f3a-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="b3f3a-107">例子</span><span class="sxs-lookup"><span data-stu-id="b3f3a-107">EXAMPLES</span></span>

### <span data-ttu-id="b3f3a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b3f3a-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="b3f3a-109">在註冊表下刪除存放庫測試/busybox15。</span><span class="sxs-lookup"><span data-stu-id="b3f3a-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="b3f3a-110">參數</span><span class="sxs-lookup"><span data-stu-id="b3f3a-110">PARAMETERS</span></span>

### <span data-ttu-id="b3f3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f3a-111">-DefaultProfile</span></span>
<span data-ttu-id="b3f3a-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3f3a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3f3a-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3f3a-113">-Name</span></span>
<span data-ttu-id="b3f3a-114">存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="b3f3a-114">Repository Name.</span></span>

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

### <span data-ttu-id="b3f3a-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b3f3a-115">-RegistryName</span></span>
<span data-ttu-id="b3f3a-116">Azure 容器註冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="b3f3a-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="b3f3a-117">-確認</span><span class="sxs-lookup"><span data-stu-id="b3f3a-117">-Confirm</span></span>
<span data-ttu-id="b3f3a-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3f3a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3f3a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3f3a-119">-WhatIf</span></span>
<span data-ttu-id="b3f3a-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3f3a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3f3a-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3f3a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3f3a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f3a-122">CommonParameters</span></span>
<span data-ttu-id="b3f3a-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3f3a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f3a-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3f3a-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f3a-125">輸入</span><span class="sxs-lookup"><span data-stu-id="b3f3a-125">INPUTS</span></span>

### <span data-ttu-id="b3f3a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b3f3a-126">System.String</span></span>

## <span data-ttu-id="b3f3a-127">輸出</span><span class="sxs-lookup"><span data-stu-id="b3f3a-127">OUTPUTS</span></span>

### <span data-ttu-id="b3f3a-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span><span class="sxs-lookup"><span data-stu-id="b3f3a-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="b3f3a-129">筆記</span><span class="sxs-lookup"><span data-stu-id="b3f3a-129">NOTES</span></span>

## <span data-ttu-id="b3f3a-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3f3a-130">RELATED LINKS</span></span>
