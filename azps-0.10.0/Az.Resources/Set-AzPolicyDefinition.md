---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: E1AC7139-786C-4DD6-A898-242723E0D159
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyDefinition.md
ms.openlocfilehash: feddd9645b22c554d5e78813194ecc8837fdf3fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795200"
---
# <span data-ttu-id="8bd70-101">Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8bd70-101">Set-AzPolicyDefinition</span></span>

## <span data-ttu-id="8bd70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8bd70-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd70-103">修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="8bd70-103">Modifies a policy definition.</span></span>

## <span data-ttu-id="8bd70-104">句法</span><span class="sxs-lookup"><span data-stu-id="8bd70-104">SYNTAX</span></span>

### <span data-ttu-id="8bd70-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8bd70-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8bd70-106">ManagementGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bd70-106">ManagementGroupNameParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -ManagementGroupName <String>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8bd70-107">SubscriptionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bd70-107">SubscriptionIdParameterSet</span></span>
```
Set-AzPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] -SubscriptionId <Guid>
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8bd70-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8bd70-108">IdParameterSet</span></span>
```
Set-AzPolicyDefinition -Id <String> [-DisplayName <String>] [-Description <String>] [-Policy <String>]
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8bd70-109">說明</span><span class="sxs-lookup"><span data-stu-id="8bd70-109">DESCRIPTION</span></span>
<span data-ttu-id="8bd70-110">**AzPolicyDefinition** Cmdlet 會修改原則定義。</span><span class="sxs-lookup"><span data-stu-id="8bd70-110">The **Set-AzPolicyDefinition** cmdlet modifies a policy definition.</span></span>

## <span data-ttu-id="8bd70-111">示例</span><span class="sxs-lookup"><span data-stu-id="8bd70-111">EXAMPLES</span></span>

### <span data-ttu-id="8bd70-112">範例1：更新原則定義的描述</span><span class="sxs-lookup"><span data-stu-id="8bd70-112">Example 1: Update the description of a policy definition</span></span>
```
PS C:\> $PolicyDefinition = Get-AzPolicyDefinition -Name 'VMPolicyDefinition'
PS C:\> Set-AzPolicyDefinition -Id $PolicyDefinition.ResourceId -Description 'Updated policy to not allow virtual machine creation'
```

<span data-ttu-id="8bd70-113">第一個命令會使用 Get-AzPolicyDefinition Cmdlet 來取得名為 VMPolicyDefinition 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="8bd70-113">The first command gets a policy definition named VMPolicyDefinition by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="8bd70-114">該命令會將該物件儲存在 $PolicyDefinition 變數中。</span><span class="sxs-lookup"><span data-stu-id="8bd70-114">The command stores that object in the $PolicyDefinition variable.</span></span>
<span data-ttu-id="8bd70-115">第二個命令會更新 $PolicyDefinition 的 **ResourceId** 屬性所識別之原則定義的描述。</span><span class="sxs-lookup"><span data-stu-id="8bd70-115">The second command updates the description of the policy definition identified by the **ResourceId** property of $PolicyDefinition.</span></span>

### <span data-ttu-id="8bd70-116">範例2：更新原則定義的模式</span><span class="sxs-lookup"><span data-stu-id="8bd70-116">Example 2: Update the mode of a policy definition</span></span>
```
PS C:\> Set-AzPolicyDefinition -Name 'VMPolicyDefinition' -Mode 'All'
```

<span data-ttu-id="8bd70-117">這個命令會使用 Set-AzPolicyDefinition Cmdlet 來更新名為 VMPolicyDefinition 的原則定義，將其 mode 屬性設定為 ' All」。</span><span class="sxs-lookup"><span data-stu-id="8bd70-117">This command updates the policy definition named VMPolicyDefinition by using the Set-AzPolicyDefinition cmdlet to set its mode property to 'All'.</span></span>

## <span data-ttu-id="8bd70-118">參數</span><span class="sxs-lookup"><span data-stu-id="8bd70-118">PARAMETERS</span></span>

### <span data-ttu-id="8bd70-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8bd70-119">-ApiVersion</span></span>
<span data-ttu-id="8bd70-120">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8bd70-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8bd70-121">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="8bd70-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="8bd70-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd70-122">-DefaultProfile</span></span>
<span data-ttu-id="8bd70-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8bd70-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bd70-124">-描述</span><span class="sxs-lookup"><span data-stu-id="8bd70-124">-Description</span></span>
<span data-ttu-id="8bd70-125">指定原則定義的新描述。</span><span class="sxs-lookup"><span data-stu-id="8bd70-125">Specifies a new description for the policy definition.</span></span>

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

### <span data-ttu-id="8bd70-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8bd70-126">-DisplayName</span></span>
<span data-ttu-id="8bd70-127">指定原則定義的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8bd70-127">Specifies a new display name for the policy definition.</span></span>

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

