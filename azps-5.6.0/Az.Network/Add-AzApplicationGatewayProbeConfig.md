---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 385a77c2b7b11d20b3ffb8d3728720b46c431d4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909554"
---
# <span data-ttu-id="6a7e7-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6a7e7-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="6a7e7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6a7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="6a7e7-103">為應用程式閘道新增健康狀態。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="6a7e7-104">語法</span><span class="sxs-lookup"><span data-stu-id="6a7e7-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a7e7-105">描述</span><span class="sxs-lookup"><span data-stu-id="6a7e7-105">DESCRIPTION</span></span>
<span data-ttu-id="6a7e7-106">Cmdlet Add-AzApplicationGatewayProbeConfig為應用程式閘道新增健康狀態。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="6a7e7-107">例子</span><span class="sxs-lookup"><span data-stu-id="6a7e7-107">EXAMPLES</span></span>

### <span data-ttu-id="6a7e7-108">範例 1：在應用程式閘道中新增健康提示</span><span class="sxs-lookup"><span data-stu-id="6a7e7-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="6a7e7-109">此命令會為名為 Gateway 的應用程式閘道新增名為 Command01 的健康狀態探索。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="6a7e7-110">此命令也會將不健康閾值設定為 8 次重試，120 秒之後會超過 8 次。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="6a7e7-111">參數</span><span class="sxs-lookup"><span data-stu-id="6a7e7-111">PARAMETERS</span></span>

### <span data-ttu-id="6a7e7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a7e7-112">-ApplicationGateway</span></span>
<span data-ttu-id="6a7e7-113">指定此 Cmdlet 新增專案的應用程式閘道。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="6a7e7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a7e7-114">-DefaultProfile</span></span>
<span data-ttu-id="6a7e7-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a7e7-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="6a7e7-116">-HostName</span></span>
<span data-ttu-id="6a7e7-117">指定此 Cmdlet 傳送通知的主機名稱稱。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="6a7e7-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="6a7e7-118">-Interval</span></span>
<span data-ttu-id="6a7e7-119">指定以秒為單位的間隔間隔。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="6a7e7-120">這是兩個連續的間隔時間。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="6a7e7-121">此值介於 1 秒到 86400 秒之間。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="6a7e7-122">-符合</span><span class="sxs-lookup"><span data-stu-id="6a7e7-122">-Match</span></span>
<span data-ttu-id="6a7e7-123">必須包含在健康回應中的內體。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="6a7e7-124">預設值為空白</span><span class="sxs-lookup"><span data-stu-id="6a7e7-124">Default value is empty</span></span>

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

### <span data-ttu-id="6a7e7-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="6a7e7-125">-MinServers</span></span>
<span data-ttu-id="6a7e7-126">一直標示為健康狀態的最低伺服器數量。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="6a7e7-127">預設值為 0</span><span class="sxs-lookup"><span data-stu-id="6a7e7-127">Default value is 0</span></span>

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

### <span data-ttu-id="6a7e7-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a7e7-128">-Name</span></span>
<span data-ttu-id="6a7e7-129">指定探索的名稱。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="6a7e7-130">-路徑</span><span class="sxs-lookup"><span data-stu-id="6a7e7-130">-Path</span></span>
<span data-ttu-id="6a7e7-131">指定建議的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="6a7e7-132">以斜線字元為開頭的有效路徑 (/) 。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="6a7e7-133">此通知會寄至 \<Protocol\> ：// \<host\> ： \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="6a7e7-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="6a7e7-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="6a7e7-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="6a7e7-135">是否應該從後端 HTTP 設定挑選主機標題。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="6a7e7-136">預設值為 False</span><span class="sxs-lookup"><span data-stu-id="6a7e7-136">Default value is false</span></span>

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

### <span data-ttu-id="6a7e7-137">-通訊協定</span><span class="sxs-lookup"><span data-stu-id="6a7e7-137">-Protocol</span></span>
<span data-ttu-id="6a7e7-138">指定用來傳送通知的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="6a7e7-139">此 Cmdlet 僅支援 HTTP。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="6a7e7-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="6a7e7-140">-Timeout</span></span>
<span data-ttu-id="6a7e7-141">指定以碼錶示的探索超時。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="6a7e7-142">如果在此超時期間未收到有效的回應，此 Cmdlet 會將探索標記為失敗。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="6a7e7-143">有效的值介於 1 秒到 86400 秒之間。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="6a7e7-144">-不健康Threshold</span><span class="sxs-lookup"><span data-stu-id="6a7e7-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="6a7e7-145">指定重新嘗試嘗試的次次計數。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="6a7e7-146">連續的啟動失敗計數達到不健康閾值之後，後端伺服器會標示為向下。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="6a7e7-147">有效的值介於 1 秒到 20 秒之間。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="6a7e7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a7e7-148">CommonParameters</span></span>
<span data-ttu-id="6a7e7-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a7e7-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6a7e7-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a7e7-151">輸入</span><span class="sxs-lookup"><span data-stu-id="6a7e7-151">INPUTS</span></span>

### <span data-ttu-id="6a7e7-152">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a7e7-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a7e7-153">輸出</span><span class="sxs-lookup"><span data-stu-id="6a7e7-153">OUTPUTS</span></span>

### <span data-ttu-id="6a7e7-154">Microsoft.Azure.Commands.Network.models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a7e7-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a7e7-155">筆記</span><span class="sxs-lookup"><span data-stu-id="6a7e7-155">NOTES</span></span>

## <span data-ttu-id="6a7e7-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a7e7-156">RELATED LINKS</span></span>

[<span data-ttu-id="6a7e7-157">為現有的應用程式閘道新增新結構</span><span class="sxs-lookup"><span data-stu-id="6a7e7-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="6a7e7-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6a7e7-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6a7e7-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6a7e7-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6a7e7-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6a7e7-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="6a7e7-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="6a7e7-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

