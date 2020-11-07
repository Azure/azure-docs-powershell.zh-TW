---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: fa43b462cf06b9e2cd58df5d6796c098e942fafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625077"
---
# <span data-ttu-id="1cb58-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1cb58-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="1cb58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1cb58-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb58-103">建立原則指派。</span><span class="sxs-lookup"><span data-stu-id="1cb58-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cb58-104">句法</span><span class="sxs-lookup"><span data-stu-id="1cb58-104">SYNTAX</span></span>

### <span data-ttu-id="1cb58-105"> (預設) 不含參數的原則指派</span><span class="sxs-lookup"><span data-stu-id="1cb58-105">Policy assignment without parameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1cb58-106">透過原則參數物件使用參數的原則指派</span><span class="sxs-lookup"><span data-stu-id="1cb58-106">Policy assignment with parameters via policy parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1cb58-107">透過原則參數字串使用參數的原則指派</span><span class="sxs-lookup"><span data-stu-id="1cb58-107">Policy assignment with parameters via policy parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1cb58-108">透過原則設定參數物件使用參數的原則指派</span><span class="sxs-lookup"><span data-stu-id="1cb58-108">Policy assignment with parameters via policy set parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="1cb58-109">透過原則設定參數字串使用參數的原則指派</span><span class="sxs-lookup"><span data-stu-id="1cb58-109">Policy assignment with parameters via policy set parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1cb58-110">說明</span><span class="sxs-lookup"><span data-stu-id="1cb58-110">DESCRIPTION</span></span>
<span data-ttu-id="1cb58-111">**新的-AzureRmPolicyAssignment** Cmdlet 會建立原則指派。</span><span class="sxs-lookup"><span data-stu-id="1cb58-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="1cb58-112">指定原則與範圍。</span><span class="sxs-lookup"><span data-stu-id="1cb58-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="1cb58-113">示例</span><span class="sxs-lookup"><span data-stu-id="1cb58-113">EXAMPLES</span></span>

### <span data-ttu-id="1cb58-114">範例1：資源群組層級的原則指派</span><span class="sxs-lookup"><span data-stu-id="1cb58-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="1cb58-115">第一個命令會使用 Get-AzureRMResourceGroup Cmdlet 來取得名為 ResourceGroup11 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1cb58-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="1cb58-116">該命令會將該物件儲存在 $ResourceGroup 變數中。</span><span class="sxs-lookup"><span data-stu-id="1cb58-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="1cb58-117">第二個命令會使用 Get-AzureRmPolicyDefinition Cmdlet 來取得名為 VirtualMachinePolicy 的原則定義。</span><span class="sxs-lookup"><span data-stu-id="1cb58-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="1cb58-118">該命令會將該物件儲存在 $Policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="1cb58-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="1cb58-119">最終命令會將原則指派給資源群組層級 $Policy。</span><span class="sxs-lookup"><span data-stu-id="1cb58-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="1cb58-120">$ResourceGroup 的 **ResourceId** 屬性會識別資源群組。</span><span class="sxs-lookup"><span data-stu-id="1cb58-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

## <span data-ttu-id="1cb58-121">參數</span><span class="sxs-lookup"><span data-stu-id="1cb58-121">PARAMETERS</span></span>

### <span data-ttu-id="1cb58-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1cb58-122">-ApiVersion</span></span>
<span data-ttu-id="1cb58-123">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="1cb58-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1cb58-124">如果您沒有指定版本，此 Cmdlet 會使用最新的可用版本。</span><span class="sxs-lookup"><span data-stu-id="1cb58-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1cb58-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1cb58-125">-DisplayName</span></span>
<span data-ttu-id="1cb58-126">指定原則指派的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="1cb58-126">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="1cb58-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1cb58-127">-InformationAction</span></span>
<span data-ttu-id="1cb58-128">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="1cb58-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1cb58-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1cb58-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1cb58-130">持續</span><span class="sxs-lookup"><span data-stu-id="1cb58-130">Continue</span></span>
- <span data-ttu-id="1cb58-131">理會</span><span class="sxs-lookup"><span data-stu-id="1cb58-131">Ignore</span></span>
- <span data-ttu-id="1cb58-132">看</span><span class="sxs-lookup"><span data-stu-id="1cb58-132">Inquire</span></span>
- <span data-ttu-id="1cb58-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1cb58-133">SilentlyContinue</span></span>
- <span data-ttu-id="1cb58-134">停止</span><span class="sxs-lookup"><span data-stu-id="1cb58-134">Stop</span></span>
- <span data-ttu-id="1cb58-135">封存</span><span class="sxs-lookup"><span data-stu-id="1cb58-135">Suspend</span></span>

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

