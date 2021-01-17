---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448873"
---
# <span data-ttu-id="f0d22-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f0d22-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="f0d22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0d22-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d22-103">在 Vpn 連線上啟動 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="f0d22-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="f0d22-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0d22-104">SYNTAX</span></span>

### <span data-ttu-id="f0d22-105">ByVpnConnectionName (預設) </span><span class="sxs-lookup"><span data-stu-id="f0d22-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0d22-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f0d22-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f0d22-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="f0d22-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0d22-108">說明</span><span class="sxs-lookup"><span data-stu-id="f0d22-108">DESCRIPTION</span></span>
<span data-ttu-id="f0d22-109">在 Vpn 連線上啟動 [資料包捕獲] 作業。</span><span class="sxs-lookup"><span data-stu-id="f0d22-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="f0d22-110">示例</span><span class="sxs-lookup"><span data-stu-id="f0d22-110">EXAMPLES</span></span>

### <span data-ttu-id="f0d22-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f0d22-111">Example 1</span></span>
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

### <span data-ttu-id="f0d22-112">範例2</span><span class="sxs-lookup"><span data-stu-id="f0d22-112">Example 2</span></span>
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

## <span data-ttu-id="f0d22-113">參數</span><span class="sxs-lookup"><span data-stu-id="f0d22-113">PARAMETERS</span></span>

### <span data-ttu-id="f0d22-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0d22-114">-AsJob</span></span>
<span data-ttu-id="f0d22-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f0d22-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f0d22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d22-116">-DefaultProfile</span></span>
<span data-ttu-id="f0d22-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0d22-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0d22-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="f0d22-118">-FilterData</span></span>
<span data-ttu-id="f0d22-119">在 Vpn 連線時啟動 [資料包捕獲] 的篩選選項。</span><span class="sxs-lookup"><span data-stu-id="f0d22-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="f0d22-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0d22-120">-InputObject</span></span>
<span data-ttu-id="f0d22-121">要開始建立資料包捕獲的 Vpn 連線物件。</span><span class="sxs-lookup"><span data-stu-id="f0d22-121">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="f0d22-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="f0d22-122">-LinkConnectionName</span></span>
<span data-ttu-id="f0d22-123">SiteLinkConnection 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0d22-123">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="f0d22-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="f0d22-124">-Name</span></span>
<span data-ttu-id="f0d22-125">要開始進行資料包捕獲的 Vpn 連線名稱。</span><span class="sxs-lookup"><span data-stu-id="f0d22-125">The Vpn connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="f0d22-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f0d22-126">-ParentResourceName</span></span>
<span data-ttu-id="f0d22-127">父 Vpngateway 的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0d22-127">The name of the Parent Vpngateway.</span></span>

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

### <span data-ttu-id="f0d22-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d22-128">-ResourceGroupName</span></span>
<span data-ttu-id="f0d22-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0d22-129">The resource group name.</span></span>

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

### <span data-ttu-id="f0d22-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0d22-130">-ResourceId</span></span>
<span data-ttu-id="f0d22-131">要開始進行資料包捕獲之 VpnConnection 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0d22-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="f0d22-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f0d22-132">-Confirm</span></span>
<span data-ttu-id="f0d22-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f0d22-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0d22-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0d22-134">-WhatIf</span></span>
<span data-ttu-id="f0d22-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f0d22-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0d22-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f0d22-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0d22-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d22-137">CommonParameters</span></span>
<span data-ttu-id="f0d22-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0d22-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d22-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f0d22-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d22-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f0d22-140">INPUTS</span></span>

### <span data-ttu-id="f0d22-141">PSVpnConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f0d22-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="f0d22-142">System.object</span><span class="sxs-lookup"><span data-stu-id="f0d22-142">System.String</span></span>

## <span data-ttu-id="f0d22-143">輸出</span><span class="sxs-lookup"><span data-stu-id="f0d22-143">OUTPUTS</span></span>

### <span data-ttu-id="f0d22-144">PSVpnConnectionPacketCaptureResult 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f0d22-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="f0d22-145">筆記</span><span class="sxs-lookup"><span data-stu-id="f0d22-145">NOTES</span></span>

## <span data-ttu-id="f0d22-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0d22-146">RELATED LINKS</span></span>

[<span data-ttu-id="f0d22-147">停止 AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f0d22-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)