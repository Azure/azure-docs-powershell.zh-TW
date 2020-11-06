---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: f4f28ee3f07127803e6187f00565ee8d4caf3084
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456683"
---
# <span data-ttu-id="ab3f5-101">Get-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="ab3f5-101">Get-AzureRmEventHubKey</span></span>

## <span data-ttu-id="ab3f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab3f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3f5-103">取得指定事件中心授權規則的主要金鑰詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab3f5-103">Gets the primary key details of the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab3f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab3f5-104">SYNTAX</span></span>

### <span data-ttu-id="ab3f5-105">NamespaceAuthorizationRuleSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ab3f5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> -Namespace <String> -Name <String>
```

### <span data-ttu-id="ab3f5-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ab3f5-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String> -Name <String>
```

## <span data-ttu-id="ab3f5-107">說明</span><span class="sxs-lookup"><span data-stu-id="ab3f5-107">DESCRIPTION</span></span>
<span data-ttu-id="ab3f5-108">Get-AzureRmEventHubKey Cmdlet 會傳回指定事件中心授權規則的主要和次要 connectionstrings 及金鑰詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ab3f5-108">The Get-AzureRmEventHubKey cmdlet returns Primary and Secondary connectionstrings and keys details of the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="ab3f5-109">示例</span><span class="sxs-lookup"><span data-stu-id="ab3f5-109">EXAMPLES</span></span>

### <span data-ttu-id="ab3f5-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ab3f5-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubKey -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName
```

<span data-ttu-id="ab3f5-111">取得授權規則 MyAuthRuleName 的主要和次要 connectionstrings 及金鑰的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="ab3f5-111">Gets details of Primary and Secondary connectionstrings and keys for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="ab3f5-112">參數</span><span class="sxs-lookup"><span data-stu-id="ab3f5-112">PARAMETERS</span></span>

### <span data-ttu-id="ab3f5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab3f5-113">-ResourceGroupName</span></span>
<span data-ttu-id="ab3f5-114">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ab3f5-114">Resource group name.</span></span>

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

### <span data-ttu-id="ab3f5-115">-EventHub</span><span class="sxs-lookup"><span data-stu-id="ab3f5-115">-EventHub</span></span>
<span data-ttu-id="ab3f5-116">EventHub Name。</span><span class="sxs-lookup"><span data-stu-id="ab3f5-116">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab3f5-117">-Name</span></span>
<span data-ttu-id="ab3f5-118">AuthorizationRule [名稱]。</span><span class="sxs-lookup"><span data-stu-id="ab3f5-118">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3f5-119">-命名空間</span><span class="sxs-lookup"><span data-stu-id="ab3f5-119">-Namespace</span></span>
<span data-ttu-id="ab3f5-120">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="ab3f5-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="ab3f5-121">輸入</span><span class="sxs-lookup"><span data-stu-id="ab3f5-121">INPUTS</span></span>

### <span data-ttu-id="ab3f5-122">System.object</span><span class="sxs-lookup"><span data-stu-id="ab3f5-122">System.String</span></span>

## <span data-ttu-id="ab3f5-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ab3f5-123">OUTPUTS</span></span>

### <span data-ttu-id="ab3f5-124">ListKeysAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="ab3f5-124">Microsoft.Azure.Commands.EventHub.Models.ListKeysAttributes</span></span>

## <span data-ttu-id="ab3f5-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ab3f5-125">NOTES</span></span>

## <span data-ttu-id="ab3f5-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab3f5-126">RELATED LINKS</span></span>

