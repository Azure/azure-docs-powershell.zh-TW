---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
ms.openlocfilehash: d65e19cb86a2ba850311fa937e64432ee8588d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454232"
---
# <span data-ttu-id="e8a37-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e8a37-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="e8a37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8a37-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a37-103">取得事件中心命名空間的詳細資料，或取得目前 Azure 訂閱中所有事件中心命名空間的清單。</span><span class="sxs-lookup"><span data-stu-id="e8a37-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8a37-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8a37-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8a37-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8a37-105">DESCRIPTION</span></span>
<span data-ttu-id="e8a37-106">Get-AzureRmEventHubNamespace Cmdlet 會取得指定事件中樞命名空間的詳細資料，或目前 Azure 訂閱中所有事件中心命名空間的清單。</span><span class="sxs-lookup"><span data-stu-id="e8a37-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="e8a37-107">如果提供命名空間名稱，則會傳回單一事件中樞命名空間的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e8a37-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="e8a37-108">如果未提供命名空間名稱，則會傳回命名空間清單。</span><span class="sxs-lookup"><span data-stu-id="e8a37-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="e8a37-109">示例</span><span class="sxs-lookup"><span data-stu-id="e8a37-109">EXAMPLES</span></span>

### <span data-ttu-id="e8a37-110">範例1</span><span class="sxs-lookup"><span data-stu-id="e8a37-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="e8a37-111">取得 \` \` 資源群組 MyResourceGroupName 中事件中心命名空間 MyNamespaceName 的詳細資料 \` \` 。</span><span class="sxs-lookup"><span data-stu-id="e8a37-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e8a37-112">參數</span><span class="sxs-lookup"><span data-stu-id="e8a37-112">PARAMETERS</span></span>

### <span data-ttu-id="e8a37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a37-113">-DefaultProfile</span></span>
<span data-ttu-id="e8a37-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8a37-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8a37-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8a37-115">-Name</span></span>
<span data-ttu-id="e8a37-116">EventHub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="e8a37-116">EventHub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8a37-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8a37-117">-ResourceGroupName</span></span>
<span data-ttu-id="e8a37-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e8a37-118">Resource Group Name</span></span>

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

### <span data-ttu-id="e8a37-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a37-119">CommonParameters</span></span>
<span data-ttu-id="e8a37-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8a37-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e8a37-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8a37-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a37-122">輸入</span><span class="sxs-lookup"><span data-stu-id="e8a37-122">INPUTS</span></span>

### <span data-ttu-id="e8a37-123">System.object</span><span class="sxs-lookup"><span data-stu-id="e8a37-123">System.String</span></span>


## <span data-ttu-id="e8a37-124">輸出</span><span class="sxs-lookup"><span data-stu-id="e8a37-124">OUTPUTS</span></span>

### <span data-ttu-id="e8a37-125">[System.object]。清單 ' 1 [PSNamespaceAttributes，0.5.0.0，，版本 =，Culture = 中性，PublicKeyToken = null]]。）））</span><span class="sxs-lookup"><span data-stu-id="e8a37-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="e8a37-126">筆記</span><span class="sxs-lookup"><span data-stu-id="e8a37-126">NOTES</span></span>

## <span data-ttu-id="e8a37-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8a37-127">RELATED LINKS</span></span>
