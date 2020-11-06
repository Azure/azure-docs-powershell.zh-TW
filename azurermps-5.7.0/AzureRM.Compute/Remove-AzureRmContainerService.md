---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: da4f9846f8fceaaecc6d4385374f6525d3243e3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446360"
---
# <span data-ttu-id="43e97-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="43e97-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="43e97-102">摘要</span><span class="sxs-lookup"><span data-stu-id="43e97-102">SYNOPSIS</span></span>
<span data-ttu-id="43e97-103">移除容器服務。</span><span class="sxs-lookup"><span data-stu-id="43e97-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43e97-104">句法</span><span class="sxs-lookup"><span data-stu-id="43e97-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43e97-105">說明</span><span class="sxs-lookup"><span data-stu-id="43e97-105">DESCRIPTION</span></span>
<span data-ttu-id="43e97-106">**AzureRmContainerService** Cmdlet 會從您的 Azure 帳戶中移除容器服務。</span><span class="sxs-lookup"><span data-stu-id="43e97-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="43e97-107">示例</span><span class="sxs-lookup"><span data-stu-id="43e97-107">EXAMPLES</span></span>

### <span data-ttu-id="43e97-108">範例1：移除容器服務</span><span class="sxs-lookup"><span data-stu-id="43e97-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="43e97-109">這個命令會移除名為 CSResourceGroup17 的容器服務。</span><span class="sxs-lookup"><span data-stu-id="43e97-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="43e97-110">參數</span><span class="sxs-lookup"><span data-stu-id="43e97-110">PARAMETERS</span></span>

### <span data-ttu-id="43e97-111">-Force</span><span class="sxs-lookup"><span data-stu-id="43e97-111">-Force</span></span>
<span data-ttu-id="43e97-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="43e97-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e97-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="43e97-113">-Name</span></span>
<span data-ttu-id="43e97-114">指定此 Cmdlet 移除的容器服務名稱。</span><span class="sxs-lookup"><span data-stu-id="43e97-114">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43e97-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43e97-115">-ResourceGroupName</span></span>
<span data-ttu-id="43e97-116">指定此 Cmdlet 移除之容器服務的 [資源] 群組。</span><span class="sxs-lookup"><span data-stu-id="43e97-116">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43e97-117">-確認</span><span class="sxs-lookup"><span data-stu-id="43e97-117">-Confirm</span></span>
<span data-ttu-id="43e97-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="43e97-118">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e97-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43e97-119">-WhatIf</span></span>
<span data-ttu-id="43e97-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="43e97-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="43e97-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="43e97-121">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43e97-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43e97-122">CommonParameters</span></span>
<span data-ttu-id="43e97-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="43e97-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43e97-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="43e97-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43e97-125">輸入</span><span class="sxs-lookup"><span data-stu-id="43e97-125">INPUTS</span></span>

### <span data-ttu-id="43e97-126">所有</span><span class="sxs-lookup"><span data-stu-id="43e97-126">None</span></span>
<span data-ttu-id="43e97-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="43e97-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="43e97-128">輸出</span><span class="sxs-lookup"><span data-stu-id="43e97-128">OUTPUTS</span></span>

## <span data-ttu-id="43e97-129">筆記</span><span class="sxs-lookup"><span data-stu-id="43e97-129">NOTES</span></span>

## <span data-ttu-id="43e97-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="43e97-130">RELATED LINKS</span></span>

[<span data-ttu-id="43e97-131">AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="43e97-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="43e97-132">新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="43e97-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="43e97-133">更新-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="43e97-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)

