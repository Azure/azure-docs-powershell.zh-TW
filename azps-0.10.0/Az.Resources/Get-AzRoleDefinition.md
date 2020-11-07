---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: d43ec874af02d57abedddb1b49b3cc8723af5c2e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795301"
---
# <span data-ttu-id="af935-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="af935-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="af935-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af935-102">SYNOPSIS</span></span>
<span data-ttu-id="af935-103">列出所有可指派的 Azure RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="af935-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="af935-104">句法</span><span class="sxs-lookup"><span data-stu-id="af935-104">SYNTAX</span></span>

### <span data-ttu-id="af935-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af935-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af935-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af935-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af935-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="af935-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af935-108">說明</span><span class="sxs-lookup"><span data-stu-id="af935-108">DESCRIPTION</span></span>
<span data-ttu-id="af935-109">將 Get-AzRoleDefinition 命令與特定角色名稱搭配使用，即可查看其詳細資料。</span><span class="sxs-lookup"><span data-stu-id="af935-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="af935-110">若要檢查角色授與存取權的個別作業，請檢查該角色的動作和 NotActions 屬性。</span><span class="sxs-lookup"><span data-stu-id="af935-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="af935-111">示例</span><span class="sxs-lookup"><span data-stu-id="af935-111">EXAMPLES</span></span>

### <span data-ttu-id="af935-112">範例1</span><span class="sxs-lookup"><span data-stu-id="af935-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="af935-113">取得閱讀者角色定義</span><span class="sxs-lookup"><span data-stu-id="af935-113">Get the Reader role definition</span></span>

### <span data-ttu-id="af935-114">範例2</span><span class="sxs-lookup"><span data-stu-id="af935-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="af935-115">列出所有 RBAC 角色定義</span><span class="sxs-lookup"><span data-stu-id="af935-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="af935-116">參數</span><span class="sxs-lookup"><span data-stu-id="af935-116">PARAMETERS</span></span>

### <span data-ttu-id="af935-117">-自訂</span><span class="sxs-lookup"><span data-stu-id="af935-117">-Custom</span></span>
<span data-ttu-id="af935-118">如果已指定，只會在目錄中顯示自訂建立的角色。</span><span class="sxs-lookup"><span data-stu-id="af935-118">If specified, only displays the custom created roles in the directory.</span></span>

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

### <span data-ttu-id="af935-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af935-119">-DefaultProfile</span></span>
<span data-ttu-id="af935-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="af935-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af935-121">-識別碼</span><span class="sxs-lookup"><span data-stu-id="af935-121">-Id</span></span>
<span data-ttu-id="af935-122">角色定義 Id。</span><span class="sxs-lookup"><span data-stu-id="af935-122">Role definition Id.</span></span>

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

### <span data-ttu-id="af935-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="af935-123">-Name</span></span>
<span data-ttu-id="af935-124">角色定義名稱。</span><span class="sxs-lookup"><span data-stu-id="af935-124">Role definition name.</span></span>
<span data-ttu-id="af935-125">例如，讀取器、參與者、虛擬機器參與者。</span><span class="sxs-lookup"><span data-stu-id="af935-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

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

### <span data-ttu-id="af935-126">-範圍</span><span class="sxs-lookup"><span data-stu-id="af935-126">-Scope</span></span>
<span data-ttu-id="af935-127">角色定義範圍。</span><span class="sxs-lookup"><span data-stu-id="af935-127">Role definition scope.</span></span>

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

### <span data-ttu-id="af935-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af935-128">CommonParameters</span></span>
<span data-ttu-id="af935-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af935-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af935-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af935-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af935-131">輸入</span><span class="sxs-lookup"><span data-stu-id="af935-131">INPUTS</span></span>

### <span data-ttu-id="af935-132">System.object</span><span class="sxs-lookup"><span data-stu-id="af935-132">System.String</span></span>
<span data-ttu-id="af935-133">參數： Scope (ByValue) </span><span class="sxs-lookup"><span data-stu-id="af935-133">Parameters: Scope (ByValue)</span></span>

### <span data-ttu-id="af935-134">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="af935-134">System.Guid</span></span>

### <span data-ttu-id="af935-135">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="af935-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="af935-136">輸出</span><span class="sxs-lookup"><span data-stu-id="af935-136">OUTPUTS</span></span>

### <span data-ttu-id="af935-137">PSRoleDefinition 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="af935-137">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="af935-138">筆記</span><span class="sxs-lookup"><span data-stu-id="af935-138">NOTES</span></span>
<span data-ttu-id="af935-139">關鍵字： azure，Az，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="af935-139">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="af935-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="af935-140">RELATED LINKS</span></span>

[<span data-ttu-id="af935-141">新-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="af935-141">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="af935-142">AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="af935-142">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="af935-143">新-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="af935-143">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="af935-144">移除-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="af935-144">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

