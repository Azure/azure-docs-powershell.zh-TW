---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 8c3741f7e1a3e25dfbc3a3b6f7fb655e5db19fe8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142133"
---
# <span data-ttu-id="13042-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="13042-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="13042-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13042-102">SYNOPSIS</span></span>
<span data-ttu-id="13042-103">刪除局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="13042-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="13042-104">句法</span><span class="sxs-lookup"><span data-stu-id="13042-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13042-105">說明</span><span class="sxs-lookup"><span data-stu-id="13042-105">DESCRIPTION</span></span>
<span data-ttu-id="13042-106">本機網路閘道是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="13042-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="13042-107">**AzLocalNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，刪除代表您的內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="13042-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="13042-108">示例</span><span class="sxs-lookup"><span data-stu-id="13042-108">EXAMPLES</span></span>

### <span data-ttu-id="13042-109">範例1：刪除局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="13042-109">Example 1: Delete a Local Network Gateway</span></span>
```powershell
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="13042-110">在資源群組 "myRG" 中刪除名為 "myLocalGW" 的本機網路閘道物件：您必須先使用 **Remove-AzVirtualNetworkGatewayConnection** Cmdlet 刪除到本機網路閘道的所有連線。</span><span class="sxs-lookup"><span data-stu-id="13042-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="13042-111">參數</span><span class="sxs-lookup"><span data-stu-id="13042-111">PARAMETERS</span></span>

### <span data-ttu-id="13042-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="13042-112">-AsJob</span></span>
<span data-ttu-id="13042-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="13042-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="13042-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13042-114">-DefaultProfile</span></span>
<span data-ttu-id="13042-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13042-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13042-116">-Force</span><span class="sxs-lookup"><span data-stu-id="13042-116">-Force</span></span>
<span data-ttu-id="13042-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="13042-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="13042-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="13042-118">-Name</span></span>
<span data-ttu-id="13042-119">指定此 Cmdlet 移除之本機網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="13042-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="13042-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="13042-120">-PassThru</span></span>
<span data-ttu-id="13042-121">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="13042-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="13042-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="13042-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="13042-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13042-123">-ResourceGroupName</span></span>
<span data-ttu-id="13042-124">指定包含局域網閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13042-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="13042-125">-確認</span><span class="sxs-lookup"><span data-stu-id="13042-125">-Confirm</span></span>
<span data-ttu-id="13042-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13042-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13042-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13042-127">-WhatIf</span></span>
<span data-ttu-id="13042-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13042-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13042-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13042-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13042-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13042-130">CommonParameters</span></span>
<span data-ttu-id="13042-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13042-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13042-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13042-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13042-133">輸入</span><span class="sxs-lookup"><span data-stu-id="13042-133">INPUTS</span></span>

### <span data-ttu-id="13042-134">System.object</span><span class="sxs-lookup"><span data-stu-id="13042-134">System.String</span></span>

## <span data-ttu-id="13042-135">輸出</span><span class="sxs-lookup"><span data-stu-id="13042-135">OUTPUTS</span></span>

### <span data-ttu-id="13042-136">System.object</span><span class="sxs-lookup"><span data-stu-id="13042-136">System.Boolean</span></span>

## <span data-ttu-id="13042-137">筆記</span><span class="sxs-lookup"><span data-stu-id="13042-137">NOTES</span></span>

## <span data-ttu-id="13042-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="13042-138">RELATED LINKS</span></span>

[<span data-ttu-id="13042-139">AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="13042-139">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="13042-140">新-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="13042-140">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="13042-141">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="13042-141">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
