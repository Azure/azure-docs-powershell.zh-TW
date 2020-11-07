---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967240"
---
# <span data-ttu-id="60eae-101">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="60eae-101">Set-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="60eae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60eae-102">SYNOPSIS</span></span>
<span data-ttu-id="60eae-103">更新流量管理器設定檔的屬性。</span><span class="sxs-lookup"><span data-stu-id="60eae-103">Updates the properties of a Traffic Manager profile.</span></span>

## <span data-ttu-id="60eae-104">句法</span><span class="sxs-lookup"><span data-stu-id="60eae-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="60eae-105">說明</span><span class="sxs-lookup"><span data-stu-id="60eae-105">DESCRIPTION</span></span>
<span data-ttu-id="60eae-106">**AzureTrafficManagerProfile** Cmdlet 會更新 Microsoft Azure 流量管理器設定檔的屬性。</span><span class="sxs-lookup"><span data-stu-id="60eae-106">The **Set-AzureTrafficManagerProfile** cmdlet updates the properties of a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="60eae-107">針對您已將 *LoadBalancingMethod* 值設定為「容錯移轉」的設定檔，您可以使用 Add-AzureTrafficManagerEndpoint Cmdlet 來判斷您已新增至設定檔的端點的容錯移轉順序。</span><span class="sxs-lookup"><span data-stu-id="60eae-107">For profiles for which you have set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you have added to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="60eae-108">如需詳細資訊，請參閱下方的範例3。</span><span class="sxs-lookup"><span data-stu-id="60eae-108">For more information, see Example 3 below.</span></span>

## <span data-ttu-id="60eae-109">示例</span><span class="sxs-lookup"><span data-stu-id="60eae-109">EXAMPLES</span></span>

### <span data-ttu-id="60eae-110">範例1：設定流量管理器設定檔的 TTL</span><span class="sxs-lookup"><span data-stu-id="60eae-110">Example 1: Set the TTL for a Traffic Manager profile</span></span>
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

<span data-ttu-id="60eae-111">這個命令會將流量管理器設定檔物件 MyTrafficManagerProfile 的 TTL 設定為60秒。</span><span class="sxs-lookup"><span data-stu-id="60eae-111">This command sets the TTL to 60 seconds for the Traffic Manager profile object MyTrafficManagerProfile.</span></span>

### <span data-ttu-id="60eae-112">範例2：設定多個設定檔的值</span><span class="sxs-lookup"><span data-stu-id="60eae-112">Example 2: Set several values for a profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="60eae-113">這個命令會使用 **AzureTrafficManagerProfile** Cmdlet 取得名為 MyProfile 的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="60eae-113">This command gets a Traffic Manager profile named MyProfile by using the **Get-AzureTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="60eae-114">設定檔會使用 RoundRobin 負載平衡方法、30秒的 TTL、監視器通訊協定 HTTP、監視器埠，以及流量管理器設定檔的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="60eae-114">The profile uses the RoundRobin load balancing method, a TTL of 30 seconds,  the monitor protocol HTTP, the monitor port, and the relative path for a Traffic Manager profile.</span></span>

### <span data-ttu-id="60eae-115">範例3：將端點重新排序至所需的容錯移轉順序</span><span class="sxs-lookup"><span data-stu-id="60eae-115">Example 3: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="60eae-116">這個範例會將新增至 MyProfile 的端點重新排序為想要的容錯移轉順序。</span><span class="sxs-lookup"><span data-stu-id="60eae-116">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="60eae-117">第一個命令會取得名為 MyProfile 的流量管理器設定檔物件，並將物件儲存在 $Profile 變數中。</span><span class="sxs-lookup"><span data-stu-id="60eae-117">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="60eae-118">第二個命令會將端點陣列中的端點重新排序為應發生容錯移轉的順序。</span><span class="sxs-lookup"><span data-stu-id="60eae-118">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="60eae-119">最後一個命令會使用新的端點順序，更新 $Profile 中儲存的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="60eae-119">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="60eae-120">參數</span><span class="sxs-lookup"><span data-stu-id="60eae-120">PARAMETERS</span></span>

### <span data-ttu-id="60eae-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="60eae-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="60eae-122">指定用來散佈連接的負載平衡方法。</span><span class="sxs-lookup"><span data-stu-id="60eae-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="60eae-123">有效值為：</span><span class="sxs-lookup"><span data-stu-id="60eae-123">Valid values are:</span></span> 

- <span data-ttu-id="60eae-124">提高</span><span class="sxs-lookup"><span data-stu-id="60eae-124">Performance</span></span>
- <span data-ttu-id="60eae-125">實現</span><span class="sxs-lookup"><span data-stu-id="60eae-125">Failover</span></span>
- <span data-ttu-id="60eae-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="60eae-126">RoundRobin</span></span>

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

