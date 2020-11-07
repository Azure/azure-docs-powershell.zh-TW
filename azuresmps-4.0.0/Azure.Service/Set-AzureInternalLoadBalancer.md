---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6D23ECB-C06E-4EB7-8096-33787E39694D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66f6bac80b219a2b3629b399bb568140a5cef217
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967400"
---
# <span data-ttu-id="159e2-101">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="159e2-101">Set-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="159e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="159e2-102">SYNOPSIS</span></span>
<span data-ttu-id="159e2-103">修改 Azure 服務中的內部負載平衡器設定。</span><span class="sxs-lookup"><span data-stu-id="159e2-103">Modifies an internal load balancer configuration in an Azure service.</span></span>

## <span data-ttu-id="159e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="159e2-104">SYNTAX</span></span>

### <span data-ttu-id="159e2-105">ServiceAndSlot (預設) </span><span class="sxs-lookup"><span data-stu-id="159e2-105">ServiceAndSlot (Default)</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="159e2-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="159e2-106">SubnetNameOnly</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="159e2-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="159e2-107">SubnetNameAndIP</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="159e2-108">說明</span><span class="sxs-lookup"><span data-stu-id="159e2-108">DESCRIPTION</span></span>
<span data-ttu-id="159e2-109">**AzureInternalLoadBalancer** Cmdlet 會修改 Azure 服務中的內部負載平衡器設定。</span><span class="sxs-lookup"><span data-stu-id="159e2-109">The **Set-AzureInternalLoadBalancer** cmdlet modifies an internal load balancer configuration in an Azure service.</span></span>
<span data-ttu-id="159e2-110">針對虛擬網路，您可以指定子網或內部負載平衡器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="159e2-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="159e2-111">示例</span><span class="sxs-lookup"><span data-stu-id="159e2-111">EXAMPLES</span></span>

### <span data-ttu-id="159e2-112">sr-1</span><span class="sxs-lookup"><span data-stu-id="159e2-112">1:</span></span>
```

```

## <span data-ttu-id="159e2-113">參數</span><span class="sxs-lookup"><span data-stu-id="159e2-113">PARAMETERS</span></span>

### <span data-ttu-id="159e2-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="159e2-114">-InformationAction</span></span>
<span data-ttu-id="159e2-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="159e2-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="159e2-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="159e2-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="159e2-117">持續</span><span class="sxs-lookup"><span data-stu-id="159e2-117">Continue</span></span>
- <span data-ttu-id="159e2-118">理會</span><span class="sxs-lookup"><span data-stu-id="159e2-118">Ignore</span></span>
- <span data-ttu-id="159e2-119">看</span><span class="sxs-lookup"><span data-stu-id="159e2-119">Inquire</span></span>
- <span data-ttu-id="159e2-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="159e2-120">SilentlyContinue</span></span>
- <span data-ttu-id="159e2-121">停止</span><span class="sxs-lookup"><span data-stu-id="159e2-121">Stop</span></span>
- <span data-ttu-id="159e2-122">封存</span><span class="sxs-lookup"><span data-stu-id="159e2-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159e2-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="159e2-123">-InformationVariable</span></span>
<span data-ttu-id="159e2-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="159e2-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="159e2-125">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="159e2-125">-InternalLoadBalancerName</span></span>
<span data-ttu-id="159e2-126">指定此 Cmdlet 所修改之內部負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="159e2-126">Specifies the name of the internal load balancer that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159e2-127">-設定檔</span><span class="sxs-lookup"><span data-stu-id="159e2-127">-Profile</span></span>
<span data-ttu-id="159e2-128">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="159e2-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="159e2-129">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="159e2-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="159e2-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="159e2-130">-ServiceName</span></span>
<span data-ttu-id="159e2-131">指定此 Cmdlet 修改內部負載平衡器的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="159e2-131">Specifies the name of the service in which this cmdlet modifies an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159e2-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="159e2-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="159e2-133">指定內部負載平衡器的虛擬網路 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="159e2-133">Specifies the virtual network IP address for an internal load balancer.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159e2-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="159e2-134">-SubnetName</span></span>
<span data-ttu-id="159e2-135">指定內部負載平衡器的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="159e2-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="159e2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="159e2-136">CommonParameters</span></span>
<span data-ttu-id="159e2-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="159e2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="159e2-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="159e2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="159e2-139">輸入</span><span class="sxs-lookup"><span data-stu-id="159e2-139">INPUTS</span></span>

## <span data-ttu-id="159e2-140">輸出</span><span class="sxs-lookup"><span data-stu-id="159e2-140">OUTPUTS</span></span>

## <span data-ttu-id="159e2-141">筆記</span><span class="sxs-lookup"><span data-stu-id="159e2-141">NOTES</span></span>

## <span data-ttu-id="159e2-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="159e2-142">RELATED LINKS</span></span>

[<span data-ttu-id="159e2-143">附加 AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="159e2-143">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="159e2-144">AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="159e2-144">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="159e2-145">新-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="159e2-145">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="159e2-146">移除-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="159e2-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)


