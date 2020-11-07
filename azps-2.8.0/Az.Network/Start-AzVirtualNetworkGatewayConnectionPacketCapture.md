---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 3a1d9c2f415d56263529fcd66aa1ee9535823bbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791513"
---
# <span data-ttu-id="d6413-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6413-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="d6413-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d6413-102">SYNOPSIS</span></span>
<span data-ttu-id="d6413-103">啟動虛擬網路閘道連線的 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="d6413-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="d6413-104">句法</span><span class="sxs-lookup"><span data-stu-id="d6413-104">SYNTAX</span></span>

### <span data-ttu-id="d6413-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="d6413-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6413-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d6413-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6413-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d6413-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6413-108">說明</span><span class="sxs-lookup"><span data-stu-id="d6413-108">DESCRIPTION</span></span>
<span data-ttu-id="d6413-109">啟動虛擬網路閘道連線的 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="d6413-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="d6413-110">示例</span><span class="sxs-lookup"><span data-stu-id="d6413-110">EXAMPLES</span></span>

### <span data-ttu-id="d6413-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d6413-111">Example 1</span></span>
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
### <span data-ttu-id="d6413-112">範例2</span><span class="sxs-lookup"><span data-stu-id="d6413-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
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

## <span data-ttu-id="d6413-113">參數</span><span class="sxs-lookup"><span data-stu-id="d6413-113">PARAMETERS</span></span>

### <span data-ttu-id="d6413-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6413-114">-AsJob</span></span>
<span data-ttu-id="d6413-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d6413-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d6413-116">-確認</span><span class="sxs-lookup"><span data-stu-id="d6413-116">-Confirm</span></span>
<span data-ttu-id="d6413-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d6413-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6413-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6413-118">-DefaultProfile</span></span>
<span data-ttu-id="d6413-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6413-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6413-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="d6413-120">-FilterData</span></span>
<span data-ttu-id="d6413-121">[篩選] 選項可讓您在虛擬網路閘道連線時開始進行資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="d6413-121">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="d6413-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6413-122">-InputObject</span></span>
<span data-ttu-id="d6413-123">要開始建立資料包捕獲的虛擬網路閘道連線物件。</span><span class="sxs-lookup"><span data-stu-id="d6413-123">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="d6413-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6413-124">-Name</span></span>
<span data-ttu-id="d6413-125">要開始建立資料包捕獲的虛擬網路閘道連線名稱。</span><span class="sxs-lookup"><span data-stu-id="d6413-125">The virtual network gateway connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="d6413-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6413-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6413-127">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d6413-127">The resource group name.</span></span>

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

### <span data-ttu-id="d6413-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6413-128">-ResourceId</span></span>
<span data-ttu-id="d6413-129">要開始進行資料包捕獲之 VirtualNetworkGatewayConnection 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d6413-129">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="d6413-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6413-130">-WhatIf</span></span>
<span data-ttu-id="d6413-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6413-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6413-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6413-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6413-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6413-133">CommonParameters</span></span>
<span data-ttu-id="d6413-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d6413-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6413-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d6413-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6413-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d6413-136">INPUTS</span></span>

### <span data-ttu-id="d6413-137">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d6413-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="d6413-138">System.object</span><span class="sxs-lookup"><span data-stu-id="d6413-138">System.String</span></span>

## <span data-ttu-id="d6413-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d6413-139">OUTPUTS</span></span>

### <span data-ttu-id="d6413-140">PSVirtualNetworkGatewayPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d6413-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="d6413-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d6413-141">NOTES</span></span>

## <span data-ttu-id="d6413-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6413-142">RELATED LINKS</span></span>
[<span data-ttu-id="d6413-143">停止 AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d6413-143">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)