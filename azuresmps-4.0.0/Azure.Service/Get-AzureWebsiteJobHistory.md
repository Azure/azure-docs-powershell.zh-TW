---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A2CBF963-1FAE-41B0-964E-EFF52076AB32
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2c4bb84111b8ec22b1b529622e61ca476cf6081b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967953"
---
# <span data-ttu-id="816ae-101">Get-AzureWebsiteJobHistory</span><span class="sxs-lookup"><span data-stu-id="816ae-101">Get-AzureWebsiteJobHistory</span></span>

## <span data-ttu-id="816ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="816ae-102">SYNOPSIS</span></span>
<span data-ttu-id="816ae-103">取得 web 作業歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="816ae-103">Gets a web job history.</span></span>

## <span data-ttu-id="816ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="816ae-104">SYNTAX</span></span>

### <span data-ttu-id="816ae-105">HistoryParameterSetName</span><span class="sxs-lookup"><span data-stu-id="816ae-105">HistoryParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="816ae-106">RunIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="816ae-106">RunIdParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> -RunId <String> [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="816ae-107">LatestParameterSetName</span><span class="sxs-lookup"><span data-stu-id="816ae-107">LatestParameterSetName</span></span>
```
Get-AzureWebsiteJobHistory -JobName <String> [-Latest] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="816ae-108">說明</span><span class="sxs-lookup"><span data-stu-id="816ae-108">DESCRIPTION</span></span>
<span data-ttu-id="816ae-109">取得 web 作業歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="816ae-109">Gets a web job history.</span></span>

## <span data-ttu-id="816ae-110">示例</span><span class="sxs-lookup"><span data-stu-id="816ae-110">EXAMPLES</span></span>

### <span data-ttu-id="816ae-111">範例1：取得網頁作業的完整歷程記錄</span><span class="sxs-lookup"><span data-stu-id="816ae-111">Example 1: Get complete history for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="816ae-112">取得 MyWebJob 的完整歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="816ae-112">Gets complete history for MyWebJob.</span></span>

### <span data-ttu-id="816ae-113">範例2：取得網站工作的最新執行</span><span class="sxs-lookup"><span data-stu-id="816ae-113">Example 2: Get latest run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -Latest
```

<span data-ttu-id="816ae-114">取得 MyWebJob 的最新執行資訊。</span><span class="sxs-lookup"><span data-stu-id="816ae-114">Gets latest run info for MyWebJob.</span></span>

### <span data-ttu-id="816ae-115">範例3：取得網頁作業的特定執行</span><span class="sxs-lookup"><span data-stu-id="816ae-115">Example 3: Get specific run for a web job</span></span>
```
PS C:\> Get-AzureWebsiteJobHistory -Name MyWebsite -JobName MyWebJob -RunId 10
```

<span data-ttu-id="816ae-116">取得 MyWebJob 的 id 10 執行的所有相關資訊。</span><span class="sxs-lookup"><span data-stu-id="816ae-116">Gets all info about run with id 10 for MyWebJob.</span></span>

## <span data-ttu-id="816ae-117">參數</span><span class="sxs-lookup"><span data-stu-id="816ae-117">PARAMETERS</span></span>

### <span data-ttu-id="816ae-118">-JobName</span><span class="sxs-lookup"><span data-stu-id="816ae-118">-JobName</span></span>
<span data-ttu-id="816ae-119">Web 作業名稱。</span><span class="sxs-lookup"><span data-stu-id="816ae-119">The web job name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="816ae-120">-最新</span><span class="sxs-lookup"><span data-stu-id="816ae-120">-Latest</span></span>
<span data-ttu-id="816ae-121">如果已指定，則會傳回最新的執行歷程記錄。</span><span class="sxs-lookup"><span data-stu-id="816ae-121">If specified, return the latest run history.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LatestParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="816ae-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="816ae-122">-Name</span></span>
<span data-ttu-id="816ae-123">Azure 網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="816ae-123">The name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="816ae-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="816ae-124">-Profile</span></span>
<span data-ttu-id="816ae-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="816ae-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="816ae-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="816ae-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="816ae-127">-RunId</span><span class="sxs-lookup"><span data-stu-id="816ae-127">-RunId</span></span>
<span data-ttu-id="816ae-128">指定您想要查看的運行歷程記錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="816ae-128">Specifies the ID of the run history you want to see.</span></span>

```yaml
Type: String
Parameter Sets: RunIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="816ae-129">-槽</span><span class="sxs-lookup"><span data-stu-id="816ae-129">-Slot</span></span>
<span data-ttu-id="816ae-130">Azure 網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="816ae-130">The slot name of the Azure website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="816ae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="816ae-131">CommonParameters</span></span>
<span data-ttu-id="816ae-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="816ae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="816ae-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="816ae-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="816ae-134">輸入</span><span class="sxs-lookup"><span data-stu-id="816ae-134">INPUTS</span></span>

## <span data-ttu-id="816ae-135">輸出</span><span class="sxs-lookup"><span data-stu-id="816ae-135">OUTPUTS</span></span>

## <span data-ttu-id="816ae-136">筆記</span><span class="sxs-lookup"><span data-stu-id="816ae-136">NOTES</span></span>

## <span data-ttu-id="816ae-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="816ae-137">RELATED LINKS</span></span>

[<span data-ttu-id="816ae-138">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="816ae-138">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="816ae-139">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="816ae-139">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="816ae-140">AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="816ae-140">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="816ae-141">新-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="816ae-141">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="816ae-142">移除-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="816ae-142">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)


