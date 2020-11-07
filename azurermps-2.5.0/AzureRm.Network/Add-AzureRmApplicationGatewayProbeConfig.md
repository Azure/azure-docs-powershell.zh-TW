---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 87c064cbd3672a5e8d8f198432de87c0facf29cd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801629"
---
# <span data-ttu-id="ab3fa-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ab3fa-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ab3fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab3fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3fa-103">將健全性探測新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab3fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab3fa-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab3fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="ab3fa-105">DESCRIPTION</span></span>
<span data-ttu-id="ab3fa-106">Add-AzureRmApplicationGatewayProbeConfig Cmdlet 會將健康探測新增至應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="ab3fa-107">示例</span><span class="sxs-lookup"><span data-stu-id="ab3fa-107">EXAMPLES</span></span>

### <span data-ttu-id="ab3fa-108">範例1：將健全性探測器新增至應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="ab3fa-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="ab3fa-109">這個命令會將名為 Probe01 的 health 探測，新增到名為 Gateway 的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="ab3fa-110">此命令也會將不健康閾值設定為8次重試，並在120秒後超時。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="ab3fa-111">參數</span><span class="sxs-lookup"><span data-stu-id="ab3fa-111">PARAMETERS</span></span>

### <span data-ttu-id="ab3fa-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab3fa-112">-ApplicationGateway</span></span>
<span data-ttu-id="ab3fa-113">指定此 Cmdlet 新增探測的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="ab3fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab3fa-114">-DefaultProfile</span></span>
<span data-ttu-id="ab3fa-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab3fa-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="ab3fa-116">-HostName</span></span>
<span data-ttu-id="ab3fa-117">指定此 Cmdlet 傳送探測的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="ab3fa-118">間隔</span><span class="sxs-lookup"><span data-stu-id="ab3fa-118">-Interval</span></span>
<span data-ttu-id="ab3fa-119">指定探測間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="ab3fa-120">這是兩個連續探測器之間的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="ab3fa-121">這個值介於1秒與86400秒之間。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ab3fa-122">相符</span><span class="sxs-lookup"><span data-stu-id="ab3fa-122">-Match</span></span>
<span data-ttu-id="ab3fa-123">在健康情況回應中必須包含的主體。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="ab3fa-124">預設值為空白</span><span class="sxs-lookup"><span data-stu-id="ab3fa-124">Default value is empty</span></span>

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

### <span data-ttu-id="ab3fa-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="ab3fa-125">-MinServers</span></span>
<span data-ttu-id="ab3fa-126">最少標示為 [良好] 的伺服器數目。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="ab3fa-127">預設值為0</span><span class="sxs-lookup"><span data-stu-id="ab3fa-127">Default value is 0</span></span>

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

### <span data-ttu-id="ab3fa-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab3fa-128">-Name</span></span>
<span data-ttu-id="ab3fa-129">指定探測器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="ab3fa-130">-Path</span><span class="sxs-lookup"><span data-stu-id="ab3fa-130">-Path</span></span>
<span data-ttu-id="ab3fa-131">指定探測的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="ab3fa-132">有效路徑是以斜線字元開頭 (/) 。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="ab3fa-133">探測會傳送至 \<Protocol\> ：// \<host\> ： \<port\> \<path\> 。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="ab3fa-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ab3fa-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="ab3fa-135">是否應從後端 HTTP 設定中挑選主機標頭。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="ab3fa-136">預設值為 false</span><span class="sxs-lookup"><span data-stu-id="ab3fa-136">Default value is false</span></span>

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

### <span data-ttu-id="ab3fa-137">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="ab3fa-137">-Protocol</span></span>
<span data-ttu-id="ab3fa-138">指定用來傳送探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="ab3fa-139">這個 Cmdlet 只支援 HTTP。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="ab3fa-140">-超時</span><span class="sxs-lookup"><span data-stu-id="ab3fa-140">-Timeout</span></span>
<span data-ttu-id="ab3fa-141">指定探測超時（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="ab3fa-142">如果沒有收到此超時期間的有效回應，此 Cmdlet 會將探測標示為失敗。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="ab3fa-143">有效值為1秒到86400秒。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ab3fa-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="ab3fa-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="ab3fa-145">指定 [探測重試計數]。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="ab3fa-146">連續探測失敗計數達到不正常閾值之後，後端伺服器會標示為關閉。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="ab3fa-147">有效值為1秒到20秒。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="ab3fa-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3fa-148">CommonParameters</span></span>
<span data-ttu-id="ab3fa-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3fa-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ab3fa-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3fa-151">輸入</span><span class="sxs-lookup"><span data-stu-id="ab3fa-151">INPUTS</span></span>

### <span data-ttu-id="ab3fa-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ab3fa-152">PSApplicationGateway</span></span>
<span data-ttu-id="ab3fa-153">形參 "ApplicationGateway" 接受管線中 "PSApplicationGateway" 類型的值</span><span class="sxs-lookup"><span data-stu-id="ab3fa-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ab3fa-154">輸出</span><span class="sxs-lookup"><span data-stu-id="ab3fa-154">OUTPUTS</span></span>

### <span data-ttu-id="ab3fa-155">PSApplicationGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab3fa-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ab3fa-156">筆記</span><span class="sxs-lookup"><span data-stu-id="ab3fa-156">NOTES</span></span>

## <span data-ttu-id="ab3fa-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab3fa-157">RELATED LINKS</span></span>

[<span data-ttu-id="ab3fa-158">新增探測至現有的應用程式閘道</span><span class="sxs-lookup"><span data-stu-id="ab3fa-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="ab3fa-159">AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ab3fa-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ab3fa-160">新-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ab3fa-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ab3fa-161">移除-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ab3fa-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ab3fa-162">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ab3fa-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

