---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3422EFD0-88DC-4DF0-868C-5C63C9FA95EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d9aa78f34abf17c2aa5858697f492f76ee124d91
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967136"
---
# <span data-ttu-id="c561b-101">Disable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c561b-101">Disable-AzureWebsiteApplicationDiagnostic</span></span>

## <span data-ttu-id="c561b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c561b-102">SYNOPSIS</span></span>
<span data-ttu-id="c561b-103">針對 Azure 網站停用應用程式診斷。</span><span class="sxs-lookup"><span data-stu-id="c561b-103">Disables application diagnostics for an Azure website.</span></span>

## <span data-ttu-id="c561b-104">句法</span><span class="sxs-lookup"><span data-stu-id="c561b-104">SYNTAX</span></span>

```
Disable-AzureWebsiteApplicationDiagnostic [-PassThru] [-File] [-TableStorage] [-BlobStorage] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c561b-105">說明</span><span class="sxs-lookup"><span data-stu-id="c561b-105">DESCRIPTION</span></span>
<span data-ttu-id="c561b-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c561b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="c561b-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="c561b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="c561b-108">針對 Azure 網站停用應用程式診斷。</span><span class="sxs-lookup"><span data-stu-id="c561b-108">Disables application diagnostics for an Azure website.</span></span>
<span data-ttu-id="c561b-109">停用已設定儲存在檔案系統或 Azure 上的記錄。</span><span class="sxs-lookup"><span data-stu-id="c561b-109">Disables logging configured to be stored on a file system or on Azure.</span></span>

## <span data-ttu-id="c561b-110">示例</span><span class="sxs-lookup"><span data-stu-id="c561b-110">EXAMPLES</span></span>

### <span data-ttu-id="c561b-111">範例1：停用應用程式記錄檔</span><span class="sxs-lookup"><span data-stu-id="c561b-111">Example 1:  Disable application logging file</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -File
```

<span data-ttu-id="c561b-112">下列範例會停用檔案系統上的應用程式記錄。</span><span class="sxs-lookup"><span data-stu-id="c561b-112">The following example disables application logging on the file system.</span></span>

### <span data-ttu-id="c561b-113">範例2：使用 Azure 儲存空間停用記錄</span><span class="sxs-lookup"><span data-stu-id="c561b-113">Example 2:  Disable logging using Azure storage</span></span>
```
PS C:\> Disable-AzureWebsiteApplicationDiagnostic -Name MyWebsite -Storage
```

<span data-ttu-id="c561b-114">下列範例會停用「儲存」的應用程式記錄。</span><span class="sxs-lookup"><span data-stu-id="c561b-114">The following example disables application logging using storage.</span></span>

## <span data-ttu-id="c561b-115">參數</span><span class="sxs-lookup"><span data-stu-id="c561b-115">PARAMETERS</span></span>

### <span data-ttu-id="c561b-116">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="c561b-116">-BlobStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c561b-117">檔案</span><span class="sxs-lookup"><span data-stu-id="c561b-117">-File</span></span>
<span data-ttu-id="c561b-118">指定您要使用檔案系統來儲存記錄檔。</span><span class="sxs-lookup"><span data-stu-id="c561b-118">Specifies that you want to use the file system to store the log files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c561b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c561b-119">-Name</span></span>
<span data-ttu-id="c561b-120">指定網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="c561b-120">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="c561b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c561b-121">-PassThru</span></span>
<span data-ttu-id="c561b-122">[標誌]，如果成功，則傳回 true。</span><span class="sxs-lookup"><span data-stu-id="c561b-122">Flag to return true if succeeded.</span></span>

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

### <span data-ttu-id="c561b-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c561b-123">-Profile</span></span>
<span data-ttu-id="c561b-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c561b-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c561b-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c561b-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c561b-126">-槽</span><span class="sxs-lookup"><span data-stu-id="c561b-126">-Slot</span></span>
<span data-ttu-id="c561b-127">指定槽的名稱。</span><span class="sxs-lookup"><span data-stu-id="c561b-127">Specifies the name of slot.</span></span>

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

### <span data-ttu-id="c561b-128">-TableStorage</span><span class="sxs-lookup"><span data-stu-id="c561b-128">-TableStorage</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c561b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c561b-129">CommonParameters</span></span>
<span data-ttu-id="c561b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c561b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c561b-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c561b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c561b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c561b-132">INPUTS</span></span>

## <span data-ttu-id="c561b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c561b-133">OUTPUTS</span></span>

## <span data-ttu-id="c561b-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c561b-134">NOTES</span></span>

## <span data-ttu-id="c561b-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="c561b-135">RELATED LINKS</span></span>

[<span data-ttu-id="c561b-136">Enable-AzureWebsiteApplicationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="c561b-136">Enable-AzureWebsiteApplicationDiagnostic</span></span>](./Enable-AzureWebsiteApplicationDiagnostic.md)

[<span data-ttu-id="c561b-137">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c561b-137">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="c561b-138">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c561b-138">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="c561b-139">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c561b-139">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="c561b-140">開始-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="c561b-140">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


