---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: EFBC8DCD-00CC-4BBF-9383-EA15376535F3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42780f62bc68659874f7aae1e64ad5ce89038fdf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967289"
---
# <span data-ttu-id="6eba8-101">Update-AzureWebsiteRepository</span><span class="sxs-lookup"><span data-stu-id="6eba8-101">Update-AzureWebsiteRepository</span></span>

## <span data-ttu-id="6eba8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6eba8-102">SYNOPSIS</span></span>
<span data-ttu-id="6eba8-103">針對所有的槽更新本機 git 儲存庫的遠端儲存庫。</span><span class="sxs-lookup"><span data-stu-id="6eba8-103">Updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="6eba8-104">句法</span><span class="sxs-lookup"><span data-stu-id="6eba8-104">SYNTAX</span></span>

```
Update-AzureWebsiteRepository [-Name <String>] -PublishingUsername <String> [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eba8-105">說明</span><span class="sxs-lookup"><span data-stu-id="6eba8-105">DESCRIPTION</span></span>
<span data-ttu-id="6eba8-106">**AzureWebsiteRepository** Cmdlet 會為所有槽更新本機 git 儲存庫的遠端儲存庫。</span><span class="sxs-lookup"><span data-stu-id="6eba8-106">The **Update-AzureWebsiteRepository** cmdlet updates the remote repositories of a local git repository for all the slots.</span></span>

## <span data-ttu-id="6eba8-107">示例</span><span class="sxs-lookup"><span data-stu-id="6eba8-107">EXAMPLES</span></span>

### <span data-ttu-id="6eba8-108">範例1：更新網站遠端資料庫</span><span class="sxs-lookup"><span data-stu-id="6eba8-108">Example 1: Update Website Remote Repositories</span></span>
```
PS C:\> Update-AzureWebsiteRepository -Name MyWebsite
```

<span data-ttu-id="6eba8-109">針對網站 MyWebsite 的所有槽更新本機 git 儲存庫的遠端儲存庫。</span><span class="sxs-lookup"><span data-stu-id="6eba8-109">Updates the remote repositories of a local git repository for all the slots for website MyWebsite.</span></span>

## <span data-ttu-id="6eba8-110">參數</span><span class="sxs-lookup"><span data-stu-id="6eba8-110">PARAMETERS</span></span>

### <span data-ttu-id="6eba8-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="6eba8-111">-Name</span></span>
<span data-ttu-id="6eba8-112">網站的名稱。</span><span class="sxs-lookup"><span data-stu-id="6eba8-112">The name of the website.</span></span>

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

### <span data-ttu-id="6eba8-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6eba8-113">-Profile</span></span>
<span data-ttu-id="6eba8-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6eba8-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6eba8-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6eba8-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6eba8-116">-PublishingUsername</span><span class="sxs-lookup"><span data-stu-id="6eba8-116">-PublishingUsername</span></span>
<span data-ttu-id="6eba8-117">您在使用 Git 部署的 Microsoft Azure 入口網站中指定的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="6eba8-117">The username you have specified in the Microsoft Azure Portal for Git deployment.</span></span>

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

### <span data-ttu-id="6eba8-118">-確認</span><span class="sxs-lookup"><span data-stu-id="6eba8-118">-Confirm</span></span>
<span data-ttu-id="6eba8-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6eba8-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eba8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eba8-120">-WhatIf</span></span>
<span data-ttu-id="6eba8-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6eba8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eba8-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6eba8-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6eba8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eba8-123">CommonParameters</span></span>
<span data-ttu-id="6eba8-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6eba8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eba8-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6eba8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eba8-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6eba8-126">INPUTS</span></span>

## <span data-ttu-id="6eba8-127">輸出</span><span class="sxs-lookup"><span data-stu-id="6eba8-127">OUTPUTS</span></span>

## <span data-ttu-id="6eba8-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6eba8-128">NOTES</span></span>

## <span data-ttu-id="6eba8-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6eba8-129">RELATED LINKS</span></span>

[<span data-ttu-id="6eba8-130">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6eba8-130">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="6eba8-131">新-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6eba8-131">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="6eba8-132">開始-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6eba8-132">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)

[<span data-ttu-id="6eba8-133">停止 AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="6eba8-133">Stop-AzureWebsite</span></span>](./Stop-AzureWebsite.md)


