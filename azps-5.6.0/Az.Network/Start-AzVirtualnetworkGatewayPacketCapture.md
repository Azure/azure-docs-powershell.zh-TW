---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: 4f17777d366884f2b71c16c289e50dbf8425d729
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901894"
---
# <span data-ttu-id="d0a77-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0a77-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="d0a77-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d0a77-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a77-103">在虛擬網路閘道上啟動封包捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="d0a77-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="d0a77-104">語法</span><span class="sxs-lookup"><span data-stu-id="d0a77-104">SYNTAX</span></span>

### <span data-ttu-id="d0a77-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="d0a77-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0a77-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d0a77-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0a77-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d0a77-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0a77-108">描述</span><span class="sxs-lookup"><span data-stu-id="d0a77-108">DESCRIPTION</span></span>
<span data-ttu-id="d0a77-109">在虛擬網路閘道上啟動封包捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="d0a77-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="d0a77-110">例子</span><span class="sxs-lookup"><span data-stu-id="d0a77-110">EXAMPLES</span></span>

### <span data-ttu-id="d0a77-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d0a77-111">Example 1</span></span>
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
### <span data-ttu-id="d0a77-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="d0a77-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
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
### <span data-ttu-id="d0a77-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="d0a77-113">Example 3</span></span>
<span data-ttu-id="d0a77-114">封包捕獲範例，用於捕獲所有內外封包</span><span class="sxs-lookup"><span data-stu-id="d0a77-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
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

## <span data-ttu-id="d0a77-115">參數</span><span class="sxs-lookup"><span data-stu-id="d0a77-115">PARAMETERS</span></span>

### <span data-ttu-id="d0a77-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0a77-116">-AsJob</span></span>
<span data-ttu-id="d0a77-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d0a77-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0a77-118">-確認</span><span class="sxs-lookup"><span data-stu-id="d0a77-118">-Confirm</span></span>
<span data-ttu-id="d0a77-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d0a77-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0a77-120">-DefaultProfile</span></span>
<span data-ttu-id="d0a77-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0a77-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0a77-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="d0a77-122">-FilterData</span></span>
<span data-ttu-id="d0a77-123">在虛擬網路閘道上開始封包捕獲的篩選選項。</span><span class="sxs-lookup"><span data-stu-id="d0a77-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="d0a77-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0a77-124">-InputObject</span></span>
<span data-ttu-id="d0a77-125">要開始封包捕獲的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="d0a77-125">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="d0a77-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0a77-126">-Name</span></span>
<span data-ttu-id="d0a77-127">要開始封包捕獲的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="d0a77-127">The virtual network gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="d0a77-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a77-128">-ResourceGroupName</span></span>
<span data-ttu-id="d0a77-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="d0a77-129">The resource group name.</span></span>

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

### <span data-ttu-id="d0a77-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0a77-130">-ResourceId</span></span>
<span data-ttu-id="d0a77-131">VirtualNetworkGateway 的 Azure 資源識別碼，其中要開始封包捕獲。</span><span class="sxs-lookup"><span data-stu-id="d0a77-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="d0a77-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a77-132">-WhatIf</span></span>
<span data-ttu-id="d0a77-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d0a77-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0a77-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d0a77-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a77-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a77-135">CommonParameters</span></span>
<span data-ttu-id="d0a77-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d0a77-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a77-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0a77-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a77-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d0a77-138">INPUTS</span></span>

### <span data-ttu-id="d0a77-139">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="d0a77-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="d0a77-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d0a77-140">System.String</span></span>

## <span data-ttu-id="d0a77-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d0a77-141">OUTPUTS</span></span>

### <span data-ttu-id="d0a77-142">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="d0a77-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="d0a77-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d0a77-143">NOTES</span></span>

## <span data-ttu-id="d0a77-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0a77-144">RELATED LINKS</span></span>
[<span data-ttu-id="d0a77-145">Stop-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d0a77-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)