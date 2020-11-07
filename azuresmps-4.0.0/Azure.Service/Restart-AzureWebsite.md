---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E7F6EEF0-8896-4639-89A8-810F19161211
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4b32c031a91adc3ab56e06898a1aa8ad70ac4e8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966916"
---
# <span data-ttu-id="6c85f-101">Restart-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6c85f-101">Restart-AzureWebsite</span></span>

## <span data-ttu-id="6c85f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c85f-102">SYNOPSIS</span></span>
<span data-ttu-id="6c85f-103">停止並重新啟動指定的網站。</span><span class="sxs-lookup"><span data-stu-id="6c85f-103">Stops and then restarts the specified website.</span></span>

## <span data-ttu-id="6c85f-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c85f-104">SYNTAX</span></span>

```
Restart-AzureWebsite [-PassThru] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6c85f-105">說明</span><span class="sxs-lookup"><span data-stu-id="6c85f-105">DESCRIPTION</span></span>
<span data-ttu-id="6c85f-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c85f-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="6c85f-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="6c85f-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="6c85f-108">**Restart AzureWebsite** Cmdlet 會停止並重新啟動指定的網站。</span><span class="sxs-lookup"><span data-stu-id="6c85f-108">The **Restart-AzureWebsite** cmdlet stops and then restarts the specified website.</span></span>

## <span data-ttu-id="6c85f-109">示例</span><span class="sxs-lookup"><span data-stu-id="6c85f-109">EXAMPLES</span></span>

### <span data-ttu-id="6c85f-110">範例1：重新開機網站</span><span class="sxs-lookup"><span data-stu-id="6c85f-110">Example 1: Restart a website</span></span>
```
PS C:\> Restart-AzureWebsite -Name MyWebsite
```

<span data-ttu-id="6c85f-111">這個範例會重新開機名為 MyWebsite 的網站。</span><span class="sxs-lookup"><span data-stu-id="6c85f-111">This example restarts a website named MyWebsite.</span></span>

## <span data-ttu-id="6c85f-112">參數</span><span class="sxs-lookup"><span data-stu-id="6c85f-112">PARAMETERS</span></span>

### <span data-ttu-id="6c85f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c85f-113">-Name</span></span>
<span data-ttu-id="6c85f-114">指定要重新開機之 Azure 網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="6c85f-114">Specifies the name of the Azure website to restart.</span></span>

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

### <span data-ttu-id="6c85f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c85f-115">-PassThru</span></span>
<span data-ttu-id="6c85f-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="6c85f-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6c85f-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="6c85f-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6c85f-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6c85f-118">-Profile</span></span>
<span data-ttu-id="6c85f-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6c85f-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6c85f-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6c85f-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6c85f-121">-槽</span><span class="sxs-lookup"><span data-stu-id="6c85f-121">-Slot</span></span>
<span data-ttu-id="6c85f-122">指定網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="6c85f-122">Specifies the slot name of the website.</span></span>

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

### <span data-ttu-id="6c85f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c85f-123">CommonParameters</span></span>
<span data-ttu-id="6c85f-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c85f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c85f-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6c85f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c85f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6c85f-126">INPUTS</span></span>

## <span data-ttu-id="6c85f-127">輸出</span><span class="sxs-lookup"><span data-stu-id="6c85f-127">OUTPUTS</span></span>

## <span data-ttu-id="6c85f-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6c85f-128">NOTES</span></span>

## <span data-ttu-id="6c85f-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c85f-129">RELATED LINKS</span></span>

[<span data-ttu-id="6c85f-130">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6c85f-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="6c85f-131">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6c85f-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="6c85f-132">移除-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6c85f-132">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="6c85f-133">開始-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6c85f-133">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


