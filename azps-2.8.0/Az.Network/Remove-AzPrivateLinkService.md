---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: 3b0ba9527ca7d0354429a90439bbe33d973bf550
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789113"
---
# <span data-ttu-id="12440-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="12440-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="12440-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12440-102">SYNOPSIS</span></span>
<span data-ttu-id="12440-103">移除私人連結服務</span><span class="sxs-lookup"><span data-stu-id="12440-103">Removes a private link service</span></span>

## <span data-ttu-id="12440-104">句法</span><span class="sxs-lookup"><span data-stu-id="12440-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12440-105">說明</span><span class="sxs-lookup"><span data-stu-id="12440-105">DESCRIPTION</span></span>
<span data-ttu-id="12440-106">**AzPrivateLinkService** Cmdlet 會移除私人連結服務</span><span class="sxs-lookup"><span data-stu-id="12440-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="12440-107">示例</span><span class="sxs-lookup"><span data-stu-id="12440-107">EXAMPLES</span></span>

### <span data-ttu-id="12440-108">範例1</span><span class="sxs-lookup"><span data-stu-id="12440-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="12440-109">這個範例會移除名為 TestPrivateLinkService 的私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="12440-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="12440-110">參數</span><span class="sxs-lookup"><span data-stu-id="12440-110">PARAMETERS</span></span>

### <span data-ttu-id="12440-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12440-111">-AsJob</span></span>
<span data-ttu-id="12440-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="12440-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12440-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12440-113">-DefaultProfile</span></span>
<span data-ttu-id="12440-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12440-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12440-115">-Force</span><span class="sxs-lookup"><span data-stu-id="12440-115">-Force</span></span>
<span data-ttu-id="12440-116">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="12440-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="12440-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="12440-117">-Name</span></span>
<span data-ttu-id="12440-118">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="12440-118">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12440-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12440-119">-PassThru</span></span>
<span data-ttu-id="12440-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="12440-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="12440-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="12440-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="12440-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12440-122">-ResourceGroupName</span></span>
<span data-ttu-id="12440-123">私人連結服務的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="12440-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="12440-124">-確認</span><span class="sxs-lookup"><span data-stu-id="12440-124">-Confirm</span></span>
<span data-ttu-id="12440-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12440-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12440-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12440-126">-WhatIf</span></span>
<span data-ttu-id="12440-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12440-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12440-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12440-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12440-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12440-129">CommonParameters</span></span>
<span data-ttu-id="12440-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12440-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12440-131">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="12440-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12440-132">輸入</span><span class="sxs-lookup"><span data-stu-id="12440-132">INPUTS</span></span>

### <span data-ttu-id="12440-133">System.object</span><span class="sxs-lookup"><span data-stu-id="12440-133">System.String</span></span>

## <span data-ttu-id="12440-134">輸出</span><span class="sxs-lookup"><span data-stu-id="12440-134">OUTPUTS</span></span>

### <span data-ttu-id="12440-135">System.object</span><span class="sxs-lookup"><span data-stu-id="12440-135">System.Boolean</span></span>

## <span data-ttu-id="12440-136">筆記</span><span class="sxs-lookup"><span data-stu-id="12440-136">NOTES</span></span>

## <span data-ttu-id="12440-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="12440-137">RELATED LINKS</span></span>

[<span data-ttu-id="12440-138">AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="12440-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="12440-139">新-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="12440-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)