### <span data-ttu-id="60eae-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="60eae-127">-MonitorPort</span></span>
<span data-ttu-id="60eae-128">指定用來監視端點健康情況的埠。</span><span class="sxs-lookup"><span data-stu-id="60eae-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="60eae-129">有效值為大於0且小於或等於65535的整數值。</span><span class="sxs-lookup"><span data-stu-id="60eae-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

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

### <span data-ttu-id="60eae-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="60eae-130">-MonitorProtocol</span></span>
<span data-ttu-id="60eae-131">指定用來監視端點健康情況的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="60eae-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="60eae-132">有效值為：</span><span class="sxs-lookup"><span data-stu-id="60eae-132">Valid values are:</span></span> 

- <span data-ttu-id="60eae-133">Http</span><span class="sxs-lookup"><span data-stu-id="60eae-133">Http</span></span>
- <span data-ttu-id="60eae-134">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="60eae-134">Https</span></span>

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

### <span data-ttu-id="60eae-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="60eae-135">-MonitorRelativePath</span></span>
<span data-ttu-id="60eae-136">指定要探測健康狀態的端點網功能變數名稱稱相對路徑。</span><span class="sxs-lookup"><span data-stu-id="60eae-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="60eae-137">路徑必須符合下列限制：</span><span class="sxs-lookup"><span data-stu-id="60eae-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="60eae-138">路徑必須是1到1000個字元。</span><span class="sxs-lookup"><span data-stu-id="60eae-138">The path must be from 1 through 1000 characters.</span></span>
- <span data-ttu-id="60eae-139">它必須以正斜線（/）開頭。</span><span class="sxs-lookup"><span data-stu-id="60eae-139">It must start with a forward slash, /.</span></span>
- <span data-ttu-id="60eae-140">它不能包含 XML 元素 \<\> 。</span><span class="sxs-lookup"><span data-stu-id="60eae-140">It must contain no XML elements, \<\>.</span></span>
- <span data-ttu-id="60eae-141">它必須不包含雙斜杠（//）。</span><span class="sxs-lookup"><span data-stu-id="60eae-141">It must contain no double slashes, //.</span></span>
- <span data-ttu-id="60eae-142">它必須包含不正確 HTML 逸出字元。</span><span class="sxs-lookup"><span data-stu-id="60eae-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="60eae-143">例如，% XY。</span><span class="sxs-lookup"><span data-stu-id="60eae-143">For example, %XY.</span></span>

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

### <span data-ttu-id="60eae-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="60eae-144">-Name</span></span>
<span data-ttu-id="60eae-145">指定要更新的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="60eae-145">Specifies the name of the Traffic Manager profile to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60eae-146">-設定檔</span><span class="sxs-lookup"><span data-stu-id="60eae-146">-Profile</span></span>
<span data-ttu-id="60eae-147">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="60eae-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="60eae-148">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="60eae-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="60eae-149">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="60eae-149">-TrafficManagerProfile</span></span>
<span data-ttu-id="60eae-150">指定您用來設定設定檔的流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="60eae-150">Specifies the Traffic Manager profile object you use to set the profile.</span></span>

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

### <span data-ttu-id="60eae-151">-Ttl</span><span class="sxs-lookup"><span data-stu-id="60eae-151">-Ttl</span></span>
<span data-ttu-id="60eae-152">指定 DNS 存留時間 (TTL) ，該 TTL 會通知當地的 DNS 解析程式緩存 DNS 專案的時間長度。</span><span class="sxs-lookup"><span data-stu-id="60eae-152">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="60eae-153">有效值為30到999999的整數。</span><span class="sxs-lookup"><span data-stu-id="60eae-153">Valid values are an integer from 30 through 999,999.</span></span>

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

### <span data-ttu-id="60eae-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60eae-154">CommonParameters</span></span>
<span data-ttu-id="60eae-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60eae-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60eae-156">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60eae-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60eae-157">輸入</span><span class="sxs-lookup"><span data-stu-id="60eae-157">INPUTS</span></span>

## <span data-ttu-id="60eae-158">輸出</span><span class="sxs-lookup"><span data-stu-id="60eae-158">OUTPUTS</span></span>

### <span data-ttu-id="60eae-159">TrafficManager. IProfileWithDefinition （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="60eae-159">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="60eae-160">這個 Cmdlet 會產生流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="60eae-160">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="60eae-161">筆記</span><span class="sxs-lookup"><span data-stu-id="60eae-161">NOTES</span></span>

## <span data-ttu-id="60eae-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="60eae-162">RELATED LINKS</span></span>

[<span data-ttu-id="60eae-163">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="60eae-163">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="60eae-164">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="60eae-164">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="60eae-165">AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="60eae-165">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="60eae-166">新-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="60eae-166">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="60eae-167">移除-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="60eae-167">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)


