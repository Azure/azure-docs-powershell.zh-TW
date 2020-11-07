---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D39F4C9-F37A-4BBE-BF02-1F036A9FC5E8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0ec095393d68bb6764fa463941f1cd2b9644092f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967284"
---
# <span data-ttu-id="aff78-101">Stop-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="aff78-101">Stop-AzureWebsiteJob</span></span>

## <span data-ttu-id="aff78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aff78-102">SYNOPSIS</span></span>
<span data-ttu-id="aff78-103">停止網站的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="aff78-103">Stops a web job for a website.</span></span>

## <span data-ttu-id="aff78-104">句法</span><span class="sxs-lookup"><span data-stu-id="aff78-104">SYNTAX</span></span>

```
Stop-AzureWebsiteJob -JobName <String> [-PassThru] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="aff78-105">說明</span><span class="sxs-lookup"><span data-stu-id="aff78-105">DESCRIPTION</span></span>
<span data-ttu-id="aff78-106">**Stop-AzureWebsiteJob** Cmdlet 會停止網站的 web 作業。</span><span class="sxs-lookup"><span data-stu-id="aff78-106">The **Stop-AzureWebsiteJob** cmdlet stops a web job for a website.</span></span>

## <span data-ttu-id="aff78-107">示例</span><span class="sxs-lookup"><span data-stu-id="aff78-107">EXAMPLES</span></span>

### <span data-ttu-id="aff78-108">範例1：停止網站的 web 作業</span><span class="sxs-lookup"><span data-stu-id="aff78-108">Example 1: Stop a web job for a website</span></span>
```
PS C:\> Stop-AzureWebsiteJob -Name MyWebsite -JobName MyWebJob
```

<span data-ttu-id="aff78-109">停止稱為 MyWebJob 的網頁作業來 MyWebSite。</span><span class="sxs-lookup"><span data-stu-id="aff78-109">Stops a web job called MyWebJob for MyWebSite.</span></span>

## <span data-ttu-id="aff78-110">參數</span><span class="sxs-lookup"><span data-stu-id="aff78-110">PARAMETERS</span></span>

### <span data-ttu-id="aff78-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="aff78-111">-JobName</span></span>
<span data-ttu-id="aff78-112">Web 作業名稱。</span><span class="sxs-lookup"><span data-stu-id="aff78-112">The web job name.</span></span>

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

### <span data-ttu-id="aff78-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="aff78-113">-Name</span></span>
<span data-ttu-id="aff78-114">Azure 網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="aff78-114">The name of the Azure website.</span></span>

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

### <span data-ttu-id="aff78-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aff78-115">-PassThru</span></span>
<span data-ttu-id="aff78-116">會傳回一個 boolean 值，指出作業已順利停止。</span><span class="sxs-lookup"><span data-stu-id="aff78-116">Returns a boolean value indicating that the job stopped successfully.</span></span>
<span data-ttu-id="aff78-117">根據預設，這個 Cmdlet 不會傳回任何輸出。</span><span class="sxs-lookup"><span data-stu-id="aff78-117">By default, this cmdlet does not return any output.</span></span>

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

### <span data-ttu-id="aff78-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="aff78-118">-Profile</span></span>
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

### <span data-ttu-id="aff78-119">-槽</span><span class="sxs-lookup"><span data-stu-id="aff78-119">-Slot</span></span>
<span data-ttu-id="aff78-120">Azure 網站的槽名稱。</span><span class="sxs-lookup"><span data-stu-id="aff78-120">The slot name of the Azure website.</span></span>

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

### <span data-ttu-id="aff78-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff78-121">CommonParameters</span></span>
<span data-ttu-id="aff78-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aff78-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff78-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aff78-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff78-124">輸入</span><span class="sxs-lookup"><span data-stu-id="aff78-124">INPUTS</span></span>

## <span data-ttu-id="aff78-125">輸出</span><span class="sxs-lookup"><span data-stu-id="aff78-125">OUTPUTS</span></span>

## <span data-ttu-id="aff78-126">筆記</span><span class="sxs-lookup"><span data-stu-id="aff78-126">NOTES</span></span>

## <span data-ttu-id="aff78-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="aff78-127">RELATED LINKS</span></span>

[<span data-ttu-id="aff78-128">停止 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="aff78-128">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)

[<span data-ttu-id="aff78-129">AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="aff78-129">Get-AzureWebsiteJob</span></span>](./Get-AzureWebsiteJob.md)

[<span data-ttu-id="aff78-130">新-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="aff78-130">New-AzureWebsiteJob</span></span>](./New-AzureWebsiteJob.md)

[<span data-ttu-id="aff78-131">移除-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="aff78-131">Remove-AzureWebsiteJob</span></span>](./Remove-AzureWebsiteJob.md)

[<span data-ttu-id="aff78-132">開始-AzureWebsiteJob</span><span class="sxs-lookup"><span data-stu-id="aff78-132">Start-AzureWebsiteJob</span></span>](./Start-AzureWebsiteJob.md)


