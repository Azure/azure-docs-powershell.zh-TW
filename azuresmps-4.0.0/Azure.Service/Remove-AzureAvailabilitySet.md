---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F956CC89-A2CA-4D73-8014-C36778C51927
online version: ''
schema: 2.0.0
ms.openlocfilehash: eba992b183795d016108419834c38bcf64a82d41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967614"
---
# <span data-ttu-id="83fa6-101">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="83fa6-101">Remove-AzureAvailabilitySet</span></span>

## <span data-ttu-id="83fa6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83fa6-102">SYNOPSIS</span></span>
<span data-ttu-id="83fa6-103">從 Azure 虛擬機器移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="83fa6-103">Removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="83fa6-104">句法</span><span class="sxs-lookup"><span data-stu-id="83fa6-104">SYNTAX</span></span>

```
Remove-AzureAvailabilitySet -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="83fa6-105">說明</span><span class="sxs-lookup"><span data-stu-id="83fa6-105">DESCRIPTION</span></span>
<span data-ttu-id="83fa6-106">**AzureAvailabilitySet** Cmdlet 會從 Azure 虛擬機器中移除可用性集。</span><span class="sxs-lookup"><span data-stu-id="83fa6-106">The **Remove-AzureAvailabilitySet** cmdlet removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="83fa6-107">示例</span><span class="sxs-lookup"><span data-stu-id="83fa6-107">EXAMPLES</span></span>

### <span data-ttu-id="83fa6-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="83fa6-108">1:</span></span>
```

```

## <span data-ttu-id="83fa6-109">參數</span><span class="sxs-lookup"><span data-stu-id="83fa6-109">PARAMETERS</span></span>

### <span data-ttu-id="83fa6-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="83fa6-110">-InformationAction</span></span>
<span data-ttu-id="83fa6-111">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="83fa6-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="83fa6-112">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="83fa6-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="83fa6-113">持續</span><span class="sxs-lookup"><span data-stu-id="83fa6-113">Continue</span></span>
- <span data-ttu-id="83fa6-114">理會</span><span class="sxs-lookup"><span data-stu-id="83fa6-114">Ignore</span></span>
- <span data-ttu-id="83fa6-115">看</span><span class="sxs-lookup"><span data-stu-id="83fa6-115">Inquire</span></span>
- <span data-ttu-id="83fa6-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="83fa6-116">SilentlyContinue</span></span>
- <span data-ttu-id="83fa6-117">停止</span><span class="sxs-lookup"><span data-stu-id="83fa6-117">Stop</span></span>
- <span data-ttu-id="83fa6-118">封存</span><span class="sxs-lookup"><span data-stu-id="83fa6-118">Suspend</span></span>

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

### <span data-ttu-id="83fa6-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="83fa6-119">-InformationVariable</span></span>
<span data-ttu-id="83fa6-120">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="83fa6-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="83fa6-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="83fa6-121">-Profile</span></span>
<span data-ttu-id="83fa6-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="83fa6-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="83fa6-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="83fa6-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="83fa6-124">-VM</span><span class="sxs-lookup"><span data-stu-id="83fa6-124">-VM</span></span>
<span data-ttu-id="83fa6-125">指定此 Cmdlet 移除可用性集的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="83fa6-125">Specifies the virtual machine from which this cmdlet removes an availability set.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83fa6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fa6-126">CommonParameters</span></span>
<span data-ttu-id="83fa6-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83fa6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fa6-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="83fa6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fa6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="83fa6-129">INPUTS</span></span>

## <span data-ttu-id="83fa6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="83fa6-130">OUTPUTS</span></span>

## <span data-ttu-id="83fa6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="83fa6-131">NOTES</span></span>

## <span data-ttu-id="83fa6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="83fa6-132">RELATED LINKS</span></span>

[<span data-ttu-id="83fa6-133">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="83fa6-133">Set-AzureAvailabilitySet</span></span>](./Set-AzureAvailabilitySet.md)


