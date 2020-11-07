---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6396AEC3-DFE6-45DA-BCF4-69C55C5D051B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyDefinition.md
ms.openlocfilehash: 66901872a6a7c3e871ce95287b45966aee974b52
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795320"
---
# <span data-ttu-id="f08a9-101">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f08a9-101">Get-AzPolicyDefinition</span></span>

## <span data-ttu-id="f08a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f08a9-102">SYNOPSIS</span></span>
<span data-ttu-id="f08a9-103">取得原則定義。</span><span class="sxs-lookup"><span data-stu-id="f08a9-103">Gets policy definitions.</span></span>

## <span data-ttu-id="f08a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="f08a9-104">SYNTAX</span></span>

### <span data-ttu-id="f08a9-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f08a9-105">NameParameterSet (Default)</span></span>
```
Get-AzPolicyDefinition [-Name <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f08a9-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f08a9-106">ManagementGroupNameParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -ManagementGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f08a9-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f08a9-107">SubscriptionIdParameterSet</span></span>
```
Get-AzPolicyDefinition [-Name <String>] -SubscriptionId <Guid> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f08a9-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f08a9-108">IdParameterSet</span></span>
```
Get-AzPolicyDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f08a9-109">BuiltinFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="f08a9-109">BuiltinFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Builtin]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f08a9-110">CustomFilterParameterSet</span><span class="sxs-lookup"><span data-stu-id="f08a9-110">CustomFilterParameterSet</span></span>
```
Get-AzPolicyDefinition [-ManagementGroupName <String>] [-SubscriptionId <Guid>] [-Custom]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f08a9-111">說明</span><span class="sxs-lookup"><span data-stu-id="f08a9-111">DESCRIPTION</span></span>
<span data-ttu-id="f08a9-112">**AzPolicyDefinition** Cmdlet 會取得原則定義或由名稱或 ID 所識別的特定原則定義的集合。</span><span class="sxs-lookup"><span data-stu-id="f08a9-112">The **Get-AzPolicyDefinition** cmdlet gets a collection of policy definitions or a specific policy definition identified by name or ID.</span></span>

## <span data-ttu-id="f08a9-113">示例</span><span class="sxs-lookup"><span data-stu-id="f08a9-113">EXAMPLES</span></span>

### <span data-ttu-id="f08a9-114">範例1：取得所有原則定義</span><span class="sxs-lookup"><span data-stu-id="f08a9-114">Example 1: Get all policy definitions</span></span>
```
PS C:\> Get-AzPolicyDefinition
```

<span data-ttu-id="f08a9-115">這個命令會取得所有原則定義。</span><span class="sxs-lookup"><span data-stu-id="f08a9-115">This command gets all the policy definitions.</span></span>

