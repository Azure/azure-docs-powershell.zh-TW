---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: 5a0994a5328390a928fd60cda8e8004deaaab162
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956960"
---
# <span data-ttu-id="78f72-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="78f72-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span></span>

## <span data-ttu-id="78f72-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78f72-102">SYNOPSIS</span></span>
<span data-ttu-id="78f72-103">建立用來針對 TCP、HTTP 或 ICMP 執行測試評估的通訊協定設定。</span><span class="sxs-lookup"><span data-stu-id="78f72-103">Create protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="78f72-104">句法</span><span class="sxs-lookup"><span data-stu-id="78f72-104">SYNTAX</span></span>

### <span data-ttu-id="78f72-105">TCP-OUT</span><span class="sxs-lookup"><span data-stu-id="78f72-105">TCP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <Int32>
 [-DisableTraceRoute] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78f72-106">HTTP</span><span class="sxs-lookup"><span data-stu-id="78f72-106">HTTP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <Int32>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78f72-107">ICMP</span><span class="sxs-lookup"><span data-stu-id="78f72-107">ICMP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78f72-108">說明</span><span class="sxs-lookup"><span data-stu-id="78f72-108">DESCRIPTION</span></span>
<span data-ttu-id="78f72-109">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject Cmdlet 會建立用來針對 TCP、HTTP 或 ICMP 執行測試評估的通訊協定配置。</span><span class="sxs-lookup"><span data-stu-id="78f72-109">The New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet creates protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="78f72-110">示例</span><span class="sxs-lookup"><span data-stu-id="78f72-110">EXAMPLES</span></span>

### <span data-ttu-id="78f72-111">範例1</span><span class="sxs-lookup"><span data-stu-id="78f72-111">Example 1</span></span>
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

<span data-ttu-id="78f72-112">埠： 80 DisableTraceRoute： False</span><span class="sxs-lookup"><span data-stu-id="78f72-112">Port              : 80 DisableTraceRoute : False</span></span>

## <span data-ttu-id="78f72-113">參數</span><span class="sxs-lookup"><span data-stu-id="78f72-113">PARAMETERS</span></span>

### <span data-ttu-id="78f72-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f72-114">-DefaultProfile</span></span>
<span data-ttu-id="78f72-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78f72-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78f72-116">-DisableTraceRoute</span><span class="sxs-lookup"><span data-stu-id="78f72-116">-DisableTraceRoute</span></span>
<span data-ttu-id="78f72-117">指示是否應該停用追蹤路線的路徑評估的值。</span><span class="sxs-lookup"><span data-stu-id="78f72-117">Value indicating whether path evaluation with trace route should be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f72-118">-HttpProtocol</span><span class="sxs-lookup"><span data-stu-id="78f72-118">-HttpProtocol</span></span>
<span data-ttu-id="78f72-119">HTTP 通訊協定開關</span><span class="sxs-lookup"><span data-stu-id="78f72-119">HTTP protocol switch</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f72-120">-IcmpProtocol</span><span class="sxs-lookup"><span data-stu-id="78f72-120">-IcmpProtocol</span></span>
<span data-ttu-id="78f72-121">ICMP 通訊協定交換器。</span><span class="sxs-lookup"><span data-stu-id="78f72-121">ICMP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f72-122">-方法</span><span class="sxs-lookup"><span data-stu-id="78f72-122">-Method</span></span>
<span data-ttu-id="78f72-123">要使用的 HTTP 方法。</span><span class="sxs-lookup"><span data-stu-id="78f72-123">The HTTP method to use.</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f72-124">-Path</span><span class="sxs-lookup"><span data-stu-id="78f72-124">-Path</span></span>
<span data-ttu-id="78f72-125">URI 的路徑元件。</span><span class="sxs-lookup"><span data-stu-id="78f72-125">The path component of the URI.</span></span> <span data-ttu-id="78f72-126">例如， \" /dir1/dir2 \" 。</span><span class="sxs-lookup"><span data-stu-id="78f72-126">For instance, \"/dir1/dir2\".</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f72-127">-埠</span><span class="sxs-lookup"><span data-stu-id="78f72-127">-Port</span></span>
<span data-ttu-id="78f72-128">要連接的埠。</span><span class="sxs-lookup"><span data-stu-id="78f72-128">The port to connect to.</span></span>

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f72-129">-PreferHTTPS</span><span class="sxs-lookup"><span data-stu-id="78f72-129">-PreferHTTPS</span></span>
<span data-ttu-id="78f72-130">值，指出在不明確的情況下，是否優先在 HTTP 中選擇 HTTPS。</span><span class="sxs-lookup"><span data-stu-id="78f72-130">Value indicating whether HTTPS is preferred over HTTP in cases where the choice is not explicit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f72-131">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="78f72-131">-RequestHeader</span></span>
<span data-ttu-id="78f72-132">要與要求一起傳輸的 HTTP 標頭。</span><span class="sxs-lookup"><span data-stu-id="78f72-132">The HTTP headers to transmit with the request.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f72-133">-TcpProtocol</span><span class="sxs-lookup"><span data-stu-id="78f72-133">-TcpProtocol</span></span>
<span data-ttu-id="78f72-134">TCP 通訊協定開關。</span><span class="sxs-lookup"><span data-stu-id="78f72-134">TCP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f72-135">-ValidStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="78f72-135">-ValidStatusCodeRange</span></span>
<span data-ttu-id="78f72-136">要考慮成功的 HTTP 狀態碼。</span><span class="sxs-lookup"><span data-stu-id="78f72-136">HTTP status codes to consider successful.</span></span> <span data-ttu-id="78f72-137">例如， \" 2xx、304418 \" 。</span><span class="sxs-lookup"><span data-stu-id="78f72-137">For instance, \"2xx,301-304,418\".</span></span>

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78f72-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f72-138">CommonParameters</span></span>
<span data-ttu-id="78f72-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78f72-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f72-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="78f72-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f72-141">輸入</span><span class="sxs-lookup"><span data-stu-id="78f72-141">INPUTS</span></span>

### <span data-ttu-id="78f72-142">所有</span><span class="sxs-lookup"><span data-stu-id="78f72-142">None</span></span>

## <span data-ttu-id="78f72-143">輸出</span><span class="sxs-lookup"><span data-stu-id="78f72-143">OUTPUTS</span></span>

### <span data-ttu-id="78f72-144">PSConnectionMonitorTcpConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="78f72-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorTcpConfiguration</span></span>

### <span data-ttu-id="78f72-145">PSConnectionMonitorHttpConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="78f72-145">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorHttpConfiguration</span></span>

### <span data-ttu-id="78f72-146">PSConnectionMonitorIcmpConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="78f72-146">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorIcmpConfiguration</span></span>

## <span data-ttu-id="78f72-147">筆記</span><span class="sxs-lookup"><span data-stu-id="78f72-147">NOTES</span></span>

## <span data-ttu-id="78f72-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="78f72-148">RELATED LINKS</span></span>
