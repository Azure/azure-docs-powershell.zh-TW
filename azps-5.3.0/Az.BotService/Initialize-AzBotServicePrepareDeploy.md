---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/initialize-azbotservicepreparedeploy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Initialize-AzBotServicePrepareDeploy.md
ms.openlocfilehash: 97f13dc7c9a74fef3775d0aed0db9d7acfa4da43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449963"
---
# <span data-ttu-id="78b5a-101">Initialize-AzBotServicePrepareDeploy</span><span class="sxs-lookup"><span data-stu-id="78b5a-101">Initialize-AzBotServicePrepareDeploy</span></span>

## <span data-ttu-id="78b5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="78b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="78b5a-103">傳回由參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="78b5a-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="78b5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="78b5a-104">SYNTAX</span></span>

```
Initialize-AzBotServicePrepareDeploy [-CodeDir <String>] [-Language <String>] [-ProjFileName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="78b5a-105">說明</span><span class="sxs-lookup"><span data-stu-id="78b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="78b5a-106">傳回由參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="78b5a-106">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="78b5a-107">示例</span><span class="sxs-lookup"><span data-stu-id="78b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="78b5a-108">範例1：初始化 Project FileFolder</span><span class="sxs-lookup"><span data-stu-id="78b5a-108">Example 1: Initialize the Project FileFolder</span></span>
```powershell
PS C:\> Initialize-AzBotServicePrepareDeploy -CodeDir D:\zips\MyEchoBot -ProjFileName MyEchoBot.csproj

```

<span data-ttu-id="78b5a-109">初始化準備要使用的資源，並將它設定為預設狀態</span><span class="sxs-lookup"><span data-stu-id="78b5a-109">Initialize Prepares a resource for use, and sets it to a default state</span></span>

## <span data-ttu-id="78b5a-110">參數</span><span class="sxs-lookup"><span data-stu-id="78b5a-110">PARAMETERS</span></span>

### <span data-ttu-id="78b5a-111">-CodeDir</span><span class="sxs-lookup"><span data-stu-id="78b5a-111">-CodeDir</span></span>
<span data-ttu-id="78b5a-112">使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="78b5a-112">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="78b5a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b5a-113">-DefaultProfile</span></span>
<span data-ttu-id="78b5a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="78b5a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78b5a-115">-語言</span><span class="sxs-lookup"><span data-stu-id="78b5a-115">-Language</span></span>


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

### <span data-ttu-id="78b5a-116">-ProjFileName</span><span class="sxs-lookup"><span data-stu-id="78b5a-116">-ProjFileName</span></span>


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

### <span data-ttu-id="78b5a-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="78b5a-117">-SubscriptionId</span></span>
<span data-ttu-id="78b5a-118">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="78b5a-118">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="78b5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b5a-119">CommonParameters</span></span>
<span data-ttu-id="78b5a-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="78b5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b5a-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="78b5a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b5a-122">輸入</span><span class="sxs-lookup"><span data-stu-id="78b5a-122">INPUTS</span></span>

## <span data-ttu-id="78b5a-123">輸出</span><span class="sxs-lookup"><span data-stu-id="78b5a-123">OUTPUTS</span></span>

### <span data-ttu-id="78b5a-124">IBot （BotService）。 Api20180712。</span><span class="sxs-lookup"><span data-stu-id="78b5a-124">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="78b5a-125">筆記</span><span class="sxs-lookup"><span data-stu-id="78b5a-125">NOTES</span></span>

<span data-ttu-id="78b5a-126">別名</span><span class="sxs-lookup"><span data-stu-id="78b5a-126">ALIASES</span></span>

## <span data-ttu-id="78b5a-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="78b5a-127">RELATED LINKS</span></span>

