---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: ab383b1fb46759c2369d94d4bb57284ba59cf671
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137560"
---
# <span data-ttu-id="fe79a-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="fe79a-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="fe79a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fe79a-102">SYNOPSIS</span></span>
<span data-ttu-id="fe79a-103">取得一或多個藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="fe79a-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="fe79a-104">句法</span><span class="sxs-lookup"><span data-stu-id="fe79a-104">SYNTAX</span></span>

### <span data-ttu-id="fe79a-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="fe79a-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe79a-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="fe79a-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe79a-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="fe79a-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe79a-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="fe79a-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fe79a-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="fe79a-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe79a-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="fe79a-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe79a-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="fe79a-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe79a-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="fe79a-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe79a-113">說明</span><span class="sxs-lookup"><span data-stu-id="fe79a-113">DESCRIPTION</span></span>
<span data-ttu-id="fe79a-114">取得一或多個藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="fe79a-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="fe79a-115">[管理] 群組或 [訂閱] 範圍中存在藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="fe79a-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="fe79a-116">示例</span><span class="sxs-lookup"><span data-stu-id="fe79a-116">EXAMPLES</span></span>

### <span data-ttu-id="fe79a-117">範例1</span><span class="sxs-lookup"><span data-stu-id="fe79a-117">Example 1</span></span>
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

<span data-ttu-id="fe79a-118">在目前的訂閱和訂閱的管理群組階層中取得藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="fe79a-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="fe79a-119">範例2</span><span class="sxs-lookup"><span data-stu-id="fe79a-119">Example 2</span></span>
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

<span data-ttu-id="fe79a-120">在指定的管理群組中取得藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="fe79a-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="fe79a-121">範例3</span><span class="sxs-lookup"><span data-stu-id="fe79a-121">Example 3</span></span>
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

<span data-ttu-id="fe79a-122">在指定的訂閱和訂閱的管理群組階層中取得藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="fe79a-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="fe79a-123">範例4</span><span class="sxs-lookup"><span data-stu-id="fe79a-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="fe79a-124">在指定的訂閱中取得具有指定名稱的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="fe79a-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="fe79a-125">範例5</span><span class="sxs-lookup"><span data-stu-id="fe79a-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="fe79a-126">在指定的管理群組中，以指定的名稱和版本來取得藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="fe79a-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="fe79a-127">範例6</span><span class="sxs-lookup"><span data-stu-id="fe79a-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="fe79a-128">在指定的管理群組中取得具有指定名稱的最新發佈藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="fe79a-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="fe79a-129">參數</span><span class="sxs-lookup"><span data-stu-id="fe79a-129">PARAMETERS</span></span>

### <span data-ttu-id="fe79a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe79a-130">-DefaultProfile</span></span>
<span data-ttu-id="fe79a-131">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fe79a-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe79a-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="fe79a-132">-LatestPublished</span></span>
<span data-ttu-id="fe79a-133">最近發佈的藍圖定義標誌。</span><span class="sxs-lookup"><span data-stu-id="fe79a-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="fe79a-134">設定時，執行會傳回藍圖定義的最新發行版本本。</span><span class="sxs-lookup"><span data-stu-id="fe79a-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="fe79a-135">預設值為 false。</span><span class="sxs-lookup"><span data-stu-id="fe79a-135">Defaults to false.</span></span>

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

### <span data-ttu-id="fe79a-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="fe79a-136">-ManagementGroupId</span></span>
<span data-ttu-id="fe79a-137">儲存藍圖定義的管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe79a-137">Management Group Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="fe79a-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="fe79a-138">-Name</span></span>
<span data-ttu-id="fe79a-139">藍圖定義名稱。</span><span class="sxs-lookup"><span data-stu-id="fe79a-139">Blueprint definition name.</span></span>

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

### <span data-ttu-id="fe79a-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fe79a-140">-SubscriptionId</span></span>
<span data-ttu-id="fe79a-141">儲存藍圖定義的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="fe79a-141">Subscription Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="fe79a-142">-版本</span><span class="sxs-lookup"><span data-stu-id="fe79a-142">-Version</span></span>
<span data-ttu-id="fe79a-143">已發佈藍圖定義版本。</span><span class="sxs-lookup"><span data-stu-id="fe79a-143">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="fe79a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe79a-144">CommonParameters</span></span>
<span data-ttu-id="fe79a-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fe79a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe79a-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fe79a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe79a-147">輸入</span><span class="sxs-lookup"><span data-stu-id="fe79a-147">INPUTS</span></span>

### <span data-ttu-id="fe79a-148">System.object</span><span class="sxs-lookup"><span data-stu-id="fe79a-148">System.String</span></span>

## <span data-ttu-id="fe79a-149">輸出</span><span class="sxs-lookup"><span data-stu-id="fe79a-149">OUTPUTS</span></span>

### <span data-ttu-id="fe79a-150">System.object</span><span class="sxs-lookup"><span data-stu-id="fe79a-150">System.Object</span></span>
## <span data-ttu-id="fe79a-151">筆記</span><span class="sxs-lookup"><span data-stu-id="fe79a-151">NOTES</span></span>

## <span data-ttu-id="fe79a-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="fe79a-152">RELATED LINKS</span></span>
