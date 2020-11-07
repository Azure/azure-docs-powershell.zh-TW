---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 102d297f53fe51779f8831e4890c7d55bb59d2eb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795203"
---
# <span data-ttu-id="d8de3-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d8de3-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="d8de3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8de3-102">SYNOPSIS</span></span>
<span data-ttu-id="d8de3-103">修改原則分派。</span><span class="sxs-lookup"><span data-stu-id="d8de3-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="d8de3-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8de3-104">SYNTAX</span></span>

### <span data-ttu-id="d8de3-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d8de3-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d8de3-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8de3-106">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d8de3-107">說明</span><span class="sxs-lookup"><span data-stu-id="d8de3-107">DESCRIPTION</span></span>
<span data-ttu-id="d8de3-108">**AzPolicyAssignment** Cmdlet 會修改原則指派。</span><span class="sxs-lookup"><span data-stu-id="d8de3-108">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="d8de3-109">依識別碼或名稱和範圍指定作業。</span><span class="sxs-lookup"><span data-stu-id="d8de3-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="d8de3-110">示例</span><span class="sxs-lookup"><span data-stu-id="d8de3-110">EXAMPLES</span></span>

### <span data-ttu-id="d8de3-111">範例1：更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="d8de3-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="d8de3-112">第一個命令會使用 Get-AzResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="d8de3-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="d8de3-113">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="d8de3-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="d8de3-114">第二個命令會使用 Get-AzPolicyAssignment Cmdlet 來取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="d8de3-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="d8de3-115">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="d8de3-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="d8de3-116">最後一個命令會更新由 $ResourceGroup 的 **ResourceId** 屬性所識別之資源群組上的原則指派顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d8de3-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="d8de3-117">範例2：在原則指派中加入 managed 身分識別</span><span class="sxs-lookup"><span data-stu-id="d8de3-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="d8de3-118">第一個命令會使用 Get-AzPolicyAssignment Cmdlet，從目前訂閱取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="d8de3-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="d8de3-119">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="d8de3-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="d8de3-120">最終命令會為原則指派指派受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="d8de3-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="d8de3-121">參數</span><span class="sxs-lookup"><span data-stu-id="d8de3-121">PARAMETERS</span></span>

### <span data-ttu-id="d8de3-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d8de3-122">-ApiVersion</span></span>
<span data-ttu-id="d8de3-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d8de3-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d8de3-124">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="d8de3-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d8de3-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d8de3-125">-AssignIdentity</span></span>
<span data-ttu-id="d8de3-126">針對此原則指派產生並指派 Azure Active Directory 身分識別。</span><span class="sxs-lookup"><span data-stu-id="d8de3-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="d8de3-127">在執行「deployIfNotExists」原則的部署時，就會使用該身分識別。</span><span class="sxs-lookup"><span data-stu-id="d8de3-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="d8de3-128">指派身分識別時，位置是必要的。</span><span class="sxs-lookup"><span data-stu-id="d8de3-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="d8de3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8de3-129">-DefaultProfile</span></span>
<span data-ttu-id="d8de3-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d8de3-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8de3-131">-描述</span><span class="sxs-lookup"><span data-stu-id="d8de3-131">-Description</span></span>
<span data-ttu-id="d8de3-132">原則指派的描述</span><span class="sxs-lookup"><span data-stu-id="d8de3-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="d8de3-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d8de3-133">-DisplayName</span></span>
<span data-ttu-id="d8de3-134">指定原則指派的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="d8de3-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="d8de3-135">-識別碼</span><span class="sxs-lookup"><span data-stu-id="d8de3-135">-Id</span></span>
<span data-ttu-id="d8de3-136">指定此 Cmdlet 所修改之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d8de3-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="d8de3-137">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d8de3-137">-InformationAction</span></span>
<span data-ttu-id="d8de3-138">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="d8de3-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="d8de3-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d8de3-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8de3-140">持續</span><span class="sxs-lookup"><span data-stu-id="d8de3-140">Continue</span></span>
- <span data-ttu-id="d8de3-141">理會</span><span class="sxs-lookup"><span data-stu-id="d8de3-141">Ignore</span></span>
- <span data-ttu-id="d8de3-142">看</span><span class="sxs-lookup"><span data-stu-id="d8de3-142">Inquire</span></span>
- <span data-ttu-id="d8de3-143">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d8de3-143">SilentlyContinue</span></span>
- <span data-ttu-id="d8de3-144">停止</span><span class="sxs-lookup"><span data-stu-id="d8de3-144">Stop</span></span>
- <span data-ttu-id="d8de3-145">封存</span><span class="sxs-lookup"><span data-stu-id="d8de3-145">Suspend</span></span>

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

### <span data-ttu-id="d8de3-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d8de3-146">-InformationVariable</span></span>
<span data-ttu-id="d8de3-147">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="d8de3-147">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d8de3-148">-位置</span><span class="sxs-lookup"><span data-stu-id="d8de3-148">-Location</span></span>
<span data-ttu-id="d8de3-149">原則指派資源身分識別的位置。</span><span class="sxs-lookup"><span data-stu-id="d8de3-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="d8de3-150">使用-AssignIdentity 切換時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="d8de3-150">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="d8de3-151">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="d8de3-151">-Metadata</span></span>
<span data-ttu-id="d8de3-152">原則指派的更新中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d8de3-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="d8de3-153">這可以是包含中繼資料之檔案名的路徑，或是中繼資料作為字串。</span><span class="sxs-lookup"><span data-stu-id="d8de3-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="d8de3-154">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8de3-154">-Name</span></span>
<span data-ttu-id="d8de3-155">指定此 Cmdlet 所修改之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8de3-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8de3-156">-NotScope</span><span class="sxs-lookup"><span data-stu-id="d8de3-156">-NotScope</span></span>
<span data-ttu-id="d8de3-157">原則指派不是作用中的範圍。</span><span class="sxs-lookup"><span data-stu-id="d8de3-157">The policy assignment not scopes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8de3-158">-預先</span><span class="sxs-lookup"><span data-stu-id="d8de3-158">-Pre</span></span>
<span data-ttu-id="d8de3-159">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="d8de3-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d8de3-160">-範圍</span><span class="sxs-lookup"><span data-stu-id="d8de3-160">-Scope</span></span>
<span data-ttu-id="d8de3-161">指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="d8de3-161">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8de3-162">-Sku</span><span class="sxs-lookup"><span data-stu-id="d8de3-162">-Sku</span></span>
<span data-ttu-id="d8de3-163">代表 sku 屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d8de3-163">A hash table which represents sku properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8de3-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8de3-164">CommonParameters</span></span>
<span data-ttu-id="d8de3-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8de3-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8de3-166">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8de3-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8de3-167">輸入</span><span class="sxs-lookup"><span data-stu-id="d8de3-167">INPUTS</span></span>

## <span data-ttu-id="d8de3-168">輸出</span><span class="sxs-lookup"><span data-stu-id="d8de3-168">OUTPUTS</span></span>

## <span data-ttu-id="d8de3-169">筆記</span><span class="sxs-lookup"><span data-stu-id="d8de3-169">NOTES</span></span>

## <span data-ttu-id="d8de3-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8de3-170">RELATED LINKS</span></span>

[<span data-ttu-id="d8de3-171">AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d8de3-171">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="d8de3-172">新-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d8de3-172">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="d8de3-173">移除-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d8de3-173">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


