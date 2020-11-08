---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126344"
---
# <span data-ttu-id="a6094-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6094-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="a6094-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6094-102">SYNOPSIS</span></span>
<span data-ttu-id="a6094-103">啟動 Vpn 閘道的 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="a6094-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="a6094-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6094-104">SYNTAX</span></span>

### <span data-ttu-id="a6094-105">ByVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="a6094-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6094-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a6094-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6094-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a6094-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6094-108">說明</span><span class="sxs-lookup"><span data-stu-id="a6094-108">DESCRIPTION</span></span>
<span data-ttu-id="a6094-109">啟動 Vpn 閘道的 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="a6094-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="a6094-110">示例</span><span class="sxs-lookup"><span data-stu-id="a6094-110">EXAMPLES</span></span>

### <span data-ttu-id="a6094-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a6094-111">Example 1</span></span>
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

### <span data-ttu-id="a6094-112">範例2</span><span class="sxs-lookup"><span data-stu-id="a6094-112">Example 2</span></span>
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

## <span data-ttu-id="a6094-113">參數</span><span class="sxs-lookup"><span data-stu-id="a6094-113">PARAMETERS</span></span>

### <span data-ttu-id="a6094-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6094-114">-AsJob</span></span>
<span data-ttu-id="a6094-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6094-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6094-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6094-116">-DefaultProfile</span></span>
<span data-ttu-id="a6094-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6094-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6094-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="a6094-118">-FilterData</span></span>
<span data-ttu-id="a6094-119">Vpn 閘道的 [啟動資料包捕獲] 的篩選選項。</span><span class="sxs-lookup"><span data-stu-id="a6094-119">Filter options for start packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="a6094-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6094-120">-InputObject</span></span>
<span data-ttu-id="a6094-121">要開始進行資料包捕獲的 Vpn 閘道物件。</span><span class="sxs-lookup"><span data-stu-id="a6094-121">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="a6094-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6094-122">-Name</span></span>
<span data-ttu-id="a6094-123">要在其中開始進行資料包捕獲的 Vpn 閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="a6094-123">The Vpn Gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="a6094-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6094-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6094-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6094-125">The resource group name.</span></span>

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

### <span data-ttu-id="a6094-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6094-126">-ResourceId</span></span>
<span data-ttu-id="a6094-127">要開始進行資料包捕獲之 VpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6094-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="a6094-128">-確認</span><span class="sxs-lookup"><span data-stu-id="a6094-128">-Confirm</span></span>
<span data-ttu-id="a6094-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a6094-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6094-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6094-130">-WhatIf</span></span>
<span data-ttu-id="a6094-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6094-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6094-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6094-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6094-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6094-133">CommonParameters</span></span>
<span data-ttu-id="a6094-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6094-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6094-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a6094-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6094-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a6094-136">INPUTS</span></span>

### <span data-ttu-id="a6094-137">PSVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a6094-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="a6094-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a6094-138">System.String</span></span>

## <span data-ttu-id="a6094-139">輸出</span><span class="sxs-lookup"><span data-stu-id="a6094-139">OUTPUTS</span></span>

### <span data-ttu-id="a6094-140">PSVpnGatewayPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a6094-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="a6094-141">筆記</span><span class="sxs-lookup"><span data-stu-id="a6094-141">NOTES</span></span>

## <span data-ttu-id="a6094-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6094-142">RELATED LINKS</span></span>

[<span data-ttu-id="a6094-143">停止 AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a6094-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)