---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmRoleDefinition.md
ms.openlocfilehash: c1850cdc410df064a97950bb38f3734657649467
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453059"
---
# <span data-ttu-id="dc46a-101">Get-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dc46a-101">Get-AzureRmRoleDefinition</span></span>

## <span data-ttu-id="dc46a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dc46a-102">SYNOPSIS</span></span>
<span data-ttu-id="dc46a-103">列出所有可指派的 Azure RBAC 角色。</span><span class="sxs-lookup"><span data-stu-id="dc46a-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc46a-104">句法</span><span class="sxs-lookup"><span data-stu-id="dc46a-104">SYNTAX</span></span>

### <span data-ttu-id="dc46a-105">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc46a-105">RoleDefinitionNameParameterSet</span></span>
```
Get-AzureRmRoleDefinition [[-Name] <String>] [-Scope <String>] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc46a-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc46a-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dc46a-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc46a-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzureRmRoleDefinition [-Scope <String>] [-Custom] [-AtScopeAndBelow]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc46a-108">說明</span><span class="sxs-lookup"><span data-stu-id="dc46a-108">DESCRIPTION</span></span>
<span data-ttu-id="dc46a-109">將 Get-AzureRmRoleDefinition 命令與特定角色名稱搭配使用，即可查看其詳細資料。</span><span class="sxs-lookup"><span data-stu-id="dc46a-109">Use the Get-AzureRmRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="dc46a-110">若要檢查角色授與存取權的個別作業，請檢查該角色的動作和 NotActions 屬性。</span><span class="sxs-lookup"><span data-stu-id="dc46a-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="dc46a-111">示例</span><span class="sxs-lookup"><span data-stu-id="dc46a-111">EXAMPLES</span></span>

### <span data-ttu-id="dc46a-112">範例1</span><span class="sxs-lookup"><span data-stu-id="dc46a-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRoleDefinition -Name Reader
```

<span data-ttu-id="dc46a-113">取得閱讀者角色定義</span><span class="sxs-lookup"><span data-stu-id="dc46a-113">Get the Reader role definition</span></span>

### <span data-ttu-id="dc46a-114">範例2</span><span class="sxs-lookup"><span data-stu-id="dc46a-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRoleDefinition
```

<span data-ttu-id="dc46a-115">列出所有 RBAC 角色定義</span><span class="sxs-lookup"><span data-stu-id="dc46a-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="dc46a-116">參數</span><span class="sxs-lookup"><span data-stu-id="dc46a-116">PARAMETERS</span></span>

### <span data-ttu-id="dc46a-117">-AtScopeAndBelow</span><span class="sxs-lookup"><span data-stu-id="dc46a-117">-AtScopeAndBelow</span></span>
<span data-ttu-id="dc46a-118">如果已指定，則會顯示所有角色定義。</span><span class="sxs-lookup"><span data-stu-id="dc46a-118">If specified, displays all role definitions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionNameParameterSet, RoleDefinitionCustomParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc46a-119">-自訂</span><span class="sxs-lookup"><span data-stu-id="dc46a-119">-Custom</span></span>
<span data-ttu-id="dc46a-120">如果已指定，只會在目錄中顯示自訂建立的角色。</span><span class="sxs-lookup"><span data-stu-id="dc46a-120">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc46a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc46a-121">-DefaultProfile</span></span>
<span data-ttu-id="dc46a-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="dc46a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc46a-123">-識別碼</span><span class="sxs-lookup"><span data-stu-id="dc46a-123">-Id</span></span>
<span data-ttu-id="dc46a-124">角色定義 Id。</span><span class="sxs-lookup"><span data-stu-id="dc46a-124">Role definition Id.</span></span>

```yaml
Type: Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc46a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="dc46a-125">-Name</span></span>
<span data-ttu-id="dc46a-126">角色定義名稱。</span><span class="sxs-lookup"><span data-stu-id="dc46a-126">Role definition name.</span></span>
<span data-ttu-id="dc46a-127">例如，讀取器、參與者、虛擬機器參與者。</span><span class="sxs-lookup"><span data-stu-id="dc46a-127">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc46a-128">-範圍</span><span class="sxs-lookup"><span data-stu-id="dc46a-128">-Scope</span></span>
<span data-ttu-id="dc46a-129">角色定義範圍。</span><span class="sxs-lookup"><span data-stu-id="dc46a-129">Role definition scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc46a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc46a-130">CommonParameters</span></span>
<span data-ttu-id="dc46a-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dc46a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc46a-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dc46a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc46a-133">輸入</span><span class="sxs-lookup"><span data-stu-id="dc46a-133">INPUTS</span></span>

### <span data-ttu-id="dc46a-134">字串</span><span class="sxs-lookup"><span data-stu-id="dc46a-134">String</span></span>
<span data-ttu-id="dc46a-135">形參 "Scope" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="dc46a-135">Parameter 'Scope' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="dc46a-136">輸出</span><span class="sxs-lookup"><span data-stu-id="dc46a-136">OUTPUTS</span></span>

### <span data-ttu-id="dc46a-137">[System.object]. 清單 ' 1 [PSRoleDefinition]. [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="dc46a-137">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition]</span></span>

## <span data-ttu-id="dc46a-138">筆記</span><span class="sxs-lookup"><span data-stu-id="dc46a-138">NOTES</span></span>
<span data-ttu-id="dc46a-139">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="dc46a-139">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="dc46a-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc46a-140">RELATED LINKS</span></span>

[<span data-ttu-id="dc46a-141">新-AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dc46a-141">New-AzureRmRoleAssignment</span></span>](./New-AzureRmRoleAssignment.md)

[<span data-ttu-id="dc46a-142">AzureRmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="dc46a-142">Get-AzureRmRoleAssignment</span></span>](./Get-AzureRmRoleAssignment.md)

[<span data-ttu-id="dc46a-143">新-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dc46a-143">New-AzureRmRoleDefinition</span></span>](./New-AzureRmRoleDefinition.md)

[<span data-ttu-id="dc46a-144">移除-AzureRmRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="dc46a-144">Remove-AzureRmRoleDefinition</span></span>](./Remove-AzureRmRoleDefinition.md)

