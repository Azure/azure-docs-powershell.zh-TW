---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: 4016809ed2592c5d10bc284e4a692381d7965107
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792185"
---
# <span data-ttu-id="23ff2-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23ff2-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="23ff2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23ff2-102">SYNOPSIS</span></span>
<span data-ttu-id="23ff2-103">修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="23ff2-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="23ff2-104">句法</span><span class="sxs-lookup"><span data-stu-id="23ff2-104">SYNTAX</span></span>

### <span data-ttu-id="23ff2-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="23ff2-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ff2-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23ff2-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ff2-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23ff2-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] -SubscriptionId <Guid> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ff2-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23ff2-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23ff2-109">說明</span><span class="sxs-lookup"><span data-stu-id="23ff2-109">DESCRIPTION</span></span>
<span data-ttu-id="23ff2-110">**AzPolicyDefinition** Cmdlet 會修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="23ff2-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="23ff2-111">示例</span><span class="sxs-lookup"><span data-stu-id="23ff2-111">EXAMPLES</span></span>

### <span data-ttu-id="23ff2-112">範例1：更新原則定義的描述</span><span class="sxs-lookup"><span data-stu-id="23ff2-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="23ff2-113">第一個命令會使用 Get-AzPolicyDefinition Cmdlet 來取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="23ff2-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="23ff2-114">該命令會將該物件儲存在 $PolicyDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="23ff2-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="23ff2-115">第二個命令會更新 $PolicyDefinition 的 **ResourceId** 屬性所識別之原則定義的描述。</span><span class="sxs-lookup"><span data-stu-id="23ff2-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="23ff2-116">範例2：更新原則定義的模式</span><span class="sxs-lookup"><span data-stu-id="23ff2-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="23ff2-117">這個命令會使用 Set-AzPolicyDefinition Cmdlet 來更新名為 VMPolicyDefinition 的原則定義，將其 mode 屬性設定為 ' All」。</span><span class="sxs-lookup"><span data-stu-id="23ff2-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

### <span data-ttu-id="23ff2-118">範例3：更新原則定義的中繼資料</span><span class="sxs-lookup"><span data-stu-id="23ff2-118">Example 3: Update the metadata of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Metadata '{"category":"Virtual Machine"}'


Name               : VMPolicyDefinition
ResourceId         : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
ResourceName       : VMPolicyDefinition
ResourceType       : Microsoft.Authorization/policyDefinitions
SubscriptionId     : 11111111-1111-1111-1111-111111111111
Properties         : @{displayName=VMPolicyDefinition; policyType=Custom; mode=All; metadata=; policyRule=}
PolicyDefinitionId : /subscriptions/11111111-1111-1111-1111-111111111111/providers/Microsoft.Authorization/policyDefinitions/VMPolicyDefinition
```

<span data-ttu-id="23ff2-119">這個命令會更新名為 VMPolicyDefinition 的原則定義中繼資料，以指出其類別是「虛擬機器」。</span><span class="sxs-lookup"><span data-stu-id="23ff2-119">This command updates the metadata of a policy definition named VMPolicyDefinition to indicate its category is "Virtual Machine".</span></span>

## <span data-ttu-id="23ff2-120">參數</span><span class="sxs-lookup"><span data-stu-id="23ff2-120">PARAMETERS</span></span>

### <span data-ttu-id="23ff2-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="23ff2-121">-ApiVersion</span></span>
<span data-ttu-id="23ff2-122">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="23ff2-122">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="23ff2-123">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="23ff2-123">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="23ff2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ff2-124">-DefaultProfile</span></span>
<span data-ttu-id="23ff2-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="23ff2-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23ff2-126">-描述</span><span class="sxs-lookup"><span data-stu-id="23ff2-126">-Description</span></span>
<span data-ttu-id="23ff2-127">指定原則定義的新描述。</span><span class="sxs-lookup"><span data-stu-id="23ff2-127">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="23ff2-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="23ff2-128">-DisplayName</span></span>
<span data-ttu-id="23ff2-129">指定原則定義的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="23ff2-129">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="23ff2-130">-識別碼</span><span class="sxs-lookup"><span data-stu-id="23ff2-130">-Id</span></span>
<span data-ttu-id="23ff2-131">指定此 Cmdlet 所修改之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="23ff2-131">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="23ff2-132">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="23ff2-132">-ManagementGroupName</span></span>
<span data-ttu-id="23ff2-133">要更新之原則定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="23ff2-133">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="23ff2-134">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="23ff2-134">-Metadata</span></span>
<span data-ttu-id="23ff2-135">原則定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="23ff2-135">The metadata for policy definition.</span></span> <span data-ttu-id="23ff2-136">這可以是包含中繼資料之檔案名的路徑，或以字串形式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="23ff2-136">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="23ff2-137">模式</span><span class="sxs-lookup"><span data-stu-id="23ff2-137">-Mode</span></span>
<span data-ttu-id="23ff2-138">新原則定義的模式。</span><span class="sxs-lookup"><span data-stu-id="23ff2-138">The mode of the new policy definition.</span></span>

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

### <span data-ttu-id="23ff2-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="23ff2-139">-Name</span></span>
<span data-ttu-id="23ff2-140">指定此 Cmdlet 所修改之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="23ff2-140">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="23ff2-141">-參數</span><span class="sxs-lookup"><span data-stu-id="23ff2-141">-Parameter</span></span>
<span data-ttu-id="23ff2-142">原則定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="23ff2-142">The parameters declaration for policy definition.</span></span> <span data-ttu-id="23ff2-143">這可以是包含參數宣告之檔案名或 uri 的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="23ff2-143">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="23ff2-144">-原則</span><span class="sxs-lookup"><span data-stu-id="23ff2-144">-Policy</span></span>
<span data-ttu-id="23ff2-145">指定原則定義的新原則規則。</span><span class="sxs-lookup"><span data-stu-id="23ff2-145">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="23ff2-146">您可以指定 json 檔案的路徑，或是包含 JavaScript 物件符號 (JSON) 格式之原則的字串。</span><span class="sxs-lookup"><span data-stu-id="23ff2-146">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="23ff2-147">-預先</span><span class="sxs-lookup"><span data-stu-id="23ff2-147">-Pre</span></span>
<span data-ttu-id="23ff2-148">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="23ff2-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="23ff2-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23ff2-149">-SubscriptionId</span></span>
<span data-ttu-id="23ff2-150">要更新之原則定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="23ff2-150">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="23ff2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ff2-151">CommonParameters</span></span>
<span data-ttu-id="23ff2-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23ff2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ff2-153">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="23ff2-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ff2-154">輸入</span><span class="sxs-lookup"><span data-stu-id="23ff2-154">INPUTS</span></span>

### <span data-ttu-id="23ff2-155">System.object</span><span class="sxs-lookup"><span data-stu-id="23ff2-155">System.String</span></span>

### <span data-ttu-id="23ff2-156">"CoreLib" 1 [[System. Guid.empty]、[System.] = 4.0.0.0、Culture = 中性、PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="23ff2-156">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="23ff2-157">輸出</span><span class="sxs-lookup"><span data-stu-id="23ff2-157">OUTPUTS</span></span>

### <span data-ttu-id="23ff2-158">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="23ff2-158">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="23ff2-159">筆記</span><span class="sxs-lookup"><span data-stu-id="23ff2-159">NOTES</span></span>

## <span data-ttu-id="23ff2-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="23ff2-160">RELATED LINKS</span></span>

[<span data-ttu-id="23ff2-161">AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23ff2-161">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="23ff2-162">新-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23ff2-162">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="23ff2-163">移除-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="23ff2-163">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


