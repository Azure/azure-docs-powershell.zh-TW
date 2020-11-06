---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: c09e812762867dc6aa89945f50d9658bb61bf5a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446928"
---
# <span data-ttu-id="2edba-101">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2edba-101">Remove-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="2edba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2edba-102">SYNOPSIS</span></span>
<span data-ttu-id="2edba-103">刪除局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="2edba-103">Deletes a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2edba-104">句法</span><span class="sxs-lookup"><span data-stu-id="2edba-104">SYNTAX</span></span>

```
Remove-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2edba-105">說明</span><span class="sxs-lookup"><span data-stu-id="2edba-105">DESCRIPTION</span></span>
<span data-ttu-id="2edba-106">本機網路閘道是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="2edba-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="2edba-107">**AzureRmLocalNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，刪除代表您的內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="2edba-107">The **Remove-AzureRmLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="2edba-108">示例</span><span class="sxs-lookup"><span data-stu-id="2edba-108">EXAMPLES</span></span>

### <span data-ttu-id="2edba-109">1：刪除局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="2edba-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="2edba-110">在資源群組 "myRG" 中刪除名為 "myLocalGW" 的本機網路閘道物件：您必須先使用 **Remove-AzureRmVirtualNetworkGatewayConnection** Cmdlet 刪除到本機網路閘道的所有連線。</span><span class="sxs-lookup"><span data-stu-id="2edba-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzureRmVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="2edba-111">參數</span><span class="sxs-lookup"><span data-stu-id="2edba-111">PARAMETERS</span></span>

### <span data-ttu-id="2edba-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2edba-112">-AsJob</span></span>
<span data-ttu-id="2edba-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2edba-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2edba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2edba-114">-DefaultProfile</span></span>
<span data-ttu-id="2edba-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2edba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2edba-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2edba-116">-Force</span></span>
<span data-ttu-id="2edba-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2edba-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2edba-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="2edba-118">-Name</span></span>
<span data-ttu-id="2edba-119">指定此 Cmdlet 移除之本機網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="2edba-119">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2edba-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2edba-120">-PassThru</span></span>
<span data-ttu-id="2edba-121">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="2edba-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2edba-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2edba-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2edba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2edba-123">-ResourceGroupName</span></span>
<span data-ttu-id="2edba-124">指定包含局域網閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2edba-124">Specifies the name of the resource group that contains the local network gateway.</span></span>

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

### <span data-ttu-id="2edba-125">-確認</span><span class="sxs-lookup"><span data-stu-id="2edba-125">-Confirm</span></span>
<span data-ttu-id="2edba-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2edba-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2edba-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2edba-127">-WhatIf</span></span>
<span data-ttu-id="2edba-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2edba-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2edba-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2edba-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2edba-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2edba-130">CommonParameters</span></span>
<span data-ttu-id="2edba-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2edba-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2edba-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2edba-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2edba-133">輸入</span><span class="sxs-lookup"><span data-stu-id="2edba-133">INPUTS</span></span>

### <span data-ttu-id="2edba-134">System.object</span><span class="sxs-lookup"><span data-stu-id="2edba-134">System.String</span></span>

## <span data-ttu-id="2edba-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2edba-135">OUTPUTS</span></span>

### <span data-ttu-id="2edba-136">System.object</span><span class="sxs-lookup"><span data-stu-id="2edba-136">System.Boolean</span></span>

## <span data-ttu-id="2edba-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2edba-137">NOTES</span></span>

## <span data-ttu-id="2edba-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2edba-138">RELATED LINKS</span></span>

[<span data-ttu-id="2edba-139">AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2edba-139">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="2edba-140">新-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2edba-140">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="2edba-141">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2edba-141">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)


