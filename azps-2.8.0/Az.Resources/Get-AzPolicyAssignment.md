---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: e2cce15271b1289a2d6bfe5f8874f004ba95a04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792244"
---
# <span data-ttu-id="b7a93-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b7a93-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="b7a93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7a93-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a93-103">取得原則指派。</span><span class="sxs-lookup"><span data-stu-id="b7a93-103">Gets policy assignments.</span></span>

## <span data-ttu-id="b7a93-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7a93-104">SYNTAX</span></span>

### <span data-ttu-id="b7a93-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b7a93-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7a93-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a93-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7a93-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a93-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7a93-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a93-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7a93-109">說明</span><span class="sxs-lookup"><span data-stu-id="b7a93-109">DESCRIPTION</span></span>
<span data-ttu-id="b7a93-110">**AzPolicyAssignment** Cmdlet 會取得所有原則指派或特定作業。</span><span class="sxs-lookup"><span data-stu-id="b7a93-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="b7a93-111">找出要依名稱、範圍或識別碼來取得的原則指派。</span><span class="sxs-lookup"><span data-stu-id="b7a93-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="b7a93-112">示例</span><span class="sxs-lookup"><span data-stu-id="b7a93-112">EXAMPLES</span></span>

### <span data-ttu-id="b7a93-113">範例1：取得所有原則指派</span><span class="sxs-lookup"><span data-stu-id="b7a93-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="b7a93-114">這個命令會取得所有原則指派。</span><span class="sxs-lookup"><span data-stu-id="b7a93-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="b7a93-115">範例2：取得特定原則指派</span><span class="sxs-lookup"><span data-stu-id="b7a93-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="b7a93-116">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組，並將它儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="b7a93-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b7a93-117">第二個命令會針對 $ResourceGroup 的 **ResourceId** 屬性所識別的範圍，取得名為 PolicyAssignment07 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="b7a93-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="b7a93-118">範例3：取得指派給管理群組的所有原則指派</span><span class="sxs-lookup"><span data-stu-id="b7a93-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="b7a93-119">第一個命令指定要查詢之管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7a93-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="b7a93-120">第二個命令會取得指派給 ID 為 ' myManagementGroup」之管理群組的所有原則指派。</span><span class="sxs-lookup"><span data-stu-id="b7a93-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="b7a93-121">參數</span><span class="sxs-lookup"><span data-stu-id="b7a93-121">PARAMETERS</span></span>

### <span data-ttu-id="b7a93-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b7a93-122">-ApiVersion</span></span>
<span data-ttu-id="b7a93-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b7a93-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b7a93-124">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="b7a93-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b7a93-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a93-125">-DefaultProfile</span></span>
<span data-ttu-id="b7a93-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="b7a93-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7a93-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b7a93-127">-Id</span></span>
<span data-ttu-id="b7a93-128">指定此 Cmdlet 所取得之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7a93-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b7a93-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="b7a93-129">-IncludeDescendent</span></span>
<span data-ttu-id="b7a93-130">使傳回原則指派的清單包含所有與指定範圍相關的工作分派，包括來自上級範圍的所有作業，以及來自後代範圍的那些作業。</span><span class="sxs-lookup"><span data-stu-id="b7a93-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="b7a93-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7a93-131">-Name</span></span>
<span data-ttu-id="b7a93-132">指定此 Cmdlet 所取得之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7a93-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b7a93-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b7a93-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="b7a93-134">指定此 Cmdlet 所取得之原則指派的原則定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="b7a93-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b7a93-135">-預先</span><span class="sxs-lookup"><span data-stu-id="b7a93-135">-Pre</span></span>
<span data-ttu-id="b7a93-136">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="b7a93-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b7a93-137">-範圍</span><span class="sxs-lookup"><span data-stu-id="b7a93-137">-Scope</span></span>
<span data-ttu-id="b7a93-138">針對此 Cmdlet 所取得的作業，指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="b7a93-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b7a93-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a93-139">CommonParameters</span></span>
<span data-ttu-id="b7a93-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7a93-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a93-141">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b7a93-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a93-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b7a93-142">INPUTS</span></span>

### <span data-ttu-id="b7a93-143">System.object</span><span class="sxs-lookup"><span data-stu-id="b7a93-143">System.String</span></span>

### <span data-ttu-id="b7a93-144">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="b7a93-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b7a93-145">輸出</span><span class="sxs-lookup"><span data-stu-id="b7a93-145">OUTPUTS</span></span>

### <span data-ttu-id="b7a93-146">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="b7a93-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b7a93-147">筆記</span><span class="sxs-lookup"><span data-stu-id="b7a93-147">NOTES</span></span>

## <span data-ttu-id="b7a93-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7a93-148">RELATED LINKS</span></span>

[<span data-ttu-id="b7a93-149">新-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b7a93-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="b7a93-150">移除-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b7a93-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="b7a93-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b7a93-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


