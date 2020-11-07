---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967822"
---
# <span data-ttu-id="a7b2a-101">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7b2a-101">Add-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="a7b2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b2a-103">將端點新增到流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-103">Adds an endpoint to a Traffic Manager profile.</span></span>

## <span data-ttu-id="a7b2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7b2a-104">SYNTAX</span></span>

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a7b2a-105">說明</span><span class="sxs-lookup"><span data-stu-id="a7b2a-105">DESCRIPTION</span></span>
<span data-ttu-id="a7b2a-106">**AzureTrafficManagerEndpoint** Cmdlet 會將端點新增到 Microsoft Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-106">The **Add-AzureTrafficManagerEndpoint** cmdlet adds an endpoint to a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="a7b2a-107">在您新增端點之後，使用管線運算子將結果傳遞給 **AzureTrafficManagerProfile** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-107">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a7b2a-108">該 Cmdlet 會連線至 Azure 以儲存您的變更。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="a7b2a-109">示例</span><span class="sxs-lookup"><span data-stu-id="a7b2a-109">EXAMPLES</span></span>

### <span data-ttu-id="a7b2a-110">範例1：在設定檔中新增端點</span><span class="sxs-lookup"><span data-stu-id="a7b2a-110">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="a7b2a-111">第一個命令使用 **AzureTrafficManagerProfile** Cmdlet 來取得名為 ContosoProfile 的設定檔，然後將它儲存在 $TrafficManagerProfile 變數中。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="a7b2a-112">第二個命令會將端點新增至儲存在 $TrafficManagerProfile 的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-112">The second command adds an endpoint to Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="a7b2a-113">端點會有 [功能變數名稱 Contoso02App.couldapp.net]。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-113">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="a7b2a-114">該命令也會指定是否已啟用它及其類型。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-114">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="a7b2a-115">命令會將設定檔物件傳遞給 **AzureTrafficManagerProfile** Cmdlet 以連線至 Azure，以儲存您的變更。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-115">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

### <span data-ttu-id="a7b2a-116">範例2：新增具有指定位置和寬度的端點</span><span class="sxs-lookup"><span data-stu-id="a7b2a-116">Example 2: Add an endpoint that has a specified location and weight</span></span>
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="a7b2a-117">這個命令會將端點新增到流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-117">This command adds an endpoint to a Traffic Manager profile.</span></span>
<span data-ttu-id="a7b2a-118">端點會有 [功能變數名稱 Contoso02App.couldapp.net]。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-118">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="a7b2a-119">該命令也會指定是否已啟用它及其類型。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-119">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="a7b2a-120">此命令也會指定端點的粗細和位置。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-120">The command also specifies the weight and location for the endpoint.</span></span>
<span data-ttu-id="a7b2a-121">命令會將設定檔物件傳遞給 **AzureTrafficManagerProfile** ，以連接至 Azure 以儲存變更。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-121">The command passes the profile object to **Set-AzureTrafficManagerProfile** to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="a7b2a-122">參數</span><span class="sxs-lookup"><span data-stu-id="a7b2a-122">PARAMETERS</span></span>

### <span data-ttu-id="a7b2a-123">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="a7b2a-123">-DomainName</span></span>
<span data-ttu-id="a7b2a-124">指定要新增之端點的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-124">Specifies the domain name of the endpoint to add.</span></span>

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

### <span data-ttu-id="a7b2a-125">-位置</span><span class="sxs-lookup"><span data-stu-id="a7b2a-125">-Location</span></span>
<span data-ttu-id="a7b2a-126">指定 Cmdlet 所新增之端點的位置。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-126">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="a7b2a-127">這必須是 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-127">This must be an Azure location.</span></span>

