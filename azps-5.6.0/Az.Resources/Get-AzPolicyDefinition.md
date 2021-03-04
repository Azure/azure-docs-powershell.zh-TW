---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: a04dac8b0c8774e325f052bb6425d9ece81e0f38
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917937"
---
# <span data-ttu-id="e3851-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3851-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="e3851-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e3851-102">SYNOPSIS</span></span>
<span data-ttu-id="e3851-103">獲得策略定義。</span><span class="sxs-lookup"><span data-stu-id="e3851-103">Gets policy definitions.</span></span>

## <span data-ttu-id="e3851-104">語法</span><span class="sxs-lookup"><span data-stu-id="e3851-104">SYNTAX</span></span>

### <span data-ttu-id="e3851-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e3851-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3851-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3851-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3851-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3851-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3851-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3851-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3851-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3851-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3851-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3851-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3851-111">描述</span><span class="sxs-lookup"><span data-stu-id="e3851-111">DESCRIPTION</span></span>
<span data-ttu-id="e3851-112">**Get-AzPolicyDefinition Cmdlet** 會取得一組由名稱或識別碼識別的一群組原則定義或特定政策定義。</span><span class="sxs-lookup"><span data-stu-id="e3851-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="e3851-113">例子</span><span class="sxs-lookup"><span data-stu-id="e3851-113">EXAMPLES</span></span>

### <span data-ttu-id="e3851-114">範例 1：取得所有策略定義</span><span class="sxs-lookup"><span data-stu-id="e3851-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="e3851-115">此命令會獲得所有政策定義。</span><span class="sxs-lookup"><span data-stu-id="e3851-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="e3851-116">範例 2：根據名稱從目前的訂閱取得策略定義</span><span class="sxs-lookup"><span data-stu-id="e3851-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="e3851-117">此命令會從目前的預設訂閱中，獲得名為 VMPolicyDefinition 的策略定義。</span><span class="sxs-lookup"><span data-stu-id="e3851-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="e3851-118">範例 3：根據名稱從管理群組取得策略定義</span><span class="sxs-lookup"><span data-stu-id="e3851-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="e3851-119">此命令會從名為 Dept42 的管理群組中，獲得名為 VMPolicyDefinition 的策略定義。</span><span class="sxs-lookup"><span data-stu-id="e3851-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="e3851-120">範例 4：從訂閱取得所有內建策略定義</span><span class="sxs-lookup"><span data-stu-id="e3851-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="e3851-121">此命令會從訂閱獲得 ID 3bf44b72-c631-427a-b8c8-53e2595398ca 的所有內建策略定義。</span><span class="sxs-lookup"><span data-stu-id="e3851-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="e3851-122">範例 5：從給定類別取得策略定義</span><span class="sxs-lookup"><span data-stu-id="e3851-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="e3851-123">此命令會獲得「虛擬機器」類別中的所有策略定義。</span><span class="sxs-lookup"><span data-stu-id="e3851-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="e3851-124">參數</span><span class="sxs-lookup"><span data-stu-id="e3851-124">PARAMETERS</span></span>

### <span data-ttu-id="e3851-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e3851-125">-ApiVersion</span></span>
<span data-ttu-id="e3851-126">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e3851-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e3851-127">如果您未指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="e3851-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e3851-128">-內建</span><span class="sxs-lookup"><span data-stu-id="e3851-128">-Builtin</span></span>
<span data-ttu-id="e3851-129">將結果清單限制為僅內建策略定義。</span><span class="sxs-lookup"><span data-stu-id="e3851-129">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="e3851-130">-自訂</span><span class="sxs-lookup"><span data-stu-id="e3851-130">-Custom</span></span>
<span data-ttu-id="e3851-131">將結果清單限制為只有自訂策略定義。</span><span class="sxs-lookup"><span data-stu-id="e3851-131">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="e3851-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3851-132">-DefaultProfile</span></span>
<span data-ttu-id="e3851-133">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e3851-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3851-134">-Id</span><span class="sxs-lookup"><span data-stu-id="e3851-134">-Id</span></span>
<span data-ttu-id="e3851-135">指定此 Cmdlet 取得之策略定義之完整資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3851-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e3851-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="e3851-136">-ManagementGroupName</span></span>
<span data-ttu-id="e3851-137">這是要取得之 (組) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3851-137">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="e3851-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3851-138">-Name</span></span>
<span data-ttu-id="e3851-139">指定此 Cmdlet 獲得之策略定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3851-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e3851-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="e3851-140">-Pre</span></span>
<span data-ttu-id="e3851-141">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e3851-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e3851-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3851-142">-SubscriptionId</span></span>
<span data-ttu-id="e3851-143">要取得之 (訂閱) 識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3851-143">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="e3851-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3851-144">CommonParameters</span></span>
<span data-ttu-id="e3851-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e3851-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3851-146">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3851-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3851-147">輸入</span><span class="sxs-lookup"><span data-stu-id="e3851-147">INPUTS</span></span>

### <span data-ttu-id="e3851-148">System.String</span><span class="sxs-lookup"><span data-stu-id="e3851-148">System.String</span></span>

### <span data-ttu-id="e3851-149">System.Nullable'1[[System.Guid， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e3851-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e3851-150">輸出</span><span class="sxs-lookup"><span data-stu-id="e3851-150">OUTPUTS</span></span>

### <span data-ttu-id="e3851-151">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e3851-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e3851-152">筆記</span><span class="sxs-lookup"><span data-stu-id="e3851-152">NOTES</span></span>

## <span data-ttu-id="e3851-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3851-153">RELATED LINKS</span></span>

[<span data-ttu-id="e3851-154">New-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3851-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="e3851-155">Remove-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3851-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="e3851-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3851-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


