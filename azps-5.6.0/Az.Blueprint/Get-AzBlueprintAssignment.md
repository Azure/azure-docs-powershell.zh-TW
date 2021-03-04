---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 375eca319a1db467e97addac50faa3f91fe0ecc5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902638"
---
# <span data-ttu-id="54111-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="54111-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="54111-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54111-102">SYNOPSIS</span></span>
<span data-ttu-id="54111-103">取得一或多個藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="54111-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="54111-104">語法</span><span class="sxs-lookup"><span data-stu-id="54111-104">SYNTAX</span></span>

### <span data-ttu-id="54111-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="54111-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54111-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="54111-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54111-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="54111-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54111-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="54111-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54111-109">描述</span><span class="sxs-lookup"><span data-stu-id="54111-109">DESCRIPTION</span></span>
<span data-ttu-id="54111-110">取得一或多個藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="54111-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="54111-111">藍圖指派存在於訂閱範圍中。</span><span class="sxs-lookup"><span data-stu-id="54111-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="54111-112">例子</span><span class="sxs-lookup"><span data-stu-id="54111-112">EXAMPLES</span></span>

### <span data-ttu-id="54111-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="54111-113">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="54111-114">取得指定訂閱內的藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="54111-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="54111-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="54111-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="54111-116">取得指定訂閱中指定名稱的藍圖工作分派。</span><span class="sxs-lookup"><span data-stu-id="54111-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="54111-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="54111-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="54111-118">取得指定管理群組內的藍圖指派。</span><span class="sxs-lookup"><span data-stu-id="54111-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="54111-119">範例 4</span><span class="sxs-lookup"><span data-stu-id="54111-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="54111-120">取得指定管理群組中指定名稱的藍圖工作分派。</span><span class="sxs-lookup"><span data-stu-id="54111-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="54111-121">參數</span><span class="sxs-lookup"><span data-stu-id="54111-121">PARAMETERS</span></span>

### <span data-ttu-id="54111-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54111-122">-DefaultProfile</span></span>
<span data-ttu-id="54111-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="54111-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54111-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="54111-124">-ManagementGroupId</span></span>
<span data-ttu-id="54111-125">儲存藍圖工作分派之管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="54111-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54111-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="54111-126">-Name</span></span>
<span data-ttu-id="54111-127">藍圖工作分派名稱。</span><span class="sxs-lookup"><span data-stu-id="54111-127">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54111-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="54111-128">-SubscriptionId</span></span>
<span data-ttu-id="54111-129">部署藍圖指派的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="54111-129">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54111-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54111-130">CommonParameters</span></span>
<span data-ttu-id="54111-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54111-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54111-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54111-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54111-133">輸入</span><span class="sxs-lookup"><span data-stu-id="54111-133">INPUTS</span></span>

### <span data-ttu-id="54111-134">System.String</span><span class="sxs-lookup"><span data-stu-id="54111-134">System.String</span></span>

## <span data-ttu-id="54111-135">輸出</span><span class="sxs-lookup"><span data-stu-id="54111-135">OUTPUTS</span></span>

### <span data-ttu-id="54111-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="54111-136">System.Object</span></span>
## <span data-ttu-id="54111-137">筆記</span><span class="sxs-lookup"><span data-stu-id="54111-137">NOTES</span></span>

## <span data-ttu-id="54111-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="54111-138">RELATED LINKS</span></span>
