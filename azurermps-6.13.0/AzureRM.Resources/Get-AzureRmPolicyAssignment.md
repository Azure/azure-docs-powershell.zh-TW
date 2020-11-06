---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAssignment.md
ms.openlocfilehash: 71f3c6ab80fd0ba44d715cb25b4bf690e44359c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447261"
---
# <span data-ttu-id="2ea8b-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2ea8b-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="2ea8b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ea8b-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea8b-103">取得原則指派。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ea8b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ea8b-104">SYNTAX</span></span>

### <span data-ttu-id="2ea8b-105">DefaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2ea8b-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2ea8b-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ea8b-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2ea8b-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ea8b-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2ea8b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ea8b-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2ea8b-109">說明</span><span class="sxs-lookup"><span data-stu-id="2ea8b-109">DESCRIPTION</span></span>
<span data-ttu-id="2ea8b-110">**AzureRmPolicyAssignment** Cmdlet 會取得所有原則指派或特定作業。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="2ea8b-111">找出要依名稱、範圍或識別碼來取得的原則指派。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="2ea8b-112">示例</span><span class="sxs-lookup"><span data-stu-id="2ea8b-112">EXAMPLES</span></span>

### <span data-ttu-id="2ea8b-113">範例1：取得所有原則指派</span><span class="sxs-lookup"><span data-stu-id="2ea8b-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="2ea8b-114">這個命令會取得所有原則指派。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="2ea8b-115">範例2：取得特定原則指派</span><span class="sxs-lookup"><span data-stu-id="2ea8b-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="2ea8b-116">第一個命令會透過使用 Get-AzureRMResourceGroup Cmdletand 將其儲存在 $ResourceGroup 變數中，來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="2ea8b-117">第二個命令會針對 $ResourceGroup 的 **ResourceId** 屬性所識別的範圍，取得名為 PolicyAssignment07 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="2ea8b-118">範例3：取得指派給管理群組的所有原則指派</span><span class="sxs-lookup"><span data-stu-id="2ea8b-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="2ea8b-119">第一個命令指定要查詢之管理群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="2ea8b-120">第二個命令會取得指派給 ID 為 ' myManagementGroup」之管理群組的所有原則指派。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="2ea8b-121">參數</span><span class="sxs-lookup"><span data-stu-id="2ea8b-121">PARAMETERS</span></span>

### <span data-ttu-id="2ea8b-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2ea8b-122">-ApiVersion</span></span>
<span data-ttu-id="2ea8b-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2ea8b-124">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2ea8b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea8b-125">-DefaultProfile</span></span>
<span data-ttu-id="2ea8b-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2ea8b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ea8b-127">-識別碼</span><span class="sxs-lookup"><span data-stu-id="2ea8b-127">-Id</span></span>
<span data-ttu-id="2ea8b-128">指定此 Cmdlet 所取得之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2ea8b-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="2ea8b-129">-IncludeDescendent</span></span>
<span data-ttu-id="2ea8b-130">使傳回原則指派的清單包含所有與指定範圍相關的工作分派，包括來自上級範圍的所有作業，以及來自後代範圍的那些作業。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="2ea8b-131">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2ea8b-131">-InformationAction</span></span>
<span data-ttu-id="2ea8b-132">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="2ea8b-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2ea8b-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2ea8b-134">持續</span><span class="sxs-lookup"><span data-stu-id="2ea8b-134">Continue</span></span>
- <span data-ttu-id="2ea8b-135">理會</span><span class="sxs-lookup"><span data-stu-id="2ea8b-135">Ignore</span></span>
- <span data-ttu-id="2ea8b-136">看</span><span class="sxs-lookup"><span data-stu-id="2ea8b-136">Inquire</span></span>
- <span data-ttu-id="2ea8b-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2ea8b-137">SilentlyContinue</span></span>
- <span data-ttu-id="2ea8b-138">停止</span><span class="sxs-lookup"><span data-stu-id="2ea8b-138">Stop</span></span>
- <span data-ttu-id="2ea8b-139">封存</span><span class="sxs-lookup"><span data-stu-id="2ea8b-139">Suspend</span></span>

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

### <span data-ttu-id="2ea8b-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2ea8b-140">-InformationVariable</span></span>
<span data-ttu-id="2ea8b-141">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-141">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2ea8b-142">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ea8b-142">-Name</span></span>
<span data-ttu-id="2ea8b-143">指定此 Cmdlet 所取得之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2ea8b-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="2ea8b-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="2ea8b-145">指定此 Cmdlet 所取得之原則指派的原則定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2ea8b-146">-預先</span><span class="sxs-lookup"><span data-stu-id="2ea8b-146">-Pre</span></span>
<span data-ttu-id="2ea8b-147">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2ea8b-148">-範圍</span><span class="sxs-lookup"><span data-stu-id="2ea8b-148">-Scope</span></span>
<span data-ttu-id="2ea8b-149">針對此 Cmdlet 所取得的作業，指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2ea8b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea8b-150">CommonParameters</span></span>
<span data-ttu-id="2ea8b-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea8b-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ea8b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea8b-153">輸入</span><span class="sxs-lookup"><span data-stu-id="2ea8b-153">INPUTS</span></span>

## <span data-ttu-id="2ea8b-154">輸出</span><span class="sxs-lookup"><span data-stu-id="2ea8b-154">OUTPUTS</span></span>

## <span data-ttu-id="2ea8b-155">筆記</span><span class="sxs-lookup"><span data-stu-id="2ea8b-155">NOTES</span></span>

## <span data-ttu-id="2ea8b-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ea8b-156">RELATED LINKS</span></span>

[<span data-ttu-id="2ea8b-157">新-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2ea8b-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="2ea8b-158">移除-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2ea8b-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="2ea8b-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="2ea8b-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


