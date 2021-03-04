---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 11f3124c98e84dcaec40c3b8ecd9b8831b572617
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916588"
---
# <span data-ttu-id="875c1-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="875c1-101">New-AzBotService</span></span>

## <span data-ttu-id="875c1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="875c1-102">SYNOPSIS</span></span>
<span data-ttu-id="875c1-103">會返回參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="875c1-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="875c1-104">語法</span><span class="sxs-lookup"><span data-stu-id="875c1-104">SYNTAX</span></span>

### <span data-ttu-id="875c1-105">註冊 (預設) </span><span class="sxs-lookup"><span data-stu-id="875c1-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="875c1-106">WebApp</span><span class="sxs-lookup"><span data-stu-id="875c1-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="875c1-107">描述</span><span class="sxs-lookup"><span data-stu-id="875c1-107">DESCRIPTION</span></span>
<span data-ttu-id="875c1-108">會返回參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="875c1-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="875c1-109">例子</span><span class="sxs-lookup"><span data-stu-id="875c1-109">EXAMPLES</span></span>

### <span data-ttu-id="875c1-110">範例 1：建立新 Bot</span><span class="sxs-lookup"><span data-stu-id="875c1-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="875c1-111">根據 ResourceGroupName 和 ApplicationId 建立新 Bot</span><span class="sxs-lookup"><span data-stu-id="875c1-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="875c1-112">範例 2：建立新 Web App</span><span class="sxs-lookup"><span data-stu-id="875c1-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="875c1-113">根據 ResourceGroupName 和 ApplicationId 建立新 Web App</span><span class="sxs-lookup"><span data-stu-id="875c1-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="875c1-114">參數</span><span class="sxs-lookup"><span data-stu-id="875c1-114">PARAMETERS</span></span>

### <span data-ttu-id="875c1-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="875c1-115">-ApplicationId</span></span>


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

### <span data-ttu-id="875c1-116">-ApplicationSecret</span><span class="sxs-lookup"><span data-stu-id="875c1-116">-ApplicationSecret</span></span>


```yaml
Type: System.Security.SecureString
Parameter Sets: WebApp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875c1-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="875c1-117">-BotTemplateType</span></span>


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

### <span data-ttu-id="875c1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="875c1-118">-DefaultProfile</span></span>
<span data-ttu-id="875c1-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="875c1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="875c1-120">-描述</span><span class="sxs-lookup"><span data-stu-id="875c1-120">-Description</span></span>


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

### <span data-ttu-id="875c1-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="875c1-121">-DisplayName</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875c1-122">-端點</span><span class="sxs-lookup"><span data-stu-id="875c1-122">-Endpoint</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875c1-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="875c1-123">-ExistingServerFarmId</span></span>


```yaml
Type: System.String
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875c1-124">-語言</span><span class="sxs-lookup"><span data-stu-id="875c1-124">-Language</span></span>


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

### <span data-ttu-id="875c1-125">-位置</span><span class="sxs-lookup"><span data-stu-id="875c1-125">-Location</span></span>


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

### <span data-ttu-id="875c1-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="875c1-126">-Name</span></span>
<span data-ttu-id="875c1-127">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="875c1-127">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875c1-128">-註冊</span><span class="sxs-lookup"><span data-stu-id="875c1-128">-Registration</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875c1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="875c1-129">-ResourceGroupName</span></span>
<span data-ttu-id="875c1-130">使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="875c1-130">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="875c1-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="875c1-131">-Sku</span></span>
<span data-ttu-id="875c1-132">SKU 名稱</span><span class="sxs-lookup"><span data-stu-id="875c1-132">The sku name</span></span>

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

### <span data-ttu-id="875c1-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="875c1-133">-SubscriptionId</span></span>
<span data-ttu-id="875c1-134">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="875c1-134">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="875c1-135">-Webapp</span><span class="sxs-lookup"><span data-stu-id="875c1-135">-Webapp</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875c1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875c1-136">CommonParameters</span></span>
<span data-ttu-id="875c1-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="875c1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875c1-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="875c1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875c1-139">輸入</span><span class="sxs-lookup"><span data-stu-id="875c1-139">INPUTS</span></span>

## <span data-ttu-id="875c1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="875c1-140">OUTPUTS</span></span>

### <span data-ttu-id="875c1-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="875c1-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="875c1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="875c1-142">NOTES</span></span>

<span data-ttu-id="875c1-143">別名</span><span class="sxs-lookup"><span data-stu-id="875c1-143">ALIASES</span></span>

## <span data-ttu-id="875c1-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="875c1-144">RELATED LINKS</span></span>

