---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138737"
---
# <span data-ttu-id="20464-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="20464-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="20464-102">摘要</span><span class="sxs-lookup"><span data-stu-id="20464-102">SYNOPSIS</span></span>
<span data-ttu-id="20464-103">建立 Azns 動作群組類型的物件</span><span class="sxs-lookup"><span data-stu-id="20464-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="20464-104">句法</span><span class="sxs-lookup"><span data-stu-id="20464-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20464-105">說明</span><span class="sxs-lookup"><span data-stu-id="20464-105">DESCRIPTION</span></span>
<span data-ttu-id="20464-106">建立 Azns 動作群組類型的物件。</span><span class="sxs-lookup"><span data-stu-id="20464-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="20464-107">這個物件會傳遞到建立記錄提醒規則的命令。</span><span class="sxs-lookup"><span data-stu-id="20464-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="20464-108">示例</span><span class="sxs-lookup"><span data-stu-id="20464-108">EXAMPLES</span></span>

### <span data-ttu-id="20464-109">範例1</span><span class="sxs-lookup"><span data-stu-id="20464-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="20464-110">參數</span><span class="sxs-lookup"><span data-stu-id="20464-110">PARAMETERS</span></span>

### <span data-ttu-id="20464-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="20464-111">-ActionGroup</span></span>
<span data-ttu-id="20464-112">要傳送通知的動作群組清單</span><span class="sxs-lookup"><span data-stu-id="20464-112">The list of action groups to send notification to</span></span>

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

### <span data-ttu-id="20464-113">-CustomWebhookPayload</span><span class="sxs-lookup"><span data-stu-id="20464-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="20464-114">自訂的 webhook 負載</span><span class="sxs-lookup"><span data-stu-id="20464-114">The customized webhook payload</span></span>

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

### <span data-ttu-id="20464-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20464-115">-DefaultProfile</span></span>
<span data-ttu-id="20464-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="20464-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20464-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="20464-117">-EmailSubject</span></span>
<span data-ttu-id="20464-118">預警通知的電子郵件主題</span><span class="sxs-lookup"><span data-stu-id="20464-118">The email subject of alert notification</span></span>

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

### <span data-ttu-id="20464-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20464-119">CommonParameters</span></span>
<span data-ttu-id="20464-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="20464-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20464-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="20464-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20464-122">輸入</span><span class="sxs-lookup"><span data-stu-id="20464-122">INPUTS</span></span>

### <span data-ttu-id="20464-123">所有</span><span class="sxs-lookup"><span data-stu-id="20464-123">None</span></span>

## <span data-ttu-id="20464-124">輸出</span><span class="sxs-lookup"><span data-stu-id="20464-124">OUTPUTS</span></span>

### <span data-ttu-id="20464-125">PSScheduledQueryRuleAznsAction 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="20464-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="20464-126">筆記</span><span class="sxs-lookup"><span data-stu-id="20464-126">NOTES</span></span>

## <span data-ttu-id="20464-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="20464-127">RELATED LINKS</span></span>
