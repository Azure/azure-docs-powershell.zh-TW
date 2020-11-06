---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 78dc06f53a94f6fe1524189a0cea32f214439f66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620876"
---
# <span data-ttu-id="929b3-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="929b3-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="929b3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="929b3-102">SYNOPSIS</span></span>
<span data-ttu-id="929b3-103">取得原則定義。</span><span class="sxs-lookup"><span data-stu-id="929b3-103">Gets policy definitions.</span></span>

## <span data-ttu-id="929b3-104">句法</span><span class="sxs-lookup"><span data-stu-id="929b3-104">SYNTAX</span></span>

### <span data-ttu-id="929b3-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="929b3-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="929b3-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="929b3-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="929b3-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="929b3-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="929b3-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="929b3-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="929b3-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="929b3-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="929b3-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="929b3-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="929b3-111">說明</span><span class="sxs-lookup"><span data-stu-id="929b3-111">DESCRIPTION</span></span>
<span data-ttu-id="929b3-112">**AzPolicyDefinition** Cmdlet 會取得原則定義或由名稱或 ID 所識別的特定原則定義的集合。</span><span class="sxs-lookup"><span data-stu-id="929b3-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="929b3-113">示例</span><span class="sxs-lookup"><span data-stu-id="929b3-113">EXAMPLES</span></span>

### <span data-ttu-id="929b3-114">範例1：取得所有原則定義</span><span class="sxs-lookup"><span data-stu-id="929b3-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="929b3-115">這個命令會取得所有原則定義。</span><span class="sxs-lookup"><span data-stu-id="929b3-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="929b3-116">範例2：透過名稱從目前的訂閱取得原則定義</span><span class="sxs-lookup"><span data-stu-id="929b3-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="929b3-117">這個命令會從目前的預設訂閱取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="929b3-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="929b3-118">範例3：從管理群組依名稱取得原則定義</span><span class="sxs-lookup"><span data-stu-id="929b3-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="929b3-119">這個命令會從名為 Dept42 的管理群組中取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="929b3-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="929b3-120">範例4：從訂閱取得所有內建原則定義</span><span class="sxs-lookup"><span data-stu-id="929b3-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="929b3-121">這個命令會從 ID 為3bf44b72-c631-427a-b8c8-53e2595398ca 的訂閱中取得所有內建的原則定義。</span><span class="sxs-lookup"><span data-stu-id="929b3-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="929b3-122">參數</span><span class="sxs-lookup"><span data-stu-id="929b3-122">PARAMETERS</span></span>

### <span data-ttu-id="929b3-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="929b3-123">-ApiVersion</span></span>
<span data-ttu-id="929b3-124">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="929b3-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="929b3-125">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="929b3-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="929b3-126">-內建</span><span class="sxs-lookup"><span data-stu-id="929b3-126">-Builtin</span></span>
<span data-ttu-id="929b3-127">將結果清單限制為僅限內建的原則定義。</span><span class="sxs-lookup"><span data-stu-id="929b3-127">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="929b3-128">-自訂</span><span class="sxs-lookup"><span data-stu-id="929b3-128">-Custom</span></span>
<span data-ttu-id="929b3-129">將結果清單限制為僅限自訂原則定義。</span><span class="sxs-lookup"><span data-stu-id="929b3-129">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="929b3-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="929b3-130">-DefaultProfile</span></span>
<span data-ttu-id="929b3-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="929b3-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="929b3-132">-識別碼</span><span class="sxs-lookup"><span data-stu-id="929b3-132">-Id</span></span>
<span data-ttu-id="929b3-133">指定此 Cmdlet 所取得之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="929b3-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="929b3-134">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="929b3-134">-ManagementGroupName</span></span>
<span data-ttu-id="929b3-135">原則定義的管理群組名稱 (s) 取得。</span><span class="sxs-lookup"><span data-stu-id="929b3-135">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="929b3-136">-名稱</span><span class="sxs-lookup"><span data-stu-id="929b3-136">-Name</span></span>
<span data-ttu-id="929b3-137">指定此 Cmdlet 所取得之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="929b3-137">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="929b3-138">-預先</span><span class="sxs-lookup"><span data-stu-id="929b3-138">-Pre</span></span>
<span data-ttu-id="929b3-139">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="929b3-139">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="929b3-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="929b3-140">-SubscriptionId</span></span>
<span data-ttu-id="929b3-141">原則定義的訂閱識別碼， (s) 取得。</span><span class="sxs-lookup"><span data-stu-id="929b3-141">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="929b3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="929b3-142">CommonParameters</span></span>
<span data-ttu-id="929b3-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="929b3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="929b3-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="929b3-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="929b3-145">輸入</span><span class="sxs-lookup"><span data-stu-id="929b3-145">INPUTS</span></span>

### <span data-ttu-id="929b3-146">System.object</span><span class="sxs-lookup"><span data-stu-id="929b3-146">System.String</span></span>

### <span data-ttu-id="929b3-147">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="929b3-147">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="929b3-148">輸出</span><span class="sxs-lookup"><span data-stu-id="929b3-148">OUTPUTS</span></span>

### <span data-ttu-id="929b3-149">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="929b3-149">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="929b3-150">筆記</span><span class="sxs-lookup"><span data-stu-id="929b3-150">NOTES</span></span>

## <span data-ttu-id="929b3-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="929b3-151">RELATED LINKS</span></span>

[<span data-ttu-id="929b3-152">新-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="929b3-152">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="929b3-153">移除-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="929b3-153">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="929b3-154">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="929b3-154">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


