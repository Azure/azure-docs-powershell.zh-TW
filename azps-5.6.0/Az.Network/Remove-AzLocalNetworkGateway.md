---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: c8e0e5a3d503b4fa587f2a0bdb284b059bff4eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912669"
---
# <span data-ttu-id="59625-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59625-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="59625-102">簡介</span><span class="sxs-lookup"><span data-stu-id="59625-102">SYNOPSIS</span></span>
<span data-ttu-id="59625-103">刪除本地網路閘道</span><span class="sxs-lookup"><span data-stu-id="59625-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="59625-104">語法</span><span class="sxs-lookup"><span data-stu-id="59625-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59625-105">描述</span><span class="sxs-lookup"><span data-stu-id="59625-105">DESCRIPTION</span></span>
<span data-ttu-id="59625-106">Local Network Gateway 是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="59625-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="59625-107">**Remove-AzLocalNetworkGateway** Cmdlet 會根據名稱和資源組名，刪除代表您 on-prem 閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="59625-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="59625-108">例子</span><span class="sxs-lookup"><span data-stu-id="59625-108">EXAMPLES</span></span>

### <span data-ttu-id="59625-109">範例 1：刪除本地網路閘道</span><span class="sxs-lookup"><span data-stu-id="59625-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="59625-110">刪除資源群組 "myLocalGW" 中名稱為 "myLocalGW" 的 Local Network Gateway 物件注意：您必須先刪除使用 **Remove-AzVirtualNetworkGatewayConnection** Cmdlet 到 Local Network 閘道的所有連結。</span><span class="sxs-lookup"><span data-stu-id="59625-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="59625-111">參數</span><span class="sxs-lookup"><span data-stu-id="59625-111">PARAMETERS</span></span>

### <span data-ttu-id="59625-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59625-112">-AsJob</span></span>
<span data-ttu-id="59625-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="59625-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="59625-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59625-114">-DefaultProfile</span></span>
<span data-ttu-id="59625-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="59625-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59625-116">-強制</span><span class="sxs-lookup"><span data-stu-id="59625-116">-Force</span></span>
<span data-ttu-id="59625-117">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="59625-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="59625-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="59625-118">-Name</span></span>
<span data-ttu-id="59625-119">指定此 Cmdlet 移除的當地網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="59625-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="59625-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59625-120">-PassThru</span></span>
<span data-ttu-id="59625-121">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="59625-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="59625-122">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="59625-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59625-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59625-123">-ResourceGroupName</span></span>
<span data-ttu-id="59625-124">指定包含本地網路閘道的資源組名。</span><span class="sxs-lookup"><span data-stu-id="59625-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="59625-125">-確認</span><span class="sxs-lookup"><span data-stu-id="59625-125">-Confirm</span></span>
<span data-ttu-id="59625-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="59625-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59625-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59625-127">-WhatIf</span></span>
<span data-ttu-id="59625-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="59625-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59625-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="59625-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59625-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59625-130">CommonParameters</span></span>
<span data-ttu-id="59625-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="59625-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59625-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="59625-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59625-133">輸入</span><span class="sxs-lookup"><span data-stu-id="59625-133">INPUTS</span></span>

### <span data-ttu-id="59625-134">System.String</span><span class="sxs-lookup"><span data-stu-id="59625-134">System.String</span></span>

## <span data-ttu-id="59625-135">輸出</span><span class="sxs-lookup"><span data-stu-id="59625-135">OUTPUTS</span></span>

### <span data-ttu-id="59625-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="59625-136">System.Boolean</span></span>

## <span data-ttu-id="59625-137">筆記</span><span class="sxs-lookup"><span data-stu-id="59625-137">NOTES</span></span>

## <span data-ttu-id="59625-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="59625-138">RELATED LINKS</span></span>

[<span data-ttu-id="59625-139">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59625-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="59625-140">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59625-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="59625-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="59625-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
