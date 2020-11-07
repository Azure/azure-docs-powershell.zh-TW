---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4696BB05-F507-4FFB-8D96-6BAA2EBB0F0A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03acdfb16c7f1e7e8ee5e6b95902ef1ed056412a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966904"
---
# <span data-ttu-id="db18e-101">Save-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="db18e-101">Save-AzureWebsiteLog</span></span>

## <span data-ttu-id="db18e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db18e-102">SYNOPSIS</span></span>
<span data-ttu-id="db18e-103">下載並儲存指定網站的記錄。</span><span class="sxs-lookup"><span data-stu-id="db18e-103">Downloads and saves the logs for a specified website.</span></span>

## <span data-ttu-id="db18e-104">句法</span><span class="sxs-lookup"><span data-stu-id="db18e-104">SYNTAX</span></span>

```
Save-AzureWebsiteLog [-Output <String>] [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="db18e-105">說明</span><span class="sxs-lookup"><span data-stu-id="db18e-105">DESCRIPTION</span></span>
<span data-ttu-id="db18e-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db18e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="db18e-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="db18e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="db18e-108">**AzureWebsiteLog** Cmdlet 會下載指定網站的記錄。</span><span class="sxs-lookup"><span data-stu-id="db18e-108">The **Save-AzureWebsiteLog** cmdlet downloads the logs for a specified website.</span></span>

## <span data-ttu-id="db18e-109">示例</span><span class="sxs-lookup"><span data-stu-id="db18e-109">EXAMPLES</span></span>

### <span data-ttu-id="db18e-110">範例1：下載並儲存網站的記錄</span><span class="sxs-lookup"><span data-stu-id="db18e-110">Example 1: Download and save logs for a website</span></span>
```
PS C:\> Save-AzureWebsiteLogs -Name mySite -Output .\logs.zip
```

<span data-ttu-id="db18e-111">這個範例會將網站網站的執行時間和部署記錄下載至目前目錄中 logs.zip 的檔案。</span><span class="sxs-lookup"><span data-stu-id="db18e-111">This example downloads the runtime and deployment logs for website mySite to the file logs.zip in the current directory.</span></span>

## <span data-ttu-id="db18e-112">參數</span><span class="sxs-lookup"><span data-stu-id="db18e-112">PARAMETERS</span></span>

### <span data-ttu-id="db18e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="db18e-113">-Name</span></span>
<span data-ttu-id="db18e-114">指定網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="db18e-114">Specifies the name of the website.</span></span>

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

### <span data-ttu-id="db18e-115">-輸出</span><span class="sxs-lookup"><span data-stu-id="db18e-115">-Output</span></span>
<span data-ttu-id="db18e-116">指定儲存已下載檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="db18e-116">Specifies the path to store the downloaded file.</span></span>

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

### <span data-ttu-id="db18e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db18e-117">-PassThru</span></span>
<span data-ttu-id="db18e-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="db18e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="db18e-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="db18e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="db18e-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="db18e-120">-Profile</span></span>
<span data-ttu-id="db18e-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="db18e-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db18e-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="db18e-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db18e-123">-槽</span><span class="sxs-lookup"><span data-stu-id="db18e-123">-Slot</span></span>
<span data-ttu-id="db18e-124">指定槽名稱。</span><span class="sxs-lookup"><span data-stu-id="db18e-124">Specifies the slot name.</span></span>

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

### <span data-ttu-id="db18e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db18e-125">CommonParameters</span></span>
<span data-ttu-id="db18e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db18e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db18e-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db18e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db18e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="db18e-128">INPUTS</span></span>

## <span data-ttu-id="db18e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="db18e-129">OUTPUTS</span></span>

## <span data-ttu-id="db18e-130">筆記</span><span class="sxs-lookup"><span data-stu-id="db18e-130">NOTES</span></span>

## <span data-ttu-id="db18e-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="db18e-131">RELATED LINKS</span></span>

[<span data-ttu-id="db18e-132">Restore-AzureWebsiteDeployment</span><span class="sxs-lookup"><span data-stu-id="db18e-132">Restore-AzureWebsiteDeployment</span></span>](./Restore-AzureWebsiteDeployment.md)


