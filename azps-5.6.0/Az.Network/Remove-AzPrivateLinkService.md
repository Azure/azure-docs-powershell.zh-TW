---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatelinkservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateLinkService.md
ms.openlocfilehash: e06a29422a7abed55dbf1e8508c8715a36cf7d76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913377"
---
# <span data-ttu-id="b4c72-101">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4c72-101">Remove-AzPrivateLinkService</span></span>

## <span data-ttu-id="b4c72-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b4c72-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c72-103">移除私人連結服務</span><span class="sxs-lookup"><span data-stu-id="b4c72-103">Removes a private link service</span></span>

## <span data-ttu-id="b4c72-104">語法</span><span class="sxs-lookup"><span data-stu-id="b4c72-104">SYNTAX</span></span>

```
Remove-AzPrivateLinkService -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4c72-105">描述</span><span class="sxs-lookup"><span data-stu-id="b4c72-105">DESCRIPTION</span></span>
<span data-ttu-id="b4c72-106">**Remove-AzPrivateLinkService** Cmdlet 會移除私人連結服務</span><span class="sxs-lookup"><span data-stu-id="b4c72-106">The **Remove-AzPrivateLinkService** cmdlet removes a private link service</span></span>

## <span data-ttu-id="b4c72-107">例子</span><span class="sxs-lookup"><span data-stu-id="b4c72-107">EXAMPLES</span></span>

### <span data-ttu-id="b4c72-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b4c72-108">Example 1</span></span>
```
Remove-AzPrivateLinkService -ResourceGroupName TestResourceGroup -Name TestPrivateLinkService
```

<span data-ttu-id="b4c72-109">此範例會移除名為 TestPrivateLinkService 的私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="b4c72-109">This example removes a private link service named TestPrivateLinkService.</span></span>

## <span data-ttu-id="b4c72-110">參數</span><span class="sxs-lookup"><span data-stu-id="b4c72-110">PARAMETERS</span></span>

### <span data-ttu-id="b4c72-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4c72-111">-AsJob</span></span>
<span data-ttu-id="b4c72-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b4c72-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4c72-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c72-113">-DefaultProfile</span></span>
<span data-ttu-id="b4c72-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b4c72-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4c72-115">-強制</span><span class="sxs-lookup"><span data-stu-id="b4c72-115">-Force</span></span>
<span data-ttu-id="b4c72-116">如果您要刪除資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="b4c72-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="b4c72-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="b4c72-117">-Name</span></span>
<span data-ttu-id="b4c72-118">服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4c72-118">The name of the service.</span></span>

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

### <span data-ttu-id="b4c72-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4c72-119">-PassThru</span></span>
<span data-ttu-id="b4c72-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b4c72-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b4c72-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b4c72-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b4c72-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4c72-122">-ResourceGroupName</span></span>
<span data-ttu-id="b4c72-123">私人連結服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b4c72-123">The resource group name of the private link service.</span></span>

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

### <span data-ttu-id="b4c72-124">-確認</span><span class="sxs-lookup"><span data-stu-id="b4c72-124">-Confirm</span></span>
<span data-ttu-id="b4c72-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b4c72-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4c72-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4c72-126">-WhatIf</span></span>
<span data-ttu-id="b4c72-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b4c72-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4c72-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b4c72-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4c72-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c72-129">CommonParameters</span></span>
<span data-ttu-id="b4c72-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b4c72-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c72-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4c72-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4c72-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b4c72-132">INPUTS</span></span>

### <span data-ttu-id="b4c72-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b4c72-133">System.String</span></span>

## <span data-ttu-id="b4c72-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b4c72-134">OUTPUTS</span></span>

### <span data-ttu-id="b4c72-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4c72-135">System.Boolean</span></span>

## <span data-ttu-id="b4c72-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b4c72-136">NOTES</span></span>

## <span data-ttu-id="b4c72-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b4c72-137">RELATED LINKS</span></span>

[<span data-ttu-id="b4c72-138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4c72-138">Get-AzPrivateLinkService</span></span>](./Get-AzPrivateLinkService.md)

[<span data-ttu-id="b4c72-139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="b4c72-139">New-AzPrivateLinkService</span></span>](./New-AzPrivateLinkService.md)