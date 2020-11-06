---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmRoleDefinition.md
ms.openlocfilehash: 79b1c647e192e3ce093c084ef89cf8535468727e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447667"
---
# <span data-ttu-id="1b4c1-101">New-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b4c1-101">New-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="1b4c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b4c1-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4c1-103">在 Azure RBAC 中建立自訂角色。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-103">Creates a custom role in Azure RBAC.</span></span>
<span data-ttu-id="1b4c1-104">提供 JSON 角色定義檔案或 PSRoleDefinition 物件做為輸入。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-104">Provide either a JSON role definition file or a PSRoleDefinition object as input.</span></span>
<span data-ttu-id="1b4c1-105">首先，請使用 Get-AzureRmRoleDefinition 命令來產生比較基準角色定義物件。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-105">First, use the Get-AzureRmRoleDefinition command to generate a baseline role definition object.</span></span>
<span data-ttu-id="1b4c1-106">然後，根據需要修改其屬性。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-106">Then, modify its properties as required.</span></span>
<span data-ttu-id="1b4c1-107">最後，使用此命令來建立使用角色定義的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-107">Finally, use this command to create a custom role using role definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b4c1-108">句法</span><span class="sxs-lookup"><span data-stu-id="1b4c1-108">SYNTAX</span></span>

### <span data-ttu-id="1b4c1-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b4c1-109">InputFileParameterSet</span></span>
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b4c1-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b4c1-110">RoleDefinitionParameterSet</span></span>
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b4c1-111">說明</span><span class="sxs-lookup"><span data-stu-id="1b4c1-111">DESCRIPTION</span></span>
<span data-ttu-id="1b4c1-112">New-AzureRmRoleDefinition Cmdlet 會在 Azure Role-Based 存取控制中建立自訂角色。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-112">The New-AzureRmRoleDefinition cmdlet creates a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="1b4c1-113">以 JSON 檔案或 PSRoleDefinition 物件的形式，提供角色定義做為命令的輸入。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-113">Provide a role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>

<span data-ttu-id="1b4c1-114">輸入角色定義必須包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="1b4c1-114">The input role definition MUST contain the following properties:</span></span>

1) <span data-ttu-id="1b4c1-115">DisplayName：自訂角色的名稱</span><span class="sxs-lookup"><span data-stu-id="1b4c1-115">DisplayName: the name of the custom role</span></span>

2) <span data-ttu-id="1b4c1-116">描述：總結角色所准許之存取權的角色簡短描述。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-116">Description: a short description of the role that summarizes the access that the role grants.</span></span>

3) <span data-ttu-id="1b4c1-117">動作：自訂角色准許存取的一組作業。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-117">Actions: the set of operations to which the custom role grants access.</span></span>
<span data-ttu-id="1b4c1-118">使用 Get-AzureRmProviderOperation 來取得可使用 Azure RBAC 加以保護的 Azure 資源提供者作業。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-118">Use Get-AzureRmProviderOperation to get the operation for Azure resource providers that can be secured using Azure RBAC.</span></span>
<span data-ttu-id="1b4c1-119">以下是一些有效的操作字串：</span><span class="sxs-lookup"><span data-stu-id="1b4c1-119">Following are some valid operation strings:</span></span>
 - <span data-ttu-id="1b4c1-120">"\*/read" 授與所有 Azure 資源提供者讀取作業的存取權。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-120">"\*/read" grants access to read operations of all Azure resource providers.</span></span>
 - <span data-ttu-id="1b4c1-121">"Microsoft. Network/\*/read" 會針對 Microsoft. Azure 的網路資源提供者中的所有資源類型，授予讀取作業的存取權。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-121">"Microsoft.Network/\*/read" grants access to read operations for all resource types in the Microsoft.Network resource provider of Azure.</span></span>
 - <span data-ttu-id="1b4c1-122">"Microsoft. Compute/virtualMachines/\*" 授與所有虛擬機器及其子資源類型的所有作業的存取權。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-122">"Microsoft.Compute/virtualMachines/\*" grants access to all operations of virtual machines and its child resource types.</span></span>

4) <span data-ttu-id="1b4c1-123">AssignableScopes：一組作用域 (Azure 訂閱或資源群組) ，自訂角色就可供作業。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-123">AssignableScopes: the set of scopes (Azure subscriptions or resource groups) in which the custom role will be available for assignment.</span></span>
<span data-ttu-id="1b4c1-124">您可以使用 AssignableScopes，讓自訂角色只能在所需的訂閱或資源群組中使用，而不會打亂其餘訂閱或資源群組的使用者經驗。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-124">Using AssignableScopes you can make the custom role available for assignment in only the subscriptions or resource groups that need it, and not clutter the user experience for the rest of the subscriptions or resource groups.</span></span>
<span data-ttu-id="1b4c1-125">下列是一些有效的可賦值範圍：</span><span class="sxs-lookup"><span data-stu-id="1b4c1-125">Following are some valid assignable scopes:</span></span>
 - <span data-ttu-id="1b4c1-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e"，"/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624"：使角色可用於兩個訂閱中的作業。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-126">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": makes the role available for assignment in two subscriptions.</span></span>
 - <span data-ttu-id="1b4c1-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e"：使角色可在單一訂閱中供作業。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-127">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": makes the role available for assignment in a single subscription.</span></span>
 - <span data-ttu-id="1b4c1-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network"：使角色只能在 [網路資源] 群組中供作業使用。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-128">"/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": makes the role available for assignment only in the Network resource group.</span></span>

