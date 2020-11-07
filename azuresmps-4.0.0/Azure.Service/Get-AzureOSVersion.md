---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967083"
---
# <span data-ttu-id="ac7ca-101">Get-AzureOSVersion</span><span class="sxs-lookup"><span data-stu-id="ac7ca-101">Get-AzureOSVersion</span></span>

## <span data-ttu-id="ac7ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ac7ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ac7ca-103">列出所有的 Azure 客體作業系統。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-103">Lists all Azure guest operating systems.</span></span>

## <span data-ttu-id="ac7ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="ac7ca-104">SYNTAX</span></span>

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ac7ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="ac7ca-105">DESCRIPTION</span></span>
<span data-ttu-id="ac7ca-106">**AzureOSVersion** Cmdlet 會列出所有可用的 Azure 客體作業系統。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-106">The **Get-AzureOSVersion** cmdlet lists all the available Azure guest operating systems.</span></span>

## <span data-ttu-id="ac7ca-107">示例</span><span class="sxs-lookup"><span data-stu-id="ac7ca-107">EXAMPLES</span></span>

### <span data-ttu-id="ac7ca-108">範例1：取得所有可用的作業系統</span><span class="sxs-lookup"><span data-stu-id="ac7ca-108">Example 1: Get all available operating systems</span></span>
```
PS C:\> Get-AzureOSVersion
```

<span data-ttu-id="ac7ca-109">這個命令會檢索一個物件，其中包含目前訂閱中可用之所有客體作業系統版本的清單。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-109">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>

### <span data-ttu-id="ac7ca-110">範例2：在表格中顯示作業系統資訊</span><span class="sxs-lookup"><span data-stu-id="ac7ca-110">Example 2: Display operating system information in a table</span></span>
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

<span data-ttu-id="ac7ca-111">這個命令會檢索一個物件，其中包含目前訂閱中可用之所有客體作業系統版本的清單。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-111">This command retrieves an object that contains a list of all versions of guest operating systems that are available in the current subscription.</span></span>
<span data-ttu-id="ac7ca-112">命令會使用管線運算子將它們傳遞到 **Format 資料表** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-112">The command passes them to the **Format-Table** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ac7ca-113">這個 Cmdlet 會將它們的格式設為表格，顯示作業系統系列、作業系統系列標籤及版本。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-113">That cmdlet formats them as a table that shows the operating system family, operating system family label, and version.</span></span>

## <span data-ttu-id="ac7ca-114">參數</span><span class="sxs-lookup"><span data-stu-id="ac7ca-114">PARAMETERS</span></span>

### <span data-ttu-id="ac7ca-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ac7ca-115">-InformationAction</span></span>
<span data-ttu-id="ac7ca-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ac7ca-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ac7ca-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ac7ca-118">持續</span><span class="sxs-lookup"><span data-stu-id="ac7ca-118">Continue</span></span>
- <span data-ttu-id="ac7ca-119">理會</span><span class="sxs-lookup"><span data-stu-id="ac7ca-119">Ignore</span></span>
- <span data-ttu-id="ac7ca-120">看</span><span class="sxs-lookup"><span data-stu-id="ac7ca-120">Inquire</span></span>
- <span data-ttu-id="ac7ca-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ac7ca-121">SilentlyContinue</span></span>
- <span data-ttu-id="ac7ca-122">停止</span><span class="sxs-lookup"><span data-stu-id="ac7ca-122">Stop</span></span>
- <span data-ttu-id="ac7ca-123">封存</span><span class="sxs-lookup"><span data-stu-id="ac7ca-123">Suspend</span></span>

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

### <span data-ttu-id="ac7ca-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ac7ca-124">-InformationVariable</span></span>
<span data-ttu-id="ac7ca-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ac7ca-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ac7ca-126">-Profile</span></span>
<span data-ttu-id="ac7ca-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ac7ca-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ac7ca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac7ca-129">CommonParameters</span></span>
<span data-ttu-id="ac7ca-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac7ca-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ac7ca-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac7ca-132">輸入</span><span class="sxs-lookup"><span data-stu-id="ac7ca-132">INPUTS</span></span>

## <span data-ttu-id="ac7ca-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ac7ca-133">OUTPUTS</span></span>

## <span data-ttu-id="ac7ca-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ac7ca-134">NOTES</span></span>

## <span data-ttu-id="ac7ca-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac7ca-135">RELATED LINKS</span></span>

[<span data-ttu-id="ac7ca-136">AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="ac7ca-136">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)


