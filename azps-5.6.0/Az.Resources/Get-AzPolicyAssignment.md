---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 010f8be0a96499415ac78c584ebad1c10acf4523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902842"
---
# <span data-ttu-id="2549b-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2549b-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="2549b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2549b-102">SYNOPSIS</span></span>
<span data-ttu-id="2549b-103">獲得策略指派。</span><span class="sxs-lookup"><span data-stu-id="2549b-103">Gets policy assignments.</span></span>

## <span data-ttu-id="2549b-104">語法</span><span class="sxs-lookup"><span data-stu-id="2549b-104">SYNTAX</span></span>

### <span data-ttu-id="2549b-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2549b-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2549b-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2549b-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2549b-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="2549b-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2549b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2549b-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2549b-109">描述</span><span class="sxs-lookup"><span data-stu-id="2549b-109">DESCRIPTION</span></span>
<span data-ttu-id="2549b-110">**Get-AzPolicyAssignment Cmdlet** 會取得所有政策指派或特定工作分派。</span><span class="sxs-lookup"><span data-stu-id="2549b-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="2549b-111">識別要根據名稱和範圍或識別碼取得的策略指派。</span><span class="sxs-lookup"><span data-stu-id="2549b-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="2549b-112">例子</span><span class="sxs-lookup"><span data-stu-id="2549b-112">EXAMPLES</span></span>

### <span data-ttu-id="2549b-113">範例 1：取得所有政策指派</span><span class="sxs-lookup"><span data-stu-id="2549b-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="2549b-114">此命令會獲得所有政策指派。</span><span class="sxs-lookup"><span data-stu-id="2549b-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="2549b-115">範例 2：取得特定政策指派</span><span class="sxs-lookup"><span data-stu-id="2549b-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="2549b-116">第一個命令會使用 Get-AzResourceGroup Cmdlet，將資源群組命名為 ResourceGroup11，並儲存在$ResourceGroup變數中。</span><span class="sxs-lookup"><span data-stu-id="2549b-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="2549b-117">第二個命令會針對 **resourceId** 屬性所識別的範圍，獲得名為 PolicyAssignment07$ResourceGroup工作分派。</span><span class="sxs-lookup"><span data-stu-id="2549b-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="2549b-118">範例 3：取得指派給管理群組的所有策略指派</span><span class="sxs-lookup"><span data-stu-id="2549b-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="2549b-119">第一個命令會指定要查詢的管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="2549b-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="2549b-120">第二個命令會獲得指派給管理群組的所有策略指派，其識別碼為 "myManagementGroup"。</span><span class="sxs-lookup"><span data-stu-id="2549b-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="2549b-121">參數</span><span class="sxs-lookup"><span data-stu-id="2549b-121">PARAMETERS</span></span>

### <span data-ttu-id="2549b-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2549b-122">-ApiVersion</span></span>
<span data-ttu-id="2549b-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2549b-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2549b-124">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="2549b-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2549b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2549b-125">-DefaultProfile</span></span>
<span data-ttu-id="2549b-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2549b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2549b-127">-Id</span><span class="sxs-lookup"><span data-stu-id="2549b-127">-Id</span></span>
<span data-ttu-id="2549b-128">指定此 Cmdlet 取得之策略工作分派的完全合格資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2549b-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2549b-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="2549b-129">-IncludeDescendent</span></span>
<span data-ttu-id="2549b-130">讓傳回之策略指派的清單包含與指定範圍相關的所有工作分派，包括來自上線範圍和遞減範圍的工作分派。</span><span class="sxs-lookup"><span data-stu-id="2549b-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2549b-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="2549b-131">-Name</span></span>
<span data-ttu-id="2549b-132">指定此 Cmdlet 獲得之策略指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="2549b-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2549b-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="2549b-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="2549b-134">指定此 Cmdlet 所獲得之策略指派之策略定義的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2549b-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2549b-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="2549b-135">-Pre</span></span>
<span data-ttu-id="2549b-136">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2549b-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2549b-137">-範圍</span><span class="sxs-lookup"><span data-stu-id="2549b-137">-Scope</span></span>
<span data-ttu-id="2549b-138">指定此 Cmdlet 所獲得之工作分派所適用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="2549b-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2549b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2549b-139">CommonParameters</span></span>
<span data-ttu-id="2549b-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2549b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2549b-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2549b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2549b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2549b-142">INPUTS</span></span>

### <span data-ttu-id="2549b-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2549b-143">System.String</span></span>

### <span data-ttu-id="2549b-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2549b-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2549b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="2549b-145">OUTPUTS</span></span>

### <span data-ttu-id="2549b-146">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="2549b-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2549b-147">筆記</span><span class="sxs-lookup"><span data-stu-id="2549b-147">NOTES</span></span>

## <span data-ttu-id="2549b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="2549b-148">RELATED LINKS</span></span>

[<span data-ttu-id="2549b-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2549b-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="2549b-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2549b-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="2549b-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2549b-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


