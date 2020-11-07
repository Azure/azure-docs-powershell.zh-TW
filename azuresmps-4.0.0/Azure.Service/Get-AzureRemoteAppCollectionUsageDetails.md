---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 0E5F05B3-F2B0-479C-8222-927C34140416
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74892352afe02ae5eb2f19e05704c23c489d2d75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967078"
---
# <span data-ttu-id="57b1c-101">Get-AzureRemoteAppCollectionUsageDetails</span><span class="sxs-lookup"><span data-stu-id="57b1c-101">Get-AzureRemoteAppCollectionUsageDetails</span></span>

## <span data-ttu-id="57b1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="57b1c-103">檢索 Azure RemoteApp 集合的使用狀況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="57b1c-103">Retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="57b1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="57b1c-104">SYNTAX</span></span>

```
Get-AzureRemoteAppCollectionUsageDetails [-CollectionName] <String> [[-UsageMonth] <String>]
 [[-UsageYear] <String>] [-AsJob] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="57b1c-105">說明</span><span class="sxs-lookup"><span data-stu-id="57b1c-105">DESCRIPTION</span></span>
<span data-ttu-id="57b1c-106">**AzureRemoteAppCollectionUsageDetails** Cmdlet 會檢索 Azure RemoteApp 集合的使用狀況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="57b1c-106">The **Get-AzureRemoteAppCollectionUsageDetails** cmdlet retrieves usage details for an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="57b1c-107">示例</span><span class="sxs-lookup"><span data-stu-id="57b1c-107">EXAMPLES</span></span>

### <span data-ttu-id="57b1c-108">範例1：取得集合的使用詳細資料</span><span class="sxs-lookup"><span data-stu-id="57b1c-108">Example 1: Get usage details for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppCollectionUsageDetails -CollectionName Contoso -UsageMonth 12 -UsageYear 2014
```

<span data-ttu-id="57b1c-109">這個命令會針對名為 Contoso 的 Azure RemoteApp 集合，取得2014年12月的使用詳細資料。</span><span class="sxs-lookup"><span data-stu-id="57b1c-109">This command gets usage details for the month of December in the year 2014, for an Azure RemoteApp collection named Contoso.</span></span>

## <span data-ttu-id="57b1c-110">參數</span><span class="sxs-lookup"><span data-stu-id="57b1c-110">PARAMETERS</span></span>

### <span data-ttu-id="57b1c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57b1c-111">-AsJob</span></span>
<span data-ttu-id="57b1c-112">表示 Cmdlet 在背景中作為 Windows PowerShell 作業執行。</span><span class="sxs-lookup"><span data-stu-id="57b1c-112">Indicates that the cmdlet runs in the background as a Windows PowerShell job.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57b1c-113">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="57b1c-113">-CollectionName</span></span>
<span data-ttu-id="57b1c-114">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="57b1c-114">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="57b1c-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="57b1c-115">-Profile</span></span>
<span data-ttu-id="57b1c-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="57b1c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="57b1c-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="57b1c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="57b1c-118">-UsageMonth</span><span class="sxs-lookup"><span data-stu-id="57b1c-118">-UsageMonth</span></span>
<span data-ttu-id="57b1c-119">指定要取得使用詳細資料之月份的兩位數數位。</span><span class="sxs-lookup"><span data-stu-id="57b1c-119">Specifies a two-digit number for the month for which to get usage details.</span></span>

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

### <span data-ttu-id="57b1c-120">-UsageYear</span><span class="sxs-lookup"><span data-stu-id="57b1c-120">-UsageYear</span></span>
<span data-ttu-id="57b1c-121">指定要取得使用狀況詳細資料的四位數年份。</span><span class="sxs-lookup"><span data-stu-id="57b1c-121">Specifies the four-digit year for which to get usage details.</span></span>

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

### <span data-ttu-id="57b1c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b1c-122">CommonParameters</span></span>
<span data-ttu-id="57b1c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57b1c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b1c-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="57b1c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b1c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="57b1c-125">INPUTS</span></span>

## <span data-ttu-id="57b1c-126">輸出</span><span class="sxs-lookup"><span data-stu-id="57b1c-126">OUTPUTS</span></span>

## <span data-ttu-id="57b1c-127">筆記</span><span class="sxs-lookup"><span data-stu-id="57b1c-127">NOTES</span></span>

## <span data-ttu-id="57b1c-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="57b1c-128">RELATED LINKS</span></span>

[<span data-ttu-id="57b1c-129">AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="57b1c-129">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="57b1c-130">AzureRemoteAppCollectionUsageSummary</span><span class="sxs-lookup"><span data-stu-id="57b1c-130">Get-AzureRemoteAppCollectionUsageSummary</span></span>](./Get-AzureRemoteAppCollectionUsageSummary.md)


