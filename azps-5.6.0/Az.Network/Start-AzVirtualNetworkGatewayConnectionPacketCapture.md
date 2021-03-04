---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 2bbf5fb703a0c8a6905dff26bf62171c24fd3eea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901897"
---
# <span data-ttu-id="3cd8f-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3cd8f-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="3cd8f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3cd8f-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd8f-103">在虛擬網路閘道連接上啟動封包捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="3cd8f-104">語法</span><span class="sxs-lookup"><span data-stu-id="3cd8f-104">SYNTAX</span></span>

### <span data-ttu-id="3cd8f-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="3cd8f-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cd8f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3cd8f-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cd8f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3cd8f-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cd8f-108">描述</span><span class="sxs-lookup"><span data-stu-id="3cd8f-108">DESCRIPTION</span></span>
<span data-ttu-id="3cd8f-109">在虛擬網路閘道連接上啟動封包捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="3cd8f-110">例子</span><span class="sxs-lookup"><span data-stu-id="3cd8f-110">EXAMPLES</span></span>

### <span data-ttu-id="3cd8f-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="3cd8f-111">Example 1</span></span>
```powershell
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn"

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="3cd8f-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="3cd8f-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="3cd8f-113">範例 3</span><span class="sxs-lookup"><span data-stu-id="3cd8f-113">Example 3</span></span>
<span data-ttu-id="3cd8f-114">封包捕獲範例，用於捕獲所有內外封包</span><span class="sxs-lookup"><span data-stu-id="3cd8f-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

## <span data-ttu-id="3cd8f-115">參數</span><span class="sxs-lookup"><span data-stu-id="3cd8f-115">PARAMETERS</span></span>

### <span data-ttu-id="3cd8f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cd8f-116">-AsJob</span></span>
<span data-ttu-id="3cd8f-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3cd8f-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cd8f-118">-確認</span><span class="sxs-lookup"><span data-stu-id="3cd8f-118">-Confirm</span></span>
<span data-ttu-id="3cd8f-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cd8f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd8f-120">-DefaultProfile</span></span>
<span data-ttu-id="3cd8f-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cd8f-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="3cd8f-122">-FilterData</span></span>
<span data-ttu-id="3cd8f-123">在虛擬網路閘道連接上開始封包捕獲的篩選選項。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="3cd8f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3cd8f-124">-InputObject</span></span>
<span data-ttu-id="3cd8f-125">要開始封包捕獲的虛擬網路閘道連線物件。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-125">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cd8f-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="3cd8f-126">-Name</span></span>
<span data-ttu-id="3cd8f-127">要開始封包捕獲的虛擬網路閘道連接名稱。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-127">The virtual network gateway connection name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cd8f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cd8f-128">-ResourceGroupName</span></span>
<span data-ttu-id="3cd8f-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-129">The resource group name.</span></span>

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

### <span data-ttu-id="3cd8f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cd8f-130">-ResourceId</span></span>
<span data-ttu-id="3cd8f-131">VirtualNetworkGatewayConnection 的 Azure 資源識別碼，其中要開始封包捕獲。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="3cd8f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cd8f-132">-WhatIf</span></span>
<span data-ttu-id="3cd8f-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cd8f-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cd8f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd8f-135">CommonParameters</span></span>
<span data-ttu-id="3cd8f-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3cd8f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd8f-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3cd8f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd8f-138">輸入</span><span class="sxs-lookup"><span data-stu-id="3cd8f-138">INPUTS</span></span>

### <span data-ttu-id="3cd8f-139">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="3cd8f-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="3cd8f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3cd8f-140">System.String</span></span>

## <span data-ttu-id="3cd8f-141">輸出</span><span class="sxs-lookup"><span data-stu-id="3cd8f-141">OUTPUTS</span></span>

### <span data-ttu-id="3cd8f-142">Microsoft.Azure.Commands.Network.models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="3cd8f-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="3cd8f-143">筆記</span><span class="sxs-lookup"><span data-stu-id="3cd8f-143">NOTES</span></span>

## <span data-ttu-id="3cd8f-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="3cd8f-144">RELATED LINKS</span></span>
[<span data-ttu-id="3cd8f-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3cd8f-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)