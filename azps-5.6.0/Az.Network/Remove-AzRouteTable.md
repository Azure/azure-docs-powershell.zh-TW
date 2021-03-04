---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: FDA33633-EB2E-4095-8498-DF8910F1D434
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzRouteTable.md
ms.openlocfilehash: df0c4f25491493254801006b443178ad1efdc537
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915994"
---
# <span data-ttu-id="b3200-101">Remove-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3200-101">Remove-AzRouteTable</span></span>

## <span data-ttu-id="b3200-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3200-102">SYNOPSIS</span></span>
<span data-ttu-id="b3200-103">移除路由資料表。</span><span class="sxs-lookup"><span data-stu-id="b3200-103">Removes a route table.</span></span>

## <span data-ttu-id="b3200-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3200-104">SYNTAX</span></span>

```
Remove-AzRouteTable -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3200-105">描述</span><span class="sxs-lookup"><span data-stu-id="b3200-105">DESCRIPTION</span></span>
<span data-ttu-id="b3200-106">**Remove-AzRouteTable** Cmdlet 會移除 Azure 路由資料表。</span><span class="sxs-lookup"><span data-stu-id="b3200-106">The **Remove-AzRouteTable** cmdlet removes an Azure route table.</span></span>

## <span data-ttu-id="b3200-107">例子</span><span class="sxs-lookup"><span data-stu-id="b3200-107">EXAMPLES</span></span>

### <span data-ttu-id="b3200-108">範例 1：移除路由資料表</span><span class="sxs-lookup"><span data-stu-id="b3200-108">Example 1: Remove a route table</span></span>
```
PS C:\>Remove-AzRouteTable -ResourceGroupName "ResourceGroup11 -Name "RouteTable01"
Confirm
Are you sure you want to remove resource 'RouteTable01'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="b3200-109">此命令會移除名為 ResourceGroup11 的資源群組中名為 RouteTable01 的路由資料表。</span><span class="sxs-lookup"><span data-stu-id="b3200-109">This command removes the route table named RouteTable01 in the resource group named ResourceGroup11.</span></span>
<span data-ttu-id="b3200-110">Cmdlet 會先提示您確認，然後再移除表格。</span><span class="sxs-lookup"><span data-stu-id="b3200-110">The cmdlet prompts you for confirmation before it removes the table.</span></span>

## <span data-ttu-id="b3200-111">參數</span><span class="sxs-lookup"><span data-stu-id="b3200-111">PARAMETERS</span></span>

### <span data-ttu-id="b3200-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3200-112">-AsJob</span></span>
<span data-ttu-id="b3200-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b3200-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b3200-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3200-114">-DefaultProfile</span></span>
<span data-ttu-id="b3200-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3200-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3200-116">-強制</span><span class="sxs-lookup"><span data-stu-id="b3200-116">-Force</span></span>
<span data-ttu-id="b3200-117">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b3200-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3200-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3200-118">-Name</span></span>
<span data-ttu-id="b3200-119">指定此 Cmdlet 移除的路由資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="b3200-119">Specifies the name of the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b3200-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3200-120">-PassThru</span></span>
<span data-ttu-id="b3200-121">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b3200-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b3200-122">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b3200-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3200-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3200-123">-ResourceGroupName</span></span>
<span data-ttu-id="b3200-124">指定包含此 Cmdlet 移除之路由資料表的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b3200-124">Specifies the name of the resource group that contains the route table that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b3200-125">-確認</span><span class="sxs-lookup"><span data-stu-id="b3200-125">-Confirm</span></span>
<span data-ttu-id="b3200-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3200-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3200-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3200-127">-WhatIf</span></span>
<span data-ttu-id="b3200-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3200-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3200-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3200-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3200-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3200-130">CommonParameters</span></span>
<span data-ttu-id="b3200-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3200-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3200-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b3200-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3200-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b3200-133">INPUTS</span></span>

### <span data-ttu-id="b3200-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b3200-134">System.String</span></span>

## <span data-ttu-id="b3200-135">輸出</span><span class="sxs-lookup"><span data-stu-id="b3200-135">OUTPUTS</span></span>

### <span data-ttu-id="b3200-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3200-136">System.Boolean</span></span>

## <span data-ttu-id="b3200-137">筆記</span><span class="sxs-lookup"><span data-stu-id="b3200-137">NOTES</span></span>

## <span data-ttu-id="b3200-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3200-138">RELATED LINKS</span></span>

[<span data-ttu-id="b3200-139">Get-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3200-139">Get-AzRouteTable</span></span>](./Get-AzRouteTable.md)

[<span data-ttu-id="b3200-140">New-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3200-140">New-AzRouteTable</span></span>](./New-AzRouteTable.md)

[<span data-ttu-id="b3200-141">Set-AzRouteTable</span><span class="sxs-lookup"><span data-stu-id="b3200-141">Set-AzRouteTable</span></span>](./Set-AzRouteTable.md)


