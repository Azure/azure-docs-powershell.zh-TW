---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288251"
---
# <span data-ttu-id="3f1a4-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f1a4-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="3f1a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f1a4-102">SYNOPSIS</span></span>
<span data-ttu-id="3f1a4-103">移除私有端點。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="3f1a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f1a4-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f1a4-105">說明</span><span class="sxs-lookup"><span data-stu-id="3f1a4-105">DESCRIPTION</span></span>
<span data-ttu-id="3f1a4-106">**AzPrivateEndpoint** Cmdlet 會移除私人端點。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="3f1a4-107">示例</span><span class="sxs-lookup"><span data-stu-id="3f1a4-107">EXAMPLES</span></span>

### <span data-ttu-id="3f1a4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3f1a4-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="3f1a4-109">這個範例會移除名為 MyPrivateEndpoint1 的私人端點。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="3f1a4-110">參數</span><span class="sxs-lookup"><span data-stu-id="3f1a4-110">PARAMETERS</span></span>

### <span data-ttu-id="3f1a4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f1a4-111">-AsJob</span></span>
<span data-ttu-id="3f1a4-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3f1a4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f1a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f1a4-113">-DefaultProfile</span></span>
<span data-ttu-id="3f1a4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f1a4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3f1a4-115">-Force</span></span>
<span data-ttu-id="3f1a4-116">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="3f1a4-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="3f1a4-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="3f1a4-117">-Name</span></span>
<span data-ttu-id="3f1a4-118">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="3f1a4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f1a4-119">-PassThru</span></span>
<span data-ttu-id="3f1a4-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3f1a4-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f1a4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f1a4-122">-ResourceGroupName</span></span>
<span data-ttu-id="3f1a4-123">私人端點的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="3f1a4-124">-確認</span><span class="sxs-lookup"><span data-stu-id="3f1a4-124">-Confirm</span></span>
<span data-ttu-id="3f1a4-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f1a4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f1a4-126">-WhatIf</span></span>
<span data-ttu-id="3f1a4-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f1a4-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f1a4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f1a4-129">CommonParameters</span></span>
<span data-ttu-id="3f1a4-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f1a4-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3f1a4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f1a4-132">輸入</span><span class="sxs-lookup"><span data-stu-id="3f1a4-132">INPUTS</span></span>

### <span data-ttu-id="3f1a4-133">System.object</span><span class="sxs-lookup"><span data-stu-id="3f1a4-133">System.String</span></span>

## <span data-ttu-id="3f1a4-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3f1a4-134">OUTPUTS</span></span>

### <span data-ttu-id="3f1a4-135">System.object</span><span class="sxs-lookup"><span data-stu-id="3f1a4-135">System.Boolean</span></span>

## <span data-ttu-id="3f1a4-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3f1a4-136">NOTES</span></span>

## <span data-ttu-id="3f1a4-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f1a4-137">RELATED LINKS</span></span>

[<span data-ttu-id="3f1a4-138">AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f1a4-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="3f1a4-139">新-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f1a4-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)