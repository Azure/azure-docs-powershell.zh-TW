---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 7763dac119ba2a2144f2c7428dfd63aeedcd3b45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621492"
---
# <span data-ttu-id="822f9-101">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="822f9-101">Set-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="822f9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="822f9-102">SYNOPSIS</span></span>
<span data-ttu-id="822f9-103">在現有的應用程式閘道上設定健康情況探針配置。</span><span class="sxs-lookup"><span data-stu-id="822f9-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="822f9-104">句法</span><span class="sxs-lookup"><span data-stu-id="822f9-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="822f9-105">說明</span><span class="sxs-lookup"><span data-stu-id="822f9-105">DESCRIPTION</span></span>
<span data-ttu-id="822f9-106">Set-AzApplicationGatewayProbeConfig Cmdlet 會在現有的應用程式閘道上設定健康情況探針配置。</span><span class="sxs-lookup"><span data-stu-id="822f9-106">The Set-AzApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="822f9-107">示例</span><span class="sxs-lookup"><span data-stu-id="822f9-107">EXAMPLES</span></span>

### <span data-ttu-id="822f9-108">範例1：在應用程式閘道設定健康情況探測的配置</span><span class="sxs-lookup"><span data-stu-id="822f9-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="822f9-109">這個命令會針對名為 [閘道] 的應用程式閘道，設定名為 Probe05 之健康情況探測的配置。</span><span class="sxs-lookup"><span data-stu-id="822f9-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="822f9-110">此命令也會將不健康閾值設定為8次重試，並在120秒後超時。</span><span class="sxs-lookup"><span data-stu-id="822f9-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="822f9-111">參數</span><span class="sxs-lookup"><span data-stu-id="822f9-111">PARAMETERS</span></span>

### <span data-ttu-id="822f9-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="822f9-112">-ApplicationGateway</span></span>
<span data-ttu-id="822f9-113">指定此 Cmdlet 傳送探測的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="822f9-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="822f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822f9-114">-DefaultProfile</span></span>
<span data-ttu-id="822f9-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="822f9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="822f9-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="822f9-116">-HostName</span></span>
<span data-ttu-id="822f9-117">指定此 Cmdlet 傳送探測的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="822f9-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="822f9-118">間隔</span><span class="sxs-lookup"><span data-stu-id="822f9-118">-Interval</span></span>
<span data-ttu-id="822f9-119">指定探測間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="822f9-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="822f9-120">這是兩個連續探測器之間的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="822f9-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="822f9-121">這個值介於1秒與86400秒之間。</span><span class="sxs-lookup"><span data-stu-id="822f9-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="822f9-122">相符</span><span class="sxs-lookup"><span data-stu-id="822f9-122">-Match</span></span>
<span data-ttu-id="822f9-123">在健康情況回應中必須包含的主體。</span><span class="sxs-lookup"><span data-stu-id="822f9-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="822f9-124">預設值為空白</span><span class="sxs-lookup"><span data-stu-id="822f9-124">Default value is empty</span></span>

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

### <span data-ttu-id="822f9-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="822f9-125">-MinServers</span></span>
<span data-ttu-id="822f9-126">最少標示為 [良好] 的伺服器數目。</span><span class="sxs-lookup"><span data-stu-id="822f9-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="822f9-127">預設值為0</span><span class="sxs-lookup"><span data-stu-id="822f9-127">Default value is 0</span></span>

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

### <span data-ttu-id="822f9-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="822f9-128">-Name</span></span>
<span data-ttu-id="822f9-129">指定探測器的名稱。</span><span class="sxs-lookup"><span data-stu-id="822f9-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="822f9-130">-Path</span><span class="sxs-lookup"><span data-stu-id="822f9-130">-Path</span></span>
<span data-ttu-id="822f9-131">指定探測的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="822f9-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="822f9-132">有效路徑是以斜線字元開頭 (/) 。</span><span class="sxs-lookup"><span data-stu-id="822f9-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="822f9-133">探測會傳送至 \< 通訊協定 \> ：// \< 主機 \> ： \< 埠 \> \< 路徑 \> 。</span><span class="sxs-lookup"><span data-stu-id="822f9-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="822f9-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="822f9-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="822f9-135">是否應從後端 HTTP 設定中挑選主機標頭。</span><span class="sxs-lookup"><span data-stu-id="822f9-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="822f9-136">預設值為 false</span><span class="sxs-lookup"><span data-stu-id="822f9-136">Default value is false</span></span>

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

### <span data-ttu-id="822f9-137">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="822f9-137">-Protocol</span></span>
<span data-ttu-id="822f9-138">指定用來傳送探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="822f9-138">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="822f9-139">-超時</span><span class="sxs-lookup"><span data-stu-id="822f9-139">-Timeout</span></span>
<span data-ttu-id="822f9-140">指定探測超時（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="822f9-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="822f9-141">如果沒有收到此超時期間的有效回應，此 Cmdlet 會將探測標示為失敗。</span><span class="sxs-lookup"><span data-stu-id="822f9-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="822f9-142">有效值為1秒到86400秒。</span><span class="sxs-lookup"><span data-stu-id="822f9-142">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="822f9-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="822f9-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="822f9-144">指定 [探測重試計數]。</span><span class="sxs-lookup"><span data-stu-id="822f9-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="822f9-145">連續探測失敗計數達到不正常閾值之後，後端伺服器會標示為關閉。</span><span class="sxs-lookup"><span data-stu-id="822f9-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="822f9-146">有效值為1秒到20秒。</span><span class="sxs-lookup"><span data-stu-id="822f9-146">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="822f9-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822f9-147">CommonParameters</span></span>
<span data-ttu-id="822f9-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="822f9-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822f9-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="822f9-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822f9-150">輸入</span><span class="sxs-lookup"><span data-stu-id="822f9-150">INPUTS</span></span>

### <span data-ttu-id="822f9-151">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="822f9-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="822f9-152">輸出</span><span class="sxs-lookup"><span data-stu-id="822f9-152">OUTPUTS</span></span>

### <span data-ttu-id="822f9-153">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="822f9-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="822f9-154">筆記</span><span class="sxs-lookup"><span data-stu-id="822f9-154">NOTES</span></span>

## <span data-ttu-id="822f9-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="822f9-155">RELATED LINKS</span></span>

[<span data-ttu-id="822f9-156">附加 AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="822f9-156">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="822f9-157">AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="822f9-157">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="822f9-158">新-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="822f9-158">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="822f9-159">移除-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="822f9-159">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

