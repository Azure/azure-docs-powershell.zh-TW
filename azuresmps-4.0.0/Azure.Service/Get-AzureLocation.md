---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CCA6334F-A193-4506-B873-76F29980C68D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25749aca2d0fb2682404d6c4d006c8ad1b1f3c6b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967782"
---
# <span data-ttu-id="8a920-101">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="8a920-101">Get-AzureLocation</span></span>

## <span data-ttu-id="8a920-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a920-102">SYNOPSIS</span></span>
<span data-ttu-id="8a920-103">取得目前 Azure 訂閱的可用資料中心位置。</span><span class="sxs-lookup"><span data-stu-id="8a920-103">Gets the available data center locations for the current Azure subscription.</span></span>

## <span data-ttu-id="8a920-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a920-104">SYNTAX</span></span>

```
Get-AzureLocation [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8a920-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a920-105">DESCRIPTION</span></span>
<span data-ttu-id="8a920-106">**AzureLocation** Cmdlet 會取得目前 azure 訂閱的可用 Azure 資料中心及其屬性清單。</span><span class="sxs-lookup"><span data-stu-id="8a920-106">The **Get-AzureLocation** cmdlet gets a list of the available Azure data centers and their properties for the current Azure subscription.</span></span>
<span data-ttu-id="8a920-107">在執行此 Cmdlet 之前，您必須使用 Select-AzureSubscription 和 Set-AzureSubscription Cmdlet 來設定您目前的訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a920-107">Before you run this cmdlet, you must set your current subscription by using the Select-AzureSubscription and Set-AzureSubscription cmdlets.</span></span>

## <span data-ttu-id="8a920-108">示例</span><span class="sxs-lookup"><span data-stu-id="8a920-108">EXAMPLES</span></span>

### <span data-ttu-id="8a920-109">範例1：取得位置</span><span class="sxs-lookup"><span data-stu-id="8a920-109">Example 1: Get locations</span></span>
```
PS C:\> Get-AzureLocation
```

<span data-ttu-id="8a920-110">這個命令會取得目前訂閱的可用資料中心及其屬性的清單。</span><span class="sxs-lookup"><span data-stu-id="8a920-110">This command gets a list of available data centers, and their properties, for the current subscription.</span></span>

## <span data-ttu-id="8a920-111">參數</span><span class="sxs-lookup"><span data-stu-id="8a920-111">PARAMETERS</span></span>

### <span data-ttu-id="8a920-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8a920-112">-InformationAction</span></span>
<span data-ttu-id="8a920-113">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8a920-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8a920-114">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8a920-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8a920-115">持續</span><span class="sxs-lookup"><span data-stu-id="8a920-115">Continue</span></span>
- <span data-ttu-id="8a920-116">理會</span><span class="sxs-lookup"><span data-stu-id="8a920-116">Ignore</span></span>
- <span data-ttu-id="8a920-117">看</span><span class="sxs-lookup"><span data-stu-id="8a920-117">Inquire</span></span>
- <span data-ttu-id="8a920-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8a920-118">SilentlyContinue</span></span>
- <span data-ttu-id="8a920-119">停止</span><span class="sxs-lookup"><span data-stu-id="8a920-119">Stop</span></span>
- <span data-ttu-id="8a920-120">封存</span><span class="sxs-lookup"><span data-stu-id="8a920-120">Suspend</span></span>

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

### <span data-ttu-id="8a920-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8a920-121">-InformationVariable</span></span>
<span data-ttu-id="8a920-122">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8a920-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8a920-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8a920-123">-Profile</span></span>
<span data-ttu-id="8a920-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8a920-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8a920-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8a920-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8a920-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a920-126">CommonParameters</span></span>
<span data-ttu-id="8a920-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a920-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a920-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8a920-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a920-129">輸入</span><span class="sxs-lookup"><span data-stu-id="8a920-129">INPUTS</span></span>

## <span data-ttu-id="8a920-130">輸出</span><span class="sxs-lookup"><span data-stu-id="8a920-130">OUTPUTS</span></span>

## <span data-ttu-id="8a920-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8a920-131">NOTES</span></span>

## <span data-ttu-id="8a920-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a920-132">RELATED LINKS</span></span>

