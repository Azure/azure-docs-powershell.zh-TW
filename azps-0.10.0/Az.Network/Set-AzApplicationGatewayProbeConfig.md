---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 50f54d258e6b5575983d8cd35f487783ea922eb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795444"
---
# <span data-ttu-id="ef6bf-101">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ef6bf-101">Set-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ef6bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef6bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6bf-103">在現有的應用程式閘道上設定健康情況探針配置。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="ef6bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef6bf-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef6bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef6bf-105">DESCRIPTION</span></span>
<span data-ttu-id="ef6bf-106">Set-AzApplicationGatewayProbeConfig Cmdlet 會在現有的應用程式閘道上設定健康情況探針配置。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-106">The Set-AzApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="ef6bf-107">示例</span><span class="sxs-lookup"><span data-stu-id="ef6bf-107">EXAMPLES</span></span>

### <span data-ttu-id="ef6bf-108">範例1：在應用程式閘道設定健康情況探測的配置</span><span class="sxs-lookup"><span data-stu-id="ef6bf-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="ef6bf-109">這個命令會針對名為 [閘道] 的應用程式閘道，設定名為 Probe05 之健康情況探測的配置。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="ef6bf-110">此命令也會將不健康閾值設定為8次重試，並在120秒後超時。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="ef6bf-111">參數</span><span class="sxs-lookup"><span data-stu-id="ef6bf-111">PARAMETERS</span></span>

### <span data-ttu-id="ef6bf-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef6bf-112">-ApplicationGateway</span></span>
<span data-ttu-id="ef6bf-113">指定此 Cmdlet 傳送探測的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef6bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6bf-114">-DefaultProfile</span></span>
<span data-ttu-id="ef6bf-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6bf-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="ef6bf-116">-HostName</span></span>
<span data-ttu-id="ef6bf-117">指定此 Cmdlet 傳送探測的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="ef6bf-118">間隔</span><span class="sxs-lookup"><span data-stu-id="ef6bf-118">-Interval</span></span>
<span data-ttu-id="ef6bf-119">指定探測間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="ef6bf-120">這是兩個連續探測器之間的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="ef6bf-121">這個值介於1秒與86400秒之間。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-121">This value is between 1 second and 86400 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6bf-122">相符</span><span class="sxs-lookup"><span data-stu-id="ef6bf-122">-Match</span></span>
<span data-ttu-id="ef6bf-123">在健康情況回應中必須包含的主體。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="ef6bf-124">預設值為空白</span><span class="sxs-lookup"><span data-stu-id="ef6bf-124">Default value is empty</span></span>

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6bf-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="ef6bf-125">-MinServers</span></span>
<span data-ttu-id="ef6bf-126">最少標示為 [良好] 的伺服器數目。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="ef6bf-127">預設值為0</span><span class="sxs-lookup"><span data-stu-id="ef6bf-127">Default value is 0</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6bf-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef6bf-128">-Name</span></span>
<span data-ttu-id="ef6bf-129">指定探測器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-129">Specifies the name of the probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6bf-130">-Path</span><span class="sxs-lookup"><span data-stu-id="ef6bf-130">-Path</span></span>
<span data-ttu-id="ef6bf-131">指定探測的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="ef6bf-132">有效路徑是以斜線字元開頭 (/) 。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-132">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="ef6bf-133">探測會傳送至 \< 通訊協定 \> ：// \< 主機 \> ： \< 埠 \> \< 路徑 \> 。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6bf-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ef6bf-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="ef6bf-135">是否應從後端 HTTP 設定中挑選主機標頭。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="ef6bf-136">預設值為 false</span><span class="sxs-lookup"><span data-stu-id="ef6bf-136">Default value is false</span></span>

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

### <span data-ttu-id="ef6bf-137">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="ef6bf-137">-Protocol</span></span>
<span data-ttu-id="ef6bf-138">指定用來傳送探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-138">Specifies the protocol used to send probe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6bf-139">-超時</span><span class="sxs-lookup"><span data-stu-id="ef6bf-139">-Timeout</span></span>
<span data-ttu-id="ef6bf-140">指定探測超時（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-140">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="ef6bf-141">如果沒有收到此超時期間的有效回應，此 Cmdlet 會將探測標示為失敗。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-141">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="ef6bf-142">有效值為1秒到86400秒。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-142">Valid values are between 1 second and 86400 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6bf-143">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="ef6bf-143">-UnhealthyThreshold</span></span>
<span data-ttu-id="ef6bf-144">指定 [探測重試計數]。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-144">Specifies the probe retry count.</span></span>
<span data-ttu-id="ef6bf-145">連續探測失敗計數達到不正常閾值之後，後端伺服器會標示為關閉。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-145">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="ef6bf-146">有效值為1秒到20秒。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-146">Valid values are between 1 second and 20 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef6bf-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6bf-147">CommonParameters</span></span>
<span data-ttu-id="ef6bf-148">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6bf-149">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef6bf-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6bf-150">輸入</span><span class="sxs-lookup"><span data-stu-id="ef6bf-150">INPUTS</span></span>

### <span data-ttu-id="ef6bf-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ef6bf-151">PSApplicationGateway</span></span>
<span data-ttu-id="ef6bf-152">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ef6bf-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ef6bf-153">輸出</span><span class="sxs-lookup"><span data-stu-id="ef6bf-153">OUTPUTS</span></span>

### <span data-ttu-id="ef6bf-154">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ef6bf-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ef6bf-155">筆記</span><span class="sxs-lookup"><span data-stu-id="ef6bf-155">NOTES</span></span>

## <span data-ttu-id="ef6bf-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef6bf-156">RELATED LINKS</span></span>

[<span data-ttu-id="ef6bf-157">附加 AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ef6bf-157">Add-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ef6bf-158">AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ef6bf-158">Get-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ef6bf-159">新-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ef6bf-159">New-AzApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ef6bf-160">移除-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ef6bf-160">Remove-AzApplicationGatewayProbeConfig</span></span>]()

