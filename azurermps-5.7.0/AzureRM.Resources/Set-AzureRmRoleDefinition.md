---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 2282bdef70f6352caa535b4d7a68d5e4046f831e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444356"
---
# <span data-ttu-id="7716b-101">Set-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7716b-101">Set-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="7716b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7716b-102">SYNOPSIS</span></span>
<span data-ttu-id="7716b-103">修改 Azure RBAC 中的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="7716b-103">Modifies a custom role in Azure RBAC.</span></span>
<span data-ttu-id="7716b-104">以 JSON 檔案或 PSRoleDefinition 的形式提供已修改的角色定義。</span><span class="sxs-lookup"><span data-stu-id="7716b-104">Provide the modified role definition either as a JSON file or as a PSRoleDefinition.</span></span>
<span data-ttu-id="7716b-105">首先，請使用 Get-AzureRmRoleDefinition 命令來檢索您要修改的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="7716b-105">First, use the Get-AzureRmRoleDefinition command to retrieve the custom role that you wish to modify.</span></span>
<span data-ttu-id="7716b-106">然後，修改您想要變更的屬性。</span><span class="sxs-lookup"><span data-stu-id="7716b-106">Then, modify the properties that you wish to change.</span></span>
<span data-ttu-id="7716b-107">最後，使用此命令儲存角色定義。</span><span class="sxs-lookup"><span data-stu-id="7716b-107">Finally, save the role definition using this command.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7716b-108">句法</span><span class="sxs-lookup"><span data-stu-id="7716b-108">SYNTAX</span></span>

### <span data-ttu-id="7716b-109">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="7716b-109">InputFileParameterSet</span></span>
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7716b-110">RoleDefinitionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7716b-110">RoleDefinitionParameterSet</span></span>
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7716b-111">說明</span><span class="sxs-lookup"><span data-stu-id="7716b-111">DESCRIPTION</span></span>
<span data-ttu-id="7716b-112">Set-AzureRmRoleDefinition Cmdlet 會更新 Azure Role-Based 存取控制中現有的自訂角色。</span><span class="sxs-lookup"><span data-stu-id="7716b-112">The Set-AzureRmRoleDefinition cmdlet updates an existing custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="7716b-113">以 JSON 檔案或 PSRoleDefinition 物件的形式，提供更新的角色定義做為命令的輸入。</span><span class="sxs-lookup"><span data-stu-id="7716b-113">Provide the updated role definition as an input to the command as a JSON file or a PSRoleDefinition object.</span></span>
<span data-ttu-id="7716b-114">已更新的自訂角色的角色定義必須包含該角色的識別碼及所有其他必要屬性，即使它們未更新： DisplayName、Description、動作、AssignableScopes。</span><span class="sxs-lookup"><span data-stu-id="7716b-114">The role definition for the updated custom role MUST contain the Id and all other required properties of the role even if they are not updated: DisplayName, Description, Actions, AssignableScopes.</span></span>
<span data-ttu-id="7716b-115">NotActions、DataActions、NotDataActions 是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="7716b-115">NotActions, DataActions, NotDataActions are optional.</span></span>

<span data-ttu-id="7716b-116">下列是 Set-AzureRmRoleDefinition 的更新角色定義 json 範例</span><span class="sxs-lookup"><span data-stu-id="7716b-116">Following is a sample updated role definition json for Set-AzureRmRoleDefinition</span></span>

