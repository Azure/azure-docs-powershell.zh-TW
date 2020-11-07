---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicysetdefinition
schema: 2.0.0
ms.openlocfilehash: 2e5bc38e8fa98160df66cdfc29bbd249ab56b809
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802181"
---
# <span data-ttu-id="bc391-101">Set-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="bc391-101">Set-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="bc391-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc391-102">SYNOPSIS</span></span>
<span data-ttu-id="bc391-103">修改原則集定義</span><span class="sxs-lookup"><span data-stu-id="bc391-103">Modifies a policy set definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc391-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc391-104">SYNTAX</span></span>

### <span data-ttu-id="bc391-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bc391-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc391-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc391-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc391-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc391-107">SubscriptionIdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc391-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc391-108">IdParameterSet</span></span>
```
Set-AzureRmPolicySetDefinition -Id <String> [-DisplayName <String>] [-Description <String>]
 [-PolicyDefinition <String>] [-Metadata <String>] [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc391-109">說明</span><span class="sxs-lookup"><span data-stu-id="bc391-109">DESCRIPTION</span></span>
<span data-ttu-id="bc391-110">**AzureRmPolicySetDefinition** Cmdlet 會修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="bc391-110">The **Set-AzureRmPolicySetDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="bc391-111">示例</span><span class="sxs-lookup"><span data-stu-id="bc391-111">EXAMPLES</span></span>

### <span data-ttu-id="bc391-112">範例1：更新原則集定義的描述</span><span class="sxs-lookup"><span data-stu-id="bc391-112">Example 1: Update the description of a policy set definition</span></span>
```
PS C:\> $PolicySetDefinition = Get-AzureRmPolicySetDefinition -ResourceId '/subscriptions/mySub/Microsoft.Authorization/policySetDefinitions/myPSSetDefinition'
PS C:\> Set-AzureRmPolicySetDefinition -Id $PolicySetDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="bc391-113">第一個命令會使用 Get-AzureRmPolicySetDefinition Cmdlet 來取得原則集定義。</span><span class="sxs-lookup"><span data-stu-id="bc391-113">The first command gets a policy set definition by using the Get-AzureRmPolicySetDefinition cmdlet.</span></span>
<span data-ttu-id="bc391-114">該命令會將該物件儲存在 $PolicySetDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="bc391-114">The command stores that object in the $PolicySetDefinition variable.</span></span>
<span data-ttu-id="bc391-115">第二個命令會更新由 $PolicySetDefinition 的 **ResourceId** 屬性所識別之原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="bc391-115">The second command updates the description of the policy set definition identified by the **ResourceId** property of $PolicySetDefinition.</span></span>

## <span data-ttu-id="bc391-116">參數</span><span class="sxs-lookup"><span data-stu-id="bc391-116">PARAMETERS</span></span>

### <span data-ttu-id="bc391-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bc391-117">-ApiVersion</span></span>
<span data-ttu-id="bc391-118">設定時，會指出要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="bc391-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="bc391-119">如果未指定，API 版本會自動決定為最新的可用。</span><span class="sxs-lookup"><span data-stu-id="bc391-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="bc391-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc391-120">-DefaultProfile</span></span>
<span data-ttu-id="bc391-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bc391-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc391-122">-描述</span><span class="sxs-lookup"><span data-stu-id="bc391-122">-Description</span></span>
<span data-ttu-id="bc391-123">原則集定義的描述。</span><span class="sxs-lookup"><span data-stu-id="bc391-123">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc391-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bc391-124">-DisplayName</span></span>
<span data-ttu-id="bc391-125">原則集定義的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="bc391-125">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc391-126">-識別碼</span><span class="sxs-lookup"><span data-stu-id="bc391-126">-Id</span></span>
<span data-ttu-id="bc391-127">完全合格的原則定義識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="bc391-127">The fully qualified policy definition Id, including the subscription.</span></span>
<span data-ttu-id="bc391-128">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="bc391-128">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

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

### <span data-ttu-id="bc391-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="bc391-129">-ManagementGroupName</span></span>
<span data-ttu-id="bc391-130">要更新之原則集定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bc391-130">The name of the management group of the policy set definition to update.</span></span>

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

### <span data-ttu-id="bc391-131">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="bc391-131">-Metadata</span></span>
<span data-ttu-id="bc391-132">更新之原則集定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="bc391-132">The metadata of the updated policy set definition.</span></span> <span data-ttu-id="bc391-133">這可以是包含中繼資料之檔案名的路徑，或是中繼資料作為字串。</span><span class="sxs-lookup"><span data-stu-id="bc391-133">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc391-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="bc391-134">-Name</span></span>
<span data-ttu-id="bc391-135">原則集定義名稱。</span><span class="sxs-lookup"><span data-stu-id="bc391-135">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ManagementGroupNameParameterSet, SubscriptionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc391-136">-參數</span><span class="sxs-lookup"><span data-stu-id="bc391-136">-Parameter</span></span>
<span data-ttu-id="bc391-137">更新之原則集定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="bc391-137">The parameters declaration of the updated policy set definition.</span></span> <span data-ttu-id="bc391-138">這可以是包含參數宣告之檔案名或 uri 的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="bc391-138">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as a string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc391-139">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="bc391-139">-PolicyDefinition</span></span>
<span data-ttu-id="bc391-140">原則集定義。</span><span class="sxs-lookup"><span data-stu-id="bc391-140">The policy set definition.</span></span> <span data-ttu-id="bc391-141">這可以是包含原則定義的檔案名路徑，或原則集定義（字串）。</span><span class="sxs-lookup"><span data-stu-id="bc391-141">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc391-142">-預先</span><span class="sxs-lookup"><span data-stu-id="bc391-142">-Pre</span></span>
<span data-ttu-id="bc391-143">設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。</span><span class="sxs-lookup"><span data-stu-id="bc391-143">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="bc391-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc391-144">-SubscriptionId</span></span>
<span data-ttu-id="bc391-145">要更新之原則集定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc391-145">The subscription ID of the policy set definition to update.</span></span>

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

### <span data-ttu-id="bc391-146">-確認</span><span class="sxs-lookup"><span data-stu-id="bc391-146">-Confirm</span></span>
<span data-ttu-id="bc391-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bc391-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc391-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc391-148">-WhatIf</span></span>
<span data-ttu-id="bc391-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc391-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bc391-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc391-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc391-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc391-151">CommonParameters</span></span>
<span data-ttu-id="bc391-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc391-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc391-153">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc391-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc391-154">輸入</span><span class="sxs-lookup"><span data-stu-id="bc391-154">INPUTS</span></span>

### <span data-ttu-id="bc391-155">System.object</span><span class="sxs-lookup"><span data-stu-id="bc391-155">System.String</span></span>

### <span data-ttu-id="bc391-156">系統. Nullable "1 [[System. Guid，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="bc391-156">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="bc391-157">輸出</span><span class="sxs-lookup"><span data-stu-id="bc391-157">OUTPUTS</span></span>

### <span data-ttu-id="bc391-158">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="bc391-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bc391-159">筆記</span><span class="sxs-lookup"><span data-stu-id="bc391-159">NOTES</span></span>

## <span data-ttu-id="bc391-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc391-160">RELATED LINKS</span></span>
