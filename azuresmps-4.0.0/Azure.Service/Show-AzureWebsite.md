---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7785F288-1CDF-444E-B72F-597E75B76074
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1e6e6d9921710bbed81eab727d2fe60927d2ed7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967231"
---
# <span data-ttu-id="48456-101">Show-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="48456-101">Show-AzureWebsite</span></span>

## <span data-ttu-id="48456-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48456-102">SYNOPSIS</span></span>
<span data-ttu-id="48456-103">在指定的網站上開啟瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="48456-103">Opens a browser on a specified website.</span></span>

## <span data-ttu-id="48456-104">句法</span><span class="sxs-lookup"><span data-stu-id="48456-104">SYNTAX</span></span>

```
Show-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="48456-105">說明</span><span class="sxs-lookup"><span data-stu-id="48456-105">DESCRIPTION</span></span>
<span data-ttu-id="48456-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48456-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="48456-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="48456-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="48456-108">**AzureWebsite** Cmdlet 會在指定的網站上開啟瀏覽器。</span><span class="sxs-lookup"><span data-stu-id="48456-108">The **Show-AzureWebsite** cmdlet opens a browser on a specified website.</span></span>

## <span data-ttu-id="48456-109">示例</span><span class="sxs-lookup"><span data-stu-id="48456-109">EXAMPLES</span></span>

## <span data-ttu-id="48456-110">參數</span><span class="sxs-lookup"><span data-stu-id="48456-110">PARAMETERS</span></span>

### <span data-ttu-id="48456-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="48456-111">-Name</span></span>
<span data-ttu-id="48456-112">指定要在瀏覽器中開啟之網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="48456-112">Specifies the name of the site to open in the browser.</span></span>

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

### <span data-ttu-id="48456-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="48456-113">-Profile</span></span>
<span data-ttu-id="48456-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="48456-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="48456-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="48456-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48456-116">-槽</span><span class="sxs-lookup"><span data-stu-id="48456-116">-Slot</span></span>
<span data-ttu-id="48456-117">指定網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="48456-117">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="48456-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48456-118">CommonParameters</span></span>
<span data-ttu-id="48456-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48456-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48456-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="48456-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48456-121">輸入</span><span class="sxs-lookup"><span data-stu-id="48456-121">INPUTS</span></span>

## <span data-ttu-id="48456-122">輸出</span><span class="sxs-lookup"><span data-stu-id="48456-122">OUTPUTS</span></span>

## <span data-ttu-id="48456-123">筆記</span><span class="sxs-lookup"><span data-stu-id="48456-123">NOTES</span></span>

## <span data-ttu-id="48456-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="48456-124">RELATED LINKS</span></span>

[<span data-ttu-id="48456-125">顯示-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="48456-125">Show-AzurePortal</span></span>](./Show-AzurePortal.md)

[<span data-ttu-id="48456-126">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="48456-126">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="48456-127">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="48456-127">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="48456-128">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="48456-128">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="48456-129">重新開機-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="48456-129">Restart-AzureWebsite</span></span>](./Restart-AzureWebsite.md)

[<span data-ttu-id="48456-130">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="48456-130">Set-AzureWebsite</span></span>](./Set-AzureWebsite.md)


