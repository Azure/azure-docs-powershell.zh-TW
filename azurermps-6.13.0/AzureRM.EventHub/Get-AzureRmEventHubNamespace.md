---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
ms.openlocfilehash: 35f9342fa66b46cfd029d6440d8d82134a6822a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445611"
---
# <span data-ttu-id="d0f74-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="d0f74-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="d0f74-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d0f74-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f74-103">取得事件中心命名空間的詳細資料，或取得目前 Azure 訂閱中所有事件中心命名空間的清單。</span><span class="sxs-lookup"><span data-stu-id="d0f74-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0f74-104">句法</span><span class="sxs-lookup"><span data-stu-id="d0f74-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0f74-105">說明</span><span class="sxs-lookup"><span data-stu-id="d0f74-105">DESCRIPTION</span></span>
<span data-ttu-id="d0f74-106">Get-AzureRmEventHubNamespace Cmdlet 會取得指定事件中樞命名空間的詳細資料，或目前 Azure 訂閱中所有事件中心命名空間的清單。</span><span class="sxs-lookup"><span data-stu-id="d0f74-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="d0f74-107">如果提供命名空間名稱，則會傳回單一事件中樞命名空間的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d0f74-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="d0f74-108">如果未提供命名空間名稱，則會傳回命名空間清單。</span><span class="sxs-lookup"><span data-stu-id="d0f74-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="d0f74-109">示例</span><span class="sxs-lookup"><span data-stu-id="d0f74-109">EXAMPLES</span></span>

### <span data-ttu-id="d0f74-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d0f74-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="d0f74-111">取得 \` \` 資源群組 MyResourceGroupName 中命名空間 MyNamespaceName 的詳細 \` 資料 \` 。</span><span class="sxs-lookup"><span data-stu-id="d0f74-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d0f74-112">參數</span><span class="sxs-lookup"><span data-stu-id="d0f74-112">PARAMETERS</span></span>

### <span data-ttu-id="d0f74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f74-113">-DefaultProfile</span></span>
<span data-ttu-id="d0f74-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d0f74-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f74-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="d0f74-115">-Name</span></span>
<span data-ttu-id="d0f74-116">EventHub 命名空間名稱</span><span class="sxs-lookup"><span data-stu-id="d0f74-116">EventHub Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f74-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f74-117">-ResourceGroupName</span></span>
<span data-ttu-id="d0f74-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="d0f74-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0f74-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f74-119">CommonParameters</span></span>
<span data-ttu-id="d0f74-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d0f74-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f74-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d0f74-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f74-122">輸入</span><span class="sxs-lookup"><span data-stu-id="d0f74-122">INPUTS</span></span>

### <span data-ttu-id="d0f74-123">System.object</span><span class="sxs-lookup"><span data-stu-id="d0f74-123">System.String</span></span>

## <span data-ttu-id="d0f74-124">輸出</span><span class="sxs-lookup"><span data-stu-id="d0f74-124">OUTPUTS</span></span>

### <span data-ttu-id="d0f74-125">PSNamespaceAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="d0f74-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="d0f74-126">筆記</span><span class="sxs-lookup"><span data-stu-id="d0f74-126">NOTES</span></span>

## <span data-ttu-id="d0f74-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="d0f74-127">RELATED LINKS</span></span>
