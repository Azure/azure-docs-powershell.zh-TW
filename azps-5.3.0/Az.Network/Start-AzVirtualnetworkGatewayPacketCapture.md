---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: b0010134ac6b819afc3e8621b11d5530a08008a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448874"
---
# <span data-ttu-id="de8ee-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="de8ee-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="de8ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="de8ee-103">啟動虛擬網路閘道的 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="de8ee-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="de8ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="de8ee-104">SYNTAX</span></span>

### <span data-ttu-id="de8ee-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="de8ee-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de8ee-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="de8ee-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de8ee-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="de8ee-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de8ee-108">說明</span><span class="sxs-lookup"><span data-stu-id="de8ee-108">DESCRIPTION</span></span>
<span data-ttu-id="de8ee-109">啟動虛擬網路閘道的 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="de8ee-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="de8ee-110">示例</span><span class="sxs-lookup"><span data-stu-id="de8ee-110">EXAMPLES</span></span>

### <span data-ttu-id="de8ee-111">範例1</span><span class="sxs-lookup"><span data-stu-id="de8ee-111">Example 1</span></span>
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
### <span data-ttu-id="de8ee-112">範例2</span><span class="sxs-lookup"><span data-stu-id="de8ee-112">Example 2</span></span>
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
### <span data-ttu-id="de8ee-113">範例3</span><span class="sxs-lookup"><span data-stu-id="de8ee-113">Example 3</span></span>
<span data-ttu-id="de8ee-114">捕獲所有內部和外部資料包的資料包捕獲範例</span><span class="sxs-lookup"><span data-stu-id="de8ee-114">Packet Capture example for capture all inner and outer packets</span></span>
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

## <span data-ttu-id="de8ee-115">參數</span><span class="sxs-lookup"><span data-stu-id="de8ee-115">PARAMETERS</span></span>

### <span data-ttu-id="de8ee-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de8ee-116">-AsJob</span></span>
<span data-ttu-id="de8ee-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="de8ee-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de8ee-118">-確認</span><span class="sxs-lookup"><span data-stu-id="de8ee-118">-Confirm</span></span>
<span data-ttu-id="de8ee-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="de8ee-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de8ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de8ee-120">-DefaultProfile</span></span>
<span data-ttu-id="de8ee-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de8ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de8ee-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="de8ee-122">-FilterData</span></span>
<span data-ttu-id="de8ee-123">在虛擬網路閘道開始進行資料包捕獲的篩選選項。</span><span class="sxs-lookup"><span data-stu-id="de8ee-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="de8ee-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de8ee-124">-InputObject</span></span>
<span data-ttu-id="de8ee-125">要開始進行資料包捕獲的虛擬網路閘道物件。</span><span class="sxs-lookup"><span data-stu-id="de8ee-125">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="de8ee-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="de8ee-126">-Name</span></span>
<span data-ttu-id="de8ee-127">要在其中開始進行資料包捕獲的虛擬網路閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="de8ee-127">The virtual network gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="de8ee-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de8ee-128">-ResourceGroupName</span></span>
<span data-ttu-id="de8ee-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="de8ee-129">The resource group name.</span></span>

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

### <span data-ttu-id="de8ee-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de8ee-130">-ResourceId</span></span>
<span data-ttu-id="de8ee-131">要開始進行資料包捕獲之 VirtualNetworkGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="de8ee-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="de8ee-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de8ee-132">-WhatIf</span></span>
<span data-ttu-id="de8ee-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de8ee-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de8ee-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de8ee-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de8ee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de8ee-135">CommonParameters</span></span>
<span data-ttu-id="de8ee-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de8ee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de8ee-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="de8ee-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de8ee-138">輸入</span><span class="sxs-lookup"><span data-stu-id="de8ee-138">INPUTS</span></span>

### <span data-ttu-id="de8ee-139">PSVirtualNetworkGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="de8ee-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="de8ee-140">System.object</span><span class="sxs-lookup"><span data-stu-id="de8ee-140">System.String</span></span>

## <span data-ttu-id="de8ee-141">輸出</span><span class="sxs-lookup"><span data-stu-id="de8ee-141">OUTPUTS</span></span>

### <span data-ttu-id="de8ee-142">PSVirtualNetworkGatewayPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="de8ee-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="de8ee-143">筆記</span><span class="sxs-lookup"><span data-stu-id="de8ee-143">NOTES</span></span>

## <span data-ttu-id="de8ee-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="de8ee-144">RELATED LINKS</span></span>
[<span data-ttu-id="de8ee-145">停止 AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="de8ee-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)