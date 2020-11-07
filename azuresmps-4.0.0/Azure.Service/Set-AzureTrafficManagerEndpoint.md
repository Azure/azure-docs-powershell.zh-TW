---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966880"
---
# <span data-ttu-id="f6c96-101">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6c96-101">Set-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="f6c96-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6c96-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c96-103">更新流量管理器設定檔中端點的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6c96-103">Updates the properties of an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="f6c96-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6c96-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f6c96-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6c96-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c96-106">**AzureTrafficManagerEndpoint** Cmdlet 會更新 Microsoft Azure 流量管理器設定檔中端點的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6c96-106">The **Set-AzureTrafficManagerEndpoint** cmdlet updates the properties of an endpoint in a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f6c96-107">如果端點在目前的設定檔中不存在，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="f6c96-107">If the endpoint does not exist in the current profile, this cmdlet creates it.</span></span>
<span data-ttu-id="f6c96-108">在您新增端點之後，使用管線運算子將結果傳遞給 **AzureTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6c96-108">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f6c96-109">該 Cmdlet 會連線至 Azure 以儲存您的變更。</span><span class="sxs-lookup"><span data-stu-id="f6c96-109">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="f6c96-110">示例</span><span class="sxs-lookup"><span data-stu-id="f6c96-110">EXAMPLES</span></span>

### <span data-ttu-id="f6c96-111">範例1：更新設定檔的端點</span><span class="sxs-lookup"><span data-stu-id="f6c96-111">Example 1: Update an endpoint for a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="f6c96-112">第一個命令使用 **AzureTrafficManagerProfile** Cmdlet 來取得名為 ContosoProfile 的設定檔，然後將它儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="f6c96-112">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="f6c96-113">第二個命令會更新 $TrafficManagerProfile 中儲存的流量管理器設定檔中的端點。</span><span class="sxs-lookup"><span data-stu-id="f6c96-113">The second command updates the endpoint in the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f6c96-114">端點會有 [功能變數名稱 ContosoApp02.cloudapp.net]。</span><span class="sxs-lookup"><span data-stu-id="f6c96-114">The endpoint has the domain name ContosoApp02.cloudapp.net.</span></span>
<span data-ttu-id="f6c96-115">該命令也會指定端點的狀態、類型、粗細和位置。</span><span class="sxs-lookup"><span data-stu-id="f6c96-115">The command also specifies the status, type, weight, and location of the endpoint.</span></span>
<span data-ttu-id="f6c96-116">該命令會將修改過的設定檔傳遞給 **AzureTrafficManagerProfile** Cmdlet，以連線至 Azure 以儲存您的變更。</span><span class="sxs-lookup"><span data-stu-id="f6c96-116">The command passes the modified profile to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="f6c96-117">參數</span><span class="sxs-lookup"><span data-stu-id="f6c96-117">PARAMETERS</span></span>

### <span data-ttu-id="f6c96-118">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="f6c96-118">-DomainName</span></span>
<span data-ttu-id="f6c96-119">指定要修改之端點的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="f6c96-119">Specifies the domain name of the endpoint to modify.</span></span>

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

### <span data-ttu-id="f6c96-120">-位置</span><span class="sxs-lookup"><span data-stu-id="f6c96-120">-Location</span></span>
<span data-ttu-id="f6c96-121">指定 Cmdlet 所新增之端點的位置。</span><span class="sxs-lookup"><span data-stu-id="f6c96-121">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="f6c96-122">這必須是 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="f6c96-122">This must be an Azure location.</span></span>

<span data-ttu-id="f6c96-123">此參數必須在已將負載平衡方法設定為 "效能" 的設定檔中，包含類型 "Any" 或 "TrafficManager" 類型的端點的值。</span><span class="sxs-lookup"><span data-stu-id="f6c96-123">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="f6c96-124">可能的值是 Azure 地區名稱，如所列  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ 。</span><span class="sxs-lookup"><span data-stu-id="f6c96-124">The possible values are the Azure region names, as listed at  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="f6c96-125">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="f6c96-125">-MinChildEndpoints</span></span>
<span data-ttu-id="f6c96-126">指定嵌套設定檔必須以線上方式將此端點視為線上的最小端點數。</span><span class="sxs-lookup"><span data-stu-id="f6c96-126">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="f6c96-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="f6c96-127">-Profile</span></span>
<span data-ttu-id="f6c96-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="f6c96-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f6c96-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="f6c96-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6c96-130">-狀態</span><span class="sxs-lookup"><span data-stu-id="f6c96-130">-Status</span></span>
<span data-ttu-id="f6c96-131">指定監視端點的狀態。</span><span class="sxs-lookup"><span data-stu-id="f6c96-131">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="f6c96-132">有效值為：</span><span class="sxs-lookup"><span data-stu-id="f6c96-132">Valid values are:</span></span> 

