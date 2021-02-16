---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 97f13dc7c9a74fef3775d0aed0db9d7acfa4da43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139442"
---
# <span data-ttu-id="cec3b-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="cec3b-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="cec3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cec3b-102">SYNOPSIS</span></span>
<span data-ttu-id="cec3b-103">傳回由參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="cec3b-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="cec3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="cec3b-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cec3b-105">說明</span><span class="sxs-lookup"><span data-stu-id="cec3b-105">DESCRIPTION</span></span>
<span data-ttu-id="cec3b-106">傳回由參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="cec3b-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="cec3b-107">示例</span><span class="sxs-lookup"><span data-stu-id="cec3b-107">EXAMPLES</span></span>

### <span data-ttu-id="cec3b-108">範例1：初始化 Project FileFolder</span><span class="sxs-lookup"><span data-stu-id="cec3b-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="cec3b-109">初始化準備要使用的資源，並將它設定為預設狀態</span><span class="sxs-lookup"><span data-stu-id="cec3b-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="cec3b-110">參數</span><span class="sxs-lookup"><span data-stu-id="cec3b-110">PARAMETERS</span></span>

### <span data-ttu-id="cec3b-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="cec3b-111">-CodeDir</span></span>
<span data-ttu-id="cec3b-112">使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cec3b-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="cec3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec3b-113">-DefaultProfile</span></span>
<span data-ttu-id="cec3b-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cec3b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cec3b-115">-語言</span><span class="sxs-lookup"><span data-stu-id="cec3b-115">-Language</span></span>


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

### <span data-ttu-id="cec3b-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="cec3b-116">-ProjFileName</span></span>


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

### <span data-ttu-id="cec3b-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cec3b-117">-SubscriptionId</span></span>
<span data-ttu-id="cec3b-118">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="cec3b-118">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="cec3b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec3b-119">CommonParameters</span></span>
<span data-ttu-id="cec3b-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cec3b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec3b-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cec3b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec3b-122">輸入</span><span class="sxs-lookup"><span data-stu-id="cec3b-122">INPUTS</span></span>

## <span data-ttu-id="cec3b-123">輸出</span><span class="sxs-lookup"><span data-stu-id="cec3b-123">OUTPUTS</span></span>

### <span data-ttu-id="cec3b-124">IBot （BotService）。 Api20180712。</span><span class="sxs-lookup"><span data-stu-id="cec3b-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="cec3b-125">筆記</span><span class="sxs-lookup"><span data-stu-id="cec3b-125">NOTES</span></span>

<span data-ttu-id="cec3b-126">別名</span><span class="sxs-lookup"><span data-stu-id="cec3b-126">ALIASES</span></span>

## <span data-ttu-id="cec3b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="cec3b-127">RELATED LINKS</span></span>

