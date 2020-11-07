---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957814"
---
# <span data-ttu-id="907f4-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="907f4-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="907f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="907f4-102">SYNOPSIS</span></span>
<span data-ttu-id="907f4-103">取得目前 Azure 訂閱中的命名空間事件中心 NetworkruleSet 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="907f4-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="907f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="907f4-104">SYNTAX</span></span>

### <span data-ttu-id="907f4-105">NetworkRuleSetPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="907f4-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="907f4-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="907f4-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="907f4-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="907f4-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="907f4-108">說明</span><span class="sxs-lookup"><span data-stu-id="907f4-108">DESCRIPTION</span></span>
<span data-ttu-id="907f4-109">取得目前 Azure 訂閱中的命名空間事件中心 NetworkruleSet 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="907f4-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="907f4-110">示例</span><span class="sxs-lookup"><span data-stu-id="907f4-110">EXAMPLES</span></span>

### <span data-ttu-id="907f4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="907f4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="907f4-112">使用 ResourceGroup 和命名空間參數，取得命名空間之事件中心 NetworkruleSet 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="907f4-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="907f4-113">範例2</span><span class="sxs-lookup"><span data-stu-id="907f4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="907f4-114">使用目前訂閱中的命名空間來取得 namespace 事件中心 NetworkruleSet 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="907f4-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="907f4-115">範例3</span><span class="sxs-lookup"><span data-stu-id="907f4-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="907f4-116">使用其他命名空間的資源識別碼來取得命名空間之事件中心 NetworkruleSet 的詳細資料</span><span class="sxs-lookup"><span data-stu-id="907f4-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="907f4-117">參數</span><span class="sxs-lookup"><span data-stu-id="907f4-117">PARAMETERS</span></span>

### <span data-ttu-id="907f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="907f4-118">-DefaultProfile</span></span>
<span data-ttu-id="907f4-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="907f4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="907f4-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="907f4-120">-Namespace</span></span>
<span data-ttu-id="907f4-121">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="907f4-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="907f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="907f4-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="907f4-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="907f4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="907f4-124">-ResourceId</span></span>
<span data-ttu-id="907f4-125">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="907f4-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="907f4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="907f4-126">CommonParameters</span></span>
<span data-ttu-id="907f4-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="907f4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="907f4-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="907f4-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="907f4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="907f4-129">INPUTS</span></span>

### <span data-ttu-id="907f4-130">System.object</span><span class="sxs-lookup"><span data-stu-id="907f4-130">System.String</span></span>

## <span data-ttu-id="907f4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="907f4-131">OUTPUTS</span></span>

### <span data-ttu-id="907f4-132">PSNetworkRuleSetAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="907f4-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="907f4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="907f4-133">NOTES</span></span>

## <span data-ttu-id="907f4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="907f4-134">RELATED LINKS</span></span>