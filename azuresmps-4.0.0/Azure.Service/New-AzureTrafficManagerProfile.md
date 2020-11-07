---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967648"
---
# <span data-ttu-id="74582-101">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="74582-101">New-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="74582-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74582-102">SYNOPSIS</span></span>
<span data-ttu-id="74582-103">建立流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="74582-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="74582-104">句法</span><span class="sxs-lookup"><span data-stu-id="74582-104">SYNTAX</span></span>

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="74582-105">說明</span><span class="sxs-lookup"><span data-stu-id="74582-105">DESCRIPTION</span></span>
<span data-ttu-id="74582-106">**新的-AzureTrafficManagerProfile** Cmdlet 會建立 Microsoft Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="74582-106">The **New-AzureTrafficManagerProfile** cmdlet creates a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="74582-107">建立設定檔（在其中將 *LoadBalancingMethod* 值設定為「容錯移轉」）之後，您可以使用 Add-AzureTrafficManagerEndpoint Cmdlet 來判斷您新增到設定檔中的端點的容錯移轉順序。</span><span class="sxs-lookup"><span data-stu-id="74582-107">After you create a profile where you set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you add to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="74582-108">如需詳細資訊，請參閱下方的範例2。</span><span class="sxs-lookup"><span data-stu-id="74582-108">For more information, see Example 2 below.</span></span>

## <span data-ttu-id="74582-109">示例</span><span class="sxs-lookup"><span data-stu-id="74582-109">EXAMPLES</span></span>

### <span data-ttu-id="74582-110">範例1：建立流量管理器設定檔</span><span class="sxs-lookup"><span data-stu-id="74582-110">Example 1: Create a Traffic Manager profile</span></span>
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="74582-111">這個命令會在指定的流量管理器網域中使用迴圈負載平衡方法建立名為 MyProfile 的流量管理器設定檔，TTL 為30秒、HTTP 監視通訊協定、監視埠80，以及使用指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="74582-111">This command creates a Traffic Manager profile named MyProfile in the specified Traffic Manager domain with a Round Robin load balancing method, a TTL of 30 seconds, HTTP monitoring protocol, monitoring port 80, and with the specified path.</span></span>

### <span data-ttu-id="74582-112">範例2：重新排列端點至所需的容錯移轉順序</span><span class="sxs-lookup"><span data-stu-id="74582-112">Example 2: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="74582-113">這個範例會將新增至 MyProfile 的端點重新排序為想要的容錯移轉順序。</span><span class="sxs-lookup"><span data-stu-id="74582-113">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="74582-114">第一個命令會取得名為 MyProfile 的流量管理器設定檔物件，並將物件儲存在 $Profile 變數中。</span><span class="sxs-lookup"><span data-stu-id="74582-114">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="74582-115">第二個命令會將端點陣列中的端點重新排序為應發生容錯移轉的順序。</span><span class="sxs-lookup"><span data-stu-id="74582-115">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="74582-116">最後一個命令會使用新的端點順序，更新 $Profile 中儲存的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="74582-116">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="74582-117">參數</span><span class="sxs-lookup"><span data-stu-id="74582-117">PARAMETERS</span></span>

### <span data-ttu-id="74582-118">-功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="74582-118">-DomainName</span></span>
<span data-ttu-id="74582-119">指定流量管理器設定檔的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="74582-119">Specifies the domain name of the Traffic Manager profile.</span></span>
<span data-ttu-id="74582-120">這必須是 trafficmanager.net 的子域。</span><span class="sxs-lookup"><span data-stu-id="74582-120">This must be a subdomain of trafficmanager.net.</span></span>

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

### <span data-ttu-id="74582-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="74582-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="74582-122">指定用來散佈連接的負載平衡方法。</span><span class="sxs-lookup"><span data-stu-id="74582-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="74582-123">有效值為：</span><span class="sxs-lookup"><span data-stu-id="74582-123">Valid values are:</span></span> 

- <span data-ttu-id="74582-124">提高</span><span class="sxs-lookup"><span data-stu-id="74582-124">Performance</span></span>
- <span data-ttu-id="74582-125">實現</span><span class="sxs-lookup"><span data-stu-id="74582-125">Failover</span></span>
- <span data-ttu-id="74582-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="74582-126">RoundRobin</span></span>

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

