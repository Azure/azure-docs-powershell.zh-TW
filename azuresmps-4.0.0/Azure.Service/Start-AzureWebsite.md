---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: A9542EA9-C709-48D7-8066-496015AB977E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6c1e7aab4f7818cbfc7200b521a535d54fb08dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967216"
---
# <span data-ttu-id="ba56b-101">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ba56b-101">Start-AzureWebsite</span></span>

## <span data-ttu-id="ba56b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba56b-102">SYNOPSIS</span></span>
<span data-ttu-id="ba56b-103">啟動指定的網站。</span><span class="sxs-lookup"><span data-stu-id="ba56b-103">Starts the specified website.</span></span>

## <span data-ttu-id="ba56b-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba56b-104">SYNTAX</span></span>

```
Start-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba56b-105">說明</span><span class="sxs-lookup"><span data-stu-id="ba56b-105">DESCRIPTION</span></span>
<span data-ttu-id="ba56b-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ba56b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ba56b-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="ba56b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ba56b-108">**Start AzureWebsite** Cmdlet 會啟動在 Azure 中執行的指定網站。</span><span class="sxs-lookup"><span data-stu-id="ba56b-108">The **Start-AzureWebsite** cmdlet starts a specified website running in Azure.</span></span>

## <span data-ttu-id="ba56b-109">示例</span><span class="sxs-lookup"><span data-stu-id="ba56b-109">EXAMPLES</span></span>

## <span data-ttu-id="ba56b-110">參數</span><span class="sxs-lookup"><span data-stu-id="ba56b-110">PARAMETERS</span></span>

### <span data-ttu-id="ba56b-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba56b-111">-Name</span></span>
<span data-ttu-id="ba56b-112">指定要啟動的網站名稱。</span><span class="sxs-lookup"><span data-stu-id="ba56b-112">Specifies the name of the website to start.</span></span>

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

### <span data-ttu-id="ba56b-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba56b-113">-PassThru</span></span>
<span data-ttu-id="ba56b-114">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ba56b-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ba56b-115">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ba56b-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ba56b-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ba56b-116">-Profile</span></span>
<span data-ttu-id="ba56b-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ba56b-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba56b-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ba56b-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba56b-119">-槽</span><span class="sxs-lookup"><span data-stu-id="ba56b-119">-Slot</span></span>
<span data-ttu-id="ba56b-120">指定網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="ba56b-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="ba56b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba56b-121">CommonParameters</span></span>
<span data-ttu-id="ba56b-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba56b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba56b-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ba56b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba56b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ba56b-124">INPUTS</span></span>

## <span data-ttu-id="ba56b-125">輸出</span><span class="sxs-lookup"><span data-stu-id="ba56b-125">OUTPUTS</span></span>

## <span data-ttu-id="ba56b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ba56b-126">NOTES</span></span>

## <span data-ttu-id="ba56b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba56b-127">RELATED LINKS</span></span>

[<span data-ttu-id="ba56b-128">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ba56b-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="ba56b-129">重新開機-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ba56b-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="ba56b-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ba56b-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)

[<span data-ttu-id="ba56b-131">顯示-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ba56b-131">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)

[<span data-ttu-id="ba56b-132">停止 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="ba56b-132">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


