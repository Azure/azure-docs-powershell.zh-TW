---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: dc54d84886bc9c13fa6a4ecef4e41ef80fa6d4e4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800693"
---
# <span data-ttu-id="106ac-101">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="106ac-101">Set-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="106ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="106ac-102">SYNOPSIS</span></span>
<span data-ttu-id="106ac-103">修改原則分派。</span><span class="sxs-lookup"><span data-stu-id="106ac-103">Modifies a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="106ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="106ac-104">SYNTAX</span></span>

### <span data-ttu-id="106ac-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="106ac-105">NameParameterSet (Default)</span></span>
```
Set-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="106ac-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="106ac-106">IdParameterSet</span></span>
```
Set-AzureRmPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="106ac-107">說明</span><span class="sxs-lookup"><span data-stu-id="106ac-107">DESCRIPTION</span></span>
<span data-ttu-id="106ac-108">**AzureRmPolicyAssignment** Cmdlet 會修改原則指派。</span><span class="sxs-lookup"><span data-stu-id="106ac-108">The **Set-AzureRmPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="106ac-109">依識別碼或名稱和範圍指定作業。</span><span class="sxs-lookup"><span data-stu-id="106ac-109">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="106ac-110">示例</span><span class="sxs-lookup"><span data-stu-id="106ac-110">EXAMPLES</span></span>

### <span data-ttu-id="106ac-111">範例1：更新顯示名稱</span><span class="sxs-lookup"><span data-stu-id="106ac-111">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="106ac-112">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="106ac-112">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="106ac-113">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="106ac-113">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="106ac-114">第二個命令會使用 Get-AzureRmPolicyAssignment Cmdlet 來取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="106ac-114">The second command gets the policy assignment named PolicyAssignment by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="106ac-115">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="106ac-115">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="106ac-116">最後一個命令會更新由 $ResourceGroup 的 **ResourceId** 屬性所識別之資源群組上的原則指派顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="106ac-116">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="106ac-117">範例2：在原則指派中加入 managed 身分識別</span><span class="sxs-lookup"><span data-stu-id="106ac-117">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzureRmPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzureRmPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="106ac-118">第一個命令會使用 Get-AzureRmPolicyAssignment Cmdlet，從目前訂閱取得名為 PolicyAssignment 的原則指派。</span><span class="sxs-lookup"><span data-stu-id="106ac-118">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzureRmPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="106ac-119">該命令會將該物件儲存在 $PolicyAssignment 變數中。</span><span class="sxs-lookup"><span data-stu-id="106ac-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="106ac-120">最終命令會為原則指派指派受管理的身分識別。</span><span class="sxs-lookup"><span data-stu-id="106ac-120">The final command assigns a managed identity to the policy assignment.</span></span>

## <span data-ttu-id="106ac-121">參數</span><span class="sxs-lookup"><span data-stu-id="106ac-121">PARAMETERS</span></span>

### <span data-ttu-id="106ac-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="106ac-122">-ApiVersion</span></span>
<span data-ttu-id="106ac-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="106ac-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="106ac-124">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="106ac-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="106ac-125">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="106ac-125">-AssignIdentity</span></span>
<span data-ttu-id="106ac-126">針對此原則指派產生並指派 Azure Active Directory 身分識別。</span><span class="sxs-lookup"><span data-stu-id="106ac-126">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="106ac-127">在執行「deployIfNotExists」原則的部署時，就會使用該身分識別。</span><span class="sxs-lookup"><span data-stu-id="106ac-127">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="106ac-128">指派身分識別時，位置是必要的。</span><span class="sxs-lookup"><span data-stu-id="106ac-128">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="106ac-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106ac-129">-DefaultProfile</span></span>
<span data-ttu-id="106ac-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="106ac-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="106ac-131">-描述</span><span class="sxs-lookup"><span data-stu-id="106ac-131">-Description</span></span>
<span data-ttu-id="106ac-132">原則指派的描述</span><span class="sxs-lookup"><span data-stu-id="106ac-132">The description for policy assignment</span></span>

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