### <span data-ttu-id="8bd70-128">-識別碼</span><span class="sxs-lookup"><span data-stu-id="8bd70-128">-Id</span></span>
<span data-ttu-id="8bd70-129">指定此 Cmdlet 所修改之原則定義的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bd70-129">Specifies the fully qualified resource ID for the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8bd70-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8bd70-130">-InformationAction</span></span>
<span data-ttu-id="8bd70-131">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8bd70-131">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="8bd70-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8bd70-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8bd70-133">持續</span><span class="sxs-lookup"><span data-stu-id="8bd70-133">Continue</span></span>
- <span data-ttu-id="8bd70-134">理會</span><span class="sxs-lookup"><span data-stu-id="8bd70-134">Ignore</span></span>
- <span data-ttu-id="8bd70-135">看</span><span class="sxs-lookup"><span data-stu-id="8bd70-135">Inquire</span></span>
- <span data-ttu-id="8bd70-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8bd70-136">SilentlyContinue</span></span>
- <span data-ttu-id="8bd70-137">停止</span><span class="sxs-lookup"><span data-stu-id="8bd70-137">Stop</span></span>
- <span data-ttu-id="8bd70-138">封存</span><span class="sxs-lookup"><span data-stu-id="8bd70-138">Suspend</span></span>

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

### <span data-ttu-id="8bd70-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8bd70-139">-InformationVariable</span></span>
<span data-ttu-id="8bd70-140">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8bd70-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8bd70-141">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="8bd70-141">-ManagementGroupName</span></span>
<span data-ttu-id="8bd70-142">要更新之原則定義之管理群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bd70-142">The name of the management group of the policy definition to update.</span></span>

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

### <span data-ttu-id="8bd70-143">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="8bd70-143">-Metadata</span></span>
<span data-ttu-id="8bd70-144">原則定義的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8bd70-144">The metadata for policy definition.</span></span> <span data-ttu-id="8bd70-145">這可以是包含中繼資料之檔案名的路徑，或以字串形式的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8bd70-145">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

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

### <span data-ttu-id="8bd70-146">模式</span><span class="sxs-lookup"><span data-stu-id="8bd70-146">-Mode</span></span>
<span data-ttu-id="8bd70-147">新原則定義的模式。</span><span class="sxs-lookup"><span data-stu-id="8bd70-147">The mode of the new policy definition.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bd70-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="8bd70-148">-Name</span></span>
<span data-ttu-id="8bd70-149">指定此 Cmdlet 所修改之原則定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="8bd70-149">Specifies the name of the policy definition that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="8bd70-150">-參數</span><span class="sxs-lookup"><span data-stu-id="8bd70-150">-Parameter</span></span>
<span data-ttu-id="8bd70-151">原則定義的參數宣告。</span><span class="sxs-lookup"><span data-stu-id="8bd70-151">The parameters declaration for policy definition.</span></span> <span data-ttu-id="8bd70-152">這可以是包含參數宣告之檔案名或 uri 的路徑，或是參數宣告（字串）。</span><span class="sxs-lookup"><span data-stu-id="8bd70-152">This can either be a path to a file name or uri containing the parameters declaration, or the parameters declaration as string.</span></span>

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

### <span data-ttu-id="8bd70-153">-原則</span><span class="sxs-lookup"><span data-stu-id="8bd70-153">-Policy</span></span>
<span data-ttu-id="8bd70-154">指定原則定義的新原則規則。</span><span class="sxs-lookup"><span data-stu-id="8bd70-154">Specifies new policy rule for the policy definition.</span></span>
<span data-ttu-id="8bd70-155">您可以指定 json 檔案的路徑，或是包含 JavaScript 物件符號 (JSON) 格式之原則的字串。</span><span class="sxs-lookup"><span data-stu-id="8bd70-155">You can specify the path of a .json file or a string that contains the policy in JavaScript Object Notation (JSON) format.</span></span>

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

### <span data-ttu-id="8bd70-156">-預先</span><span class="sxs-lookup"><span data-stu-id="8bd70-156">-Pre</span></span>
<span data-ttu-id="8bd70-157">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="8bd70-157">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8bd70-158">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8bd70-158">-SubscriptionId</span></span>
<span data-ttu-id="8bd70-159">要更新之原則定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8bd70-159">The subscription ID of the policy definition to update.</span></span>

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

### <span data-ttu-id="8bd70-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd70-160">CommonParameters</span></span>
<span data-ttu-id="8bd70-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8bd70-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd70-162">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8bd70-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd70-163">輸入</span><span class="sxs-lookup"><span data-stu-id="8bd70-163">INPUTS</span></span>

## <span data-ttu-id="8bd70-164">輸出</span><span class="sxs-lookup"><span data-stu-id="8bd70-164">OUTPUTS</span></span>

## <span data-ttu-id="8bd70-165">筆記</span><span class="sxs-lookup"><span data-stu-id="8bd70-165">NOTES</span></span>

## <span data-ttu-id="8bd70-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="8bd70-166">RELATED LINKS</span></span>

[<span data-ttu-id="8bd70-167">AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8bd70-167">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="8bd70-168">新-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8bd70-168">New-AzPolicyDefinition</span></span>](./New-AzPolicyDefinition.md)

[<span data-ttu-id="8bd70-169">移除-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="8bd70-169">Remove-AzPolicyDefinition</span></span>](./Remove-AzPolicyDefinition.md)


