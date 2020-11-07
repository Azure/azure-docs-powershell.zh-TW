---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: 1f0b539e2f5a6e2c387738558fb6db8cbe647457
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791510"
---
# <span data-ttu-id="96c03-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="96c03-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="96c03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96c03-102">SYNOPSIS</span></span>
<span data-ttu-id="96c03-103">啟動虛擬網路閘道的 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="96c03-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="96c03-104">句法</span><span class="sxs-lookup"><span data-stu-id="96c03-104">SYNTAX</span></span>

### <span data-ttu-id="96c03-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="96c03-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c03-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="96c03-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c03-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="96c03-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96c03-108">說明</span><span class="sxs-lookup"><span data-stu-id="96c03-108">DESCRIPTION</span></span>
<span data-ttu-id="96c03-109">啟動虛擬網路閘道的 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="96c03-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="96c03-110">示例</span><span class="sxs-lookup"><span data-stu-id="96c03-110">EXAMPLES</span></span>

### <span data-ttu-id="96c03-111">範例1</span><span class="sxs-lookup"><span data-stu-id="96c03-111">Example 1</span></span>
```powershell
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="96c03-112">範例2</span><span class="sxs-lookup"><span data-stu-id="96c03-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

## <span data-ttu-id="96c03-113">參數</span><span class="sxs-lookup"><span data-stu-id="96c03-113">PARAMETERS</span></span>

### <span data-ttu-id="96c03-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96c03-114">-AsJob</span></span>
<span data-ttu-id="96c03-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="96c03-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96c03-116">-確認</span><span class="sxs-lookup"><span data-stu-id="96c03-116">-Confirm</span></span>
<span data-ttu-id="96c03-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="96c03-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96c03-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c03-118">-DefaultProfile</span></span>
<span data-ttu-id="96c03-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96c03-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96c03-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="96c03-120">-FilterData</span></span>
<span data-ttu-id="96c03-121">在虛擬網路閘道開始進行資料包捕獲的篩選選項。</span><span class="sxs-lookup"><span data-stu-id="96c03-121">Filter options for start packet capture on virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96c03-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96c03-122">-InputObject</span></span>
<span data-ttu-id="96c03-123">要開始進行資料包捕獲的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="96c03-123">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96c03-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="96c03-124">-Name</span></span>
<span data-ttu-id="96c03-125">要在其中開始進行資料包捕獲的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="96c03-125">The virtual network gateway name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96c03-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c03-126">-ResourceGroupName</span></span>
<span data-ttu-id="96c03-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96c03-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96c03-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96c03-128">-ResourceId</span></span>
<span data-ttu-id="96c03-129">要開始進行資料包捕獲之 VirtualNetworkGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="96c03-129">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96c03-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c03-130">-WhatIf</span></span>
<span data-ttu-id="96c03-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="96c03-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96c03-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="96c03-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96c03-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c03-133">CommonParameters</span></span>
<span data-ttu-id="96c03-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96c03-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c03-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="96c03-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c03-136">輸入</span><span class="sxs-lookup"><span data-stu-id="96c03-136">INPUTS</span></span>

### <span data-ttu-id="96c03-137">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="96c03-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="96c03-138">System.object</span><span class="sxs-lookup"><span data-stu-id="96c03-138">System.String</span></span>

## <span data-ttu-id="96c03-139">輸出</span><span class="sxs-lookup"><span data-stu-id="96c03-139">OUTPUTS</span></span>

### <span data-ttu-id="96c03-140">PSVirtualNetworkGatewayPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="96c03-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="96c03-141">筆記</span><span class="sxs-lookup"><span data-stu-id="96c03-141">NOTES</span></span>

## <span data-ttu-id="96c03-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="96c03-142">RELATED LINKS</span></span>
[<span data-ttu-id="96c03-143">停止 AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="96c03-143">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)