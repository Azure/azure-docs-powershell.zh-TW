---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 70b58b53b8e1ef88c59983b9da134a0fb935bcd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449510"
---
# <span data-ttu-id="340ae-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="340ae-101">Get-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="340ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="340ae-102">SYNOPSIS</span></span>
<span data-ttu-id="340ae-103">針對特定命名空間取得指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="340ae-103">Gets a description of the specified authorization rule for a given namespace.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="340ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="340ae-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="340ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="340ae-105">DESCRIPTION</span></span>
<span data-ttu-id="340ae-106">**AzureRmServiceBusNamespaceAuthorizationRule** Cmdlet 會在指定的命名空間中取得指定授權規則的描述。</span><span class="sxs-lookup"><span data-stu-id="340ae-106">The **Get-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given namespace.</span></span>

## <span data-ttu-id="340ae-107">示例</span><span class="sxs-lookup"><span data-stu-id="340ae-107">EXAMPLES</span></span>

### <span data-ttu-id="340ae-108">範例1</span><span class="sxs-lookup"><span data-stu-id="340ae-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="340ae-109">針對指定的命名空間傳回指定的授權規則描述。</span><span class="sxs-lookup"><span data-stu-id="340ae-109">Returns the specified authorization rule description for a specified namespace.</span></span>

## <span data-ttu-id="340ae-110">參數</span><span class="sxs-lookup"><span data-stu-id="340ae-110">PARAMETERS</span></span>

### <span data-ttu-id="340ae-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="340ae-111">-ResourceGroup</span></span>
<span data-ttu-id="340ae-112">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="340ae-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="340ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340ae-113">-DefaultProfile</span></span>
<span data-ttu-id="340ae-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="340ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="340ae-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="340ae-115">-Name</span></span>
<span data-ttu-id="340ae-116">[AuthorizationRule] 命名空間的名稱。</span><span class="sxs-lookup"><span data-stu-id="340ae-116">ServiceBus Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="340ae-117">-命名空間</span><span class="sxs-lookup"><span data-stu-id="340ae-117">-Namespace</span></span>
<span data-ttu-id="340ae-118">已將命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="340ae-118">ServiceBus Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="340ae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340ae-119">CommonParameters</span></span>
<span data-ttu-id="340ae-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="340ae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340ae-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="340ae-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340ae-122">輸入</span><span class="sxs-lookup"><span data-stu-id="340ae-122">INPUTS</span></span>

### <span data-ttu-id="340ae-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="340ae-123">-ResourceGroup</span></span>
 <span data-ttu-id="340ae-124">System.object</span><span class="sxs-lookup"><span data-stu-id="340ae-124">System.String</span></span>
 

### <span data-ttu-id="340ae-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="340ae-125">-NamespaceName</span></span>
 <span data-ttu-id="340ae-126">System.object</span><span class="sxs-lookup"><span data-stu-id="340ae-126">System.String</span></span>
 

### <span data-ttu-id="340ae-127">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="340ae-127">-AuthorizationRuleName</span></span>
 <span data-ttu-id="340ae-128">System.object</span><span class="sxs-lookup"><span data-stu-id="340ae-128">System.String</span></span>

## <span data-ttu-id="340ae-129">輸出</span><span class="sxs-lookup"><span data-stu-id="340ae-129">OUTPUTS</span></span>

### <span data-ttu-id="340ae-130">[System.object]。清單 ' 1 [0.0.1.0，SharedAccessAuthorizationRuleAttributes，，版本 =，Culture = 中性，PublicKeyToken = null]」））。）</span><span class="sxs-lookup"><span data-stu-id="340ae-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="340ae-131">識別碼：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 類型： AuthorizationRules Name： AuthoRule1 Location：標記：許可權： {偵聽、傳送}</span><span class="sxs-lookup"><span data-stu-id="340ae-131">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="340ae-132">筆記</span><span class="sxs-lookup"><span data-stu-id="340ae-132">NOTES</span></span>

## <span data-ttu-id="340ae-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="340ae-133">RELATED LINKS</span></span>

