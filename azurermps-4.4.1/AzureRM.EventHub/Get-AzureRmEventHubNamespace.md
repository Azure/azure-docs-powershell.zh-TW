---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 971312367815c8dc9c8c4f3f8fb6f2face0b7408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454379"
---
# <span data-ttu-id="f2a36-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="f2a36-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="f2a36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2a36-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a36-103">取得事件中心命名空間的詳細資料，或取得目前 Azure 訂閱中所有事件中心命名空間的清單。</span><span class="sxs-lookup"><span data-stu-id="f2a36-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2a36-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2a36-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [-Name <String>]
```

## <span data-ttu-id="f2a36-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2a36-105">DESCRIPTION</span></span>
<span data-ttu-id="f2a36-106">Get-AzureRmEventHubNamespace Cmdlet 會取得指定事件中樞命名空間的詳細資料，或目前 Azure 訂閱中所有事件中心命名空間的清單。</span><span class="sxs-lookup"><span data-stu-id="f2a36-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="f2a36-107">如果提供命名空間名稱，則會傳回單一事件中樞命名空間的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f2a36-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="f2a36-108">如果未提供命名空間名稱，則會傳回命名空間清單。</span><span class="sxs-lookup"><span data-stu-id="f2a36-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="f2a36-109">示例</span><span class="sxs-lookup"><span data-stu-id="f2a36-109">EXAMPLES</span></span>

### <span data-ttu-id="f2a36-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f2a36-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="f2a36-111">取得 \` \` 資源群組 MyResourceGroupName 中事件中心命名空間 MyNamespaceName 的詳細資料 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="f2a36-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f2a36-112">參數</span><span class="sxs-lookup"><span data-stu-id="f2a36-112">PARAMETERS</span></span>

### <span data-ttu-id="f2a36-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2a36-113">-ResourceGroupName</span></span>
<span data-ttu-id="f2a36-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f2a36-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2a36-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f2a36-115">-Name</span></span>
<span data-ttu-id="f2a36-116">EventHub 命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f2a36-116">EventHub Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="f2a36-117">輸入</span><span class="sxs-lookup"><span data-stu-id="f2a36-117">INPUTS</span></span>

### <span data-ttu-id="f2a36-118">System.object</span><span class="sxs-lookup"><span data-stu-id="f2a36-118">System.String</span></span>

## <span data-ttu-id="f2a36-119">輸出</span><span class="sxs-lookup"><span data-stu-id="f2a36-119">OUTPUTS</span></span>

### <span data-ttu-id="f2a36-120">[System.object]。清單 ' 1 [NamespaceAttributes，0.0.1.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="f2a36-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f2a36-121">筆記</span><span class="sxs-lookup"><span data-stu-id="f2a36-121">NOTES</span></span>

## <span data-ttu-id="f2a36-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2a36-122">RELATED LINKS</span></span>

