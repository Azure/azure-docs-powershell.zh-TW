---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 4ec965e63a779a5b0ebb606819e5e9f7f20b035e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435508"
---
# <span data-ttu-id="c486f-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="c486f-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="c486f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c486f-102">SYNOPSIS</span></span>
<span data-ttu-id="c486f-103">取得原則集定義。</span><span class="sxs-lookup"><span data-stu-id="c486f-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="c486f-104">句法</span><span class="sxs-lookup"><span data-stu-id="c486f-104">SYNTAX</span></span>

### <span data-ttu-id="c486f-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c486f-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c486f-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c486f-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c486f-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c486f-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c486f-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c486f-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c486f-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="c486f-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c486f-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="c486f-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c486f-111">說明</span><span class="sxs-lookup"><span data-stu-id="c486f-111">DESCRIPTION</span></span>
<span data-ttu-id="c486f-112">**AzPolicySetDefinition** Cmdlet 會取得原則集定義的集合，或由名稱或 ID 所識別的特定原則集定義。</span><span class="sxs-lookup"><span data-stu-id="c486f-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="c486f-113">示例</span><span class="sxs-lookup"><span data-stu-id="c486f-113">EXAMPLES</span></span>

### <span data-ttu-id="c486f-114">範例1：取得所有原則集定義</span><span class="sxs-lookup"><span data-stu-id="c486f-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="c486f-115">這個命令會取得所有原則集定義。</span><span class="sxs-lookup"><span data-stu-id="c486f-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="c486f-116">範例2：從目前的訂閱取得原則集定義（依名稱）</span><span class="sxs-lookup"><span data-stu-id="c486f-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="c486f-117">這個命令會從目前的預設訂閱取得名為 VMPolicySetDefinition 的原則集定義。</span><span class="sxs-lookup"><span data-stu-id="c486f-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="c486f-118">範例3：從訂閱取得原則集定義（依名稱）</span><span class="sxs-lookup"><span data-stu-id="c486f-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="c486f-119">這個命令會從 ID 3bf44b72-c631-427a-b8c8-53e2595398ca 的訂閱中取得名為 VMPolicySetDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="c486f-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="c486f-120">範例4：從管理群組取得所有自訂原則集定義</span><span class="sxs-lookup"><span data-stu-id="c486f-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="c486f-121">這個命令會從名為 Dept42 的管理群組中取得所有自訂原則集定義。</span><span class="sxs-lookup"><span data-stu-id="c486f-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="c486f-122">範例5：從指定類別取得原則集定義</span><span class="sxs-lookup"><span data-stu-id="c486f-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="c486f-123">這個命令會取得類別「虛擬機器」中的所有原則集定義。</span><span class="sxs-lookup"><span data-stu-id="c486f-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="c486f-124">參數</span><span class="sxs-lookup"><span data-stu-id="c486f-124">PARAMETERS</span></span>

### <span data-ttu-id="c486f-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c486f-125">-ApiVersion</span></span>
<span data-ttu-id="c486f-126">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="c486f-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c486f-127">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="c486f-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c486f-128">-內建</span><span class="sxs-lookup"><span data-stu-id="c486f-128">-Builtin</span></span>
<span data-ttu-id="c486f-129">將結果清單限制為僅限內建的原則集定義。</span><span class="sxs-lookup"><span data-stu-id="c486f-129">Limits list of results to only built-in policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BuiltinFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c486f-130">-自訂</span><span class="sxs-lookup"><span data-stu-id="c486f-130">-Custom</span></span>
<span data-ttu-id="c486f-131">將結果清單限制為僅限自訂原則集定義。</span><span class="sxs-lookup"><span data-stu-id="c486f-131">Limits list of results to only custom policy set definitions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CustomFilterParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c486f-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c486f-132">-DefaultProfile</span></span>
<span data-ttu-id="c486f-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c486f-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c486f-134">-識別碼</span><span class="sxs-lookup"><span data-stu-id="c486f-134">-Id</span></span>
<span data-ttu-id="c486f-135">完全限定的原則集定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="c486f-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="c486f-136">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="c486f-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="c486f-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="c486f-137">-ManagementGroupName</span></span>
<span data-ttu-id="c486f-138">策略集定義的管理群組名稱 (s) 取得。</span><span class="sxs-lookup"><span data-stu-id="c486f-138">The name of the management group of the policy set definition(s) to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagementGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c486f-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="c486f-139">-Name</span></span>
<span data-ttu-id="c486f-140">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="c486f-140">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c486f-141">-預先</span><span class="sxs-lookup"><span data-stu-id="c486f-141">-Pre</span></span>
<span data-ttu-id="c486f-142">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="c486f-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c486f-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c486f-143">-SubscriptionId</span></span>
<span data-ttu-id="c486f-144">原則集定義的訂閱識別碼， (s) 取得。</span><span class="sxs-lookup"><span data-stu-id="c486f-144">The subscription ID of the policy set definition(s) to get.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: BuiltinFilterParameterSet, CustomFilterParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c486f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c486f-145">CommonParameters</span></span>
<span data-ttu-id="c486f-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c486f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c486f-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c486f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c486f-148">輸入</span><span class="sxs-lookup"><span data-stu-id="c486f-148">INPUTS</span></span>

### <span data-ttu-id="c486f-149">System.object</span><span class="sxs-lookup"><span data-stu-id="c486f-149">System.String</span></span>

### <span data-ttu-id="c486f-150">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c486f-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c486f-151">輸出</span><span class="sxs-lookup"><span data-stu-id="c486f-151">OUTPUTS</span></span>

### <span data-ttu-id="c486f-152">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="c486f-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c486f-153">筆記</span><span class="sxs-lookup"><span data-stu-id="c486f-153">NOTES</span></span>

## <span data-ttu-id="c486f-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="c486f-154">RELATED LINKS</span></span>
