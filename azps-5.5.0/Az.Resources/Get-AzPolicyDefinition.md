---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 52de80f1ad3cf84a7aa309b5e97b7fa24e9419b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132258"
---
# <span data-ttu-id="6f547-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f547-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="6f547-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f547-102">SYNOPSIS</span></span>
<span data-ttu-id="6f547-103">取得原則定義。</span><span class="sxs-lookup"><span data-stu-id="6f547-103">Gets policy definitions.</span></span>

## <span data-ttu-id="6f547-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f547-104">SYNTAX</span></span>

### <span data-ttu-id="6f547-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6f547-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f547-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f547-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f547-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f547-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f547-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f547-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6f547-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f547-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f547-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f547-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f547-111">說明</span><span class="sxs-lookup"><span data-stu-id="6f547-111">DESCRIPTION</span></span>
<span data-ttu-id="6f547-112">**AzPolicyDefinition** Cmdlet 會取得原則定義或由名稱或 ID 所識別的特定原則定義的集合。</span><span class="sxs-lookup"><span data-stu-id="6f547-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="6f547-113">示例</span><span class="sxs-lookup"><span data-stu-id="6f547-113">EXAMPLES</span></span>

### <span data-ttu-id="6f547-114">範例1：取得所有原則定義</span><span class="sxs-lookup"><span data-stu-id="6f547-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="6f547-115">這個命令會取得所有原則定義。</span><span class="sxs-lookup"><span data-stu-id="6f547-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="6f547-116">範例2：透過名稱從目前的訂閱取得原則定義</span><span class="sxs-lookup"><span data-stu-id="6f547-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="6f547-117">這個命令會從目前的預設訂閱取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="6f547-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="6f547-118">範例3：從管理群組依名稱取得原則定義</span><span class="sxs-lookup"><span data-stu-id="6f547-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="6f547-119">這個命令會從名為 Dept42 的管理群組中取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="6f547-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="6f547-120">範例4：從訂閱取得所有內建原則定義</span><span class="sxs-lookup"><span data-stu-id="6f547-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="6f547-121">這個命令會從 ID 為3bf44b72-c631-427a-b8c8-53e2595398ca 的訂閱中取得所有內建的原則定義。</span><span class="sxs-lookup"><span data-stu-id="6f547-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

### <span data-ttu-id="6f547-122">範例5：從指定類別取得原則定義</span><span class="sxs-lookup"><span data-stu-id="6f547-122">Example 5: Get policy definitions from a given category</span></span>
```
PS C:\> Get-AzPolicyDefinition | where-object {$_.Properties.metadata.category -eq "Virtual Machine"}
```

<span data-ttu-id="6f547-123">這個命令會取得類別「虛擬機器」中的所有原則定義。</span><span class="sxs-lookup"><span data-stu-id="6f547-123">This command gets all policy definitions in category "Virtual Machine".</span></span>

## <span data-ttu-id="6f547-124">參數</span><span class="sxs-lookup"><span data-stu-id="6f547-124">PARAMETERS</span></span>

### <span data-ttu-id="6f547-125">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6f547-125">-ApiVersion</span></span>
<span data-ttu-id="6f547-126">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="6f547-126">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6f547-127">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="6f547-127">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6f547-128">-內建</span><span class="sxs-lookup"><span data-stu-id="6f547-128">-Builtin</span></span>
<span data-ttu-id="6f547-129">將結果清單限制為僅限內建的原則定義。</span><span class="sxs-lookup"><span data-stu-id="6f547-129">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="6f547-130">-自訂</span><span class="sxs-lookup"><span data-stu-id="6f547-130">-Custom</span></span>
<span data-ttu-id="6f547-131">將結果清單限制為僅限自訂原則定義。</span><span class="sxs-lookup"><span data-stu-id="6f547-131">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="6f547-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f547-132">-DefaultProfile</span></span>
<span data-ttu-id="6f547-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6f547-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f547-134">-識別碼</span><span class="sxs-lookup"><span data-stu-id="6f547-134">-Id</span></span>
<span data-ttu-id="6f547-135">指定此 Cmdlet 所取得之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f547-135">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6f547-136">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="6f547-136">-ManagementGroupName</span></span>
<span data-ttu-id="6f547-137">原則定義的管理群組名稱 (s) 取得。</span><span class="sxs-lookup"><span data-stu-id="6f547-137">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="6f547-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f547-138">-Name</span></span>
<span data-ttu-id="6f547-139">指定此 Cmdlet 所取得之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f547-139">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6f547-140">-預先</span><span class="sxs-lookup"><span data-stu-id="6f547-140">-Pre</span></span>
<span data-ttu-id="6f547-141">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="6f547-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6f547-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6f547-142">-SubscriptionId</span></span>
<span data-ttu-id="6f547-143">原則定義的訂閱識別碼， (s) 取得。</span><span class="sxs-lookup"><span data-stu-id="6f547-143">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="6f547-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f547-144">CommonParameters</span></span>
<span data-ttu-id="6f547-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f547-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f547-146">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6f547-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f547-147">輸入</span><span class="sxs-lookup"><span data-stu-id="6f547-147">INPUTS</span></span>

### <span data-ttu-id="6f547-148">System.object</span><span class="sxs-lookup"><span data-stu-id="6f547-148">System.String</span></span>

### <span data-ttu-id="6f547-149">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6f547-149">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6f547-150">輸出</span><span class="sxs-lookup"><span data-stu-id="6f547-150">OUTPUTS</span></span>

### <span data-ttu-id="6f547-151">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="6f547-151">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6f547-152">筆記</span><span class="sxs-lookup"><span data-stu-id="6f547-152">NOTES</span></span>

## <span data-ttu-id="6f547-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f547-153">RELATED LINKS</span></span>

[<span data-ttu-id="6f547-154">新-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f547-154">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="6f547-155">移除-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f547-155">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="6f547-156">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="6f547-156">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


