---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cea6f92ba15e43d5977af03dfee1054240f5ecad
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436884"
---
# <span data-ttu-id="5ffd7-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5ffd7-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="5ffd7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ffd7-102">SYNOPSIS</span></span>
<span data-ttu-id="5ffd7-103">將健全性探測新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="5ffd7-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ffd7-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ffd7-105">說明</span><span class="sxs-lookup"><span data-stu-id="5ffd7-105">DESCRIPTION</span></span>
<span data-ttu-id="5ffd7-106">Add-AzApplicationGatewayProbeConfig Cmdlet 會將健康探測新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="5ffd7-107">示例</span><span class="sxs-lookup"><span data-stu-id="5ffd7-107">EXAMPLES</span></span>

### <span data-ttu-id="5ffd7-108">範例1：將健全性探測器新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="5ffd7-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="5ffd7-109">這個命令會將名為 Probe01 的 health 探測，新增到名為 Gateway 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="5ffd7-110">此命令也會將不健康閾值設定為8次重試，並在120秒後超時。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="5ffd7-111">參數</span><span class="sxs-lookup"><span data-stu-id="5ffd7-111">PARAMETERS</span></span>

### <span data-ttu-id="5ffd7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5ffd7-112">-ApplicationGateway</span></span>
<span data-ttu-id="5ffd7-113">指定此 Cmdlet 新增探測的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ffd7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ffd7-114">-DefaultProfile</span></span>
<span data-ttu-id="5ffd7-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ffd7-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="5ffd7-116">-HostName</span></span>
<span data-ttu-id="5ffd7-117">指定此 Cmdlet 傳送探測的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="5ffd7-118">間隔</span><span class="sxs-lookup"><span data-stu-id="5ffd7-118">-Interval</span></span>
<span data-ttu-id="5ffd7-119">指定探測間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="5ffd7-120">這是兩個連續探測器之間的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="5ffd7-121">這個值介於1秒與86400秒之間。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-121">This value is between 1 second and 86400 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffd7-122">相符</span><span class="sxs-lookup"><span data-stu-id="5ffd7-122">-Match</span></span>
<span data-ttu-id="5ffd7-123">在健康情況回應中必須包含的主體。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="5ffd7-124">預設值為空白</span><span class="sxs-lookup"><span data-stu-id="5ffd7-124">Default value is empty</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffd7-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="5ffd7-125">-MinServers</span></span>
<span data-ttu-id="5ffd7-126">最少標示為 [良好] 的伺服器數目。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="5ffd7-127">預設值為0</span><span class="sxs-lookup"><span data-stu-id="5ffd7-127">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffd7-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ffd7-128">-Name</span></span>
<span data-ttu-id="5ffd7-129">指定探測器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="5ffd7-130">-Path</span><span class="sxs-lookup"><span data-stu-id="5ffd7-130">-Path</span></span>
<span data-ttu-id="5ffd7-131">指定探測的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="5ffd7-132">有效路徑是以斜線字元開頭 (/) 。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="5ffd7-133">探測會傳送至 \<Protocol\> ：// \<host\> ： \<port\> \<path\> 。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="5ffd7-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5ffd7-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="5ffd7-135">是否應從後端 HTTP 設定中挑選主機標頭。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="5ffd7-136">預設值為 false</span><span class="sxs-lookup"><span data-stu-id="5ffd7-136">Default value is false</span></span>

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

### <span data-ttu-id="5ffd7-137">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="5ffd7-137">-Protocol</span></span>
<span data-ttu-id="5ffd7-138">指定用來傳送探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="5ffd7-139">這個 Cmdlet 只支援 HTTP。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-139">This cmdlet supports HTTP only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffd7-140">-超時</span><span class="sxs-lookup"><span data-stu-id="5ffd7-140">-Timeout</span></span>
<span data-ttu-id="5ffd7-141">指定探測超時（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="5ffd7-142">如果沒有收到此超時期間的有效回應，此 Cmdlet 會將探測標示為失敗。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="5ffd7-143">有效值為1秒到86400秒。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-143">Valid values are between 1 second and 86400 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffd7-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="5ffd7-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="5ffd7-145">指定 [探測重試計數]。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="5ffd7-146">連續探測失敗計數達到不正常閾值之後，後端伺服器會標示為關閉。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="5ffd7-147">有效值為1秒到20秒。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-147">Valid values are between 1 second and 20 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ffd7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ffd7-148">CommonParameters</span></span>
<span data-ttu-id="5ffd7-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ffd7-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ffd7-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ffd7-151">輸入</span><span class="sxs-lookup"><span data-stu-id="5ffd7-151">INPUTS</span></span>

### <span data-ttu-id="5ffd7-152">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5ffd7-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ffd7-153">輸出</span><span class="sxs-lookup"><span data-stu-id="5ffd7-153">OUTPUTS</span></span>

### <span data-ttu-id="5ffd7-154">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="5ffd7-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5ffd7-155">筆記</span><span class="sxs-lookup"><span data-stu-id="5ffd7-155">NOTES</span></span>

## <span data-ttu-id="5ffd7-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ffd7-156">RELATED LINKS</span></span>

[<span data-ttu-id="5ffd7-157">新增探測至現有的應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="5ffd7-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="5ffd7-158">AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5ffd7-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="5ffd7-159">新-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5ffd7-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="5ffd7-160">移除-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5ffd7-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="5ffd7-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="5ffd7-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

