---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 724daa3cce0bd8fe38a645fcdd3acd2d3ce7bf1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911846"
---
# <span data-ttu-id="f13a0-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f13a0-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="f13a0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f13a0-102">SYNOPSIS</span></span>
<span data-ttu-id="f13a0-103">列出可供指派的所有 Azure RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="f13a0-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="f13a0-104">語法</span><span class="sxs-lookup"><span data-stu-id="f13a0-104">SYNTAX</span></span>

### <span data-ttu-id="f13a0-105">RoleDefinitionNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f13a0-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f13a0-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f13a0-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f13a0-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="f13a0-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f13a0-108">描述</span><span class="sxs-lookup"><span data-stu-id="f13a0-108">DESCRIPTION</span></span>
<span data-ttu-id="f13a0-109">使用Get-AzRoleDefinition角色名稱的 Get-AzRoleDefinition 命令來查看其詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f13a0-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="f13a0-110">若要檢查角色授予存取權之個別作業，請檢閱角色的動作和 NotActions 屬性。</span><span class="sxs-lookup"><span data-stu-id="f13a0-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="f13a0-111">例子</span><span class="sxs-lookup"><span data-stu-id="f13a0-111">EXAMPLES</span></span>

### <span data-ttu-id="f13a0-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="f13a0-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="f13a0-113">取得讀者角色定義</span><span class="sxs-lookup"><span data-stu-id="f13a0-113">Get the Reader role definition</span></span>

### <span data-ttu-id="f13a0-114">範例 2</span><span class="sxs-lookup"><span data-stu-id="f13a0-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="f13a0-115">列出所有 RBAC 角色定義</span><span class="sxs-lookup"><span data-stu-id="f13a0-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="f13a0-116">參數</span><span class="sxs-lookup"><span data-stu-id="f13a0-116">PARAMETERS</span></span>

### <span data-ttu-id="f13a0-117">-自訂</span><span class="sxs-lookup"><span data-stu-id="f13a0-117">-Custom</span></span>
<span data-ttu-id="f13a0-118">如果指定，只會在目錄中顯示自訂建立的角色。</span><span class="sxs-lookup"><span data-stu-id="f13a0-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f13a0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f13a0-119">-DefaultProfile</span></span>
<span data-ttu-id="f13a0-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f13a0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f13a0-121">-Id</span><span class="sxs-lookup"><span data-stu-id="f13a0-121">-Id</span></span>
<span data-ttu-id="f13a0-122">角色定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="f13a0-122">Role definition Id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f13a0-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f13a0-123">-Name</span></span>
<span data-ttu-id="f13a0-124">角色定義名稱。</span><span class="sxs-lookup"><span data-stu-id="f13a0-124">Role definition name.</span></span>
<span data-ttu-id="f13a0-125">例如，讀者、參與者、虛擬機器參與者。</span><span class="sxs-lookup"><span data-stu-id="f13a0-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f13a0-126">-範圍</span><span class="sxs-lookup"><span data-stu-id="f13a0-126">-Scope</span></span>
<span data-ttu-id="f13a0-127">角色定義範圍。</span><span class="sxs-lookup"><span data-stu-id="f13a0-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f13a0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f13a0-128">CommonParameters</span></span>
<span data-ttu-id="f13a0-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f13a0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f13a0-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f13a0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f13a0-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f13a0-131">INPUTS</span></span>

### <span data-ttu-id="f13a0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f13a0-132">System.String</span></span>

### <span data-ttu-id="f13a0-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="f13a0-133">System.Guid</span></span>

### <span data-ttu-id="f13a0-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f13a0-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f13a0-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f13a0-135">OUTPUTS</span></span>

### <span data-ttu-id="f13a0-136">Microsoft.Azure.Commands.Resources.models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f13a0-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="f13a0-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f13a0-137">NOTES</span></span>
<span data-ttu-id="f13a0-138">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="f13a0-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f13a0-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="f13a0-139">RELATED LINKS</span></span>

[<span data-ttu-id="f13a0-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f13a0-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="f13a0-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f13a0-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="f13a0-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f13a0-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="f13a0-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="f13a0-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

