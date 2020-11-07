---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967921"
---
# <span data-ttu-id="38743-101">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38743-101">Remove-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="38743-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38743-102">SYNOPSIS</span></span>
<span data-ttu-id="38743-103">移除內部負載平衡器設定。</span><span class="sxs-lookup"><span data-stu-id="38743-103">Removes an internal load balancer configuration.</span></span>

## <span data-ttu-id="38743-104">句法</span><span class="sxs-lookup"><span data-stu-id="38743-104">SYNTAX</span></span>

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="38743-105">說明</span><span class="sxs-lookup"><span data-stu-id="38743-105">DESCRIPTION</span></span>
<span data-ttu-id="38743-106">**AzureInternalLoadBalancer** Cmdlet 會從 Azure 服務中移除內部負載平衡器設定。</span><span class="sxs-lookup"><span data-stu-id="38743-106">The **Remove-AzureInternalLoadBalancer** cmdlet removes the internal load balancer configuration from an Azure service.</span></span>
<span data-ttu-id="38743-107">如果有任何端點目前參照內部負載平衡器，此 Cmdlet 將無法移除該設定。</span><span class="sxs-lookup"><span data-stu-id="38743-107">If any endpoint currently refers to the internal load balancer, this cmdlet cannot remove the configuration.</span></span>

## <span data-ttu-id="38743-108">示例</span><span class="sxs-lookup"><span data-stu-id="38743-108">EXAMPLES</span></span>

### <span data-ttu-id="38743-109">範例1：移除內部負載平衡器設定</span><span class="sxs-lookup"><span data-stu-id="38743-109">Example 1: Remove an internal load balancer configuration</span></span>
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

<span data-ttu-id="38743-110">這個命令會移除名為 ContosoService 的服務的內部負載平衡器設定。</span><span class="sxs-lookup"><span data-stu-id="38743-110">This command removes the internal load balancer configuration for the service named ContosoService.</span></span>

## <span data-ttu-id="38743-111">參數</span><span class="sxs-lookup"><span data-stu-id="38743-111">PARAMETERS</span></span>

### <span data-ttu-id="38743-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="38743-112">-InformationAction</span></span>
<span data-ttu-id="38743-113">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="38743-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="38743-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="38743-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="38743-115">持續</span><span class="sxs-lookup"><span data-stu-id="38743-115">Continue</span></span>
- <span data-ttu-id="38743-116">理會</span><span class="sxs-lookup"><span data-stu-id="38743-116">Ignore</span></span>
- <span data-ttu-id="38743-117">看</span><span class="sxs-lookup"><span data-stu-id="38743-117">Inquire</span></span>
- <span data-ttu-id="38743-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="38743-118">SilentlyContinue</span></span>
- <span data-ttu-id="38743-119">停止</span><span class="sxs-lookup"><span data-stu-id="38743-119">Stop</span></span>
- <span data-ttu-id="38743-120">封存</span><span class="sxs-lookup"><span data-stu-id="38743-120">Suspend</span></span>

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

### <span data-ttu-id="38743-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="38743-121">-InformationVariable</span></span>
<span data-ttu-id="38743-122">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="38743-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="38743-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="38743-123">-Profile</span></span>
<span data-ttu-id="38743-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="38743-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="38743-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="38743-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="38743-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="38743-126">-ServiceName</span></span>
<span data-ttu-id="38743-127">指定此 Cmdlet 移除內部負載平衡器的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="38743-127">Specifies the name of the service from which this cmdlet removes an internal load balancer.</span></span>

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

### <span data-ttu-id="38743-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38743-128">CommonParameters</span></span>
<span data-ttu-id="38743-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38743-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38743-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38743-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38743-131">輸入</span><span class="sxs-lookup"><span data-stu-id="38743-131">INPUTS</span></span>

## <span data-ttu-id="38743-132">輸出</span><span class="sxs-lookup"><span data-stu-id="38743-132">OUTPUTS</span></span>

### <span data-ttu-id="38743-133">WindowsAzure. 常見. ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="38743-133">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="38743-134">筆記</span><span class="sxs-lookup"><span data-stu-id="38743-134">NOTES</span></span>

## <span data-ttu-id="38743-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="38743-135">RELATED LINKS</span></span>

[<span data-ttu-id="38743-136">附加 AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38743-136">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="38743-137">AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38743-137">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="38743-138">新-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="38743-138">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="38743-139">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="38743-139">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