<span data-ttu-id="a7b2a-128">此參數必須在已將負載平衡方法設定為 "效能" 的設定檔中，包含類型 "Any" 或 "TrafficManager" 類型的端點的值。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-128">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="a7b2a-129">可能的值是 Azure 地區名稱，如所列 https://azure.microsoft.com/regions/ 。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-129">The possible values are the Azure region names, as listed at https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="a7b2a-130">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="a7b2a-130">-MinChildEndpoints</span></span>
<span data-ttu-id="a7b2a-131">指定嵌套設定檔必須以線上方式將此端點視為線上的最小端點數。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-131">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="a7b2a-132">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a7b2a-132">-Profile</span></span>
<span data-ttu-id="a7b2a-133">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a7b2a-134">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a7b2a-135">-狀態</span><span class="sxs-lookup"><span data-stu-id="a7b2a-135">-Status</span></span>
<span data-ttu-id="a7b2a-136">指定監視端點的狀態。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-136">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="a7b2a-137">有效值為：</span><span class="sxs-lookup"><span data-stu-id="a7b2a-137">Valid values are:</span></span> 

- <span data-ttu-id="a7b2a-138">後</span><span class="sxs-lookup"><span data-stu-id="a7b2a-138">Enabled</span></span>
- <span data-ttu-id="a7b2a-139">禁止</span><span class="sxs-lookup"><span data-stu-id="a7b2a-139">Disabled</span></span>

<span data-ttu-id="a7b2a-140">如果您指定的值為 [已啟用]，流量管理器會監視端點，且負載平衡方法會在管理流量時考慮它。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-140">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="a7b2a-141">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a7b2a-141">-TrafficManagerProfile</span></span>
<span data-ttu-id="a7b2a-142">指定要新增端點的流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-142">Specifies the Traffic Manager profile object to which to add the endpoint.</span></span>

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

### <span data-ttu-id="a7b2a-143">-類型</span><span class="sxs-lookup"><span data-stu-id="a7b2a-143">-Type</span></span>
<span data-ttu-id="a7b2a-144">指定端點的類型。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-144">Specifies the type of endpoint.</span></span>
<span data-ttu-id="a7b2a-145">有效值為：</span><span class="sxs-lookup"><span data-stu-id="a7b2a-145">Valid values are:</span></span> 

- <span data-ttu-id="a7b2a-146">CloudService</span><span class="sxs-lookup"><span data-stu-id="a7b2a-146">CloudService</span></span>
- <span data-ttu-id="a7b2a-147">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="a7b2a-147">AzureWebsite</span></span>
- <span data-ttu-id="a7b2a-148">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="a7b2a-148">TrafficManager</span></span>

- <span data-ttu-id="a7b2a-149">每</span><span class="sxs-lookup"><span data-stu-id="a7b2a-149">Any</span></span> 

<span data-ttu-id="a7b2a-150">如果有一個以上的 AzureWebsite 端點，端點必須位於不同的資料中心。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-150">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="a7b2a-151">寬度</span><span class="sxs-lookup"><span data-stu-id="a7b2a-151">-Weight</span></span>
<span data-ttu-id="a7b2a-152">指定 Cmdlet 所新增之端點的權重。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-152">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="a7b2a-153">這個參數的有效值範圍是 \[ 1，1000 \] 。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-153">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="a7b2a-154">這個參數只適用于 RoundRobin 負載平衡原則。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-154">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="a7b2a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b2a-155">CommonParameters</span></span>
<span data-ttu-id="a7b2a-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b2a-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b2a-158">輸入</span><span class="sxs-lookup"><span data-stu-id="a7b2a-158">INPUTS</span></span>

## <span data-ttu-id="a7b2a-159">輸出</span><span class="sxs-lookup"><span data-stu-id="a7b2a-159">OUTPUTS</span></span>

### <span data-ttu-id="a7b2a-160">TrafficManager. IProfileWithDefinition （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="a7b2a-160">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="a7b2a-161">這個 Cmdlet 會產生流量管理器設定檔物件，其中包含已更新設定檔的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a7b2a-161">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="a7b2a-162">筆記</span><span class="sxs-lookup"><span data-stu-id="a7b2a-162">NOTES</span></span>

## <span data-ttu-id="a7b2a-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7b2a-163">RELATED LINKS</span></span>

[<span data-ttu-id="a7b2a-164">移除-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7b2a-164">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="a7b2a-165">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a7b2a-165">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="a7b2a-166">AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a7b2a-166">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="a7b2a-167">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a7b2a-167">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