<span data-ttu-id="7716b-117">{"Id"： "52a6cc13-ff92-47a8-a39b-2a8205c3087e"，"Name"： "已更新的角色"，"描述"： "可以監視所有資源，並啟動及重新開機虛擬機器"，"動作"： \[ " */read"，"Microsoft. ClassicCompute/virtualmachines/restart/動作"，" \] NotActions"： \[ "* /Write" \] ，"DataActions"： \[ "Microsoft. Storage/storageAccounts/blobServices/容器/blob/讀取" \] ，"NotDataActions"： "ClassicCompute" \[ \] ，"storageAccounts"： \[ "blobServices" \] }</span><span class="sxs-lookup"><span data-stu-id="7716b-117">{ "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Updated Role", "Description": "Can monitor all resources and start and restart virtual machines", "Actions": \[ " */read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action" \], "NotActions": \[ "* /write" \], "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read" \], "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \], "AssignableScopes": \["/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"\] }</span></span>

## <span data-ttu-id="7716b-118">示例</span><span class="sxs-lookup"><span data-stu-id="7716b-118">EXAMPLES</span></span>

### <span data-ttu-id="7716b-119">使用 PSRoleDefinitionObject 更新</span><span class="sxs-lookup"><span data-stu-id="7716b-119">Update using PSRoleDefinitionObject</span></span>
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

          PS C:\> Set-AzureRmRoleDefinition -Role $roleDef
```

### <span data-ttu-id="7716b-120">使用 JSON 檔案建立</span><span class="sxs-lookup"><span data-stu-id="7716b-120">Create using JSON file</span></span>
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## <span data-ttu-id="7716b-121">參數</span><span class="sxs-lookup"><span data-stu-id="7716b-121">PARAMETERS</span></span>

### <span data-ttu-id="7716b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7716b-122">-DefaultProfile</span></span>
<span data-ttu-id="7716b-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7716b-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7716b-124">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7716b-124">-InputFile</span></span>
<span data-ttu-id="7716b-125">包含要更新之單一 json 角色定義的檔案名。</span><span class="sxs-lookup"><span data-stu-id="7716b-125">File name containing a single json role definition to be updated.</span></span>
<span data-ttu-id="7716b-126">只包含要在 JSON 中更新的屬性。</span><span class="sxs-lookup"><span data-stu-id="7716b-126">Only include the properties that are to be updated in the JSON.</span></span>
<span data-ttu-id="7716b-127">必須提供識別碼屬性。</span><span class="sxs-lookup"><span data-stu-id="7716b-127">Id property is Required.</span></span>

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7716b-128">-角色</span><span class="sxs-lookup"><span data-stu-id="7716b-128">-Role</span></span>
<span data-ttu-id="7716b-129">角色定義物件要更新</span><span class="sxs-lookup"><span data-stu-id="7716b-129">Role definition object to be updated</span></span>

```yaml
Type: PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7716b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7716b-130">CommonParameters</span></span>
<span data-ttu-id="7716b-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7716b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7716b-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7716b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7716b-133">輸入</span><span class="sxs-lookup"><span data-stu-id="7716b-133">INPUTS</span></span>

### <span data-ttu-id="7716b-134">PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7716b-134">PSRoleDefinition</span></span>
<span data-ttu-id="7716b-135">"Role" 是從管線接受類型 "PSRoleDefinition" 的值</span><span class="sxs-lookup"><span data-stu-id="7716b-135">Parameter 'Role' accepts value of type 'PSRoleDefinition' from the pipeline</span></span>

## <span data-ttu-id="7716b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="7716b-136">OUTPUTS</span></span>

### <span data-ttu-id="7716b-137">PSRoleDefinition 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="7716b-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="7716b-138">筆記</span><span class="sxs-lookup"><span data-stu-id="7716b-138">NOTES</span></span>
<span data-ttu-id="7716b-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="7716b-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7716b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="7716b-140">RELATED LINKS</span></span>

[<span data-ttu-id="7716b-141">AzureRmProviderOperation</span><span class="sxs-lookup"><span data-stu-id="7716b-141">Get-AzureRmProviderOperation</span></span>](./Get-AzureRmProviderOperation.md)

[<span data-ttu-id="7716b-142">AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7716b-142">Get-AzureRmRoleDefinition</span></span>](./Get-AzureRmRoleDefinition.md)

[<span data-ttu-id="7716b-143">新-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7716b-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="7716b-144">移除-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7716b-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

