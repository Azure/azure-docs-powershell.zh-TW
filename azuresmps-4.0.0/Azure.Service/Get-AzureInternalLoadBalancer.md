---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A439ADC4-991E-4860-82AA-7BED315991B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9f28659835fef4778eac729ccd020eb82f563bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967786"
---
# <span data-ttu-id="46591-101">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46591-101">Get-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="46591-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46591-102">SYNOPSIS</span></span>
<span data-ttu-id="46591-103">取得內部負載平衡器設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="46591-103">Gets the details of the internal load balancer configuration.</span></span>

## <span data-ttu-id="46591-104">句法</span><span class="sxs-lookup"><span data-stu-id="46591-104">SYNTAX</span></span>

```
Get-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="46591-105">說明</span><span class="sxs-lookup"><span data-stu-id="46591-105">DESCRIPTION</span></span>
<span data-ttu-id="46591-106">**AzureInternalLoadBalancer** Cmdlet 會取得 Azure 服務內部負載平衡器設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="46591-106">The **Get-AzureInternalLoadBalancer** cmdlet gets the details of the internal load balancer configuration for an Azure service.</span></span>

## <span data-ttu-id="46591-107">示例</span><span class="sxs-lookup"><span data-stu-id="46591-107">EXAMPLES</span></span>

### <span data-ttu-id="46591-108">範例1：取得內部負載平衡器的詳細資料</span><span class="sxs-lookup"><span data-stu-id="46591-108">Example 1: Get details for an internal load balancer</span></span>
```
PS C:\> Get-AzureService -ServiceName "ContosoService" | Get-AzureInternalLoadBalancer
```

<span data-ttu-id="46591-109">這個命令會使用 **AzureService** Cmdlet 取得名為 ContosoService 的服務。</span><span class="sxs-lookup"><span data-stu-id="46591-109">This command gets the service named ContosoService by using the **Get-AzureService** cmdlet.</span></span>
<span data-ttu-id="46591-110">命令會使用管線運算子，將該服務傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46591-110">The command passes that service to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="46591-111">目前的 Cmdlet 會取得該服務內部負載平衡器的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="46591-111">The current cmdlet gets details for the internal load balancer for that service.</span></span>

## <span data-ttu-id="46591-112">參數</span><span class="sxs-lookup"><span data-stu-id="46591-112">PARAMETERS</span></span>

### <span data-ttu-id="46591-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="46591-113">-InformationAction</span></span>
<span data-ttu-id="46591-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="46591-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="46591-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="46591-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46591-116">持續</span><span class="sxs-lookup"><span data-stu-id="46591-116">Continue</span></span>
- <span data-ttu-id="46591-117">理會</span><span class="sxs-lookup"><span data-stu-id="46591-117">Ignore</span></span>
- <span data-ttu-id="46591-118">看</span><span class="sxs-lookup"><span data-stu-id="46591-118">Inquire</span></span>
- <span data-ttu-id="46591-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="46591-119">SilentlyContinue</span></span>
- <span data-ttu-id="46591-120">停止</span><span class="sxs-lookup"><span data-stu-id="46591-120">Stop</span></span>
- <span data-ttu-id="46591-121">封存</span><span class="sxs-lookup"><span data-stu-id="46591-121">Suspend</span></span>

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

### <span data-ttu-id="46591-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="46591-122">-InformationVariable</span></span>
<span data-ttu-id="46591-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="46591-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="46591-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="46591-124">-Profile</span></span>
<span data-ttu-id="46591-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="46591-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46591-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="46591-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46591-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="46591-127">-ServiceName</span></span>
<span data-ttu-id="46591-128">指定此 Cmdlet 針對內部負載平衡器取得詳細資料的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="46591-128">Specifies the name of the service for which this cmdlet gets details for an internal load balancer.</span></span>

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

### <span data-ttu-id="46591-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46591-129">CommonParameters</span></span>
<span data-ttu-id="46591-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46591-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46591-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46591-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46591-132">輸入</span><span class="sxs-lookup"><span data-stu-id="46591-132">INPUTS</span></span>

## <span data-ttu-id="46591-133">輸出</span><span class="sxs-lookup"><span data-stu-id="46591-133">OUTPUTS</span></span>

### <span data-ttu-id="46591-134">WindowsAzure. ServiceManagement. InternalLoadBalancerCoNtext</span><span class="sxs-lookup"><span data-stu-id="46591-134">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerContext</span></span>

## <span data-ttu-id="46591-135">筆記</span><span class="sxs-lookup"><span data-stu-id="46591-135">NOTES</span></span>

## <span data-ttu-id="46591-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="46591-136">RELATED LINKS</span></span>

[<span data-ttu-id="46591-137">附加 AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46591-137">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="46591-138">AzureService</span><span class="sxs-lookup"><span data-stu-id="46591-138">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="46591-139">新-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="46591-139">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="46591-140">移除-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46591-140">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="46591-141">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="46591-141">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