<span data-ttu-id="1b4c1-129">輸入角色定義可能會包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="1b4c1-129">The input role definition MAY contain the following properties:</span></span>

1) <span data-ttu-id="1b4c1-130">NotActions：必須從動作中排除的一組作業，才能判斷自訂角色的有效動作。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-130">NotActions: the set of operations that must be excluded from the Actions to determine the effective actions for the custom role.</span></span>
<span data-ttu-id="1b4c1-131">如果您不想在自訂角色中授與存取權，您可以使用 NotActions 排除它，而不是在動作中指定該特定操作以外的所有作業。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-131">If there is a specific operation that you do not wish to grant access to in a custom role, it is convenient to use NotActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>
2) <span data-ttu-id="1b4c1-132">DataActions：自訂角色准許存取權的資料作業集合。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-132">DataActions: the set of data operations to which the custom role grants access.</span></span>
3) <span data-ttu-id="1b4c1-133">NotDataActions：必須排除在 DataActions 中的一組作業，才能判斷自訂角色的有效 DataActions。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-133">NotDataActions: the set of operations that must be excluded from the DataActions to determine the effective dataactions for the custom role.</span></span>
<span data-ttu-id="1b4c1-134">如果您不想要在自訂角色中授與存取權的特定資料作業，請使用 NotDataActions 排除它，而不是在動作中指定該特定操作以外的所有作業。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-134">If there is a specific data operation that you do not wish to grant access to in a custom role, it is convenient to use NotDataActions to exclude it, rather than specifying all operations other than that specific operation in Actions.</span></span>

<span data-ttu-id="1b4c1-135">注意：如果指派給使用者的角色指定了 NotActions 中的某個作業，而且指派另一個角色授與同一個操作的存取權，使用者就可以執行該作業。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-135">NOTE: If a user is assigned a role that specifies an operation in NotActions and also assigned another role grants access to the same operation - the user will be able to perform that operation.</span></span>
<span data-ttu-id="1b4c1-136">NotActions 不是 deny 規則，這只是在需要排除特定作業時，可以輕鬆建立一組允許的作業的簡單方式。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-136">NotActions is not a deny rule - it is simply a convenient way to create a set of allowed operations when specific operations need to be excluded.</span></span>

<span data-ttu-id="1b4c1-137">下列是可提供為輸入 {"Name" 的範例 json 角色定義： "Description"： "可以監視所有資源，並啟動及重新開機虛擬機器"，"操作"： \[ " */read"，"Microsoft. ClassicCompute/virtualmachines/restart/動作"，" \] NotActions"： \[ "* /write" \] ，"DataActions"： \[ "microsoft. Storage/storageAccounts/blobServices/容器/blob/讀取" \] ，"NotDataActions"： "ClassicCompute" \[ \] ，"storageAccounts"： \[ "blobServices" \] }</span><span class="sxs-lookup"><span data-stu-id="1b4c1-137">Following is a sample json role definition that can be provided as input { "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="1b4c1-138">示例</span><span class="sxs-lookup"><span data-stu-id="1b4c1-138">EXAMPLES</span></span>

### <span data-ttu-id="1b4c1-139">使用 PSRoleDefinitionObject 建立</span><span class="sxs-lookup"><span data-stu-id="1b4c1-139">Create using PSRoleDefinitionObject</span></span>
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
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

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### <span data-ttu-id="1b4c1-140">使用 JSON 檔案建立</span><span class="sxs-lookup"><span data-stu-id="1b4c1-140">Create using JSON file</span></span>
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="1b4c1-141">參數</span><span class="sxs-lookup"><span data-stu-id="1b4c1-141">PARAMETERS</span></span>

### <span data-ttu-id="1b4c1-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b4c1-142">-DefaultProfile</span></span>
<span data-ttu-id="1b4c1-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1b4c1-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b4c1-144">-InputFile</span><span class="sxs-lookup"><span data-stu-id="1b4c1-144">-InputFile</span></span>
<span data-ttu-id="1b4c1-145">包含單一 json 角色定義的檔案名。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-145">File name containing a single json role definition.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4c1-146">-角色</span><span class="sxs-lookup"><span data-stu-id="1b4c1-146">-Role</span></span>
<span data-ttu-id="1b4c1-147">角色定義物件。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-147">Role definition object.</span></span>

```yaml
Type: PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b4c1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4c1-148">CommonParameters</span></span>
<span data-ttu-id="1b4c1-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b4c1-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4c1-151">輸入</span><span class="sxs-lookup"><span data-stu-id="1b4c1-151">INPUTS</span></span>

### <span data-ttu-id="1b4c1-152">所有</span><span class="sxs-lookup"><span data-stu-id="1b4c1-152">None</span></span>
<span data-ttu-id="1b4c1-153">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="1b4c1-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b4c1-154">輸出</span><span class="sxs-lookup"><span data-stu-id="1b4c1-154">OUTPUTS</span></span>

### <span data-ttu-id="1b4c1-155">PSRoleDefinition 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="1b4c1-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="1b4c1-156">筆記</span><span class="sxs-lookup"><span data-stu-id="1b4c1-156">NOTES</span></span>
<span data-ttu-id="1b4c1-157">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="1b4c1-157">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="1b4c1-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b4c1-158">RELATED LINKS</span></span>

[<span data-ttu-id="1b4c1-159">AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="1b4c1-159">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="1b4c1-160">AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b4c1-160">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="1b4c1-161">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b4c1-161">Set-AzureRmRoleDefinition</span></span>](./Set-AzureRmRoleDefinition.md)

[<span data-ttu-id="1b4c1-162">移除-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="1b4c1-162">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

