---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 4ef38ab40f90024124f7d5f09f1a55c16520dd6b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139438"
---
# <span data-ttu-id="cf758-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="cf758-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="cf758-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf758-102">SYNOPSIS</span></span>
<span data-ttu-id="cf758-103">傳回由參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="cf758-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="cf758-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf758-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cf758-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf758-105">DESCRIPTION</span></span>
<span data-ttu-id="cf758-106">傳回由參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="cf758-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="cf758-107">示例</span><span class="sxs-lookup"><span data-stu-id="cf758-107">EXAMPLES</span></span>

### <span data-ttu-id="cf758-108">範例1：將您的 BotService 發佈至 Azure</span><span class="sxs-lookup"><span data-stu-id="cf758-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="cf758-109">透過程式碼將您的 BotService 發佈至 Azure</span><span class="sxs-lookup"><span data-stu-id="cf758-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="cf758-110">參數</span><span class="sxs-lookup"><span data-stu-id="cf758-110">PARAMETERS</span></span>

### <span data-ttu-id="cf758-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="cf758-111">-CodeDir</span></span>
<span data-ttu-id="cf758-112">這個參數定義 ZIP 的路徑</span><span class="sxs-lookup"><span data-stu-id="cf758-112">This parameter defines the Path of the ZIP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf758-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf758-113">-Name</span></span>
<span data-ttu-id="cf758-114">這個參數會定義 bot 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf758-114">This parameter defines the name of the bot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf758-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf758-115">-ResourceGroupName</span></span>
<span data-ttu-id="cf758-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf758-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf758-117">-確認</span><span class="sxs-lookup"><span data-stu-id="cf758-117">-Confirm</span></span>
<span data-ttu-id="cf758-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf758-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf758-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf758-119">-WhatIf</span></span>
<span data-ttu-id="cf758-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf758-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf758-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf758-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf758-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf758-122">CommonParameters</span></span>
<span data-ttu-id="cf758-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf758-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf758-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf758-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf758-125">輸入</span><span class="sxs-lookup"><span data-stu-id="cf758-125">INPUTS</span></span>

## <span data-ttu-id="cf758-126">輸出</span><span class="sxs-lookup"><span data-stu-id="cf758-126">OUTPUTS</span></span>

## <span data-ttu-id="cf758-127">筆記</span><span class="sxs-lookup"><span data-stu-id="cf758-127">NOTES</span></span>

<span data-ttu-id="cf758-128">別名</span><span class="sxs-lookup"><span data-stu-id="cf758-128">ALIASES</span></span>

## <span data-ttu-id="cf758-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf758-129">RELATED LINKS</span></span>

