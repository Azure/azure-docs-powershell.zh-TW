---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 18488b44ff99c44d6362de68de45e81853418e0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906862"
---
# <span data-ttu-id="f9833-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f9833-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="f9833-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f9833-102">SYNOPSIS</span></span>
<span data-ttu-id="f9833-103">修改 Azure RBAC 中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="f9833-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="f9833-104">以 JSON 檔案或 PSRoleDefinition 提供修改後的角色定義。</span><span class="sxs-lookup"><span data-stu-id="f9833-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="f9833-105">首先，使用 Get-AzRoleDefinition 命令來取回要修改的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="f9833-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="f9833-106">然後，修改要變更的屬性。</span><span class="sxs-lookup"><span data-stu-id="f9833-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="f9833-107">最後，使用此命令儲存角色定義。</span><span class="sxs-lookup"><span data-stu-id="f9833-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="f9833-108">語法</span><span class="sxs-lookup"><span data-stu-id="f9833-108">SYNTAX</span></span>

### <span data-ttu-id="f9833-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9833-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9833-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9833-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9833-111">描述</span><span class="sxs-lookup"><span data-stu-id="f9833-111">DESCRIPTION</span></span>
<span data-ttu-id="f9833-112">此Set-AzRoleDefinition Cmdlet 會更新 Azure 中現有的自訂角色Role-Based存取控制。</span><span class="sxs-lookup"><span data-stu-id="f9833-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="f9833-113">以 JSON 檔案或 PSRoleDefinition 物件提供更新的角色定義做為命令的輸入。</span><span class="sxs-lookup"><span data-stu-id="f9833-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="f9833-114">更新的自訂角色角色定義必須包含該角色的識別碼和所有其他必要的屬性，即使尚未更新：DisplayName、描述、動作、AssignableScopes。</span><span class="sxs-lookup"><span data-stu-id="f9833-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="f9833-115">NotActions、DataActions、NotDataActions 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f9833-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="f9833-116">以下是適用于 Set-AzRoleDefinition { "Id"的範例更新角色定義 json："52a6cc13-ff92-47a8-a39b-2a8205c3087e"， "Name"： "Updated Role"， "Description"： "Can monitor all resources and start and restart 虛擬機器"， "Action"： \[ "*/read"， "Microsoft.ClassicCompute/virtualmachines/restart/action"， "Microsoft.ClassicCompute/virtualmachines/start/action" \] ， "NotActions"： \[ "*/write" \] ， "DataActions"： \[ "Microsoft.storage/storageAccounts/blobServices/containers/blobs/read" \] ， "NotDataActions"： \[ "Microsoft.Storage/storage"Accounts/blobServices/containers/blobs/write" \] ， "AssignableScopes"： \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }</span><span class="sxs-lookup"><span data-stu-id="f9833-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "*/write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="f9833-117">例子</span><span class="sxs-lookup"><span data-stu-id="f9833-117">EXAMPLES</span></span>

### <span data-ttu-id="f9833-118">範例 1：使用 PSRoleDefinitionObject 更新</span><span class="sxs-lookup"><span data-stu-id="f9833-118">Example 1: Update using PSRoleDefinitionObject</span></span>
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="f9833-119">範例 2：使用 JSON 檔案建立</span><span class="sxs-lookup"><span data-stu-id="f9833-119">Example 2: Create using JSON file</span></span>
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="f9833-120">參數</span><span class="sxs-lookup"><span data-stu-id="f9833-120">PARAMETERS</span></span>

### <span data-ttu-id="f9833-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9833-121">-DefaultProfile</span></span>
<span data-ttu-id="f9833-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f9833-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9833-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f9833-123">-InputFile</span></span>
<span data-ttu-id="f9833-124">包含要更新之單一 json 角色定義的檔案名。</span><span class="sxs-lookup"><span data-stu-id="f9833-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="f9833-125">只包含 JSON 中要更新的屬性。</span><span class="sxs-lookup"><span data-stu-id="f9833-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="f9833-126">Id 屬性為必填專案。</span><span class="sxs-lookup"><span data-stu-id="f9833-126">Id property is Required.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9833-127">-角色</span><span class="sxs-lookup"><span data-stu-id="f9833-127">-Role</span></span>
<span data-ttu-id="f9833-128">要更新的角色定義物件</span><span class="sxs-lookup"><span data-stu-id="f9833-128">Role definition object to be updated</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9833-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9833-129">CommonParameters</span></span>
<span data-ttu-id="f9833-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f9833-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9833-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9833-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9833-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f9833-132">INPUTS</span></span>

### <span data-ttu-id="f9833-133">Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f9833-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="f9833-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f9833-134">OUTPUTS</span></span>

### <span data-ttu-id="f9833-135">Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f9833-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="f9833-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f9833-136">NOTES</span></span>
<span data-ttu-id="f9833-137">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="f9833-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f9833-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9833-138">RELATED LINKS</span></span>

[<span data-ttu-id="f9833-139">Get-AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="f9833-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="f9833-140">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f9833-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="f9833-141">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f9833-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="f9833-142">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f9833-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