### <span data-ttu-id="106ac-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="106ac-133">-DisplayName</span></span>
<span data-ttu-id="106ac-134">指定原則指派的新顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="106ac-134">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="106ac-135">-識別碼</span><span class="sxs-lookup"><span data-stu-id="106ac-135">-Id</span></span>
<span data-ttu-id="106ac-136">指定此 Cmdlet 所修改之原則指派的完全限定資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="106ac-136">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="106ac-137">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="106ac-137">-InformationAction</span></span>
<span data-ttu-id="106ac-138">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="106ac-138">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="106ac-139">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="106ac-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="106ac-140">持續</span><span class="sxs-lookup"><span data-stu-id="106ac-140">Continue</span></span>
- <span data-ttu-id="106ac-141">理會</span><span class="sxs-lookup"><span data-stu-id="106ac-141">Ignore</span></span>
- <span data-ttu-id="106ac-142">看</span><span class="sxs-lookup"><span data-stu-id="106ac-142">Inquire</span></span>
- <span data-ttu-id="106ac-143">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="106ac-143">SilentlyContinue</span></span>
- <span data-ttu-id="106ac-144">停止</span><span class="sxs-lookup"><span data-stu-id="106ac-144">Stop</span></span>
- <span data-ttu-id="106ac-145">封存</span><span class="sxs-lookup"><span data-stu-id="106ac-145">Suspend</span></span>

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

### <span data-ttu-id="106ac-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="106ac-146">-InformationVariable</span></span>
<span data-ttu-id="106ac-147">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="106ac-147">Specifies an information variable.</span></span>

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

### <span data-ttu-id="106ac-148">-位置</span><span class="sxs-lookup"><span data-stu-id="106ac-148">-Location</span></span>
<span data-ttu-id="106ac-149">原則指派資源身分識別的位置。</span><span class="sxs-lookup"><span data-stu-id="106ac-149">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="106ac-150">使用-AssignIdentity 切換時，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="106ac-150">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="106ac-151">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="106ac-151">-Metadata</span></span>
<span data-ttu-id="106ac-152">原則指派的更新中繼資料。</span><span class="sxs-lookup"><span data-stu-id="106ac-152">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="106ac-153">這可以是包含中繼資料之檔案名的路徑，或是中繼資料作為字串。</span><span class="sxs-lookup"><span data-stu-id="106ac-153">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="106ac-154">-名稱</span><span class="sxs-lookup"><span data-stu-id="106ac-154">-Name</span></span>
<span data-ttu-id="106ac-155">指定此 Cmdlet 所修改之原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="106ac-155">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="106ac-156">-NotScope</span><span class="sxs-lookup"><span data-stu-id="106ac-156">-NotScope</span></span>
<span data-ttu-id="106ac-157">原則指派不是作用中的範圍。</span><span class="sxs-lookup"><span data-stu-id="106ac-157">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="106ac-158">-預先</span><span class="sxs-lookup"><span data-stu-id="106ac-158">-Pre</span></span>
<span data-ttu-id="106ac-159">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="106ac-159">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="106ac-160">-範圍</span><span class="sxs-lookup"><span data-stu-id="106ac-160">-Scope</span></span>
<span data-ttu-id="106ac-161">指定應用原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="106ac-161">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="106ac-162">-Sku</span><span class="sxs-lookup"><span data-stu-id="106ac-162">-Sku</span></span>
<span data-ttu-id="106ac-163">代表 sku 屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="106ac-163">A hash table which represents sku properties.</span></span>

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

### <span data-ttu-id="106ac-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106ac-164">CommonParameters</span></span>
<span data-ttu-id="106ac-165">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="106ac-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106ac-166">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="106ac-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106ac-167">輸入</span><span class="sxs-lookup"><span data-stu-id="106ac-167">INPUTS</span></span>

## <span data-ttu-id="106ac-168">輸出</span><span class="sxs-lookup"><span data-stu-id="106ac-168">OUTPUTS</span></span>

## <span data-ttu-id="106ac-169">筆記</span><span class="sxs-lookup"><span data-stu-id="106ac-169">NOTES</span></span>

## <span data-ttu-id="106ac-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="106ac-170">RELATED LINKS</span></span>

[<span data-ttu-id="106ac-171">AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="106ac-171">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="106ac-172">新-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="106ac-172">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="106ac-173">移除-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="106ac-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)