### <span data-ttu-id="1cb58-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1cb58-136">-InformationVariable</span></span>
<span data-ttu-id="1cb58-137">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="1cb58-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1cb58-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="1cb58-138">-Name</span></span>
<span data-ttu-id="1cb58-139">指定原則指派的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cb58-139">Specifies a name for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb58-140">-NotScope</span><span class="sxs-lookup"><span data-stu-id="1cb58-140">-NotScope</span></span>
<span data-ttu-id="1cb58-141">原則指派的 not 作用中。</span><span class="sxs-lookup"><span data-stu-id="1cb58-141">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="1cb58-142">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1cb58-142">-PolicyDefinition</span></span>
<span data-ttu-id="1cb58-143">指定原則，做為包含原則規則的 **PSObject** 物件。</span><span class="sxs-lookup"><span data-stu-id="1cb58-143">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb58-144">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="1cb58-144">-PolicyParameter</span></span>
<span data-ttu-id="1cb58-145">原則參數檔案路徑或原則參數字串。</span><span class="sxs-lookup"><span data-stu-id="1cb58-145">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: Policy assignment with parameters via policy parameter string, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb58-146">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="1cb58-146">-PolicyParameterObject</span></span>
<span data-ttu-id="1cb58-147">原則參數物件。</span><span class="sxs-lookup"><span data-stu-id="1cb58-147">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy set parameter object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb58-148">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1cb58-148">-PolicySetDefinition</span></span>
<span data-ttu-id="1cb58-149">原則集定義物件。</span><span class="sxs-lookup"><span data-stu-id="1cb58-149">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb58-150">-預先</span><span class="sxs-lookup"><span data-stu-id="1cb58-150">-Pre</span></span>
<span data-ttu-id="1cb58-151">表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="1cb58-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1cb58-152">-範圍</span><span class="sxs-lookup"><span data-stu-id="1cb58-152">-Scope</span></span>
<span data-ttu-id="1cb58-153">指定指派原則的範圍。</span><span class="sxs-lookup"><span data-stu-id="1cb58-153">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="1cb58-154">例如，若要將原則指派給資源群組，請指定下列專案：</span><span class="sxs-lookup"><span data-stu-id="1cb58-154">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="1cb58-155">`/subscriptions/`訂閱識別碼 `/resourcegroups/` 資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="1cb58-155">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cb58-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb58-156">-DefaultProfile</span></span>
<span data-ttu-id="1cb58-157">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1cb58-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cb58-158">-描述</span><span class="sxs-lookup"><span data-stu-id="1cb58-158">-Description</span></span>
<span data-ttu-id="1cb58-159">原則指派的描述。</span><span class="sxs-lookup"><span data-stu-id="1cb58-159">The description for policy assignment.</span></span>

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

### <span data-ttu-id="1cb58-160">-Sku</span><span class="sxs-lookup"><span data-stu-id="1cb58-160">-Sku</span></span>
<span data-ttu-id="1cb58-161">代表 sku 屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="1cb58-161">A hash table which represents sku properties.</span></span> <span data-ttu-id="1cb58-162">預設為免費 Sku： Name = A0，雙層 = Free</span><span class="sxs-lookup"><span data-stu-id="1cb58-162">Defaults to Free Sku: Name = A0, Tier = Free</span></span>

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

### <span data-ttu-id="1cb58-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb58-163">CommonParameters</span></span>
<span data-ttu-id="1cb58-164">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1cb58-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb58-165">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1cb58-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb58-166">輸入</span><span class="sxs-lookup"><span data-stu-id="1cb58-166">INPUTS</span></span>

## <span data-ttu-id="1cb58-167">輸出</span><span class="sxs-lookup"><span data-stu-id="1cb58-167">OUTPUTS</span></span>

### <span data-ttu-id="1cb58-168">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="1cb58-168">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1cb58-169">筆記</span><span class="sxs-lookup"><span data-stu-id="1cb58-169">NOTES</span></span>

## <span data-ttu-id="1cb58-170">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cb58-170">RELATED LINKS</span></span>

[<span data-ttu-id="1cb58-171">AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1cb58-171">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="1cb58-172">AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1cb58-172">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="1cb58-173">移除-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1cb58-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="1cb58-174">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1cb58-174">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


