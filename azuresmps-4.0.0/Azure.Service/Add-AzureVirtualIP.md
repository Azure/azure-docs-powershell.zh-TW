---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FBED8515-4216-4AB6-B34E-D14A6063A3A7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2f145ec51bc6744d877661554e3d8e475d722fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967159"
---
# <span data-ttu-id="16025-101">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="16025-101">Add-AzureVirtualIP</span></span>

## <span data-ttu-id="16025-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16025-102">SYNOPSIS</span></span>
<span data-ttu-id="16025-103">將虛擬 IP 新增至雲端服務。</span><span class="sxs-lookup"><span data-stu-id="16025-103">Adds a virtual IP to a cloud service.</span></span>

## <span data-ttu-id="16025-104">句法</span><span class="sxs-lookup"><span data-stu-id="16025-104">SYNTAX</span></span>

```
Add-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="16025-105">說明</span><span class="sxs-lookup"><span data-stu-id="16025-105">DESCRIPTION</span></span>
<span data-ttu-id="16025-106">**載入 AzureVirtualIP** Cmdlet 會將新的虛擬 IP (VIP) 新增至您的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="16025-106">The **Add-AzureVirtualIP** cmdlet adds a new virtual IP (VIP) to your Azure service.</span></span>
<span data-ttu-id="16025-107">新的虛擬 IP 有一個名稱，但未分配 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="16025-107">The new virtual IP has a name but is not allocated an IP address.</span></span>

<span data-ttu-id="16025-108">只有當您將端點與 VIP 建立關聯時，才會指派 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="16025-108">The IP address is allocated only when you associate an endpoint to the VIP.</span></span>
<span data-ttu-id="16025-109">如需詳細資訊，請參閱 Add-AzureEndpoint。</span><span class="sxs-lookup"><span data-stu-id="16025-109">See Add-AzureEndpoint for more details.</span></span>

<span data-ttu-id="16025-110">只有在您的訂閱與端點相關聯之後，才會收取額外的 Vip 費用。</span><span class="sxs-lookup"><span data-stu-id="16025-110">Your subscription is charged for extra VIPs only once they are associated with an endpoint.</span></span>

## <span data-ttu-id="16025-111">示例</span><span class="sxs-lookup"><span data-stu-id="16025-111">EXAMPLES</span></span>

### <span data-ttu-id="16025-112">範例1：新增虛擬 IP 至服務</span><span class="sxs-lookup"><span data-stu-id="16025-112">Example 1: Add a virtual IP to a service</span></span>
```
PS C:\> Add-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
OperationDescription OperationId                          OperationStatus
-------------------- -----------                          ---------------
Add-AzureVirtualIP   4bd7b638-d2e7-216f-ba38-5221233d70ce Succeeded
```

<span data-ttu-id="16025-113">這個命令會將虛擬 IP 位址新增至服務。</span><span class="sxs-lookup"><span data-stu-id="16025-113">This command adds a virtual IP address to a service.</span></span>

## <span data-ttu-id="16025-114">參數</span><span class="sxs-lookup"><span data-stu-id="16025-114">PARAMETERS</span></span>

### <span data-ttu-id="16025-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="16025-115">-InformationAction</span></span>
<span data-ttu-id="16025-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="16025-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="16025-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="16025-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="16025-118">持續</span><span class="sxs-lookup"><span data-stu-id="16025-118">Continue</span></span>
- <span data-ttu-id="16025-119">理會</span><span class="sxs-lookup"><span data-stu-id="16025-119">Ignore</span></span>
- <span data-ttu-id="16025-120">看</span><span class="sxs-lookup"><span data-stu-id="16025-120">Inquire</span></span>
- <span data-ttu-id="16025-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="16025-121">SilentlyContinue</span></span>
- <span data-ttu-id="16025-122">停止</span><span class="sxs-lookup"><span data-stu-id="16025-122">Stop</span></span>
- <span data-ttu-id="16025-123">封存</span><span class="sxs-lookup"><span data-stu-id="16025-123">Suspend</span></span>

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

### <span data-ttu-id="16025-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="16025-124">-InformationVariable</span></span>
<span data-ttu-id="16025-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="16025-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="16025-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="16025-126">-Profile</span></span>
<span data-ttu-id="16025-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="16025-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="16025-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="16025-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="16025-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="16025-129">-ServiceName</span></span>
<span data-ttu-id="16025-130">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="16025-130">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16025-131">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="16025-131">-VirtualIPName</span></span>
<span data-ttu-id="16025-132">指定虛擬 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="16025-132">Specifies the name of the virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16025-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16025-133">CommonParameters</span></span>
<span data-ttu-id="16025-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16025-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16025-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16025-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16025-136">輸入</span><span class="sxs-lookup"><span data-stu-id="16025-136">INPUTS</span></span>

## <span data-ttu-id="16025-137">輸出</span><span class="sxs-lookup"><span data-stu-id="16025-137">OUTPUTS</span></span>

### <span data-ttu-id="16025-138">WindowsAzure. 常見. ManagementOperationCoNtext</span><span class="sxs-lookup"><span data-stu-id="16025-138">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="16025-139">筆記</span><span class="sxs-lookup"><span data-stu-id="16025-139">NOTES</span></span>

## <span data-ttu-id="16025-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="16025-140">RELATED LINKS</span></span>

[<span data-ttu-id="16025-141">附加 AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="16025-141">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="16025-142">移除-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="16025-142">Remove-AzureVirtualIP</span></span>](./Remove-AzureVirtualIP.md)


