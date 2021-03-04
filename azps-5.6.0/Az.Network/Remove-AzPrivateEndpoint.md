---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 3e1caeb5dec11188cf824bdcddf2b0de78f707c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913382"
---
# <span data-ttu-id="36ac7-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36ac7-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="36ac7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="36ac7-102">SYNOPSIS</span></span>
<span data-ttu-id="36ac7-103">移除私人端點。</span><span class="sxs-lookup"><span data-stu-id="36ac7-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="36ac7-104">語法</span><span class="sxs-lookup"><span data-stu-id="36ac7-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36ac7-105">描述</span><span class="sxs-lookup"><span data-stu-id="36ac7-105">DESCRIPTION</span></span>
<span data-ttu-id="36ac7-106">**Remove-AzPrivateEndpoint** Cmdlet 會移除私人端點。</span><span class="sxs-lookup"><span data-stu-id="36ac7-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="36ac7-107">例子</span><span class="sxs-lookup"><span data-stu-id="36ac7-107">EXAMPLES</span></span>

### <span data-ttu-id="36ac7-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="36ac7-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="36ac7-109">此範例會移除名為 MyPrivateEndpoint1 的私人端點。</span><span class="sxs-lookup"><span data-stu-id="36ac7-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="36ac7-110">參數</span><span class="sxs-lookup"><span data-stu-id="36ac7-110">PARAMETERS</span></span>

### <span data-ttu-id="36ac7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36ac7-111">-AsJob</span></span>
<span data-ttu-id="36ac7-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36ac7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36ac7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ac7-113">-DefaultProfile</span></span>
<span data-ttu-id="36ac7-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="36ac7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36ac7-115">-強制</span><span class="sxs-lookup"><span data-stu-id="36ac7-115">-Force</span></span>
<span data-ttu-id="36ac7-116">如果您要刪除資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="36ac7-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="36ac7-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="36ac7-117">-Name</span></span>
<span data-ttu-id="36ac7-118">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="36ac7-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ac7-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36ac7-119">-PassThru</span></span>
<span data-ttu-id="36ac7-120">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="36ac7-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36ac7-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="36ac7-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="36ac7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ac7-122">-ResourceGroupName</span></span>
<span data-ttu-id="36ac7-123">私人端點的資源組名。</span><span class="sxs-lookup"><span data-stu-id="36ac7-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="36ac7-124">-確認</span><span class="sxs-lookup"><span data-stu-id="36ac7-124">-Confirm</span></span>
<span data-ttu-id="36ac7-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="36ac7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ac7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ac7-126">-WhatIf</span></span>
<span data-ttu-id="36ac7-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36ac7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36ac7-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36ac7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ac7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ac7-129">CommonParameters</span></span>
<span data-ttu-id="36ac7-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="36ac7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ac7-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36ac7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ac7-132">輸入</span><span class="sxs-lookup"><span data-stu-id="36ac7-132">INPUTS</span></span>

### <span data-ttu-id="36ac7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="36ac7-133">System.String</span></span>

## <span data-ttu-id="36ac7-134">輸出</span><span class="sxs-lookup"><span data-stu-id="36ac7-134">OUTPUTS</span></span>

### <span data-ttu-id="36ac7-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36ac7-135">System.Boolean</span></span>

## <span data-ttu-id="36ac7-136">筆記</span><span class="sxs-lookup"><span data-stu-id="36ac7-136">NOTES</span></span>

## <span data-ttu-id="36ac7-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="36ac7-137">RELATED LINKS</span></span>

[<span data-ttu-id="36ac7-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36ac7-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="36ac7-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="36ac7-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)