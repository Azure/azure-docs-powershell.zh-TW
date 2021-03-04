---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 7fa9cb54a6790a473be419dd934927ed26783d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903225"
---
# <span data-ttu-id="348c6-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="348c6-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="348c6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="348c6-102">SYNOPSIS</span></span>
<span data-ttu-id="348c6-103">瞭解目前 Azure 訂閱中命名空間的事件中樞 NetworkruleSet 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="348c6-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="348c6-104">語法</span><span class="sxs-lookup"><span data-stu-id="348c6-104">SYNTAX</span></span>

### <span data-ttu-id="348c6-105">NetworkRuleSetPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="348c6-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="348c6-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="348c6-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="348c6-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="348c6-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="348c6-108">描述</span><span class="sxs-lookup"><span data-stu-id="348c6-108">DESCRIPTION</span></span>
<span data-ttu-id="348c6-109">瞭解目前 Azure 訂閱中命名空間的事件中樞 NetworkruleSet 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="348c6-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="348c6-110">例子</span><span class="sxs-lookup"><span data-stu-id="348c6-110">EXAMPLES</span></span>

### <span data-ttu-id="348c6-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="348c6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="348c6-112">使用 ResourceGroup 和命名空間參數取得命名空間的事件中樞 NetworkruleSet 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="348c6-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="348c6-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="348c6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="348c6-114">使用目前訂閱中的命名空間取得 Event Hubs NetworkruleSet 命名空間的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="348c6-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="348c6-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="348c6-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="348c6-116">使用其他命名空間的資源識別碼取得命名空間的事件中樞 NetworkruleSet 詳細資料</span><span class="sxs-lookup"><span data-stu-id="348c6-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="348c6-117">參數</span><span class="sxs-lookup"><span data-stu-id="348c6-117">PARAMETERS</span></span>

### <span data-ttu-id="348c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="348c6-118">-DefaultProfile</span></span>
<span data-ttu-id="348c6-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="348c6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="348c6-120">-命名空間</span><span class="sxs-lookup"><span data-stu-id="348c6-120">-Namespace</span></span>
<span data-ttu-id="348c6-121">命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="348c6-121">Namespace Name</span></span>

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

### <span data-ttu-id="348c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="348c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="348c6-123">資源組名</span><span class="sxs-lookup"><span data-stu-id="348c6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="348c6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="348c6-124">-ResourceId</span></span>
<span data-ttu-id="348c6-125">命名空間資源識別碼</span><span class="sxs-lookup"><span data-stu-id="348c6-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="348c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="348c6-126">CommonParameters</span></span>
<span data-ttu-id="348c6-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="348c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="348c6-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="348c6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="348c6-129">輸入</span><span class="sxs-lookup"><span data-stu-id="348c6-129">INPUTS</span></span>

### <span data-ttu-id="348c6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="348c6-130">System.String</span></span>

## <span data-ttu-id="348c6-131">輸出</span><span class="sxs-lookup"><span data-stu-id="348c6-131">OUTPUTS</span></span>

### <span data-ttu-id="348c6-132">Microsoft.Azure.Commands.EventHub.models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="348c6-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="348c6-133">筆記</span><span class="sxs-lookup"><span data-stu-id="348c6-133">NOTES</span></span>

## <span data-ttu-id="348c6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="348c6-134">RELATED LINKS</span></span>