- <span data-ttu-id="f6c96-133">後</span><span class="sxs-lookup"><span data-stu-id="f6c96-133">Enabled</span></span>
- <span data-ttu-id="f6c96-134">禁止</span><span class="sxs-lookup"><span data-stu-id="f6c96-134">Disabled</span></span>

<span data-ttu-id="f6c96-135">如果您指定的值為 [已啟用]，流量管理器會監視端點，且負載平衡方法會在管理流量時考慮它。</span><span class="sxs-lookup"><span data-stu-id="f6c96-135">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="f6c96-136">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6c96-136">-TrafficManagerProfile</span></span>
<span data-ttu-id="f6c96-137">指定要為其修改端點的流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="f6c96-137">Specifies the Traffic Manager profile object for which to modify the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6c96-138">-類型</span><span class="sxs-lookup"><span data-stu-id="f6c96-138">-Type</span></span>
<span data-ttu-id="f6c96-139">指定端點的類型。</span><span class="sxs-lookup"><span data-stu-id="f6c96-139">Specifies the type of endpoint.</span></span>
<span data-ttu-id="f6c96-140">有效值為：</span><span class="sxs-lookup"><span data-stu-id="f6c96-140">Valid values are:</span></span> 

- <span data-ttu-id="f6c96-141">CloudService</span><span class="sxs-lookup"><span data-stu-id="f6c96-141">CloudService</span></span>
- <span data-ttu-id="f6c96-142">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="f6c96-142">AzureWebsite</span></span>
- <span data-ttu-id="f6c96-143">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="f6c96-143">TrafficManager</span></span>

- <span data-ttu-id="f6c96-144">每</span><span class="sxs-lookup"><span data-stu-id="f6c96-144">Any</span></span> 

<span data-ttu-id="f6c96-145">如果有一個以上的 AzureWebsite 端點，端點必須位於不同的資料中心。</span><span class="sxs-lookup"><span data-stu-id="f6c96-145">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="f6c96-146">寬度</span><span class="sxs-lookup"><span data-stu-id="f6c96-146">-Weight</span></span>
<span data-ttu-id="f6c96-147">指定 Cmdlet 所新增之端點的權重。</span><span class="sxs-lookup"><span data-stu-id="f6c96-147">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="f6c96-148">這個參數的有效值範圍是 \[ 1，1000 \] 。</span><span class="sxs-lookup"><span data-stu-id="f6c96-148">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="f6c96-149">這個參數只適用于 RoundRobin 負載平衡原則。</span><span class="sxs-lookup"><span data-stu-id="f6c96-149">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="f6c96-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c96-150">CommonParameters</span></span>
<span data-ttu-id="f6c96-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6c96-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c96-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6c96-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c96-153">輸入</span><span class="sxs-lookup"><span data-stu-id="f6c96-153">INPUTS</span></span>

## <span data-ttu-id="f6c96-154">輸出</span><span class="sxs-lookup"><span data-stu-id="f6c96-154">OUTPUTS</span></span>

### <span data-ttu-id="f6c96-155">TrafficManager. IProfileWithDefinition （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="f6c96-155">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="f6c96-156">這個 Cmdlet 會產生流量管理器設定檔物件，其中包含已更新設定檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f6c96-156">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="f6c96-157">筆記</span><span class="sxs-lookup"><span data-stu-id="f6c96-157">NOTES</span></span>

## <span data-ttu-id="f6c96-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6c96-158">RELATED LINKS</span></span>

[<span data-ttu-id="f6c96-159">附加 AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6c96-159">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="f6c96-160">移除-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6c96-160">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="f6c96-161">AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6c96-161">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="f6c96-162">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f6c96-162">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


