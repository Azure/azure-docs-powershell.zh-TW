---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 3a715e0c4c2540a0905035afabc15ef46caa32bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911994"
---
# <span data-ttu-id="e49cb-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="e49cb-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="e49cb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e49cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e49cb-103">獲得 Azure 事件格線支援之主題類型的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e49cb-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="e49cb-104">語法</span><span class="sxs-lookup"><span data-stu-id="e49cb-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e49cb-105">描述</span><span class="sxs-lookup"><span data-stu-id="e49cb-105">DESCRIPTION</span></span>
<span data-ttu-id="e49cb-106">瞭解 Azure 事件格線支援的主題類型詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e49cb-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="e49cb-107">如果指定主題類型名稱，會返回該主題類型的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e49cb-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="e49cb-108">如果未指定主題類型名稱，會返回所有主題類型的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e49cb-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="e49cb-109">如果已指定 IncludeEventTypes，回應中會包含每個主題類型支援的事件種類相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e49cb-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="e49cb-110">例子</span><span class="sxs-lookup"><span data-stu-id="e49cb-110">EXAMPLES</span></span>

### <span data-ttu-id="e49cb-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e49cb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="e49cb-112">獲得主題類型的清單。</span><span class="sxs-lookup"><span data-stu-id="e49cb-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="e49cb-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="e49cb-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="e49cb-114">獲得有關 StorageAccounts 主題類型的資訊。</span><span class="sxs-lookup"><span data-stu-id="e49cb-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="e49cb-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="e49cb-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="e49cb-116">獲得有關 StorageAccount 主題類型的資訊，包括 StorageAccount 支援的事件種類。</span><span class="sxs-lookup"><span data-stu-id="e49cb-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="e49cb-117">參數</span><span class="sxs-lookup"><span data-stu-id="e49cb-117">PARAMETERS</span></span>

### <span data-ttu-id="e49cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49cb-118">-DefaultProfile</span></span>
<span data-ttu-id="e49cb-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e49cb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e49cb-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="e49cb-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="e49cb-121">如果指定，回應會包含主題類型支援的事件種類。</span><span class="sxs-lookup"><span data-stu-id="e49cb-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="e49cb-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e49cb-122">-Name</span></span>
<span data-ttu-id="e49cb-123">EventGrid 主題類型名稱。</span><span class="sxs-lookup"><span data-stu-id="e49cb-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e49cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49cb-124">CommonParameters</span></span>
<span data-ttu-id="e49cb-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e49cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49cb-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e49cb-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49cb-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e49cb-127">INPUTS</span></span>

### <span data-ttu-id="e49cb-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e49cb-128">System.String</span></span>

## <span data-ttu-id="e49cb-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e49cb-129">OUTPUTS</span></span>

### <span data-ttu-id="e49cb-130">Microsoft.Azure.Commands.EventGrid.models.PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="e49cb-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="e49cb-131">Microsoft.Azure.Commands.EventGrid.models.PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="e49cb-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="e49cb-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e49cb-132">NOTES</span></span>

## <span data-ttu-id="e49cb-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e49cb-133">RELATED LINKS</span></span>
