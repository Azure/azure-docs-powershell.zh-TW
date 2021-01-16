---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274576"
---
# <span data-ttu-id="eab75-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="eab75-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="eab75-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eab75-102">SYNOPSIS</span></span>
<span data-ttu-id="eab75-103">取得一或多個藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="eab75-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="eab75-104">句法</span><span class="sxs-lookup"><span data-stu-id="eab75-104">SYNTAX</span></span>

### <span data-ttu-id="eab75-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="eab75-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eab75-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="eab75-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eab75-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="eab75-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eab75-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="eab75-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eab75-109">說明</span><span class="sxs-lookup"><span data-stu-id="eab75-109">DESCRIPTION</span></span>
<span data-ttu-id="eab75-110">取得一或多個藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="eab75-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="eab75-111">在訂閱範圍中存在藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="eab75-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="eab75-112">示例</span><span class="sxs-lookup"><span data-stu-id="eab75-112">EXAMPLES</span></span>

### <span data-ttu-id="eab75-113">範例1</span><span class="sxs-lookup"><span data-stu-id="eab75-113">Example 1</span></span>
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

<span data-ttu-id="eab75-114">在指定的訂閱中取得藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="eab75-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="eab75-115">範例2</span><span class="sxs-lookup"><span data-stu-id="eab75-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="eab75-116">在指定的訂閱中取得具有指定名稱的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="eab75-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="eab75-117">範例3</span><span class="sxs-lookup"><span data-stu-id="eab75-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="eab75-118">在指定的管理群組中取得藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="eab75-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="eab75-119">範例4</span><span class="sxs-lookup"><span data-stu-id="eab75-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="eab75-120">在指定的管理群組中取得具有指定名稱的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="eab75-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="eab75-121">參數</span><span class="sxs-lookup"><span data-stu-id="eab75-121">PARAMETERS</span></span>

### <span data-ttu-id="eab75-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab75-122">-DefaultProfile</span></span>
<span data-ttu-id="eab75-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eab75-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eab75-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="eab75-124">-ManagementGroupId</span></span>
<span data-ttu-id="eab75-125">儲存藍圖分派的管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="eab75-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="eab75-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="eab75-126">-Name</span></span>
<span data-ttu-id="eab75-127">藍圖作業名稱。</span><span class="sxs-lookup"><span data-stu-id="eab75-127">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="eab75-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="eab75-128">-SubscriptionId</span></span>
<span data-ttu-id="eab75-129">已部署藍圖指派的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="eab75-129">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="eab75-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab75-130">CommonParameters</span></span>
<span data-ttu-id="eab75-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eab75-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab75-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eab75-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab75-133">輸入</span><span class="sxs-lookup"><span data-stu-id="eab75-133">INPUTS</span></span>

### <span data-ttu-id="eab75-134">System.object</span><span class="sxs-lookup"><span data-stu-id="eab75-134">System.String</span></span>

## <span data-ttu-id="eab75-135">輸出</span><span class="sxs-lookup"><span data-stu-id="eab75-135">OUTPUTS</span></span>

### <span data-ttu-id="eab75-136">System.object</span><span class="sxs-lookup"><span data-stu-id="eab75-136">System.Object</span></span>
## <span data-ttu-id="eab75-137">筆記</span><span class="sxs-lookup"><span data-stu-id="eab75-137">NOTES</span></span>

## <span data-ttu-id="eab75-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="eab75-138">RELATED LINKS</span></span>
