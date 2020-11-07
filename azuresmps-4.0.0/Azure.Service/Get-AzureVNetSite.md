---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967973"
---
# <span data-ttu-id="a83cb-101">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="a83cb-101">Get-AzureVNetSite</span></span>

## <span data-ttu-id="a83cb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a83cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a83cb-103">取得清單物件，其中包含有關 Azure 虛擬網路的資訊。</span><span class="sxs-lookup"><span data-stu-id="a83cb-103">Gets a list object with information about Azure virtual networks.</span></span>

## <span data-ttu-id="a83cb-104">句法</span><span class="sxs-lookup"><span data-stu-id="a83cb-104">SYNTAX</span></span>

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a83cb-105">說明</span><span class="sxs-lookup"><span data-stu-id="a83cb-105">DESCRIPTION</span></span>
<span data-ttu-id="a83cb-106">**AzureVNetSite** Cmdlet 會取得清單物件，其中包含目前訂閱之 Azure 虛擬網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a83cb-106">The **Get-AzureVNetSite** cmdlet gets a list object with information about Azure virtual networks for the current subscription.</span></span>
<span data-ttu-id="a83cb-107">如果您指定虛擬網路名稱，則只會傳回該虛擬網路的資訊。</span><span class="sxs-lookup"><span data-stu-id="a83cb-107">If you specify a virtual network name, only information for that virtual network is returned.</span></span>

## <span data-ttu-id="a83cb-108">示例</span><span class="sxs-lookup"><span data-stu-id="a83cb-108">EXAMPLES</span></span>

### <span data-ttu-id="a83cb-109">範例1：取得目前訂閱中所有虛擬網路的相關資訊</span><span class="sxs-lookup"><span data-stu-id="a83cb-109">Example 1: Get information about all virtual networks in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite
```

<span data-ttu-id="a83cb-110">這個命令會取得目前訂閱中所有虛擬網路的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a83cb-110">This command gets information about all the virtual networks in the current subscription.</span></span>

### <span data-ttu-id="a83cb-111">範例2：在目前的訂閱中取得特定虛擬網路的相關資訊</span><span class="sxs-lookup"><span data-stu-id="a83cb-111">Example 2: Get information about a specific virtual network in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

<span data-ttu-id="a83cb-112">這個命令只會檢索 MyProductionNetwork 虛擬網路上的資訊。</span><span class="sxs-lookup"><span data-stu-id="a83cb-112">This command retrieves information on the MyProductionNetwork virtual network only.</span></span>

## <span data-ttu-id="a83cb-113">參數</span><span class="sxs-lookup"><span data-stu-id="a83cb-113">PARAMETERS</span></span>

### <span data-ttu-id="a83cb-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a83cb-114">-InformationAction</span></span>
<span data-ttu-id="a83cb-115">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="a83cb-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a83cb-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a83cb-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a83cb-117">持續</span><span class="sxs-lookup"><span data-stu-id="a83cb-117">Continue</span></span>
- <span data-ttu-id="a83cb-118">理會</span><span class="sxs-lookup"><span data-stu-id="a83cb-118">Ignore</span></span>
- <span data-ttu-id="a83cb-119">看</span><span class="sxs-lookup"><span data-stu-id="a83cb-119">Inquire</span></span>
- <span data-ttu-id="a83cb-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a83cb-120">SilentlyContinue</span></span>
- <span data-ttu-id="a83cb-121">停止</span><span class="sxs-lookup"><span data-stu-id="a83cb-121">Stop</span></span>
- <span data-ttu-id="a83cb-122">封存</span><span class="sxs-lookup"><span data-stu-id="a83cb-122">Suspend</span></span>

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

### <span data-ttu-id="a83cb-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a83cb-123">-InformationVariable</span></span>
<span data-ttu-id="a83cb-124">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="a83cb-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a83cb-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a83cb-125">-Profile</span></span>
<span data-ttu-id="a83cb-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a83cb-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a83cb-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a83cb-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a83cb-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a83cb-128">-VNetName</span></span>
<span data-ttu-id="a83cb-129">指定要傳回相關資訊的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="a83cb-129">Specifies a virtual network name to return information about.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a83cb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a83cb-130">CommonParameters</span></span>
<span data-ttu-id="a83cb-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a83cb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a83cb-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a83cb-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a83cb-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a83cb-133">INPUTS</span></span>

## <span data-ttu-id="a83cb-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a83cb-134">OUTPUTS</span></span>

## <span data-ttu-id="a83cb-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a83cb-135">NOTES</span></span>

## <span data-ttu-id="a83cb-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a83cb-136">RELATED LINKS</span></span>

[<span data-ttu-id="a83cb-137">AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="a83cb-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="a83cb-138">移除-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="a83cb-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="a83cb-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="a83cb-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


