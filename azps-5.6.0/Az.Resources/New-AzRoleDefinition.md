---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 0930b66cf12d9c96d4fe00fa823cfd67c87081f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907537"
---
# <span data-ttu-id="19e99-101">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="19e99-101">New-AzRoleDefinition</span></span>

## <span data-ttu-id="19e99-102">簡介</span><span class="sxs-lookup"><span data-stu-id="19e99-102">SYNOPSIS</span></span>
<span data-ttu-id="19e99-103">在 Azure RBAC 中建立自訂角色。</span><span class="sxs-lookup"><span data-stu-id="19e99-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="19e99-104">提供 JSON 角色定義檔案或 PSRoleDefinition 物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="19e99-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="19e99-105">首先，使用 Get-AzRoleDefinition 命令來產生比較基準角色定義物件。</span><span class="sxs-lookup"><span data-stu-id="19e99-105">First, use the Get-AzRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="19e99-106">然後，根據需要修改其屬性。</span><span class="sxs-lookup"><span data-stu-id="19e99-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="19e99-107">最後，使用此命令使用角色定義來建立自訂角色。</span><span class="sxs-lookup"><span data-stu-id="19e99-107">Finally, use this command to create a custom role using role definition.</span></span>

## <span data-ttu-id="19e99-108">語法</span><span class="sxs-lookup"><span data-stu-id="19e99-108">SYNTAX</span></span>

### <span data-ttu-id="19e99-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="19e99-109">InputFileParameterSet</span></span>
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19e99-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="19e99-110">RoleDefinitionParameterSet</span></span>
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19e99-111">描述</span><span class="sxs-lookup"><span data-stu-id="19e99-111">DESCRIPTION</span></span>
<span data-ttu-id="19e99-112">Cmdlet New-AzRoleDefinition在 Azure 中建立自訂角色Role-Based存取控制。</span><span class="sxs-lookup"><span data-stu-id="19e99-112">The New-AzRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="19e99-113">提供角色定義做為 JSON 檔案或 PSRoleDefinition 物件的命令輸入。</span><span class="sxs-lookup"><span data-stu-id="19e99-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="19e99-114">輸入角色定義必須包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="19e99-114">The input role definition MUST contain the following properties:</span></span>
1) <span data-ttu-id="19e99-115">DisplayName：自訂角色的名稱</span><span class="sxs-lookup"><span data-stu-id="19e99-115">DisplayName: the name of the custom role</span></span>
2) <span data-ttu-id="19e99-116">描述：角色的簡短描述，摘要說明角色授予的存取權。</span><span class="sxs-lookup"><span data-stu-id="19e99-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>
3) <span data-ttu-id="19e99-117">動作：自訂角色授予存取權的操作集。</span><span class="sxs-lookup"><span data-stu-id="19e99-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="19e99-118">使用Get-AzProviderOperation取得 Azure 資源提供者的作業，這些提供者可以使用 Azure RBAC 進行安全保護。</span><span class="sxs-lookup"><span data-stu-id="19e99-118">Use Get-AzProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="19e99-119">以下是一些有效的運算字串：</span><span class="sxs-lookup"><span data-stu-id="19e99-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="19e99-120">"\*/read" 會授予所有 Azure 資源提供者讀取作業的存取權。</span><span class="sxs-lookup"><span data-stu-id="19e99-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="19e99-121">"Microsoft.Network/\*/read" 會授予 Azure Microsoft.Network 資源提供者中所有資源類型讀取作業的存取權。</span><span class="sxs-lookup"><span data-stu-id="19e99-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="19e99-122">「Microsoft.Compute/virtualMachines/\*」會授予虛擬機器及其子資源類型之所有作業的存取權。</span><span class="sxs-lookup"><span data-stu-id="19e99-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>
4) <span data-ttu-id="19e99-123">可指派的Scope：Azure 訂閱 (或資源群組) 自訂角色可供指派的一組範圍。</span><span class="sxs-lookup"><span data-stu-id="19e99-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="19e99-124">您可以使用 AssignableScopes，讓自訂角色僅可供需要指派的訂閱或資源群組使用，而且不會干擾其餘的訂閱或資源群組的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="19e99-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="19e99-125">以下是一些有效的可指派範圍：</span><span class="sxs-lookup"><span data-stu-id="19e99-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="19e99-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e"， "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624"：讓角色可在兩個訂閱中指派。</span><span class="sxs-lookup"><span data-stu-id="19e99-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="19e99-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e"：讓角色可在單一訂閱中指派。</span><span class="sxs-lookup"><span data-stu-id="19e99-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="19e99-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network"：讓角色只能在網路資源群組中指派。</span><span class="sxs-lookup"><span data-stu-id="19e99-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>
<span data-ttu-id="19e99-129">輸入角色定義可能包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="19e99-129">The input role definition MAY contain the following properties:</span></span>
1) <span data-ttu-id="19e99-130">NotActions：您必須從動作排除的作業集，以決定自訂角色的有效動作。</span><span class="sxs-lookup"><span data-stu-id="19e99-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="19e99-131">如果您不想將自訂角色的存取權授予特定作業，使用 NotActions 來排除該作業並不方便，而不是在動作中指定該特定作業外的所有作業。</span><span class="sxs-lookup"><span data-stu-id="19e99-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="19e99-132">DataActions：自訂角色授予存取權的資料作業集。</span><span class="sxs-lookup"><span data-stu-id="19e99-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="19e99-133">NotDataActions：一組必須排除在 DataActions 中的作業，以決定自訂角色的有效資料動作。</span><span class="sxs-lookup"><span data-stu-id="19e99-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective data actions for the custom role.</span></span>
<span data-ttu-id="19e99-134">如果您不想將自訂角色的存取權授予特定資料作業，使用 NotDataActions 來排除它，而不是在動作中指定該特定作業外的所有作業，是方便的。</span><span class="sxs-lookup"><span data-stu-id="19e99-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
<span data-ttu-id="19e99-135">注意：如果使用者獲指派角色，指定 NotActions 中的作業，同時指派另一個角色以授予相同作業的存取權，使用者將可以執行該作業。</span><span class="sxs-lookup"><span data-stu-id="19e99-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="19e99-136">NotActions 不是拒絕規則，只要排除特定作業，它就是建立一組允許作業的便利方式。</span><span class="sxs-lookup"><span data-stu-id="19e99-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>
<span data-ttu-id="19e99-137">以下是範例 json 角色定義，可做為輸入 { "Name"： "Updated Role"， "Description"： "Can monitor all resources and start and restart virtual machines"， "Actions"： \[ "*/read"， "Microsoft.ClassicCompute/virtualmachines/restart/action"， "Microsoft.ClassicCompute/virtualmachines/start/action" \] ， "NotActions"： \[ "*/write" \] ， "DataActions"： \[ "Microsoft.storage/storageAccounts/blobServices/containers/blobs/read" \] ， "NotDataActions"： \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] ， "AssignableScopes"： \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="19e99-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="19e99-138">例子</span><span class="sxs-lookup"><span data-stu-id="19e99-138">EXAMPLES</span></span>

