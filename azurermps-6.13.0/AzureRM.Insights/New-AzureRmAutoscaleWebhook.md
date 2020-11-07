---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 607976539e6bf93a0fa947741a4af4d4a7d34b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623926"
---
# <span data-ttu-id="2e1fe-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="2e1fe-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="2e1fe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2e1fe-102">SYNOPSIS</span></span>
<span data-ttu-id="2e1fe-103">建立自動縮放 webhook。</span><span class="sxs-lookup"><span data-stu-id="2e1fe-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e1fe-104">句法</span><span class="sxs-lookup"><span data-stu-id="2e1fe-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e1fe-105">說明</span><span class="sxs-lookup"><span data-stu-id="2e1fe-105">DESCRIPTION</span></span>
<span data-ttu-id="2e1fe-106">**新的-AzureRmAutoscaleWebhook** Cmdlet 會建立自動縮放 webhook。</span><span class="sxs-lookup"><span data-stu-id="2e1fe-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="2e1fe-107">示例</span><span class="sxs-lookup"><span data-stu-id="2e1fe-107">EXAMPLES</span></span>

## <span data-ttu-id="2e1fe-108">參數</span><span class="sxs-lookup"><span data-stu-id="2e1fe-108">PARAMETERS</span></span>

### <span data-ttu-id="2e1fe-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e1fe-109">-DefaultProfile</span></span>
<span data-ttu-id="2e1fe-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2e1fe-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e1fe-111">-屬性</span><span class="sxs-lookup"><span data-stu-id="2e1fe-111">-Property</span></span>
<span data-ttu-id="2e1fe-112">指定 [@ (property1 = ' value1 ",.... ) 格式的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="2e1fe-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e1fe-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="2e1fe-113">-ServiceUri</span></span>
<span data-ttu-id="2e1fe-114">指定服務 URI。</span><span class="sxs-lookup"><span data-stu-id="2e1fe-114">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e1fe-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e1fe-115">CommonParameters</span></span>
<span data-ttu-id="2e1fe-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2e1fe-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e1fe-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2e1fe-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e1fe-118">輸入</span><span class="sxs-lookup"><span data-stu-id="2e1fe-118">INPUTS</span></span>

### <span data-ttu-id="2e1fe-119">System.object</span><span class="sxs-lookup"><span data-stu-id="2e1fe-119">System.String</span></span>

### <span data-ttu-id="2e1fe-120">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2e1fe-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2e1fe-121">輸出</span><span class="sxs-lookup"><span data-stu-id="2e1fe-121">OUTPUTS</span></span>

### <span data-ttu-id="2e1fe-122">WebhookNotification 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="2e1fe-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="2e1fe-123">筆記</span><span class="sxs-lookup"><span data-stu-id="2e1fe-123">NOTES</span></span>

## <span data-ttu-id="2e1fe-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="2e1fe-124">RELATED LINKS</span></span>

[<span data-ttu-id="2e1fe-125">新-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="2e1fe-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