### <span data-ttu-id="f08a9-116">範例2：透過名稱從目前的訂閱取得原則定義</span><span class="sxs-lookup"><span data-stu-id="f08a9-116">Example 2: Get policy definition from current subscription by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
```

<span data-ttu-id="f08a9-117">這個命令會從目前的預設訂閱取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="f08a9-117">This command gets the policy definition named VMPolicyDefinition from the current default subscription.</span></span>

### <span data-ttu-id="f08a9-118">範例3：從管理群組依名稱取得原則定義</span><span class="sxs-lookup"><span data-stu-id="f08a9-118">Example 3: Get policy definition from management group by name</span></span>
```
PS C:\> Get-AzPolicyDefinition -Name 'VMPolicyDefinition' -ManagementGroupName 'Dept42'
```

<span data-ttu-id="f08a9-119">這個命令會從名為 Dept42 的管理群組中取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="f08a9-119">This command gets the policy definition named VMPolicyDefinition from the management group named Dept42.</span></span>

### <span data-ttu-id="f08a9-120">範例4：從訂閱取得所有內建原則定義</span><span class="sxs-lookup"><span data-stu-id="f08a9-120">Example 4: Get all built-in policy definitions from subscription</span></span>
```
PS C:\> Get-AzPolicyDefinition -SubscriptionId '3bf44b72-c631-427a-b8c8-53e2595398ca' -Builtin
```

<span data-ttu-id="f08a9-121">這個命令會從 ID 為3bf44b72-c631-427a-b8c8-53e2595398ca 的訂閱中取得所有內建的原則定義。</span><span class="sxs-lookup"><span data-stu-id="f08a9-121">This command gets all built-in policy definitions from the subscription with ID 3bf44b72-c631-427a-b8c8-53e2595398ca.</span></span>

## <span data-ttu-id="f08a9-122">參數</span><span class="sxs-lookup"><span data-stu-id="f08a9-122">PARAMETERS</span></span>

### <span data-ttu-id="f08a9-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f08a9-123">-ApiVersion</span></span>
<span data-ttu-id="f08a9-124">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f08a9-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f08a9-125">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="f08a9-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="f08a9-126">-內建</span><span class="sxs-lookup"><span data-stu-id="f08a9-126">-Builtin</span></span>
<span data-ttu-id="f08a9-127">將結果清單限制為僅限內建的原則定義。</span><span class="sxs-lookup"><span data-stu-id="f08a9-127">Limits list of results to only built-in policy definitions.</span></span>

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

### <span data-ttu-id="f08a9-128">-自訂</span><span class="sxs-lookup"><span data-stu-id="f08a9-128">-Custom</span></span>
<span data-ttu-id="f08a9-129">將結果清單限制為僅限自訂原則定義。</span><span class="sxs-lookup"><span data-stu-id="f08a9-129">Limits list of results to only custom policy definitions.</span></span>

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

### <span data-ttu-id="f08a9-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f08a9-130">-DefaultProfile</span></span>
<span data-ttu-id="f08a9-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f08a9-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f08a9-132">-識別碼</span><span class="sxs-lookup"><span data-stu-id="f08a9-132">-Id</span></span>
<span data-ttu-id="f08a9-133">指定此 Cmdlet 所取得之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f08a9-133">Specifies the fully qualified resource ID for the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f08a9-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="f08a9-134">-InformationAction</span></span>
<span data-ttu-id="f08a9-135">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="f08a9-135">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="f08a9-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f08a9-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f08a9-137">持續</span><span class="sxs-lookup"><span data-stu-id="f08a9-137">Continue</span></span>
- <span data-ttu-id="f08a9-138">理會</span><span class="sxs-lookup"><span data-stu-id="f08a9-138">Ignore</span></span>
- <span data-ttu-id="f08a9-139">看</span><span class="sxs-lookup"><span data-stu-id="f08a9-139">Inquire</span></span>
- <span data-ttu-id="f08a9-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f08a9-140">SilentlyContinue</span></span>
- <span data-ttu-id="f08a9-141">停止</span><span class="sxs-lookup"><span data-stu-id="f08a9-141">Stop</span></span>
- <span data-ttu-id="f08a9-142">封存</span><span class="sxs-lookup"><span data-stu-id="f08a9-142">Suspend</span></span>

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

### <span data-ttu-id="f08a9-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f08a9-143">-InformationVariable</span></span>
<span data-ttu-id="f08a9-144">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="f08a9-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f08a9-145">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="f08a9-145">-ManagementGroupName</span></span>
<span data-ttu-id="f08a9-146">原則定義的管理群組名稱 (s) 取得。</span><span class="sxs-lookup"><span data-stu-id="f08a9-146">The name of the management group of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="f08a9-147">-名稱</span><span class="sxs-lookup"><span data-stu-id="f08a9-147">-Name</span></span>
<span data-ttu-id="f08a9-148">指定此 Cmdlet 所取得之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="f08a9-148">Specifies the name of the policy definition that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f08a9-149">-預先</span><span class="sxs-lookup"><span data-stu-id="f08a9-149">-Pre</span></span>
<span data-ttu-id="f08a9-150">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f08a9-150">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="f08a9-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f08a9-151">-SubscriptionId</span></span>
<span data-ttu-id="f08a9-152">原則定義的訂閱識別碼， (s) 取得。</span><span class="sxs-lookup"><span data-stu-id="f08a9-152">The subscription ID of the policy definition(s) to get.</span></span>

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

### <span data-ttu-id="f08a9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f08a9-153">CommonParameters</span></span>
<span data-ttu-id="f08a9-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f08a9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f08a9-155">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f08a9-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f08a9-156">輸入</span><span class="sxs-lookup"><span data-stu-id="f08a9-156">INPUTS</span></span>

## <span data-ttu-id="f08a9-157">輸出</span><span class="sxs-lookup"><span data-stu-id="f08a9-157">OUTPUTS</span></span>

## <span data-ttu-id="f08a9-158">筆記</span><span class="sxs-lookup"><span data-stu-id="f08a9-158">NOTES</span></span>

## <span data-ttu-id="f08a9-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="f08a9-159">RELATED LINKS</span></span>

[<span data-ttu-id="f08a9-160">新-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f08a9-160">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="f08a9-161">移除-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f08a9-161">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)

[<span data-ttu-id="f08a9-162">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f08a9-162">Set-AzPolicyDefinition</span></span>](./Set-AzPolicyDefinition.md)


