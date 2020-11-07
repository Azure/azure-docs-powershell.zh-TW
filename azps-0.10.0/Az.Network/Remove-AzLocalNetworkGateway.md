---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 75E30205-97AD-44E3-A61F-62B81ADB532C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLocalNetworkGateway.md
ms.openlocfilehash: 0589fa3f5dd806149c243557b547455af35178b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794166"
---
# <span data-ttu-id="36fbc-101">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36fbc-101">Remove-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="36fbc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="36fbc-103">刪除局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="36fbc-103">Deletes a Local Network Gateway</span></span>

## <span data-ttu-id="36fbc-104">句法</span><span class="sxs-lookup"><span data-stu-id="36fbc-104">SYNTAX</span></span>

```
Remove-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36fbc-105">說明</span><span class="sxs-lookup"><span data-stu-id="36fbc-105">DESCRIPTION</span></span>
<span data-ttu-id="36fbc-106">本機網路閘道是代表您的 VPN 裝置內部部署的物件。</span><span class="sxs-lookup"><span data-stu-id="36fbc-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="36fbc-107">**AzLocalNetworkGateway** Cmdlet 會根據名稱和資源群組名稱，刪除代表您的內部部署閘道的物件。</span><span class="sxs-lookup"><span data-stu-id="36fbc-107">The **Remove-AzLocalNetworkGateway** cmdlet deletes the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="36fbc-108">示例</span><span class="sxs-lookup"><span data-stu-id="36fbc-108">EXAMPLES</span></span>

### <span data-ttu-id="36fbc-109">1：刪除局域網路閘道</span><span class="sxs-lookup"><span data-stu-id="36fbc-109">1: Delete a Local Network Gateway</span></span>
```
Remove-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="36fbc-110">刪除資源群組 "myRG" 中名稱為 "myLocalGW" 的本機網路閘道物件</span><span class="sxs-lookup"><span data-stu-id="36fbc-110">Deletes the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

<span data-ttu-id="36fbc-111">注意：您必須先使用 **AzVirtualNetworkGatewayConnection** Cmdlet 刪除到本機網路閘道的所有連線。</span><span class="sxs-lookup"><span data-stu-id="36fbc-111">Note: You must first delete all connections to the Local Network Gateway using the **Remove-AzVirtualNetworkGatewayConnection** cmdlet.</span></span>

## <span data-ttu-id="36fbc-112">參數</span><span class="sxs-lookup"><span data-stu-id="36fbc-112">PARAMETERS</span></span>

### <span data-ttu-id="36fbc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36fbc-113">-AsJob</span></span>
<span data-ttu-id="36fbc-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="36fbc-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36fbc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36fbc-115">-DefaultProfile</span></span>
<span data-ttu-id="36fbc-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="36fbc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36fbc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="36fbc-117">-Force</span></span>
<span data-ttu-id="36fbc-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="36fbc-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36fbc-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="36fbc-119">-Name</span></span>
<span data-ttu-id="36fbc-120">指定此 Cmdlet 移除之本機網路閘道的名稱。</span><span class="sxs-lookup"><span data-stu-id="36fbc-120">Specifies the name of the local network gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36fbc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36fbc-121">-PassThru</span></span>
<span data-ttu-id="36fbc-122">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="36fbc-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="36fbc-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="36fbc-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36fbc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36fbc-124">-ResourceGroupName</span></span>
<span data-ttu-id="36fbc-125">指定包含局域網閘道之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36fbc-125">Specifies the name of the resource group that contains the local network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36fbc-126">-確認</span><span class="sxs-lookup"><span data-stu-id="36fbc-126">-Confirm</span></span>
<span data-ttu-id="36fbc-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="36fbc-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36fbc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36fbc-128">-WhatIf</span></span>
<span data-ttu-id="36fbc-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36fbc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36fbc-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36fbc-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36fbc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36fbc-131">CommonParameters</span></span>
<span data-ttu-id="36fbc-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36fbc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36fbc-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="36fbc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36fbc-134">輸入</span><span class="sxs-lookup"><span data-stu-id="36fbc-134">INPUTS</span></span>

## <span data-ttu-id="36fbc-135">輸出</span><span class="sxs-lookup"><span data-stu-id="36fbc-135">OUTPUTS</span></span>

## <span data-ttu-id="36fbc-136">筆記</span><span class="sxs-lookup"><span data-stu-id="36fbc-136">NOTES</span></span>

## <span data-ttu-id="36fbc-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="36fbc-137">RELATED LINKS</span></span>

[<span data-ttu-id="36fbc-138">AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36fbc-138">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="36fbc-139">新-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36fbc-139">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="36fbc-140">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="36fbc-140">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)


