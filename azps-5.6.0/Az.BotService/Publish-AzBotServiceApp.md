---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/publish-azbotserviceapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Publish-AzBotServiceApp.md
ms.openlocfilehash: 551428a1c5d1737d32aeddf2dd5653586d1dbfbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905193"
---
# <span data-ttu-id="ac5de-101">Publish-AzBotServiceApp</span><span class="sxs-lookup"><span data-stu-id="ac5de-101">Publish-AzBotServiceApp</span></span>

## <span data-ttu-id="ac5de-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ac5de-102">SYNOPSIS</span></span>
<span data-ttu-id="ac5de-103">會返回參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="ac5de-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="ac5de-104">語法</span><span class="sxs-lookup"><span data-stu-id="ac5de-104">SYNTAX</span></span>

```
Publish-AzBotServiceApp -CodeDir <String> -Name <String> -ResourceGroupName <String> [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="ac5de-105">描述</span><span class="sxs-lookup"><span data-stu-id="ac5de-105">DESCRIPTION</span></span>
<span data-ttu-id="ac5de-106">會返回參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="ac5de-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="ac5de-107">例子</span><span class="sxs-lookup"><span data-stu-id="ac5de-107">EXAMPLES</span></span>

### <span data-ttu-id="ac5de-108">範例 1：將 BotService 發佈至 Azure</span><span class="sxs-lookup"><span data-stu-id="ac5de-108">Example 1: Publish your BotService to Azure</span></span>
```powershell
PS C:\> Publish-AzBotServiceApp -ResourceGroupName youriBotTest -CodeDir D:\zips\MyEchoBot -Name youriechobottest

```

<span data-ttu-id="ac5de-109">使用程式碼將 BotService 發佈至 Azure</span><span class="sxs-lookup"><span data-stu-id="ac5de-109">Publish your BotService to Azure by code</span></span>

## <span data-ttu-id="ac5de-110">參數</span><span class="sxs-lookup"><span data-stu-id="ac5de-110">PARAMETERS</span></span>

### <span data-ttu-id="ac5de-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="ac5de-111">-CodeDir</span></span>
<span data-ttu-id="ac5de-112">此參數會定義 ZIP 的路徑</span><span class="sxs-lookup"><span data-stu-id="ac5de-112">This parameter defines the Path of the ZIP</span></span>

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

### <span data-ttu-id="ac5de-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac5de-113">-Name</span></span>
<span data-ttu-id="ac5de-114">此參數會定義 Bot 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac5de-114">This parameter defines the name of the bot.</span></span>

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

### <span data-ttu-id="ac5de-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac5de-115">-ResourceGroupName</span></span>
<span data-ttu-id="ac5de-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac5de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac5de-117">-確認</span><span class="sxs-lookup"><span data-stu-id="ac5de-117">-Confirm</span></span>
<span data-ttu-id="ac5de-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ac5de-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac5de-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac5de-119">-WhatIf</span></span>
<span data-ttu-id="ac5de-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac5de-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac5de-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac5de-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac5de-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac5de-122">CommonParameters</span></span>
<span data-ttu-id="ac5de-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ac5de-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac5de-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac5de-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac5de-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ac5de-125">INPUTS</span></span>

## <span data-ttu-id="ac5de-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ac5de-126">OUTPUTS</span></span>

## <span data-ttu-id="ac5de-127">筆記</span><span class="sxs-lookup"><span data-stu-id="ac5de-127">NOTES</span></span>

<span data-ttu-id="ac5de-128">別名</span><span class="sxs-lookup"><span data-stu-id="ac5de-128">ALIASES</span></span>

## <span data-ttu-id="ac5de-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac5de-129">RELATED LINKS</span></span>

