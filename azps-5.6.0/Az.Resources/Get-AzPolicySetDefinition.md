---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicySetDefinition.md
ms.openlocfilehash: 9ea6f37d21d35736116b2e9bf4fc3fcf20becf10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907310"
---
# <span data-ttu-id="8095b-101">Get-AzPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="8095b-101">Get-AzPolicySetDefinition</span></span>

## <span data-ttu-id="8095b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8095b-102">SYNOPSIS</span></span>
<span data-ttu-id="8095b-103">獲得策略集定義。</span><span class="sxs-lookup"><span data-stu-id="8095b-103">Gets policy set definitions.</span></span>

## <span data-ttu-id="8095b-104">語法</span><span class="sxs-lookup"><span data-stu-id="8095b-104">SYNTAX</span></span>

### <span data-ttu-id="8095b-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8095b-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8095b-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8095b-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8095b-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8095b-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicySetDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8095b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8095b-108">IdParameterSet</span></span>
```
Get-AzPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8095b-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="8095b-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8095b-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="8095b-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicySetDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8095b-111">描述</span><span class="sxs-lookup"><span data-stu-id="8095b-111">DESCRIPTION</span></span>
<span data-ttu-id="8095b-112">**Get-AzPolicySetDefinition Cmdlet** 會取得一組由名稱或識別碼識別之策略集定義或特定策略集定義的集合。</span><span class="sxs-lookup"><span data-stu-id="8095b-112">The **Get-AzPolicySetDefinition** cmdlet gets a collection of policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="8095b-113">例子</span><span class="sxs-lookup"><span data-stu-id="8095b-113">EXAMPLES</span></span>

### <span data-ttu-id="8095b-114">範例 1：取得所有策略集定義</span><span class="sxs-lookup"><span data-stu-id="8095b-114">Example 1: Get all policy set definitions</span></span>
```
PS C:\> Get-AzPolicySetDefinition
```

<span data-ttu-id="8095b-115">此命令會獲得所有策略集定義。</span><span class="sxs-lookup"><span data-stu-id="8095b-115">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="8095b-116">範例 2：根據名稱從目前的訂閱取得策略集定義</span><span class="sxs-lookup"><span data-stu-id="8095b-116">Example 2: Get policy set definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition'
```

<span data-ttu-id="8095b-117">此命令會從目前的預設訂閱中，獲得名為 VMPolicySetDefinition 的組定義。</span><span class="sxs-lookup"><span data-stu-id="8095b-117">This command gets the policy set definition named VMPolicySetDefinition from the current default subscription.</span></span>

### <span data-ttu-id="8095b-118">範例 3：根據名稱從訂閱取得策略集定義</span><span class="sxs-lookup"><span data-stu-id="8095b-118">Example 3: Get policy set definition from subscription by name</span></span>
```
PS C:\> Get-AzPolicySetDefinition -Name 'VMPolicySetDefinition' -subscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca'
```

<span data-ttu-id="8095b-119">此命令會從訂閱中，從 ID 3bf44b72-c631-427a-b8c8-53e2595398ca 的訂閱中，獲得名為 VMPolicySetDefinition 的策略定義。</span><span class="sxs-lookup"><span data-stu-id="8095b-119">This command gets the policy definition named VMPolicySetDefinition from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="8095b-120">範例 4：從管理群組取得所有自訂策略集定義</span><span class="sxs-lookup"><span data-stu-id="8095b-120">Example 4: Get all custom policy set definitions from management group</span></span>
```
PS C:\> Get-AzPolicySetDefinition -ManagementGroupName 'Dept42' -Custom
```

<span data-ttu-id="8095b-121">此命令會從名為 Dept42 的管理群組中，獲得所有自訂策略集定義。</span><span class="sxs-lookup"><span data-stu-id="8095b-121">This command gets all custom policy set definitions from the management group named Dept42.</span></span>

### <span data-ttu-id="8095b-122">範例 5：從給定類別取得策略集定義</span><span class="sxs-lookup"><span data-stu-id="8095b-122">Example 5: Get policy set definitions from a given category</span></span>
```
PS C:\> Get-AzPolicySetDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="8095b-123">此命令會獲得類別 "Virtual Machine" 的所有策略集定義。</span><span class="sxs-lookup"><span data-stu-id="8095b-123">This command gets all policy set definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="8095b-124">參數</span><span class="sxs-lookup"><span data-stu-id="8095b-124">PARAMETERS</span></span>

### <span data-ttu-id="8095b-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8095b-125">-ApiVersion</span></span>
<span data-ttu-id="8095b-126">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="8095b-126">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8095b-127">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="8095b-127">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="8095b-128">-內建</span><span class="sxs-lookup"><span data-stu-id="8095b-128">-Builtin</span></span>
<span data-ttu-id="8095b-129">將結果清單限制為只有內建的組定義。</span><span class="sxs-lookup"><span data-stu-id="8095b-129">Limits list of results to only built-in policy set definitions.</span></span>

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

### <span data-ttu-id="8095b-130">-自訂</span><span class="sxs-lookup"><span data-stu-id="8095b-130">-Custom</span></span>
<span data-ttu-id="8095b-131">將結果清單限制為只有自訂策略集定義。</span><span class="sxs-lookup"><span data-stu-id="8095b-131">Limits list of results to only custom policy set definitions.</span></span>

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

### <span data-ttu-id="8095b-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8095b-132">-DefaultProfile</span></span>
<span data-ttu-id="8095b-133">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8095b-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8095b-134">-Id</span><span class="sxs-lookup"><span data-stu-id="8095b-134">-Id</span></span>
<span data-ttu-id="8095b-135">完整規定設定定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="8095b-135">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="8095b-136">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="8095b-136">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="8095b-137">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8095b-137">-ManagementGroupName</span></span>
<span data-ttu-id="8095b-138">要取得之組定義之管理 (組) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8095b-138">The name of the management group of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="8095b-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="8095b-139">-Name</span></span>
<span data-ttu-id="8095b-140">該策略集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="8095b-140">The policy set definition name.</span></span>

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

### <span data-ttu-id="8095b-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="8095b-141">-Pre</span></span>
<span data-ttu-id="8095b-142">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8095b-142">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8095b-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8095b-143">-SubscriptionId</span></span>
<span data-ttu-id="8095b-144">這是要取得之 (定義) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="8095b-144">The subscription ID of the policy set definition(s) to get.</span></span>

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

### <span data-ttu-id="8095b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8095b-145">CommonParameters</span></span>
<span data-ttu-id="8095b-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8095b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8095b-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8095b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8095b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="8095b-148">INPUTS</span></span>

### <span data-ttu-id="8095b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="8095b-149">System.String</span></span>

### <span data-ttu-id="8095b-150">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8095b-150">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8095b-151">輸出</span><span class="sxs-lookup"><span data-stu-id="8095b-151">OUTPUTS</span></span>

### <span data-ttu-id="8095b-152">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8095b-152">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8095b-153">筆記</span><span class="sxs-lookup"><span data-stu-id="8095b-153">NOTES</span></span>

## <span data-ttu-id="8095b-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="8095b-154">RELATED LINKS</span></span>
