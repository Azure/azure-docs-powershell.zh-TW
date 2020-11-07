---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: 4f2e7ea3293c9ca40271b9092673f33108a9f1be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789817"
---
# <span data-ttu-id="cca19-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="cca19-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="cca19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cca19-102">SYNOPSIS</span></span>
<span data-ttu-id="cca19-103">建立自動縮放 webhook。</span><span class="sxs-lookup"><span data-stu-id="cca19-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="cca19-104">句法</span><span class="sxs-lookup"><span data-stu-id="cca19-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cca19-105">說明</span><span class="sxs-lookup"><span data-stu-id="cca19-105">DESCRIPTION</span></span>
<span data-ttu-id="cca19-106">**新的-AzAutoscaleWebhook** Cmdlet 會建立自動縮放 webhook。</span><span class="sxs-lookup"><span data-stu-id="cca19-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="cca19-107">示例</span><span class="sxs-lookup"><span data-stu-id="cca19-107">EXAMPLES</span></span>

## <span data-ttu-id="cca19-108">參數</span><span class="sxs-lookup"><span data-stu-id="cca19-108">PARAMETERS</span></span>

### <span data-ttu-id="cca19-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca19-109">-DefaultProfile</span></span>
<span data-ttu-id="cca19-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cca19-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cca19-111">-屬性</span><span class="sxs-lookup"><span data-stu-id="cca19-111">-Property</span></span>
<span data-ttu-id="cca19-112">指定 [@ (property1 = ' value1 ",.... ) 格式的屬性清單。</span><span class="sxs-lookup"><span data-stu-id="cca19-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="cca19-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="cca19-113">-ServiceUri</span></span>
<span data-ttu-id="cca19-114">指定服務 URI。</span><span class="sxs-lookup"><span data-stu-id="cca19-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="cca19-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca19-115">CommonParameters</span></span>
<span data-ttu-id="cca19-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cca19-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca19-117">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cca19-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca19-118">輸入</span><span class="sxs-lookup"><span data-stu-id="cca19-118">INPUTS</span></span>

### <span data-ttu-id="cca19-119">System.object</span><span class="sxs-lookup"><span data-stu-id="cca19-119">System.String</span></span>

### <span data-ttu-id="cca19-120">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cca19-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cca19-121">輸出</span><span class="sxs-lookup"><span data-stu-id="cca19-121">OUTPUTS</span></span>

### <span data-ttu-id="cca19-122">WebhookNotification 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="cca19-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="cca19-123">筆記</span><span class="sxs-lookup"><span data-stu-id="cca19-123">NOTES</span></span>

## <span data-ttu-id="cca19-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="cca19-124">RELATED LINKS</span></span>

[<span data-ttu-id="cca19-125">新-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="cca19-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


