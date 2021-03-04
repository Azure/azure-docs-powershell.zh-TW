---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: 6b646e22ff32d9fe361cdedd6dbb6fa5c9fba270
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916781"
---
# <span data-ttu-id="50b7d-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="50b7d-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="50b7d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="50b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="50b7d-103">取得一或多個藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="50b7d-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="50b7d-104">語法</span><span class="sxs-lookup"><span data-stu-id="50b7d-104">SYNTAX</span></span>

### <span data-ttu-id="50b7d-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="50b7d-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50b7d-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="50b7d-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50b7d-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="50b7d-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50b7d-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="50b7d-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50b7d-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="50b7d-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50b7d-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="50b7d-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50b7d-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="50b7d-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50b7d-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="50b7d-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50b7d-113">描述</span><span class="sxs-lookup"><span data-stu-id="50b7d-113">DESCRIPTION</span></span>
<span data-ttu-id="50b7d-114">取得一或多個藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="50b7d-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="50b7d-115">藍圖定義存在於管理群組或訂閱範圍中。</span><span class="sxs-lookup"><span data-stu-id="50b7d-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="50b7d-116">例子</span><span class="sxs-lookup"><span data-stu-id="50b7d-116">EXAMPLES</span></span>

### <span data-ttu-id="50b7d-117">範例 1</span><span class="sxs-lookup"><span data-stu-id="50b7d-117">Example 1</span></span>
```powershell
PS> Get-AzBlueprint

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="50b7d-118">取得目前訂閱和訂閱管理群組階層內的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="50b7d-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="50b7d-119">範例 2</span><span class="sxs-lookup"><span data-stu-id="50b7d-119">Example 2</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId"

Name                 : PS-MG-BlueprintDefinition
Id                   : /providers/Microsoft.Management/managementGroups/myManagementGroupId/providers/Microsoft.Blueprint/blueprints/PS-MG-BlueprintDefinition
ManagementGroupId    : myManagementGroupId
Versions             : {1.0, 2.0, 3.0, 4.0}
TimeCreated          : 2019-03-04
TargetScope          : Subscription
Parameters           : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue, [Usergrouporapplicationname]:Contributor_RoleAssignmentName,
                       [Usergrouporapplicationname]:Owner_RoleAssignmentName}
ResourceGroups       : {ResourceGroup, ResourceGroup2}
```

<span data-ttu-id="50b7d-120">取得指定管理群組內的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="50b7d-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="50b7d-121">範例 3</span><span class="sxs-lookup"><span data-stu-id="50b7d-121">Example 3</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="50b7d-122">取得指定訂閱和訂閱管理群組階層內的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="50b7d-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="50b7d-123">範例 4</span><span class="sxs-lookup"><span data-stu-id="50b7d-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="50b7d-124">取得指定訂閱中指定名稱的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="50b7d-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="50b7d-125">範例 5</span><span class="sxs-lookup"><span data-stu-id="50b7d-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="50b7d-126">取得藍圖定義，並指定管理群組內的指定名稱和版本。</span><span class="sxs-lookup"><span data-stu-id="50b7d-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="50b7d-127">範例 6</span><span class="sxs-lookup"><span data-stu-id="50b7d-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="50b7d-128">取得最新發佈的藍圖定義，並指定管理群組中的指定名稱。</span><span class="sxs-lookup"><span data-stu-id="50b7d-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="50b7d-129">參數</span><span class="sxs-lookup"><span data-stu-id="50b7d-129">PARAMETERS</span></span>

### <span data-ttu-id="50b7d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b7d-130">-DefaultProfile</span></span>
<span data-ttu-id="50b7d-131">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="50b7d-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50b7d-132">-最新發佈</span><span class="sxs-lookup"><span data-stu-id="50b7d-132">-LatestPublished</span></span>
<span data-ttu-id="50b7d-133">最新發佈的藍圖定義標標。</span><span class="sxs-lookup"><span data-stu-id="50b7d-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="50b7d-134">設定完成時，執行會返回最新發佈的藍圖定義版本。</span><span class="sxs-lookup"><span data-stu-id="50b7d-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="50b7d-135">預設值為 False。</span><span class="sxs-lookup"><span data-stu-id="50b7d-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50b7d-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="50b7d-136">-ManagementGroupId</span></span>
<span data-ttu-id="50b7d-137">儲存藍圖定義的管理組識別碼。</span><span class="sxs-lookup"><span data-stu-id="50b7d-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50b7d-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="50b7d-138">-Name</span></span>
<span data-ttu-id="50b7d-139">藍圖定義名稱。</span><span class="sxs-lookup"><span data-stu-id="50b7d-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50b7d-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="50b7d-140">-SubscriptionId</span></span>
<span data-ttu-id="50b7d-141">儲存藍圖定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="50b7d-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50b7d-142">-版本</span><span class="sxs-lookup"><span data-stu-id="50b7d-142">-Version</span></span>
<span data-ttu-id="50b7d-143">已發佈的藍圖定義版本。</span><span class="sxs-lookup"><span data-stu-id="50b7d-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50b7d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b7d-144">CommonParameters</span></span>
<span data-ttu-id="50b7d-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="50b7d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b7d-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50b7d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b7d-147">輸入</span><span class="sxs-lookup"><span data-stu-id="50b7d-147">INPUTS</span></span>

### <span data-ttu-id="50b7d-148">System.String</span><span class="sxs-lookup"><span data-stu-id="50b7d-148">System.String</span></span>

## <span data-ttu-id="50b7d-149">輸出</span><span class="sxs-lookup"><span data-stu-id="50b7d-149">OUTPUTS</span></span>

### <span data-ttu-id="50b7d-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="50b7d-150">System.Object</span></span>
## <span data-ttu-id="50b7d-151">筆記</span><span class="sxs-lookup"><span data-stu-id="50b7d-151">NOTES</span></span>

## <span data-ttu-id="50b7d-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="50b7d-152">RELATED LINKS</span></span>
