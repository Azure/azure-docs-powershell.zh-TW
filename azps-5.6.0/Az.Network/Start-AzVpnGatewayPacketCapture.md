---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: ec7307b6bd6d01b7b3f6e2656026eea78e0d3704
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901890"
---
# <span data-ttu-id="b6880-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b6880-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="b6880-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b6880-102">SYNOPSIS</span></span>
<span data-ttu-id="b6880-103">在 Vpn 閘道上啟動封包捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="b6880-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="b6880-104">語法</span><span class="sxs-lookup"><span data-stu-id="b6880-104">SYNTAX</span></span>

### <span data-ttu-id="b6880-105">By VpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="b6880-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6880-106">By VpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="b6880-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6880-107">By VpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="b6880-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6880-108">描述</span><span class="sxs-lookup"><span data-stu-id="b6880-108">DESCRIPTION</span></span>
<span data-ttu-id="b6880-109">在 Vpn 閘道上啟動封包捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="b6880-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="b6880-110">例子</span><span class="sxs-lookup"><span data-stu-id="b6880-110">EXAMPLES</span></span>

### <span data-ttu-id="b6880-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b6880-111">Example 1</span></span>
```powershell
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"
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

### <span data-ttu-id="b6880-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="b6880-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a
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

## <span data-ttu-id="b6880-113">參數</span><span class="sxs-lookup"><span data-stu-id="b6880-113">PARAMETERS</span></span>

### <span data-ttu-id="b6880-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6880-114">-AsJob</span></span>
<span data-ttu-id="b6880-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b6880-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6880-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6880-116">-DefaultProfile</span></span>
<span data-ttu-id="b6880-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6880-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6880-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="b6880-118">-FilterData</span></span>
<span data-ttu-id="b6880-119">在 Vpn 閘道上篩選開始封包捕獲的選項。</span><span class="sxs-lookup"><span data-stu-id="b6880-119">Filter options for start packet capture on Vpn Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6880-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6880-120">-InputObject</span></span>
<span data-ttu-id="b6880-121">要開始封包捕獲的 Vpn 閘道物件。</span><span class="sxs-lookup"><span data-stu-id="b6880-121">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6880-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6880-122">-Name</span></span>
<span data-ttu-id="b6880-123">要開始封包捕獲的 Vpn 閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="b6880-123">The Vpn Gateway name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6880-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6880-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6880-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b6880-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6880-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6880-126">-ResourceId</span></span>
<span data-ttu-id="b6880-127">VpnGateway 的 Azure 資源識別碼，其中要開始封包捕獲。</span><span class="sxs-lookup"><span data-stu-id="b6880-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6880-128">-確認</span><span class="sxs-lookup"><span data-stu-id="b6880-128">-Confirm</span></span>
<span data-ttu-id="b6880-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b6880-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6880-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6880-130">-WhatIf</span></span>
<span data-ttu-id="b6880-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6880-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6880-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6880-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6880-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6880-133">CommonParameters</span></span>
<span data-ttu-id="b6880-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b6880-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6880-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6880-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6880-136">輸入</span><span class="sxs-lookup"><span data-stu-id="b6880-136">INPUTS</span></span>

### <span data-ttu-id="b6880-137">Microsoft.Azure.Commands.Network.models.PS VpnGateway</span><span class="sxs-lookup"><span data-stu-id="b6880-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="b6880-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b6880-138">System.String</span></span>

## <span data-ttu-id="b6880-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b6880-139">OUTPUTS</span></span>

### <span data-ttu-id="b6880-140">Microsoft.Azure.Commands.Network.models.PS VpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="b6880-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="b6880-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b6880-141">NOTES</span></span>

## <span data-ttu-id="b6880-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6880-142">RELATED LINKS</span></span>

[<span data-ttu-id="b6880-143">Stop-Az VpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b6880-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)