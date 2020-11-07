---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7E1A3988-CEEA-49E1-B6F4-1EFA39E170C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06cc64eb67f1e338ff5be28712d1c183bfefd5ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968034"
---
# <span data-ttu-id="eb159-101">Stop-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="eb159-101">Stop-AzureWebsite</span></span>

## <span data-ttu-id="eb159-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb159-102">SYNOPSIS</span></span>
<span data-ttu-id="eb159-103">停止指定的網站。</span><span class="sxs-lookup"><span data-stu-id="eb159-103">Stops the specified website.</span></span>

## <span data-ttu-id="eb159-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb159-104">SYNTAX</span></span>

```
Stop-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="eb159-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb159-105">DESCRIPTION</span></span>
<span data-ttu-id="eb159-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb159-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="eb159-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="eb159-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="eb159-108">**AzureWebsite** Cmdlet 會停止在 Azure 中託管的指定網站。</span><span class="sxs-lookup"><span data-stu-id="eb159-108">The **Stop-AzureWebsite** cmdlet stops the specified website hosted in Azure.</span></span>

## <span data-ttu-id="eb159-109">示例</span><span class="sxs-lookup"><span data-stu-id="eb159-109">EXAMPLES</span></span>

## <span data-ttu-id="eb159-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb159-110">PARAMETERS</span></span>

### <span data-ttu-id="eb159-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb159-111">-Name</span></span>
<span data-ttu-id="eb159-112">指定要停止的網站名稱。</span><span class="sxs-lookup"><span data-stu-id="eb159-112">Specifies the name of the website to stop.</span></span>

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

### <span data-ttu-id="eb159-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb159-113">-PassThru</span></span>
<span data-ttu-id="eb159-114">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="eb159-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="eb159-115">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="eb159-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="eb159-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="eb159-116">-Profile</span></span>
<span data-ttu-id="eb159-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="eb159-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="eb159-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="eb159-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="eb159-119">-槽</span><span class="sxs-lookup"><span data-stu-id="eb159-119">-Slot</span></span>
<span data-ttu-id="eb159-120">指定網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="eb159-120">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="eb159-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb159-121">CommonParameters</span></span>
<span data-ttu-id="eb159-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb159-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb159-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb159-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb159-124">輸入</span><span class="sxs-lookup"><span data-stu-id="eb159-124">INPUTS</span></span>

## <span data-ttu-id="eb159-125">輸出</span><span class="sxs-lookup"><span data-stu-id="eb159-125">OUTPUTS</span></span>

## <span data-ttu-id="eb159-126">筆記</span><span class="sxs-lookup"><span data-stu-id="eb159-126">NOTES</span></span>

## <span data-ttu-id="eb159-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb159-127">RELATED LINKS</span></span>

[<span data-ttu-id="eb159-128">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="eb159-128">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="eb159-129">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="eb159-129">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


