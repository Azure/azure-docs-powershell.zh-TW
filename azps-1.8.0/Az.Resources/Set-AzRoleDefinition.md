---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: 0ea0c0345bc57a7b1bd5c0c4cf67d6bd400542be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620748"
---
# <span data-ttu-id="28bd2-101">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="28bd2-101">Set-AzRoleDefinition</span></span>

## <span data-ttu-id="28bd2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28bd2-102">SYNOPSIS</span></span>
<span data-ttu-id="28bd2-103">修改 Azure RBAC 中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="28bd2-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="28bd2-104">以 JSON 檔案或 PSRoleDefinition 的形式提供已修改的角色定義。</span><span class="sxs-lookup"><span data-stu-id="28bd2-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="28bd2-105">首先，請使用 Get-AzRoleDefinition 命令來檢索您要修改的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="28bd2-105">First, use the Get-AzRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="28bd2-106">然後，修改您想要變更的屬性。</span><span class="sxs-lookup"><span data-stu-id="28bd2-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="28bd2-107">最後，使用此命令儲存角色定義。</span><span class="sxs-lookup"><span data-stu-id="28bd2-107">Finally, save the role definition using this command.</span></span>

## <span data-ttu-id="28bd2-108">句法</span><span class="sxs-lookup"><span data-stu-id="28bd2-108">SYNTAX</span></span>

### <span data-ttu-id="28bd2-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="28bd2-109">InputFileParameterSet</span></span>
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28bd2-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="28bd2-110">RoleDefinitionParameterSet</span></span>
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28bd2-111">說明</span><span class="sxs-lookup"><span data-stu-id="28bd2-111">DESCRIPTION</span></span>
<span data-ttu-id="28bd2-112">Set-AzRoleDefinition Cmdlet 會更新 Azure Role-Based 存取控制中現有的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="28bd2-112">The Set-AzRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="28bd2-113">以 JSON 檔案或 PSRoleDefinition 物件的形式，提供更新的角色定義做為命令的輸入。</span><span class="sxs-lookup"><span data-stu-id="28bd2-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="28bd2-114">已更新的自訂角色的角色定義必須包含該角色的識別碼及所有其他必要屬性，即使它們未更新： DisplayName、Description、動作、AssignableScopes。</span><span class="sxs-lookup"><span data-stu-id="28bd2-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="28bd2-115">NotActions、DataActions、NotDataActions 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="28bd2-115">NotActions, DataActions, NotDataActions are optional.</span></span>
<span data-ttu-id="28bd2-116">下列是 Set-AzRoleDefinition {"Id"： "52a6cc13-ff92-47a8-a39b-2a8205c3087e"、"Name"： "已更新的角色"、"描述"： "可以監視所有資源及啟動及重新開機虛擬機器的樣本更新：" \[ */read "，" Microsoft. ClassicCompute/virtualmachines/restart/動作 "，" \] NotActions "： \[ "* /write " \] ，" DataActions "： \[ " microsoft. Storage/storageAccounts/blobServices/容器/blob/讀取 " \] ，" NotDataActions "：" ClassicCompute " \[ \] ，" storageAccounts "： \[ " blobServices " \] }</span><span class="sxs-lookup"><span data-stu-id="28bd2-116">Following is a sample updated role definition json for Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="28bd2-117">示例</span><span class="sxs-lookup"><span data-stu-id="28bd2-117">EXAMPLES</span></span>

### <span data-ttu-id="28bd2-118">使用 PSRoleDefinitionObject 更新</span><span class="sxs-lookup"><span data-stu-id="28bd2-118">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### <span data-ttu-id="28bd2-119">使用 JSON 檔案建立</span><span class="sxs-lookup"><span data-stu-id="28bd2-119">Create using JSON file</span></span>
```
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="28bd2-120">參數</span><span class="sxs-lookup"><span data-stu-id="28bd2-120">PARAMETERS</span></span>

### <span data-ttu-id="28bd2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28bd2-121">-DefaultProfile</span></span>
<span data-ttu-id="28bd2-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="28bd2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28bd2-123">-InputFile</span><span class="sxs-lookup"><span data-stu-id="28bd2-123">-InputFile</span></span>
<span data-ttu-id="28bd2-124">包含要更新之單一 json 角色定義的檔案名。</span><span class="sxs-lookup"><span data-stu-id="28bd2-124">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="28bd2-125">只包含要在 JSON 中更新的屬性。</span><span class="sxs-lookup"><span data-stu-id="28bd2-125">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="28bd2-126">必須提供識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="28bd2-126">Id property is Required.</span></span>

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

### <span data-ttu-id="28bd2-127">-角色</span><span class="sxs-lookup"><span data-stu-id="28bd2-127">-Role</span></span>
<span data-ttu-id="28bd2-128">角色定義物件要更新</span><span class="sxs-lookup"><span data-stu-id="28bd2-128">Role definition object to be updated</span></span>

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

### <span data-ttu-id="28bd2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28bd2-129">CommonParameters</span></span>
<span data-ttu-id="28bd2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28bd2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28bd2-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28bd2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28bd2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="28bd2-132">INPUTS</span></span>

### <span data-ttu-id="28bd2-133">PSRoleDefinition 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="28bd2-133">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="28bd2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="28bd2-134">OUTPUTS</span></span>

### <span data-ttu-id="28bd2-135">PSRoleDefinition 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="28bd2-135">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="28bd2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="28bd2-136">NOTES</span></span>
<span data-ttu-id="28bd2-137">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="28bd2-137">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="28bd2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="28bd2-138">RELATED LINKS</span></span>

[<span data-ttu-id="28bd2-139">AzProviderOperation</span><span class="sxs-lookup"><span data-stu-id="28bd2-139">Get-AzProviderOperation</span></span>](./Get-AzProviderOperation.md)

[<span data-ttu-id="28bd2-140">AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="28bd2-140">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="28bd2-141">新-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="28bd2-141">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="28bd2-142">移除-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="28bd2-142">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)
