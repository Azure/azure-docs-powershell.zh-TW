---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 212e418c3fdaf8ba7f67ebdae0565d5d230daa0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449602"
---
# <span data-ttu-id="cbafd-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cbafd-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="cbafd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cbafd-102">SYNOPSIS</span></span>
<span data-ttu-id="cbafd-103">在現有的應用程式閘道上設定健康情況探針配置。</span><span class="sxs-lookup"><span data-stu-id="cbafd-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbafd-104">句法</span><span class="sxs-lookup"><span data-stu-id="cbafd-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbafd-105">說明</span><span class="sxs-lookup"><span data-stu-id="cbafd-105">DESCRIPTION</span></span>
<span data-ttu-id="cbafd-106">Set-AzureRmApplicationGatewayProbeConfig Cmdlet 會在現有的應用程式閘道上設定健康情況探針配置。</span><span class="sxs-lookup"><span data-stu-id="cbafd-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="cbafd-107">示例</span><span class="sxs-lookup"><span data-stu-id="cbafd-107">EXAMPLES</span></span>

### <span data-ttu-id="cbafd-108">範例1：在應用程式閘道設定健康情況探測的配置</span><span class="sxs-lookup"><span data-stu-id="cbafd-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="cbafd-109">這個命令會針對名為 [閘道] 的應用程式閘道，設定名為 Probe05 之健康情況探測的配置。</span><span class="sxs-lookup"><span data-stu-id="cbafd-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="cbafd-110">此命令也會將不健康閾值設定為8次重試，並在120秒後超時。</span><span class="sxs-lookup"><span data-stu-id="cbafd-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="cbafd-111">參數</span><span class="sxs-lookup"><span data-stu-id="cbafd-111">PARAMETERS</span></span>

### <span data-ttu-id="cbafd-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cbafd-112">-ApplicationGateway</span></span>
<span data-ttu-id="cbafd-113">指定此 Cmdlet 傳送探測的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="cbafd-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="cbafd-114">-HostName</span><span class="sxs-lookup"><span data-stu-id="cbafd-114">-HostName</span></span>
<span data-ttu-id="cbafd-115">指定此 Cmdlet 傳送探測的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="cbafd-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="cbafd-116">間隔</span><span class="sxs-lookup"><span data-stu-id="cbafd-116">-Interval</span></span>
<span data-ttu-id="cbafd-117">指定探測間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="cbafd-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="cbafd-118">這是兩個連續探測器之間的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="cbafd-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="cbafd-119">這個值介於1秒與86400秒之間。</span><span class="sxs-lookup"><span data-stu-id="cbafd-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="cbafd-120">相符</span><span class="sxs-lookup"><span data-stu-id="cbafd-120">-Match</span></span>
<span data-ttu-id="cbafd-121">在健康情況回應中必須包含的主體。</span><span class="sxs-lookup"><span data-stu-id="cbafd-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="cbafd-122">預設值為空白</span><span class="sxs-lookup"><span data-stu-id="cbafd-122">Default value is empty</span></span>

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

### <span data-ttu-id="cbafd-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="cbafd-123">-MinServers</span></span>
<span data-ttu-id="cbafd-124">最少標示為 [良好] 的伺服器數目。</span><span class="sxs-lookup"><span data-stu-id="cbafd-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="cbafd-125">預設值為0</span><span class="sxs-lookup"><span data-stu-id="cbafd-125">Default value is 0</span></span>

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

### <span data-ttu-id="cbafd-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="cbafd-126">-Name</span></span>
<span data-ttu-id="cbafd-127">指定探測器的名稱。</span><span class="sxs-lookup"><span data-stu-id="cbafd-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="cbafd-128">-Path</span><span class="sxs-lookup"><span data-stu-id="cbafd-128">-Path</span></span>
<span data-ttu-id="cbafd-129">指定探測的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="cbafd-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="cbafd-130">有效路徑是以斜線字元開頭 (/) 。</span><span class="sxs-lookup"><span data-stu-id="cbafd-130">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="cbafd-131">探測會傳送至 \<Protocol\> ：// \<host\> ： \<port\> \<path\> 。</span><span class="sxs-lookup"><span data-stu-id="cbafd-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="cbafd-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="cbafd-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="cbafd-133">是否應從後端 HTTP 設定中挑選主機標頭。</span><span class="sxs-lookup"><span data-stu-id="cbafd-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="cbafd-134">預設值為 false</span><span class="sxs-lookup"><span data-stu-id="cbafd-134">Default value is false</span></span>

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

### <span data-ttu-id="cbafd-135">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="cbafd-135">-Protocol</span></span>
<span data-ttu-id="cbafd-136">指定用來傳送探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="cbafd-136">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="cbafd-137">-超時</span><span class="sxs-lookup"><span data-stu-id="cbafd-137">-Timeout</span></span>
<span data-ttu-id="cbafd-138">指定探測超時（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="cbafd-138">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="cbafd-139">如果沒有收到此超時期間的有效回應，此 Cmdlet 會將探測標示為失敗。</span><span class="sxs-lookup"><span data-stu-id="cbafd-139">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="cbafd-140">有效值為1秒到86400秒。</span><span class="sxs-lookup"><span data-stu-id="cbafd-140">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="cbafd-141">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="cbafd-141">-UnhealthyThreshold</span></span>
<span data-ttu-id="cbafd-142">指定 [探測重試計數]。</span><span class="sxs-lookup"><span data-stu-id="cbafd-142">Specifies the probe retry count.</span></span>
<span data-ttu-id="cbafd-143">連續探測失敗計數達到不正常閾值之後，後端伺服器會標示為關閉。</span><span class="sxs-lookup"><span data-stu-id="cbafd-143">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="cbafd-144">有效值為1秒到20秒。</span><span class="sxs-lookup"><span data-stu-id="cbafd-144">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="cbafd-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbafd-145">-DefaultProfile</span></span>
<span data-ttu-id="cbafd-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cbafd-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbafd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbafd-147">CommonParameters</span></span>
<span data-ttu-id="cbafd-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cbafd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbafd-149">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cbafd-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbafd-150">輸入</span><span class="sxs-lookup"><span data-stu-id="cbafd-150">INPUTS</span></span>

### <span data-ttu-id="cbafd-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cbafd-151">PSApplicationGateway</span></span>
<span data-ttu-id="cbafd-152">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="cbafd-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="cbafd-153">輸出</span><span class="sxs-lookup"><span data-stu-id="cbafd-153">OUTPUTS</span></span>

### <span data-ttu-id="cbafd-154">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="cbafd-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="cbafd-155">筆記</span><span class="sxs-lookup"><span data-stu-id="cbafd-155">NOTES</span></span>

## <span data-ttu-id="cbafd-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="cbafd-156">RELATED LINKS</span></span>

[<span data-ttu-id="cbafd-157">附加 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cbafd-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="cbafd-158">AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cbafd-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="cbafd-159">新-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cbafd-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="cbafd-160">移除-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="cbafd-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