### <span data-ttu-id="19e99-139">範例 1：使用 PSRoleDefinitionObject 建立</span><span class="sxs-lookup"><span data-stu-id="19e99-139">Example 1: Create using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### <span data-ttu-id="19e99-140">範例 2：使用 JSON 檔案建立</span><span class="sxs-lookup"><span data-stu-id="19e99-140">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="19e99-141">參數</span><span class="sxs-lookup"><span data-stu-id="19e99-141">PARAMETERS</span></span>

### <span data-ttu-id="19e99-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19e99-142">-DefaultProfile</span></span>
<span data-ttu-id="19e99-143">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="19e99-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19e99-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="19e99-144">-InputFile</span></span>
<span data-ttu-id="19e99-145">包含單一 json 角色定義的檔案名。</span><span class="sxs-lookup"><span data-stu-id="19e99-145">File name containing a single json role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e99-146">-角色</span><span class="sxs-lookup"><span data-stu-id="19e99-146">-Role</span></span>
<span data-ttu-id="19e99-147">角色定義物件。</span><span class="sxs-lookup"><span data-stu-id="19e99-147">Role definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19e99-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19e99-148">CommonParameters</span></span>
<span data-ttu-id="19e99-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="19e99-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19e99-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19e99-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19e99-151">輸入</span><span class="sxs-lookup"><span data-stu-id="19e99-151">INPUTS</span></span>

### <span data-ttu-id="19e99-152">沒有</span><span class="sxs-lookup"><span data-stu-id="19e99-152">None</span></span>

## <span data-ttu-id="19e99-153">輸出</span><span class="sxs-lookup"><span data-stu-id="19e99-153">OUTPUTS</span></span>

### <span data-ttu-id="19e99-154">Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="19e99-154">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="19e99-155">筆記</span><span class="sxs-lookup"><span data-stu-id="19e99-155">NOTES</span></span>
<span data-ttu-id="19e99-156">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="19e99-156">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="19e99-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="19e99-157">RELATED LINKS</span></span>

[<span data-ttu-id="19e99-158">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="19e99-158">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="19e99-159">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="19e99-159">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="19e99-160">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="19e99-160">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

[<span data-ttu-id="19e99-161">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="19e99-161">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

