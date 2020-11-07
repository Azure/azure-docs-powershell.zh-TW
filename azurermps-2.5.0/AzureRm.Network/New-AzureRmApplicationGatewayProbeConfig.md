---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 0e3c0c9a3f1c47163a28dc1732ef488f87014c63
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799806"
---
# <span data-ttu-id="ec9e9-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec9e9-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ec9e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ec9e9-103">建立健全性探針。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec9e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec9e9-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec9e9-105">說明</span><span class="sxs-lookup"><span data-stu-id="ec9e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ec9e9-106">New-AzureRmApplicationGatewayProbeConfig Cmdlet 會建立健全性探測器。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="ec9e9-107">示例</span><span class="sxs-lookup"><span data-stu-id="ec9e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ec9e9-108">Example1：建立健全性探針</span><span class="sxs-lookup"><span data-stu-id="ec9e9-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="ec9e9-109">這個命令會建立一個名為 Probe03 的健康情況探測，其 HTTP 通訊協定為30秒間隔，超時為120秒，且不正常的閾值為8次。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="ec9e9-110">參數</span><span class="sxs-lookup"><span data-stu-id="ec9e9-110">PARAMETERS</span></span>

### <span data-ttu-id="ec9e9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec9e9-111">-DefaultProfile</span></span>
<span data-ttu-id="ec9e9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec9e9-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="ec9e9-113">-HostName</span></span>
<span data-ttu-id="ec9e9-114">指定此 Cmdlet 傳送探測的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="ec9e9-115">間隔</span><span class="sxs-lookup"><span data-stu-id="ec9e9-115">-Interval</span></span>
<span data-ttu-id="ec9e9-116">指定探測間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="ec9e9-117">這是兩個連續探測器之間的時間間隔。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="ec9e9-118">這個值介於1秒與86400秒之間。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ec9e9-119">相符</span><span class="sxs-lookup"><span data-stu-id="ec9e9-119">-Match</span></span>
<span data-ttu-id="ec9e9-120">在健康情況回應中必須包含的主體。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="ec9e9-121">預設值為空白</span><span class="sxs-lookup"><span data-stu-id="ec9e9-121">Default value is empty</span></span>

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

### <span data-ttu-id="ec9e9-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="ec9e9-122">-MinServers</span></span>
<span data-ttu-id="ec9e9-123">最少標示為 [良好] 的伺服器數目。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="ec9e9-124">預設值為0</span><span class="sxs-lookup"><span data-stu-id="ec9e9-124">Default value is 0</span></span>

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

### <span data-ttu-id="ec9e9-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="ec9e9-125">-Name</span></span>
<span data-ttu-id="ec9e9-126">指定探測器的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="ec9e9-127">-Path</span><span class="sxs-lookup"><span data-stu-id="ec9e9-127">-Path</span></span>
<span data-ttu-id="ec9e9-128">指定探測的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="ec9e9-129">有效路徑是以斜線字元開頭 (/) 。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="ec9e9-130">探測會傳送至 \<Protocol\> ：// \<host\> ： \<port\> \<path\> 。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="ec9e9-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ec9e9-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="ec9e9-132">是否應從後端 HTTP 設定中挑選主機標頭。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="ec9e9-133">預設值為 false</span><span class="sxs-lookup"><span data-stu-id="ec9e9-133">Default value is false</span></span>

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

### <span data-ttu-id="ec9e9-134">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="ec9e9-134">-Protocol</span></span>
<span data-ttu-id="ec9e9-135">指定用來傳送探測的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="ec9e9-136">-超時</span><span class="sxs-lookup"><span data-stu-id="ec9e9-136">-Timeout</span></span>
<span data-ttu-id="ec9e9-137">指定探測超時（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="ec9e9-138">如果沒有收到此超時期間的有效回應，此 Cmdlet 會將探測標示為失敗。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="ec9e9-139">有效值為1秒到86400秒。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ec9e9-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="ec9e9-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="ec9e9-141">指定 [探測重試計數]。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="ec9e9-142">連續探測失敗計數達到不正常閾值之後，後端伺服器會標示為關閉。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="ec9e9-143">有效值為1秒到20秒。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="ec9e9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec9e9-144">CommonParameters</span></span>
<span data-ttu-id="ec9e9-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec9e9-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec9e9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec9e9-147">輸入</span><span class="sxs-lookup"><span data-stu-id="ec9e9-147">INPUTS</span></span>

## <span data-ttu-id="ec9e9-148">輸出</span><span class="sxs-lookup"><span data-stu-id="ec9e9-148">OUTPUTS</span></span>

### <span data-ttu-id="ec9e9-149">PSApplicationGatewayProbe 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ec9e9-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="ec9e9-150">筆記</span><span class="sxs-lookup"><span data-stu-id="ec9e9-150">NOTES</span></span>

## <span data-ttu-id="ec9e9-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec9e9-151">RELATED LINKS</span></span>

[<span data-ttu-id="ec9e9-152">使用 PowerShell for Azure 資源管理器建立應用程式閘道的自訂探測</span><span class="sxs-lookup"><span data-stu-id="ec9e9-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="ec9e9-153">附加 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec9e9-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ec9e9-154">AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec9e9-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ec9e9-155">移除-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec9e9-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ec9e9-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec9e9-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

