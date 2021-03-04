---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: b5bfac31babfd4bc848f9619dc8eb8cecd1c3eaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917146"
---
# <span data-ttu-id="24705-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="24705-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="24705-102">簡介</span><span class="sxs-lookup"><span data-stu-id="24705-102">SYNOPSIS</span></span>
<span data-ttu-id="24705-103">建立 Azns 動作群組類型的物件</span><span class="sxs-lookup"><span data-stu-id="24705-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="24705-104">語法</span><span class="sxs-lookup"><span data-stu-id="24705-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="24705-105">描述</span><span class="sxs-lookup"><span data-stu-id="24705-105">DESCRIPTION</span></span>
<span data-ttu-id="24705-106">建立類型為 Azns 動作群組的物件。</span><span class="sxs-lookup"><span data-stu-id="24705-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="24705-107">這個物件會傳遞至建立記錄提醒規則的命令。</span><span class="sxs-lookup"><span data-stu-id="24705-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="24705-108">例子</span><span class="sxs-lookup"><span data-stu-id="24705-108">EXAMPLES</span></span>

### <span data-ttu-id="24705-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="24705-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="24705-110">參數</span><span class="sxs-lookup"><span data-stu-id="24705-110">PARAMETERS</span></span>

### <span data-ttu-id="24705-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="24705-111">-ActionGroup</span></span>
<span data-ttu-id="24705-112">要傳送通知的動作群組清單</span><span class="sxs-lookup"><span data-stu-id="24705-112">The list of action groups to send notification to</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24705-113">-CustomWebpayPayload</span><span class="sxs-lookup"><span data-stu-id="24705-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="24705-114">自訂的 web下一個負載</span><span class="sxs-lookup"><span data-stu-id="24705-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="24705-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24705-115">-DefaultProfile</span></span>
<span data-ttu-id="24705-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="24705-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24705-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="24705-117">-EmailSubject</span></span>
<span data-ttu-id="24705-118">警示通知的電子郵件主體</span><span class="sxs-lookup"><span data-stu-id="24705-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="24705-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24705-119">CommonParameters</span></span>
<span data-ttu-id="24705-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="24705-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24705-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="24705-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24705-122">輸入</span><span class="sxs-lookup"><span data-stu-id="24705-122">INPUTS</span></span>

### <span data-ttu-id="24705-123">沒有</span><span class="sxs-lookup"><span data-stu-id="24705-123">None</span></span>

## <span data-ttu-id="24705-124">輸出</span><span class="sxs-lookup"><span data-stu-id="24705-124">OUTPUTS</span></span>

### <span data-ttu-id="24705-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="24705-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="24705-126">筆記</span><span class="sxs-lookup"><span data-stu-id="24705-126">NOTES</span></span>

## <span data-ttu-id="24705-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="24705-127">RELATED LINKS</span></span>