### <span data-ttu-id="74582-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="74582-127">-MonitorPort</span></span>
<span data-ttu-id="74582-128">指定用來監視端點健康情況的埠。</span><span class="sxs-lookup"><span data-stu-id="74582-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="74582-129">有效值為大於0且小於或等於65535的整數值。</span><span class="sxs-lookup"><span data-stu-id="74582-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

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

### <span data-ttu-id="74582-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="74582-130">-MonitorProtocol</span></span>
<span data-ttu-id="74582-131">指定用來監視端點健康情況的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="74582-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="74582-132">有效值為：</span><span class="sxs-lookup"><span data-stu-id="74582-132">Valid values are:</span></span> 

- <span data-ttu-id="74582-133">Http</span><span class="sxs-lookup"><span data-stu-id="74582-133">Http</span></span>

- <span data-ttu-id="74582-134">Ip-HTTPs</span><span class="sxs-lookup"><span data-stu-id="74582-134">Https</span></span>

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

### <span data-ttu-id="74582-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="74582-135">-MonitorRelativePath</span></span>
<span data-ttu-id="74582-136">指定要探測健康狀態的端點網功能變數名稱稱相對路徑。</span><span class="sxs-lookup"><span data-stu-id="74582-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="74582-137">路徑必須符合下列限制：</span><span class="sxs-lookup"><span data-stu-id="74582-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="74582-138">路徑必須是1到1000個字元。</span><span class="sxs-lookup"><span data-stu-id="74582-138">The path must be from 1 through 1000 characters.</span></span>

- <span data-ttu-id="74582-139">它必須以正斜線（/）開頭。</span><span class="sxs-lookup"><span data-stu-id="74582-139">It must start with a forward slash, /.</span></span>

- <span data-ttu-id="74582-140">它不能包含 XML 元素 \<\> 。</span><span class="sxs-lookup"><span data-stu-id="74582-140">It must contain no XML elements, \<\>.</span></span>

- <span data-ttu-id="74582-141">它必須不包含雙斜杠（//）。</span><span class="sxs-lookup"><span data-stu-id="74582-141">It must contain no double slashes, //.</span></span>

- <span data-ttu-id="74582-142">它必須包含不正確 HTML 逸出字元。</span><span class="sxs-lookup"><span data-stu-id="74582-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="74582-143">例如，% XY。</span><span class="sxs-lookup"><span data-stu-id="74582-143">For example, %XY.</span></span>

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

### <span data-ttu-id="74582-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="74582-144">-Name</span></span>
<span data-ttu-id="74582-145">指定要建立的流量管理器設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="74582-145">Specifies the name of the Traffic Manager profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74582-146">-設定檔</span><span class="sxs-lookup"><span data-stu-id="74582-146">-Profile</span></span>
<span data-ttu-id="74582-147">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="74582-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="74582-148">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="74582-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="74582-149">-Ttl</span><span class="sxs-lookup"><span data-stu-id="74582-149">-Ttl</span></span>
<span data-ttu-id="74582-150">指定 DNS 存留時間 (TTL) ，該 TTL 會通知當地的 DNS 解析程式緩存 DNS 專案的時間長度。</span><span class="sxs-lookup"><span data-stu-id="74582-150">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="74582-151">有效的值是從30到999999的整數。</span><span class="sxs-lookup"><span data-stu-id="74582-151">Valid values are integers from 30 through 999,999.</span></span>

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

### <span data-ttu-id="74582-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74582-152">CommonParameters</span></span>
<span data-ttu-id="74582-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74582-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74582-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74582-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74582-155">輸入</span><span class="sxs-lookup"><span data-stu-id="74582-155">INPUTS</span></span>

## <span data-ttu-id="74582-156">輸出</span><span class="sxs-lookup"><span data-stu-id="74582-156">OUTPUTS</span></span>

### <span data-ttu-id="74582-157">TrafficManager. IProfileWithDefinition （WindowsAzure）</span><span class="sxs-lookup"><span data-stu-id="74582-157">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="74582-158">這個 Cmdlet 會產生流量管理器設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="74582-158">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="74582-159">筆記</span><span class="sxs-lookup"><span data-stu-id="74582-159">NOTES</span></span>

## <span data-ttu-id="74582-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="74582-160">RELATED LINKS</span></span>

[<span data-ttu-id="74582-161">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="74582-161">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="74582-162">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="74582-162">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="74582-163">AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="74582-163">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="74582-164">移除-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="74582-164">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="74582-165">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="74582-165">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


