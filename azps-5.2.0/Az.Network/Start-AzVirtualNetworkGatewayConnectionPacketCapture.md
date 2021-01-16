---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277411"
---
# <span data-ttu-id="8a409-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a409-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="8a409-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a409-102">SYNOPSIS</span></span>
<span data-ttu-id="8a409-103">啟動虛擬網路閘道連線的 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="8a409-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="8a409-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a409-104">SYNTAX</span></span>

### <span data-ttu-id="8a409-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="8a409-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a409-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8a409-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a409-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a409-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a409-108">說明</span><span class="sxs-lookup"><span data-stu-id="8a409-108">DESCRIPTION</span></span>
<span data-ttu-id="8a409-109">啟動虛擬網路閘道連線的 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="8a409-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="8a409-110">示例</span><span class="sxs-lookup"><span data-stu-id="8a409-110">EXAMPLES</span></span>

### <span data-ttu-id="8a409-111">範例1</span><span class="sxs-lookup"><span data-stu-id="8a409-111">Example 1</span></span>
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
### <span data-ttu-id="8a409-112">範例2</span><span class="sxs-lookup"><span data-stu-id="8a409-112">Example 2</span></span>
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
### <span data-ttu-id="8a409-113">範例3</span><span class="sxs-lookup"><span data-stu-id="8a409-113">Example 3</span></span>
<span data-ttu-id="8a409-114">捕獲所有內部和外部資料包的資料包捕獲範例</span><span class="sxs-lookup"><span data-stu-id="8a409-114">Packet Capture example for capture all inner and outer packets</span></span>
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

## <span data-ttu-id="8a409-115">參數</span><span class="sxs-lookup"><span data-stu-id="8a409-115">PARAMETERS</span></span>

### <span data-ttu-id="8a409-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a409-116">-AsJob</span></span>
<span data-ttu-id="8a409-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8a409-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a409-118">-確認</span><span class="sxs-lookup"><span data-stu-id="8a409-118">-Confirm</span></span>
<span data-ttu-id="8a409-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8a409-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a409-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a409-120">-DefaultProfile</span></span>
<span data-ttu-id="8a409-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a409-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a409-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="8a409-122">-FilterData</span></span>
<span data-ttu-id="8a409-123">[篩選] 選項可讓您在虛擬網路閘道連線時開始進行資料包捕獲。</span><span class="sxs-lookup"><span data-stu-id="8a409-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="8a409-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a409-124">-InputObject</span></span>
<span data-ttu-id="8a409-125">要開始建立資料包捕獲的虛擬網路閘道連線物件。</span><span class="sxs-lookup"><span data-stu-id="8a409-125">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="8a409-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a409-126">-Name</span></span>
<span data-ttu-id="8a409-127">要開始建立資料包捕獲的虛擬網路閘道連線名稱。</span><span class="sxs-lookup"><span data-stu-id="8a409-127">The virtual network gateway connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="8a409-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a409-128">-ResourceGroupName</span></span>
<span data-ttu-id="8a409-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8a409-129">The resource group name.</span></span>

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

### <span data-ttu-id="8a409-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a409-130">-ResourceId</span></span>
<span data-ttu-id="8a409-131">要開始進行資料包捕獲之 VirtualNetworkGatewayConnection 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8a409-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="8a409-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a409-132">-WhatIf</span></span>
<span data-ttu-id="8a409-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a409-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a409-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a409-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a409-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a409-135">CommonParameters</span></span>
<span data-ttu-id="8a409-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a409-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a409-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8a409-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a409-138">輸入</span><span class="sxs-lookup"><span data-stu-id="8a409-138">INPUTS</span></span>

### <span data-ttu-id="8a409-139">PSVirtualNetworkGatewayConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8a409-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="8a409-140">System.object</span><span class="sxs-lookup"><span data-stu-id="8a409-140">System.String</span></span>

## <span data-ttu-id="8a409-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8a409-141">OUTPUTS</span></span>

### <span data-ttu-id="8a409-142">PSVirtualNetworkGatewayPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="8a409-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="8a409-143">筆記</span><span class="sxs-lookup"><span data-stu-id="8a409-143">NOTES</span></span>

## <span data-ttu-id="8a409-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a409-144">RELATED LINKS</span></span>
[<span data-ttu-id="8a409-145">停止 AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8a409-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)