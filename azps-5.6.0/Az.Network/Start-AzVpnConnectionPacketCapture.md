---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 0b920adf2f0357db7e9babf7b8e4b4e603255fab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901893"
---
# <span data-ttu-id="60913-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="60913-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="60913-102">簡介</span><span class="sxs-lookup"><span data-stu-id="60913-102">SYNOPSIS</span></span>
<span data-ttu-id="60913-103">在 Vpn 連接上啟動封包捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="60913-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="60913-104">語法</span><span class="sxs-lookup"><span data-stu-id="60913-104">SYNTAX</span></span>

### <span data-ttu-id="60913-105">By VpnConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="60913-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60913-106">By VpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="60913-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="60913-107">By VpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="60913-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60913-108">描述</span><span class="sxs-lookup"><span data-stu-id="60913-108">DESCRIPTION</span></span>
<span data-ttu-id="60913-109">在 Vpn 連接上啟動封包捕獲作業。</span><span class="sxs-lookup"><span data-stu-id="60913-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="60913-110">例子</span><span class="sxs-lookup"><span data-stu-id="60913-110">EXAMPLES</span></span>

### <span data-ttu-id="60913-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="60913-111">Example 1</span></span>
```powershell
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1"
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1
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

### <span data-ttu-id="60913-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="60913-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1" -FilterData $a 
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1
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

## <span data-ttu-id="60913-113">參數</span><span class="sxs-lookup"><span data-stu-id="60913-113">PARAMETERS</span></span>

### <span data-ttu-id="60913-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60913-114">-AsJob</span></span>
<span data-ttu-id="60913-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="60913-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60913-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60913-116">-DefaultProfile</span></span>
<span data-ttu-id="60913-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="60913-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60913-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="60913-118">-FilterData</span></span>
<span data-ttu-id="60913-119">在 Vpn 連接上開始封包捕獲的篩選選項。</span><span class="sxs-lookup"><span data-stu-id="60913-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="60913-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60913-120">-InputObject</span></span>
<span data-ttu-id="60913-121">要開始封包捕獲的 Vpn 連線物件。</span><span class="sxs-lookup"><span data-stu-id="60913-121">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60913-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="60913-122">-LinkConnectionName</span></span>
<span data-ttu-id="60913-123">SiteLinkConnection 的名稱。</span><span class="sxs-lookup"><span data-stu-id="60913-123">The names of the SiteLinkConnection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60913-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="60913-124">-Name</span></span>
<span data-ttu-id="60913-125">要開始封包捕獲的 Vpn 連接名稱。</span><span class="sxs-lookup"><span data-stu-id="60913-125">The Vpn connection name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60913-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="60913-126">-ParentResourceName</span></span>
<span data-ttu-id="60913-127">父 Vpngateway 的名稱。</span><span class="sxs-lookup"><span data-stu-id="60913-127">The name of the Parent Vpngateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60913-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60913-128">-ResourceGroupName</span></span>
<span data-ttu-id="60913-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="60913-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60913-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60913-130">-ResourceId</span></span>
<span data-ttu-id="60913-131">要開始封包捕獲之 VpnConnection 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="60913-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60913-132">-確認</span><span class="sxs-lookup"><span data-stu-id="60913-132">-Confirm</span></span>
<span data-ttu-id="60913-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="60913-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60913-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60913-134">-WhatIf</span></span>
<span data-ttu-id="60913-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60913-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60913-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60913-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60913-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60913-137">CommonParameters</span></span>
<span data-ttu-id="60913-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="60913-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60913-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60913-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60913-140">輸入</span><span class="sxs-lookup"><span data-stu-id="60913-140">INPUTS</span></span>

### <span data-ttu-id="60913-141">Microsoft.Azure.Commands.Network.models.PS VpnConnection</span><span class="sxs-lookup"><span data-stu-id="60913-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="60913-142">System.String</span><span class="sxs-lookup"><span data-stu-id="60913-142">System.String</span></span>

## <span data-ttu-id="60913-143">輸出</span><span class="sxs-lookup"><span data-stu-id="60913-143">OUTPUTS</span></span>

### <span data-ttu-id="60913-144">Microsoft.Azure.Commands.Network.models.PS VpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="60913-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="60913-145">筆記</span><span class="sxs-lookup"><span data-stu-id="60913-145">NOTES</span></span>

## <span data-ttu-id="60913-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="60913-146">RELATED LINKS</span></span>

[<span data-ttu-id="60913-147">Stop-Az VpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="60913-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)