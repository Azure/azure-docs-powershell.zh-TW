---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 8EF86C66-498F-4183-9070-F178628483F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91c32ca5207efdff7fa65fbba599f44d276dab6d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967776"
---
# <span data-ttu-id="5e229-101">Get-AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="5e229-101">Get-AzureRemoteAppCollectionUsageSummary</span></span>

## <span data-ttu-id="5e229-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5e229-102">SYNOPSIS</span></span>
<span data-ttu-id="5e229-103">檢索 Azure RemoteApp 集合的使用方式摘要。</span><span class="sxs-lookup"><span data-stu-id="5e229-103">Retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="5e229-104">句法</span><span class="sxs-lookup"><span data-stu-id="5e229-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageSummary [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5e229-105">說明</span><span class="sxs-lookup"><span data-stu-id="5e229-105">DESCRIPTION</span></span>
<span data-ttu-id="5e229-106">**AzureRemoteAppCollectionUsageSummary** Cmdlet 會檢索 Azure RemoteApp 集合的使用方式摘要。</span><span class="sxs-lookup"><span data-stu-id="5e229-106">The **Get-AzureRemoteAppCollectionUsageSummary** cmdlet retrieves a usage summary for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="5e229-107">示例</span><span class="sxs-lookup"><span data-stu-id="5e229-107">EXAMPLES</span></span>

### <span data-ttu-id="5e229-108">範例1：取得使用方式摘要</span><span class="sxs-lookup"><span data-stu-id="5e229-108">Example 1: Get a usage summary</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageSummary -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="5e229-109">這個命令會針對名為 Contoso 的集合，取得2014年12月的使用摘要。</span><span class="sxs-lookup"><span data-stu-id="5e229-109">This command gets a usage summary for the month of December in the year 2014, for a collection named Contoso.</span></span>

## <span data-ttu-id="5e229-110">參數</span><span class="sxs-lookup"><span data-stu-id="5e229-110">PARAMETERS</span></span>

### <span data-ttu-id="5e229-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="5e229-111">-CollectionName</span></span>
<span data-ttu-id="5e229-112">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e229-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e229-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5e229-113">-Profile</span></span>
<span data-ttu-id="5e229-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5e229-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e229-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5e229-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e229-116">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="5e229-116">-UsageMonth</span></span>
<span data-ttu-id="5e229-117">指定要取得使用方式摘要之月份的兩位數數位。</span><span class="sxs-lookup"><span data-stu-id="5e229-117">Specifies a two digit number for the month for which to get a usage summary.</span></span>
<span data-ttu-id="5e229-118">如果未指定此參數，此 Cmdlet 會提供目前月份的使用方式。</span><span class="sxs-lookup"><span data-stu-id="5e229-118">If this parameter is not specified, this cmdlet provides usage for the current month.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e229-119">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="5e229-119">-UsageYear</span></span>
<span data-ttu-id="5e229-120">指定要取得使用方式摘要的四位數年份。</span><span class="sxs-lookup"><span data-stu-id="5e229-120">Specifies the four-digit year for which to get a usage summary.</span></span>
<span data-ttu-id="5e229-121">如果未指定此參數，則會使用此 Cmdlet 提供目前年份的使用方式摘要。</span><span class="sxs-lookup"><span data-stu-id="5e229-121">If this parameter is not specified, this cmdlet provides a usage summary for the current year will be used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e229-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e229-122">CommonParameters</span></span>
<span data-ttu-id="5e229-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5e229-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e229-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5e229-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e229-125">輸入</span><span class="sxs-lookup"><span data-stu-id="5e229-125">INPUTS</span></span>

## <span data-ttu-id="5e229-126">輸出</span><span class="sxs-lookup"><span data-stu-id="5e229-126">OUTPUTS</span></span>

## <span data-ttu-id="5e229-127">筆記</span><span class="sxs-lookup"><span data-stu-id="5e229-127">NOTES</span></span>

## <span data-ttu-id="5e229-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e229-128">RELATED LINKS</span></span>

[<span data-ttu-id="5e229-129">AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="5e229-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="5e229-130">AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="5e229-130">Get-AzureRemoteAppCollectionUsageDetails</span></span>](./Get-AzureRemoteAppCollectionUsageDetails.md)


