---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967952"
---
# <span data-ttu-id="6133c-101">Get-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="6133c-101">Get-AzureWebsiteLog</span></span>

## <span data-ttu-id="6133c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6133c-102">SYNOPSIS</span></span>
<span data-ttu-id="6133c-103">取得指定網站的記錄。</span><span class="sxs-lookup"><span data-stu-id="6133c-103">Gets logs for the specified website.</span></span>

## <span data-ttu-id="6133c-104">句法</span><span class="sxs-lookup"><span data-stu-id="6133c-104">SYNTAX</span></span>

### <span data-ttu-id="6133c-105">側</span><span class="sxs-lookup"><span data-stu-id="6133c-105">Tail</span></span>
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6133c-106">ListPath</span><span class="sxs-lookup"><span data-stu-id="6133c-106">ListPath</span></span>
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6133c-107">說明</span><span class="sxs-lookup"><span data-stu-id="6133c-107">DESCRIPTION</span></span>
<span data-ttu-id="6133c-108">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6133c-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6133c-109">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="6133c-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6133c-110">取得指定網站的記錄。</span><span class="sxs-lookup"><span data-stu-id="6133c-110">Gets log for the specified website.</span></span>

## <span data-ttu-id="6133c-111">示例</span><span class="sxs-lookup"><span data-stu-id="6133c-111">EXAMPLES</span></span>

### <span data-ttu-id="6133c-112">範例1：開始記錄串流</span><span class="sxs-lookup"><span data-stu-id="6133c-112">Example 1: Start log streaming</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail
```

<span data-ttu-id="6133c-113">這個範例會啟動所有應用程式記錄的記錄傳送。</span><span class="sxs-lookup"><span data-stu-id="6133c-113">This example starts log streaming for all application logs.</span></span>

### <span data-ttu-id="6133c-114">範例2：開始記錄 HTTP 記錄的資料流程</span><span class="sxs-lookup"><span data-stu-id="6133c-114">Example 2: Start log streaming for http logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

<span data-ttu-id="6133c-115">這個範例會啟動 HTTP 記錄的記錄傳送。</span><span class="sxs-lookup"><span data-stu-id="6133c-115">This example starts log streaming for http logs.</span></span>

### <span data-ttu-id="6133c-116">範例3：開始記錄資料流程以尋找錯誤記錄</span><span class="sxs-lookup"><span data-stu-id="6133c-116">Example 3: Start log streaming for error logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

<span data-ttu-id="6133c-117">這個範例會開始記錄資料流程並只顯示錯誤記錄。</span><span class="sxs-lookup"><span data-stu-id="6133c-117">This example starts log streaming and show error logs only.</span></span>

### <span data-ttu-id="6133c-118">範例4：顯示 avaiable 記錄</span><span class="sxs-lookup"><span data-stu-id="6133c-118">Example 4: Display avaiable logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

<span data-ttu-id="6133c-119">這個範例會列出網站中所有可用的記錄路徑。</span><span class="sxs-lookup"><span data-stu-id="6133c-119">This example lists all available log paths in the website.</span></span>

## <span data-ttu-id="6133c-120">參數</span><span class="sxs-lookup"><span data-stu-id="6133c-120">PARAMETERS</span></span>

### <span data-ttu-id="6133c-121">-ListPath</span><span class="sxs-lookup"><span data-stu-id="6133c-121">-ListPath</span></span>
<span data-ttu-id="6133c-122">指出是否要列出記錄路徑。</span><span class="sxs-lookup"><span data-stu-id="6133c-122">Indicates whether to list the log paths.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6133c-123">-訊息</span><span class="sxs-lookup"><span data-stu-id="6133c-123">-Message</span></span>
<span data-ttu-id="6133c-124">指定將用來篩選記錄訊息的字串。</span><span class="sxs-lookup"><span data-stu-id="6133c-124">Specifies a string which will be used to filter the log message.</span></span>
<span data-ttu-id="6133c-125">只會檢索包含此字串的記錄。</span><span class="sxs-lookup"><span data-stu-id="6133c-125">Only logs which contains this string will be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6133c-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="6133c-126">-Name</span></span>
<span data-ttu-id="6133c-127">網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="6133c-127">The name of the website.</span></span>

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

### <span data-ttu-id="6133c-128">-Path</span><span class="sxs-lookup"><span data-stu-id="6133c-128">-Path</span></span>
<span data-ttu-id="6133c-129">要從哪個路徑檢索記錄。</span><span class="sxs-lookup"><span data-stu-id="6133c-129">The path from which the log will be retrieved.</span></span>
<span data-ttu-id="6133c-130">根據預設，它是 Root，也就是包含所有路徑。</span><span class="sxs-lookup"><span data-stu-id="6133c-130">By default it is Root, which means include all the paths.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6133c-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6133c-131">-Profile</span></span>
<span data-ttu-id="6133c-132">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6133c-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6133c-133">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6133c-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6133c-134">-槽</span><span class="sxs-lookup"><span data-stu-id="6133c-134">-Slot</span></span>
<span data-ttu-id="6133c-135">指定槽名稱。</span><span class="sxs-lookup"><span data-stu-id="6133c-135">Specifies the slot name.</span></span>

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

### <span data-ttu-id="6133c-136">-尾</span><span class="sxs-lookup"><span data-stu-id="6133c-136">-Tail</span></span>
<span data-ttu-id="6133c-137">指定是否要資料流記錄。</span><span class="sxs-lookup"><span data-stu-id="6133c-137">Specifies whether to stream the logs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6133c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6133c-138">CommonParameters</span></span>
<span data-ttu-id="6133c-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6133c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6133c-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6133c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6133c-141">輸入</span><span class="sxs-lookup"><span data-stu-id="6133c-141">INPUTS</span></span>

## <span data-ttu-id="6133c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="6133c-142">OUTPUTS</span></span>

## <span data-ttu-id="6133c-143">筆記</span><span class="sxs-lookup"><span data-stu-id="6133c-143">NOTES</span></span>

## <span data-ttu-id="6133c-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="6133c-144">RELATED LINKS</span></span>

[<span data-ttu-id="6133c-145">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6133c-145">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="6133c-146">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6133c-146">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="6133c-147">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6133c-147">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="6133c-148">開始-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6133c-148">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


