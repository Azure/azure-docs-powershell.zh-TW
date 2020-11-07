---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: cabd2c86ed687b90b45e60b8078d89ad0a413c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801174"
---
# <span data-ttu-id="89de6-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="89de6-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="89de6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89de6-102">SYNOPSIS</span></span>
<span data-ttu-id="89de6-103">取得原則指派。</span><span class="sxs-lookup"><span data-stu-id="89de6-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89de6-104">句法</span><span class="sxs-lookup"><span data-stu-id="89de6-104">SYNTAX</span></span>

### <span data-ttu-id="89de6-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="89de6-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89de6-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="89de6-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89de6-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="89de6-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="89de6-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="89de6-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="89de6-109">說明</span><span class="sxs-lookup"><span data-stu-id="89de6-109">DESCRIPTION</span></span>
<span data-ttu-id="89de6-110">**AzureRmPolicyAssignment** Cmdlet 會取得所有原則指派或特定作業。</span><span class="sxs-lookup"><span data-stu-id="89de6-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="89de6-111">找出要依名稱、範圍或識別碼來取得的原則指派。</span><span class="sxs-lookup"><span data-stu-id="89de6-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="89de6-112">示例</span><span class="sxs-lookup"><span data-stu-id="89de6-112">EXAMPLES</span></span>

### <span data-ttu-id="89de6-113">範例1：取得所有原則指派</span><span class="sxs-lookup"><span data-stu-id="89de6-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="89de6-114">這個命令會取得所有原則指派。</span><span class="sxs-lookup"><span data-stu-id="89de6-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="89de6-115">範例2：取得特定原則指派</span><span class="sxs-lookup"><span data-stu-id="89de6-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="89de6-116">第一個命令會透過使用 Get-AzureRMResourceGroup Cmdletand 將其儲存在 $ResourceGroup 變數中，來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="89de6-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="89de6-117">第二個命令會針對 $ResourceGroup 的 **ResourceId** 屬性所識別的範圍，取得名為 PolicyAssignment07 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="89de6-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="89de6-118">範例3：取得指派給管理群組的所有原則指派</span><span class="sxs-lookup"><span data-stu-id="89de6-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="89de6-119">第一個命令指定要查詢之管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="89de6-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="89de6-120">第二個命令會取得指派給 ID 為 ' myManagementGroup」之管理群組的所有原則指派。</span><span class="sxs-lookup"><span data-stu-id="89de6-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="89de6-121">參數</span><span class="sxs-lookup"><span data-stu-id="89de6-121">PARAMETERS</span></span>

### <span data-ttu-id="89de6-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="89de6-122">-ApiVersion</span></span>
<span data-ttu-id="89de6-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="89de6-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="89de6-124">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="89de6-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="89de6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89de6-125">-DefaultProfile</span></span>
<span data-ttu-id="89de6-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="89de6-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89de6-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="89de6-127">-Id</span></span>
<span data-ttu-id="89de6-128">指定此 Cmdlet 所取得之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="89de6-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="89de6-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="89de6-129">-IncludeDescendent</span></span>
<span data-ttu-id="89de6-130">使傳回原則指派的清單包含所有與指定範圍相關的工作分派，包括來自上級範圍的所有作業，以及來自後代範圍的那些作業。</span><span class="sxs-lookup"><span data-stu-id="89de6-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="89de6-131">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="89de6-131">-InformationAction</span></span>
<span data-ttu-id="89de6-132">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="89de6-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="89de6-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="89de6-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="89de6-134">持續</span><span class="sxs-lookup"><span data-stu-id="89de6-134">Continue</span></span>
- <span data-ttu-id="89de6-135">理會</span><span class="sxs-lookup"><span data-stu-id="89de6-135">Ignore</span></span>
- <span data-ttu-id="89de6-136">看</span><span class="sxs-lookup"><span data-stu-id="89de6-136">Inquire</span></span>
- <span data-ttu-id="89de6-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="89de6-137">SilentlyContinue</span></span>
- <span data-ttu-id="89de6-138">停止</span><span class="sxs-lookup"><span data-stu-id="89de6-138">Stop</span></span>
- <span data-ttu-id="89de6-139">封存</span><span class="sxs-lookup"><span data-stu-id="89de6-139">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89de6-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="89de6-140">-InformationVariable</span></span>
<span data-ttu-id="89de6-141">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="89de6-141">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89de6-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="89de6-142">-Name</span></span>
<span data-ttu-id="89de6-143">指定此 Cmdlet 所取得之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="89de6-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="89de6-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="89de6-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="89de6-145">指定此 Cmdlet 所取得之原則指派的原則定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="89de6-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="89de6-146">-預先</span><span class="sxs-lookup"><span data-stu-id="89de6-146">-Pre</span></span>
<span data-ttu-id="89de6-147">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="89de6-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="89de6-148">-範圍</span><span class="sxs-lookup"><span data-stu-id="89de6-148">-Scope</span></span>
<span data-ttu-id="89de6-149">針對此 Cmdlet 所取得的作業，指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="89de6-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="89de6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89de6-150">CommonParameters</span></span>
<span data-ttu-id="89de6-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89de6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89de6-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89de6-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89de6-153">輸入</span><span class="sxs-lookup"><span data-stu-id="89de6-153">INPUTS</span></span>

## <span data-ttu-id="89de6-154">輸出</span><span class="sxs-lookup"><span data-stu-id="89de6-154">OUTPUTS</span></span>

## <span data-ttu-id="89de6-155">筆記</span><span class="sxs-lookup"><span data-stu-id="89de6-155">NOTES</span></span>

## <span data-ttu-id="89de6-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="89de6-156">RELATED LINKS</span></span>

[<span data-ttu-id="89de6-157">新-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="89de6-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="89de6-158">移除-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="89de6-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="89de6-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="89de6-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


