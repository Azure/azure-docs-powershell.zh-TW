---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: cd3182a2a00f488dabd70a97d06693362068768c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454591"
---
# <span data-ttu-id="07c4b-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="07c4b-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="07c4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="07c4b-103">取得 Azure 事件格線支援之主題類型的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="07c4b-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07c4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="07c4b-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07c4b-105">說明</span><span class="sxs-lookup"><span data-stu-id="07c4b-105">DESCRIPTION</span></span>
<span data-ttu-id="07c4b-106">取得 Azure 事件格線支援之主題類型的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="07c4b-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="07c4b-107">如果指定主題類型名稱，則會傳回該主題類型的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="07c4b-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="07c4b-108">如果未指定主題類型名稱，則會傳回有關所有主題類型的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="07c4b-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="07c4b-109">如果已指定 IncludeEventTypes，則回應中會包含每個主題類型支援之事件種類的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="07c4b-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="07c4b-110">示例</span><span class="sxs-lookup"><span data-stu-id="07c4b-110">EXAMPLES</span></span>

### <span data-ttu-id="07c4b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="07c4b-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="07c4b-112">取得主題類型的清單。</span><span class="sxs-lookup"><span data-stu-id="07c4b-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="07c4b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="07c4b-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="07c4b-114">取得 StorageAccounts 主題類型的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="07c4b-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="07c4b-115">範例3</span><span class="sxs-lookup"><span data-stu-id="07c4b-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="07c4b-116">取得 StorageAccounts 主題類型的相關資訊，包括 StorageAccounts 支援的事件種類。</span><span class="sxs-lookup"><span data-stu-id="07c4b-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="07c4b-117">參數</span><span class="sxs-lookup"><span data-stu-id="07c4b-117">PARAMETERS</span></span>

### <span data-ttu-id="07c4b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c4b-118">-DefaultProfile</span></span>
<span data-ttu-id="07c4b-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="07c4b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07c4b-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="07c4b-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="07c4b-121">如果已指定，回應將會包含主題類型支援的事件種類。</span><span class="sxs-lookup"><span data-stu-id="07c4b-121">If specified, the response will include the event types supported by a topic type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07c4b-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="07c4b-122">-Name</span></span>
<span data-ttu-id="07c4b-123">EventGrid 主題類型名稱。</span><span class="sxs-lookup"><span data-stu-id="07c4b-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="07c4b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c4b-124">CommonParameters</span></span>
<span data-ttu-id="07c4b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07c4b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c4b-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07c4b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c4b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="07c4b-127">INPUTS</span></span>

### <span data-ttu-id="07c4b-128">System.object</span><span class="sxs-lookup"><span data-stu-id="07c4b-128">System.String</span></span>

## <span data-ttu-id="07c4b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="07c4b-129">OUTPUTS</span></span>

### <span data-ttu-id="07c4b-130">PSTopicTypeInfoListInstance 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="07c4b-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="07c4b-131">PSTopicTypeInfo 中的 EventGrid。</span><span class="sxs-lookup"><span data-stu-id="07c4b-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="07c4b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="07c4b-132">NOTES</span></span>

## <span data-ttu-id="07c4b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="07c4b-133">RELATED LINKS</span></span>