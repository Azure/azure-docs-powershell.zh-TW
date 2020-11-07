---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E059EF1-740C-4AEB-AF41-BF6003BE15F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: a52f2585771ec10d6acf52b14c88bd1ed0af0427
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967382"
---
# <span data-ttu-id="9677e-101">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="9677e-101">Test-AzureStaticVNetIP</span></span>

## <span data-ttu-id="9677e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9677e-102">SYNOPSIS</span></span>
<span data-ttu-id="9677e-103">測試靜態虛擬網路 IP 位址的可用性，並在查詢的位址無法使用時取得建議清單。</span><span class="sxs-lookup"><span data-stu-id="9677e-103">Tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="9677e-104">句法</span><span class="sxs-lookup"><span data-stu-id="9677e-104">SYNTAX</span></span>

```
Test-AzureStaticVNetIP [-VNetName] <String> [-IPAddress] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9677e-105">說明</span><span class="sxs-lookup"><span data-stu-id="9677e-105">DESCRIPTION</span></span>
<span data-ttu-id="9677e-106">**AzureStaticVNetIP** Cmdlet 會測試靜態虛擬網路 IP 位址的可用性，以及如果查詢的位址無法使用，則會取得建議清單。</span><span class="sxs-lookup"><span data-stu-id="9677e-106">The **Test-AzureStaticVNetIP** cmdlet tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="9677e-107">示例</span><span class="sxs-lookup"><span data-stu-id="9677e-107">EXAMPLES</span></span>

### <span data-ttu-id="9677e-108">sr-1</span><span class="sxs-lookup"><span data-stu-id="9677e-108">1:</span></span>
```

```

## <span data-ttu-id="9677e-109">參數</span><span class="sxs-lookup"><span data-stu-id="9677e-109">PARAMETERS</span></span>

### <span data-ttu-id="9677e-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9677e-110">-InformationAction</span></span>
<span data-ttu-id="9677e-111">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="9677e-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9677e-112">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="9677e-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9677e-113">持續</span><span class="sxs-lookup"><span data-stu-id="9677e-113">Continue</span></span>
- <span data-ttu-id="9677e-114">理會</span><span class="sxs-lookup"><span data-stu-id="9677e-114">Ignore</span></span>
- <span data-ttu-id="9677e-115">看</span><span class="sxs-lookup"><span data-stu-id="9677e-115">Inquire</span></span>
- <span data-ttu-id="9677e-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9677e-116">SilentlyContinue</span></span>
- <span data-ttu-id="9677e-117">停止</span><span class="sxs-lookup"><span data-stu-id="9677e-117">Stop</span></span>
- <span data-ttu-id="9677e-118">封存</span><span class="sxs-lookup"><span data-stu-id="9677e-118">Suspend</span></span>

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

### <span data-ttu-id="9677e-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9677e-119">-InformationVariable</span></span>
<span data-ttu-id="9677e-120">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="9677e-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9677e-121">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="9677e-121">-IPAddress</span></span>
<span data-ttu-id="9677e-122">指定要查詢的靜態虛擬網路 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9677e-122">Specifies the static virtual network IP address to query.</span></span>

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

### <span data-ttu-id="9677e-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9677e-123">-Profile</span></span>
<span data-ttu-id="9677e-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9677e-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9677e-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9677e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9677e-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="9677e-126">-VNetName</span></span>
<span data-ttu-id="9677e-127">指定虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="9677e-127">Specifies the Name of the virtual network.</span></span>

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

### <span data-ttu-id="9677e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9677e-128">CommonParameters</span></span>
<span data-ttu-id="9677e-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9677e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9677e-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9677e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9677e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="9677e-131">INPUTS</span></span>

## <span data-ttu-id="9677e-132">輸出</span><span class="sxs-lookup"><span data-stu-id="9677e-132">OUTPUTS</span></span>

## <span data-ttu-id="9677e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9677e-133">NOTES</span></span>

## <span data-ttu-id="9677e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9677e-134">RELATED LINKS</span></span>

[<span data-ttu-id="9677e-135">AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="9677e-135">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="9677e-136">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="9677e-136">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


