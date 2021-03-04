---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 118fce3e75ee7ba66fa30e6e07cfce16e5dadcff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916589"
---
# <span data-ttu-id="bd061-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="bd061-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="bd061-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bd061-102">SYNOPSIS</span></span>
<span data-ttu-id="bd061-103">會返回參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="bd061-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="bd061-104">語法</span><span class="sxs-lookup"><span data-stu-id="bd061-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bd061-105">描述</span><span class="sxs-lookup"><span data-stu-id="bd061-105">DESCRIPTION</span></span>
<span data-ttu-id="bd061-106">會返回參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="bd061-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="bd061-107">例子</span><span class="sxs-lookup"><span data-stu-id="bd061-107">EXAMPLES</span></span>

### <span data-ttu-id="bd061-108">範例 1：初始化 Project FileFolder</span><span class="sxs-lookup"><span data-stu-id="bd061-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="bd061-109">初始化準備資源以使用，並設定為預設狀態</span><span class="sxs-lookup"><span data-stu-id="bd061-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="bd061-110">參數</span><span class="sxs-lookup"><span data-stu-id="bd061-110">PARAMETERS</span></span>

### <span data-ttu-id="bd061-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="bd061-111">-CodeDir</span></span>
<span data-ttu-id="bd061-112">使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="bd061-112">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd061-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd061-113">-DefaultProfile</span></span>
<span data-ttu-id="bd061-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd061-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd061-115">-語言</span><span class="sxs-lookup"><span data-stu-id="bd061-115">-Language</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd061-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="bd061-116">-ProjFileName</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd061-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd061-117">-SubscriptionId</span></span>
<span data-ttu-id="bd061-118">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd061-118">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd061-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd061-119">CommonParameters</span></span>
<span data-ttu-id="bd061-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bd061-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd061-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd061-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd061-122">輸入</span><span class="sxs-lookup"><span data-stu-id="bd061-122">INPUTS</span></span>

## <span data-ttu-id="bd061-123">輸出</span><span class="sxs-lookup"><span data-stu-id="bd061-123">OUTPUTS</span></span>

### <span data-ttu-id="bd061-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="bd061-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="bd061-125">筆記</span><span class="sxs-lookup"><span data-stu-id="bd061-125">NOTES</span></span>

<span data-ttu-id="bd061-126">別名</span><span class="sxs-lookup"><span data-stu-id="bd061-126">ALIASES</span></span>

## <span data-ttu-id="bd061-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd061-127">RELATED LINKS</span></span>

