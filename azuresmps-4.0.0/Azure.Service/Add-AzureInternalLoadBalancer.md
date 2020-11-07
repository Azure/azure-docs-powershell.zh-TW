---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967170"
---
# <span data-ttu-id="22326-101">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22326-101">Add-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="22326-102">摘要</span><span class="sxs-lookup"><span data-stu-id="22326-102">SYNOPSIS</span></span>
<span data-ttu-id="22326-103">將內部負載平衡器新增至 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="22326-103">Adds an internal load balancer to an Azure service.</span></span>

## <span data-ttu-id="22326-104">句法</span><span class="sxs-lookup"><span data-stu-id="22326-104">SYNTAX</span></span>

### <span data-ttu-id="22326-105">ServiceAndSlot (預設) </span><span class="sxs-lookup"><span data-stu-id="22326-105">ServiceAndSlot (Default)</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="22326-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="22326-106">SubnetNameOnly</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="22326-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="22326-107">SubnetNameAndIP</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="22326-108">說明</span><span class="sxs-lookup"><span data-stu-id="22326-108">DESCRIPTION</span></span>
<span data-ttu-id="22326-109">**AzureInternalLoadBalancer** Cmdlet 會將內部負載平衡器配置新增至 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="22326-109">The **Add-AzureInternalLoadBalancer** cmdlet adds an internal load balancer configuration to an Azure service.</span></span>
<span data-ttu-id="22326-110">針對虛擬網路，您可以指定子網或內部負載平衡器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="22326-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="22326-111">示例</span><span class="sxs-lookup"><span data-stu-id="22326-111">EXAMPLES</span></span>

### <span data-ttu-id="22326-112">範例1：新增內部負載平衡器</span><span class="sxs-lookup"><span data-stu-id="22326-112">Example 1: Add an internal load balancer</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

<span data-ttu-id="22326-113">這個命令會將一個名為 ContosoILB 的內部負載平衡器新增到名為 ContosoWebsite01 的服務。</span><span class="sxs-lookup"><span data-stu-id="22326-113">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>

### <span data-ttu-id="22326-114">範例2：為指定的子網新增內部負載平衡器</span><span class="sxs-lookup"><span data-stu-id="22326-114">Example 2: Add an internal load balancer for a specified subnet</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="22326-115">這個命令會將一個名為 ContosoILB 的內部負載平衡器新增到名為 ContosoWebsite01 的服務。</span><span class="sxs-lookup"><span data-stu-id="22326-115">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="22326-116">此命令會指定名為 FrontEndSubnet 的子網。</span><span class="sxs-lookup"><span data-stu-id="22326-116">The command specifies the subnet named FrontEndSubnet.</span></span>

### <span data-ttu-id="22326-117">範例3：針對指定的子網和位址新增內部負載平衡器</span><span class="sxs-lookup"><span data-stu-id="22326-117">Example 3: Add an internal load balancer for a specified subnet and address</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

<span data-ttu-id="22326-118">這個命令會將一個名為 ContosoILB 的內部負載平衡器新增到名為 ContosoWebsite01 的服務。</span><span class="sxs-lookup"><span data-stu-id="22326-118">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="22326-119">此命令會指定名為 FrontEndSubnet 的子網，以及虛擬網路的靜態位址。</span><span class="sxs-lookup"><span data-stu-id="22326-119">The command specifies the subnet named FrontEndSubnet and the static address of the virtual network.</span></span>

## <span data-ttu-id="22326-120">參數</span><span class="sxs-lookup"><span data-stu-id="22326-120">PARAMETERS</span></span>

### <span data-ttu-id="22326-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="22326-121">-InformationAction</span></span>
<span data-ttu-id="22326-122">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="22326-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="22326-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="22326-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22326-124">持續</span><span class="sxs-lookup"><span data-stu-id="22326-124">Continue</span></span>
- <span data-ttu-id="22326-125">理會</span><span class="sxs-lookup"><span data-stu-id="22326-125">Ignore</span></span>
- <span data-ttu-id="22326-126">看</span><span class="sxs-lookup"><span data-stu-id="22326-126">Inquire</span></span>
- <span data-ttu-id="22326-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="22326-127">SilentlyContinue</span></span>
- <span data-ttu-id="22326-128">停止</span><span class="sxs-lookup"><span data-stu-id="22326-128">Stop</span></span>
- <span data-ttu-id="22326-129">封存</span><span class="sxs-lookup"><span data-stu-id="22326-129">Suspend</span></span>

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

### <span data-ttu-id="22326-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="22326-130">-InformationVariable</span></span>
<span data-ttu-id="22326-131">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="22326-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="22326-132">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="22326-132">-InternalLoadBalancerName</span></span>
<span data-ttu-id="22326-133">指定此 Cmdlet 所新增之內部負載平衡器的名稱。</span><span class="sxs-lookup"><span data-stu-id="22326-133">Specifies the name of the internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="22326-134">-設定檔</span><span class="sxs-lookup"><span data-stu-id="22326-134">-Profile</span></span>
<span data-ttu-id="22326-135">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="22326-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="22326-136">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="22326-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="22326-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="22326-137">-ServiceName</span></span>
<span data-ttu-id="22326-138">指定此 Cmdlet 新增內部負載平衡器之服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="22326-138">Specifies the name of the service to which this cmdlet adds an internal load balancer.</span></span>

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

### <span data-ttu-id="22326-139">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="22326-139">-StaticVNetIPAddress</span></span>
<span data-ttu-id="22326-140">指定此 Cmdlet 所新增之內部負載等化器的虛擬網路 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="22326-140">Specifies the virtual network IP address for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="22326-141">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="22326-141">-SubnetName</span></span>
<span data-ttu-id="22326-142">指定此 Cmdlet 所新增之內部負載等化器的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="22326-142">Specifies the name of the subnet for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="22326-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22326-143">CommonParameters</span></span>
<span data-ttu-id="22326-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="22326-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22326-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="22326-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22326-146">輸入</span><span class="sxs-lookup"><span data-stu-id="22326-146">INPUTS</span></span>

## <span data-ttu-id="22326-147">輸出</span><span class="sxs-lookup"><span data-stu-id="22326-147">OUTPUTS</span></span>

### <span data-ttu-id="22326-148">WindowsAzure. 常見. ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="22326-148">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="22326-149">筆記</span><span class="sxs-lookup"><span data-stu-id="22326-149">NOTES</span></span>

## <span data-ttu-id="22326-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="22326-150">RELATED LINKS</span></span>

[<span data-ttu-id="22326-151">AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22326-151">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="22326-152">新-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="22326-152">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="22326-153">移除-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22326-153">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="22326-154">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="22326-154">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


