---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: a99d020bbdef81868fb0e4338c7bc6c722723254
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138570"
---
# <span data-ttu-id="34fb7-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="34fb7-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="34fb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="34fb7-102">SYNOPSIS</span></span>
<span data-ttu-id="34fb7-103">從 ACR 刪除儲存庫。</span><span class="sxs-lookup"><span data-stu-id="34fb7-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="34fb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="34fb7-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34fb7-105">說明</span><span class="sxs-lookup"><span data-stu-id="34fb7-105">DESCRIPTION</span></span>
<span data-ttu-id="34fb7-106">從 ACR 刪除儲存庫。</span><span class="sxs-lookup"><span data-stu-id="34fb7-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="34fb7-107">示例</span><span class="sxs-lookup"><span data-stu-id="34fb7-107">EXAMPLES</span></span>

### <span data-ttu-id="34fb7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="34fb7-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="34fb7-109">刪除 [registry] 底下的 [知識庫測試/busybox15]。</span><span class="sxs-lookup"><span data-stu-id="34fb7-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="34fb7-110">參數</span><span class="sxs-lookup"><span data-stu-id="34fb7-110">PARAMETERS</span></span>

### <span data-ttu-id="34fb7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34fb7-111">-DefaultProfile</span></span>
<span data-ttu-id="34fb7-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="34fb7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34fb7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="34fb7-113">-Name</span></span>
<span data-ttu-id="34fb7-114">儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="34fb7-114">Repository Name.</span></span>

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

### <span data-ttu-id="34fb7-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="34fb7-115">-RegistryName</span></span>
<span data-ttu-id="34fb7-116">Azure 容器登錄名。</span><span class="sxs-lookup"><span data-stu-id="34fb7-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="34fb7-117">-確認</span><span class="sxs-lookup"><span data-stu-id="34fb7-117">-Confirm</span></span>
<span data-ttu-id="34fb7-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="34fb7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34fb7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34fb7-119">-WhatIf</span></span>
<span data-ttu-id="34fb7-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="34fb7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34fb7-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="34fb7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34fb7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34fb7-122">CommonParameters</span></span>
<span data-ttu-id="34fb7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="34fb7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34fb7-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="34fb7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34fb7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="34fb7-125">INPUTS</span></span>

### <span data-ttu-id="34fb7-126">System.object</span><span class="sxs-lookup"><span data-stu-id="34fb7-126">System.String</span></span>

## <span data-ttu-id="34fb7-127">輸出</span><span class="sxs-lookup"><span data-stu-id="34fb7-127">OUTPUTS</span></span>

### <span data-ttu-id="34fb7-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span><span class="sxs-lookup"><span data-stu-id="34fb7-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="34fb7-129">筆記</span><span class="sxs-lookup"><span data-stu-id="34fb7-129">NOTES</span></span>

## <span data-ttu-id="34fb7-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="34fb7-130">RELATED LINKS</span></span>
