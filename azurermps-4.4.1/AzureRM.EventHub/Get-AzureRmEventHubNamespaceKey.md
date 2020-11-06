---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespaceKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e91b7edacc575ac98eb78ae44c88be4f6873f34c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456672"
---
# <span data-ttu-id="76bdb-101">Get-AzureRmEventHubNamespaceKey</span><span class="sxs-lookup"><span data-stu-id="76bdb-101">Get-AzureRmEventHubNamespaceKey</span></span>

## <span data-ttu-id="76bdb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="76bdb-103">取得指定事件中心命名空間授權規則之授權規則的主要、次要 connectionstrings 及金鑰的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="76bdb-103">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule of the specified Event Hubs namespace authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76bdb-104">句法</span><span class="sxs-lookup"><span data-stu-id="76bdb-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespaceKey [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthorizationRuleName] <String>
```

## <span data-ttu-id="76bdb-105">說明</span><span class="sxs-lookup"><span data-stu-id="76bdb-105">DESCRIPTION</span></span>
<span data-ttu-id="76bdb-106">Get-AzureRmEventHubNamespaceKey Cmdlet 會傳回指定的事件中樞命名空間中指定授權規則的主要和次要 connectionstrings 及金鑰詳細資料。</span><span class="sxs-lookup"><span data-stu-id="76bdb-106">The Get-AzureRmEventHubNamespaceKey cmdlet returns the Primary and Secondary connectionstrings and keys details of the specified authorization rule in the given Event Hubs namespace.</span></span>

## <span data-ttu-id="76bdb-107">示例</span><span class="sxs-lookup"><span data-stu-id="76bdb-107">EXAMPLES</span></span>

### <span data-ttu-id="76bdb-108">範例1</span><span class="sxs-lookup"><span data-stu-id="76bdb-108">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespaceKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="76bdb-109">取得 [ \` \` \` \` 資源群組 MyResourceGroupName] 中 [事件中心] 命名空間 MyNamespaceName 的 \` [主要]、[次要] connectionstrings 及 [金鑰] 的詳細資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="76bdb-109">Gets details of Primary, Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\` on the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="76bdb-110">參數</span><span class="sxs-lookup"><span data-stu-id="76bdb-110">PARAMETERS</span></span>

### <span data-ttu-id="76bdb-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="76bdb-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="76bdb-112">[事件中心] 命名空間上的授權規則名稱。</span><span class="sxs-lookup"><span data-stu-id="76bdb-112">The name of the authorization rule on the Event Hubs namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bdb-113">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="76bdb-113">-NamespaceName</span></span>
<span data-ttu-id="76bdb-114">事件中心命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="76bdb-114">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bdb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76bdb-115">-ResourceGroupName</span></span>
<span data-ttu-id="76bdb-116">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="76bdb-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="76bdb-117">輸入</span><span class="sxs-lookup"><span data-stu-id="76bdb-117">INPUTS</span></span>

### <span data-ttu-id="76bdb-118">System.object</span><span class="sxs-lookup"><span data-stu-id="76bdb-118">System.String</span></span>

## <span data-ttu-id="76bdb-119">輸出</span><span class="sxs-lookup"><span data-stu-id="76bdb-119">OUTPUTS</span></span>

### <span data-ttu-id="76bdb-120">ListKeysAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="76bdb-120">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="76bdb-121">筆記</span><span class="sxs-lookup"><span data-stu-id="76bdb-121">NOTES</span></span>

## <span data-ttu-id="76bdb-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="76bdb-122">RELATED LINKS</span></span>

