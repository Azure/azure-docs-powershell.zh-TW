---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 94D20309-5F72-4BE5-A150-2D6DD754286A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a9d793bb9bc8d96150b812474bed9f8997adbe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967550"
---
# <span data-ttu-id="bf24f-101">Remove-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="bf24f-101">Remove-AzureStaticVNetIP</span></span>

## <span data-ttu-id="bf24f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf24f-102">SYNOPSIS</span></span>
<span data-ttu-id="bf24f-103">從虛擬機器物件（如果有的話）中移除靜態虛擬網路 IP 位址資訊。</span><span class="sxs-lookup"><span data-stu-id="bf24f-103">Removes the static virtual network IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="bf24f-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf24f-104">SYNTAX</span></span>

```
Remove-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="bf24f-105">說明</span><span class="sxs-lookup"><span data-stu-id="bf24f-105">DESCRIPTION</span></span>
<span data-ttu-id="bf24f-106">**AzureStaticVNetIP** Cmdlet 會從虛擬電腦物件（如果有的話）中移除靜態虛擬網路 (VNET) IP 位址資訊。</span><span class="sxs-lookup"><span data-stu-id="bf24f-106">The **Remove-AzureStaticVNetIP** cmdlet removes the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="bf24f-107">示例</span><span class="sxs-lookup"><span data-stu-id="bf24f-107">EXAMPLES</span></span>

### <span data-ttu-id="bf24f-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="bf24f-108">1:</span></span>
```

```

## <span data-ttu-id="bf24f-109">參數</span><span class="sxs-lookup"><span data-stu-id="bf24f-109">PARAMETERS</span></span>

### <span data-ttu-id="bf24f-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bf24f-110">-InformationAction</span></span>
<span data-ttu-id="bf24f-111">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="bf24f-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="bf24f-112">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bf24f-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bf24f-113">持續</span><span class="sxs-lookup"><span data-stu-id="bf24f-113">Continue</span></span>
- <span data-ttu-id="bf24f-114">理會</span><span class="sxs-lookup"><span data-stu-id="bf24f-114">Ignore</span></span>
- <span data-ttu-id="bf24f-115">看</span><span class="sxs-lookup"><span data-stu-id="bf24f-115">Inquire</span></span>
- <span data-ttu-id="bf24f-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bf24f-116">SilentlyContinue</span></span>
- <span data-ttu-id="bf24f-117">停止</span><span class="sxs-lookup"><span data-stu-id="bf24f-117">Stop</span></span>
- <span data-ttu-id="bf24f-118">封存</span><span class="sxs-lookup"><span data-stu-id="bf24f-118">Suspend</span></span>

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

### <span data-ttu-id="bf24f-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bf24f-119">-InformationVariable</span></span>
<span data-ttu-id="bf24f-120">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="bf24f-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="bf24f-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="bf24f-121">-Profile</span></span>
<span data-ttu-id="bf24f-122">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bf24f-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bf24f-123">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="bf24f-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bf24f-124">-VM</span><span class="sxs-lookup"><span data-stu-id="bf24f-124">-VM</span></span>
<span data-ttu-id="bf24f-125">指定持久性虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="bf24f-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="bf24f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf24f-126">CommonParameters</span></span>
<span data-ttu-id="bf24f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf24f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf24f-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf24f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf24f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="bf24f-129">INPUTS</span></span>

## <span data-ttu-id="bf24f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="bf24f-130">OUTPUTS</span></span>

## <span data-ttu-id="bf24f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="bf24f-131">NOTES</span></span>

## <span data-ttu-id="bf24f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf24f-132">RELATED LINKS</span></span>

[<span data-ttu-id="bf24f-133">AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="bf24f-133">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="bf24f-134">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="bf24f-134">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


