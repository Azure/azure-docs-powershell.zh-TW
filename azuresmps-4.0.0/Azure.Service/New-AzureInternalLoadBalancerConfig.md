---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C01AFE1-65E7-4C5F-B3ED-8FCD9C4D20FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: a42ffe7ded2eb47638dd961ae79b10dd21cf08ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967360"
---
# <span data-ttu-id="e618c-101">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="e618c-101">New-AzureInternalLoadBalancerConfig</span></span>

## <span data-ttu-id="e618c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e618c-102">SYNOPSIS</span></span>
<span data-ttu-id="e618c-103">建立內部負載平衡器設定。</span><span class="sxs-lookup"><span data-stu-id="e618c-103">Creates an internal load balancer configuration.</span></span>

## <span data-ttu-id="e618c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e618c-104">SYNTAX</span></span>

### <span data-ttu-id="e618c-105">ServiceAndSlot (預設) </span><span class="sxs-lookup"><span data-stu-id="e618c-105">ServiceAndSlot (Default)</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e618c-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="e618c-106">SubnetNameOnly</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e618c-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="e618c-107">SubnetNameAndIP</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e618c-108">說明</span><span class="sxs-lookup"><span data-stu-id="e618c-108">DESCRIPTION</span></span>
<span data-ttu-id="e618c-109">**新的-AzureInternalLoadBalancerConfig** Cmdlet 會建立 **InternalLoadBalancerConfig** 物件。</span><span class="sxs-lookup"><span data-stu-id="e618c-109">The **New-AzureInternalLoadBalancerConfig** cmdlet creates an **InternalLoadBalancerConfig** object.</span></span>
<span data-ttu-id="e618c-110">當您建立 Azure 虛擬機器部署時，您可以使用內部負載平衡器配置。</span><span class="sxs-lookup"><span data-stu-id="e618c-110">You can use an internal load balancer configuration when you create an Azure virtual machine deployment.</span></span>

## <span data-ttu-id="e618c-111">示例</span><span class="sxs-lookup"><span data-stu-id="e618c-111">EXAMPLES</span></span>

### <span data-ttu-id="e618c-112">範例1：建立內部負載平衡器設定</span><span class="sxs-lookup"><span data-stu-id="e618c-112">Example 1: Create an internal load balancer configuration</span></span>
```
PS C:\> $IlbConfig = New-AzureInternalLoadBalancerConfig -InternalLoadBalancerName "Contoso" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="e618c-113">這個命令會為名為 FrontEndSubnet 的子網建立內部負載平衡器設定。</span><span class="sxs-lookup"><span data-stu-id="e618c-113">This command creates an internal load balancer configuration for the subnet named FrontEndSubnet.</span></span>
<span data-ttu-id="e618c-114">該命令會將設定儲存在 $IlbConfig 變數中，供您用來進行虛擬機器部署。</span><span class="sxs-lookup"><span data-stu-id="e618c-114">The command stores the configuration in the $IlbConfig variable for you to use for a virtual machine deployment.</span></span>

## <span data-ttu-id="e618c-115">參數</span><span class="sxs-lookup"><span data-stu-id="e618c-115">PARAMETERS</span></span>

### <span data-ttu-id="e618c-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e618c-116">-InformationAction</span></span>
<span data-ttu-id="e618c-117">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="e618c-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e618c-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="e618c-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e618c-119">持續</span><span class="sxs-lookup"><span data-stu-id="e618c-119">Continue</span></span>
- <span data-ttu-id="e618c-120">理會</span><span class="sxs-lookup"><span data-stu-id="e618c-120">Ignore</span></span>
- <span data-ttu-id="e618c-121">看</span><span class="sxs-lookup"><span data-stu-id="e618c-121">Inquire</span></span>
- <span data-ttu-id="e618c-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e618c-122">SilentlyContinue</span></span>
- <span data-ttu-id="e618c-123">停止</span><span class="sxs-lookup"><span data-stu-id="e618c-123">Stop</span></span>
- <span data-ttu-id="e618c-124">封存</span><span class="sxs-lookup"><span data-stu-id="e618c-124">Suspend</span></span>

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

### <span data-ttu-id="e618c-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e618c-125">-InformationVariable</span></span>
<span data-ttu-id="e618c-126">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="e618c-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e618c-127">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="e618c-127">-InternalLoadBalancerName</span></span>
<span data-ttu-id="e618c-128">指定此 Cmdlet 包含在配置中的內部負載等化器名稱。</span><span class="sxs-lookup"><span data-stu-id="e618c-128">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="e618c-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e618c-129">-Profile</span></span>
<span data-ttu-id="e618c-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e618c-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e618c-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e618c-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e618c-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="e618c-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="e618c-133">指定此 Cmdlet 包含在配置中的內部負載等化器虛擬網路 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e618c-133">Specifies the virtual network IP address for an internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e618c-134">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="e618c-134">-SubnetName</span></span>
<span data-ttu-id="e618c-135">指定內部負載平衡器的子網名稱。</span><span class="sxs-lookup"><span data-stu-id="e618c-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e618c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e618c-136">CommonParameters</span></span>
<span data-ttu-id="e618c-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e618c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e618c-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e618c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e618c-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e618c-139">INPUTS</span></span>

## <span data-ttu-id="e618c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e618c-140">OUTPUTS</span></span>

### <span data-ttu-id="e618c-141">WindowsAzure. ServiceManagement. InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="e618c-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerConfig</span></span>

## <span data-ttu-id="e618c-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e618c-142">NOTES</span></span>

## <span data-ttu-id="e618c-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e618c-143">RELATED LINKS</span></span>

[<span data-ttu-id="e618c-144">附加 AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e618c-144">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="e618c-145">AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e618c-145">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="e618c-146">移除-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e618c-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="e618c-147">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e618c-147">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


