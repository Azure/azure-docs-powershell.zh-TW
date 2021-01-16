---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 716606214bcd23bd51286fa3a7a0e4f8c0c4ff70
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281711"
---
# <span data-ttu-id="961d1-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="961d1-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="961d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="961d1-102">SYNOPSIS</span></span>
<span data-ttu-id="961d1-103">移除私有端點。</span><span class="sxs-lookup"><span data-stu-id="961d1-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="961d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="961d1-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="961d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="961d1-105">DESCRIPTION</span></span>
<span data-ttu-id="961d1-106">**AzPrivateEndpoint** Cmdlet 會移除私人端點。</span><span class="sxs-lookup"><span data-stu-id="961d1-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="961d1-107">示例</span><span class="sxs-lookup"><span data-stu-id="961d1-107">EXAMPLES</span></span>

### <span data-ttu-id="961d1-108">範例1</span><span class="sxs-lookup"><span data-stu-id="961d1-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="961d1-109">這個範例會移除名為 MyPrivateEndpoint1 的私人端點。</span><span class="sxs-lookup"><span data-stu-id="961d1-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="961d1-110">參數</span><span class="sxs-lookup"><span data-stu-id="961d1-110">PARAMETERS</span></span>

### <span data-ttu-id="961d1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="961d1-111">-AsJob</span></span>
<span data-ttu-id="961d1-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="961d1-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="961d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="961d1-113">-DefaultProfile</span></span>
<span data-ttu-id="961d1-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="961d1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="961d1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="961d1-115">-Force</span></span>
<span data-ttu-id="961d1-116">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="961d1-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="961d1-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="961d1-117">-Name</span></span>
<span data-ttu-id="961d1-118">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="961d1-118">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="961d1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="961d1-119">-PassThru</span></span>
<span data-ttu-id="961d1-120">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="961d1-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="961d1-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="961d1-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="961d1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="961d1-122">-ResourceGroupName</span></span>
<span data-ttu-id="961d1-123">私人端點的資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="961d1-123">The resource group name of the private endpoint.</span></span>

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

### <span data-ttu-id="961d1-124">-確認</span><span class="sxs-lookup"><span data-stu-id="961d1-124">-Confirm</span></span>
<span data-ttu-id="961d1-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="961d1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="961d1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="961d1-126">-WhatIf</span></span>
<span data-ttu-id="961d1-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="961d1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="961d1-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="961d1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="961d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="961d1-129">CommonParameters</span></span>
<span data-ttu-id="961d1-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="961d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="961d1-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="961d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="961d1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="961d1-132">INPUTS</span></span>

### <span data-ttu-id="961d1-133">System.object</span><span class="sxs-lookup"><span data-stu-id="961d1-133">System.String</span></span>

## <span data-ttu-id="961d1-134">輸出</span><span class="sxs-lookup"><span data-stu-id="961d1-134">OUTPUTS</span></span>

### <span data-ttu-id="961d1-135">System.object</span><span class="sxs-lookup"><span data-stu-id="961d1-135">System.Boolean</span></span>

## <span data-ttu-id="961d1-136">筆記</span><span class="sxs-lookup"><span data-stu-id="961d1-136">NOTES</span></span>

## <span data-ttu-id="961d1-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="961d1-137">RELATED LINKS</span></span>

[<span data-ttu-id="961d1-138">AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="961d1-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="961d1-139">新-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="961d1-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)